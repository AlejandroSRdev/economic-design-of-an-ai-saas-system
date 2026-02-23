{
  "coste_por_llamada_funciones_simples": {
    "generarFraseHome": {
      "pasadas": [
        {
          "modelo": "Gemini 2.0 Flash",
          "tokens": { "in": 205, "out": 50 },
          "coste": 0.00006075
        }
      ],
      "coste_total_dolares": 0.00006075
    },
    "hacerPreguntaVerificacion": {
      "pasadas": [
        {
          "modelo": "Gemini 2.0 Flash",
          "tokens": { "in": 216, "out": 41 },
          "coste": 0.000057000
        }
      ],
      "coste_total_dolares": 0.000057000
    }
  },

  "coste_por_llamada_funciones_complejas": {
    "generarComentarioPaso": {
      "pasadas": [
        {
          "modelo": "Gemini 2.5 Flash",
          "tokens": { "in": 600, "out": 150 },
          "coste": 0.000277500
        }
      ],
      "coste_total_dolares": 0.000277500
    },

    "generarResultadoReprogramacion": {
      "pasadas": [
        {
          "modelo": "Gemini 2.5 Pro",
          "tokens": { "in": 1200, "out": 300 },
          "coste": 0.004500000
        }
      ],
      "coste_total_dolares": 0.004500000
    },

    "analisisSemanalHabitos": {
      "pasadas": [
        {
          "modelo": "Gemini 2.5 Pro",
          "tokens": { "in": 1200, "out": 300 },
          "coste": 0.009000000
        }
      ],
      "coste_total_dolares": 0.009000000
    },

    "generarResumenEjecucion": {
      "pasadas": [
        {
          "modelo": "Gemini 2.5 Pro",
          "tokens": { "in": 4700, "out": 1500 },
          "coste": 0.018600000
        },
        {
          "modelo": "GPT-4o mini",
          "tokens": { "in": 300, "out": 300 },
          "coste": 0.000225000
        }
      ],
      "coste_total_dolares": 0.018825000
    },

    "crearSerieTematica": {
      "pasadas": [
        {
          "modelo": "Gemini 2.5 Flash",
          "tokens": { "in": 1650, "out": 550 },
          "coste": 0.000935000
        },
        {
          "modelo": "Gemini 2.5 Pro",
          "tokens": { "in": 300, "out": 300 },
          "coste": 0.005625000
        },
        {
          "modelo": "GPT-4o mini",
          "tokens": { "in": 300, "out": 300 },
          "coste": 0.000270000
        }
      ],
      "coste_total_dolares": 0.006830000
    },

    "crearAccion": {
      "pasadas": [
        {
          "modelo": "Gemini 2.5 Flash",
          "tokens": { "in": 770, "out": 300 },
          "coste": 0.000490500
        },
        {
          "modelo": "Gemini 2.5 Pro",
          "tokens": { "in": 300, "out": 300 },
          "coste": 0.005625000
        },
        {
          "modelo": "GPT-4o mini",
          "tokens": { "in": 300, "out": 300 },
          "coste": 0.000270000
        }
      ],
      "coste_total_dolares": 0.006385500
    },

    "generarRespuestaTestHabitos": {
      "pasadas": [
        {
          "modelo": "Gemini 2.5 Flash",
          "tokens": { "in": 1200, "out": 500 },
          "coste": 0.003600000
        }
      ],
      "coste_total_dolares": 0.003600000
    },

    "generarInformeConversacion": {
      "pasadas": [
        {
          "modelo": "Gemini 2.5 Flash",
          "tokens": { "in": 1000, "out": 300 },
          "coste": 0.000525000
        },
        {
          "modelo": "Gemini 2.5 Pro",
          "tokens": { "in": 300, "out": 300 },
          "coste": 0.005625000
        },
        {
          "modelo": "GPT-4o mini",
          "tokens": { "in": 300, "out": 300 },
          "coste": 0.000270000
        }
      ],
      "coste_total_dolares": 0.006420000
    },

    "evaluarRespuestaVerificacion": {
      "pasadas": [
        {
          "modelo": "Gemini 2.0 Flash",
          "tokens": { "in": 154, "out": 0 },
          "coste": 0.000023100
        },
        {
          "modelo": "Gemini 2.5 Pro",
          "tokens": { "in": 95, "out": 0 },
          "coste": 0.000356250
        },
        {
          "modelo": "GPT-4o mini",
          "tokens": { "in": 120, "out": 0 },
          "coste": 0.000018000
        }
      ],
      "coste_total_dolares": 0.000397350
    }
  }
}

{
"patrones_uso_diario_por_plan": {
"mini_60_energia": {
generarFraseHome: 1
generarRespuestaConversacional: 3
hacerPreguntaVerificacion: 1
evaluarRespuestaVerificacion: 1
analisisSemanalHabitos: 0.14
generarComentarioPaso: 0.1667
generarResultadoReprogramacion: 0.0333
generarResumenEjecucion: 0.286
crearSerieTematica: 0.07
generarRespuestaTestHabitos: 0.42
crearAccion: 0
generarInformeConversacion: 0
},
"base_150_energia": {
generarFraseHome: 1
generarRespuestaConversacional: 7
hacerPreguntaVerificacion: 3
evaluarRespuestaVerificacion: 3
analisisSemanalHabitos: 0.14
generarComentarioPaso: 0.1667
generarResultadoReprogramacion: 0.0333
generarResumenEjecucion: 0.7
crearSerieTematica: 0.14
generarRespuestaTestHabitos: 0.84
crearAccion: 0.5
generarInformeConversacion: 0.14
},
generarFraseHome: 1
generarRespuestaConversacional: 12
hacerPreguntaVerificacion: 6
evaluarRespuestaVerificacion: 6
analisisSemanalHabitos: 0.14
generarComentarioPaso: 0.1667
generarResultadoReprogramacion: 0.0333
generarResumenEjecucion: 1
crearSerieTematica: 0.28
generarRespuestaTestHabitos: 2
crearAccion: 1.2
generarInformeConversacion: 0.3
}
},

COSTE ENERGÉTICO Y RELACIÓN ENERGÍA-TOKEN

1 Energia = 100 tokens

Energía por plan: 

    Trial = 135/día x 2 días de trial
    Mini = 75/día x 30 días
    Base = 150/día x 30 días
    Pro = 300/día x 30 días

// 📌 Función auxiliar — calcula tokens de un solo fragmento de texto
int calcularTokensGeminiSolo(String texto) {
  final longitud = texto.trim().length;
  return (longitud / 3.7).round(); // ≈ 1 token por 3.7 caracteres
}

// 📌 Función antigua reconvertida a wrapper (compatibilidad)
int calcularTokensGemini(String prompt, String respuesta) {
  final tokensPrompt = calcularTokensGeminiSolo(prompt);
  final tokensRespuesta = calcularTokensGeminiSolo(respuesta);
  return tokensPrompt + tokensRespuesta;
}

// 📌 Método para calcular la energía a restar en cada llamada
final tokensPrompt = calcularTokensGeminiSolo(prompt);
final tokensRespuesta = calcularTokensGeminiSolo(respuesta);
final tokens = (tokensRespuesta + (tokensPrompt * 0.30)).round();
final energiaARestar = (tokens / 100).ceil();