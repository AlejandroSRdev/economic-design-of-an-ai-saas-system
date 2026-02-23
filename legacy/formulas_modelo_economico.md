FÓRMULAS COMPLETAS – MODELO 3 PLANES ARVI

1. Fórmulas del Trial
E_λ = f_A·e_A + f_B·e_B + f_C·e_C

    f_A = fraccion de usuarios casuales (50%) x energia consumida casual (20%)
    f_B = fraccion de usuarios moderados (% depende de la conversión) x energia consumida moderada (50%)
    f_C = fraccion de usuarios intensivos (% depende de la conversión) x energia consumida intensiva (80%)
    

E_trial = 270 · E_λ
C_trial = E_trial · (coste_energia / 100)

2. Beneficio Neto por Plan
BN_plan = (precio_neto · usuarios_plan) – (coste_API_plan · usuarios_plan)

3. Beneficio Neto Total
BN_total = BN_mini + BN_base + BN_pro – C_trial_total

4. Precio Neto
precio_neto = precio_bruto · 0.79 · 0.97

5. Coste API Diario por Usuario
C_API_diario = Σ (llamadas_función · coste_llamada)

6. Coste API Mensual por Usuario
C_API_mensual = C_API_diario · 30

7. Distribución de conversiones
usuarios_i = usuarios_convertidos · p_i

8. Beneficio Neto por Usuario (para análisis unitario)
BN_usuario = precio_neto – C_API_mensual – (C_trial_per_capita)

PRECIOS
Arvi Mini = 1.49€
Arvi Base = 5.49€
Arvi Pro = 10.49€

IVA = 21%
Comisión stripe = 3%

CONVERSIÓN = 18% y distribución interna mini 65%, base 25%, pro 10%

{
  "energia_mensual_disponible": {
    "mini": 1800,
    "base": 4500,
    "pro": 9000
  },
  "energia_para_api": {
    "mini": 1260,
    "base": 3150,
    "pro": 6300
  },
  "tokens_para_api": {
    "mini": 126000,
    "base": 315000,
    "pro": 630000
  },
  "consumo_diario_tokens": {
    "mini": 3000,
    "base": 10500,
    "pro": 21000
  },
}

INFORME DETALLADO – CÁLCULO DEL BENEFICIO NETO (BN) A DIFERENTES ESCALAS
=======================================================================

1. DATOS INICIALES
------------------
- Conversión total: 18%
- Distribución interna:
  - Mini: 65%
  - Base: 25%
  - Pro: 10%

- Precios brutos:
  - Mini: 1.49 €
  - Base: 5.49 €
  - Pro: 10.49 €

- Precio neto (aplicando IVA y comisión Stripe):
  - Mini: 1.14 €
  - Base: 4.21 €
  - Pro: 8.04 €

- Coste mensual por usuario (en USD):
  - Mini: 0.3135 USD
  - Base: 0.7311 USD
  - Pro: 1.2501 USD

- Coste mensual por usuario (convertido a EUR):
  - Mini: 0.3135 · 0.92 = 0.2884 €
  - Base: 0.7311 · 0.92 = 0.6726 €
  - Pro: 1.2501 · 0.92 = 1.1501 €

=======================================================================

2. CÁLCULO DEL COSTE DEL TRIAL
------------------------------
El Trial tiene una duración de **2 días** y utiliza el patrón de uso del **usuario base**.

**Patrón de uso diario del usuario base**:
- `generarFraseHome`: 1
- `generarRespuestaConversacional`: 7
- `hacerPreguntaVerificacion`: 3
- `evaluarRespuestaVerificacion`: 3
- `analisisSemanalHabitos`: 0.14
- `generarComentarioPaso`: 0.1667
- `generarResultadoReprogramacion`: 0.0333
- `generarResumenEjecucion`: 0.7
- `crearSerieTematica`: 0.14
- `generarRespuestaTestHabitos`: 0.84
- `crearAccion`: 0.5
- `generarInformeConversacion`: 0.14

**Coste API diario del Trial**:
C_API_diario_trial = Σ (frecuencia_de_uso * coste_por_llamada)
C_API_diario_trial ≈ 0.024367230 USD
C_API_diario_trial (en EUR) = 0.024367230 · 0.92 = 0.022415 €

**Coste total del Trial por usuario**:
C_trial_total_per_user = C_API_diario_trial * días_trial
C_trial_total_per_user = 0.024367230 * 2 = 0.048734460 USD
C_trial_total_per_user (en EUR) = 0.048734460 · 0.92 = 0.0448337 €

**Coste total del Trial para todos los usuarios**:
C_trial_total = C_trial_total_per_user * usuarios_totales

=======================================================================

3. CÁLCULO DEL BENEFICIO NETO (BN) A DIFERENTES ESCALAS
-------------------------------------------------------

**Escala de 10,000 usuarios**
-----------------------------
1. Usuarios convertidos:
   usuarios_convertidos = 10,000 · 18% = 1,800
   - Mini: 1,800 · 65% = 1,170 usuarios
   - Base: 1,800 · 25% = 450 usuarios
   - Pro: 1,800 · 10% = 180 usuarios

2. C_trial_total:
   C_trial_total = C_trial_total_per_user * usuarios_totales
   C_trial_total = 0.0448337 * 10,000 = 448.337 €

3. BN por usuario:
   - Mini: BN_usuario_mini = 1.14 – 0.2884 – 0.0448337 = 0.8068 €
   - Base: BN_usuario_base = 4.21 – 0.6726 – 0.0448337 = 3.4926 €
   - Pro: BN_usuario_pro = 8.04 – 1.1501 – 0.0448337 = 6.8451 €

4. BN total:
   BN_mini = 1,170 · 0.8068 = 944.00 €
   BN_base = 450 · 3.4926 = 1,571.67 €
   BN_pro = 180 · 6.8451 = 1,231.12 €
   BN_total = BN_mini + BN_base + BN_pro – C_trial_total
   BN_total = 944.00 + 1,571.67 + 1,231.12 – 448.337 = 3,298.45 €

-------------------------------------------------------

**Escala de 500 usuarios**
---------------------------
1. Usuarios convertidos:
   usuarios_convertidos = 500 · 18% = 90
   - Mini: 90 · 65% = 58.5 ≈ 59 usuarios
   - Base: 90 · 25% = 22.5 ≈ 23 usuarios
   - Pro: 90 · 10% = 9 usuarios

2. C_trial_total:
   C_trial_total = C_trial_total_per_user * usuarios_totales
   C_trial_total = 0.0448337 * 500 = 22.42 €

3. BN por usuario:
   - Mini: BN_usuario_mini = 1.14 – 0.2884 – 0.0448337 = 0.8068 €
   - Base: BN_usuario_base = 4.21 – 0.6726 – 0.0448337 = 3.4926 €
   - Pro: BN_usuario_pro = 8.04 – 1.1501 – 0.0448337 = 6.8451 €

4. BN total:
   BN_mini = 59 · 0.8068 = 47.60 €
   BN_base = 23 · 3.4926 = 80.33 €
   BN_pro = 9 · 6.8451 = 61.61 €
   BN_total = BN_mini + BN_base + BN_pro – C_trial_total
   BN_total = 47.60 + 80.33 + 61.61 – 22.42 = 167.12 €

-------------------------------------------------------

**Escala de 1,000 usuarios**
-----------------------------
1. Usuarios convertidos:
   usuarios_convertidos = 1,000 · 18% = 180
   - Mini: 180 · 65% = 117 usuarios
   - Base: 180 · 25% = 45 usuarios
   - Pro: 180 · 10% = 18 usuarios

2. C_trial_total:
   C_trial_total = C_trial_total_per_user * usuarios_totales
   C_trial_total = 0.0448337 * 1,000 = 44.83 €

3. BN por usuario:
   - Mini: BN_usuario_mini = 1.14 – 0.2884 – 0.0448337 = 0.8068 €
   - Base: BN_usuario_base = 4.21 – 0.6726 – 0.0448337 = 3.4926 €
   - Pro: BN_usuario_pro = 8.04 – 1.1501 – 0.0448337 = 6.8451 €

4. BN total:
   BN_mini = 117 · 0.8068 = 94.40 €
   BN_base = 45 · 3.4926 = 157.17 €
   BN_pro = 18 · 6.8451 = 123.21 €
   BN_total = BN_mini + BN_base + BN_pro – C_trial_total
   BN_total = 94.40 + 157.17 + 123.21 – 44.83 = 329.95 €

**Escala de 100,000 usuarios**
------------------------------
1. Usuarios convertidos:
   usuarios_convertidos = 100,000 · 18% = 18,000
   - Mini: 18,000 · 65% = 11,700 usuarios
   - Base: 18,000 · 25% = 4,500 usuarios
   - Pro: 18,000 · 10% = 1,800 usuarios

2. C_trial_total:
   C_trial_total = C_trial_total_per_user * usuarios_totales
   C_trial_total = 0.0448337 * 100,000 = 4,483.37 €

3. BN por usuario:
   - Mini: BN_usuario_mini = 1.14 – 0.2884 – 0.0448337 = 0.8068 €
   - Base: BN_usuario_base = 4.21 – 0.6726 – 0.0448337 = 3.4926 €
   - Pro: BN_usuario_pro = 8.04 – 1.1501 – 0.0448337 = 6.8451 €

4. BN total:
   BN_mini = 11,700 · 0.8068 = 9,440.00 €
   BN_base = 4,500 · 3.4926 = 15,716.67 €
   BN_pro = 1,800 · 6.8451 = 12,311.12 €
   BN_total = BN_mini + BN_base + BN_pro – C_trial_total
   BN_total = 9,440.00 + 15,716.67 + 12,311.12 – 4,483.37 = 32,984.42 €

-------------------------------------------------------

**Escala de 1,000,000 usuarios**
--------------------------------
1. Usuarios convertidos:
   usuarios_convertidos = 1,000,000 · 18% = 180,000
   - Mini: 180,000 · 65% = 117,000 usuarios
   - Base: 180,000 · 25% = 45,000 usuarios
   - Pro: 180,000 · 10% = 18,000 usuarios

2. C_trial_total:
   C_trial_total = C_trial_total_per_user * usuarios_totales
   C_trial_total = 0.0448337 * 1,000,000 = 44,833.70 €

3. BN por usuario:
   - Mini: BN_usuario_mini = 1.14 – 0.2884 – 0.0448337 = 0.8068 €
   - Base: BN_usuario_base = 4.21 – 0.6726 – 0.0448337 = 3.4926 €
   - Pro: BN_usuario_pro = 8.04 – 1.1501 – 0.0448337 = 6.8451 €

4. BN total:
   BN_mini = 117,000 · 0.8068 = 94,400.00 €
   BN_base = 45,000 · 3.4926 = 157,166.67 €
   BN_pro = 18,000 · 6.8451 = 123,111.12 €
   BN_total = BN_mini + BN_base + BN_pro – C_trial_total
   BN_total = 94,400.00 + 157,166.67 + 123,111.12 – 44,833.70 = 329,844.09 €

=======================================================================

4. RESULTADOS FINALES
---------------------
- Escala de 10,000 usuarios: 3,298.45 €
- Escala de 100,000 usuarios: 32,984.42 €
- Escala de 1,000,000 usuarios: 329,844.09 €
=======================================================================
