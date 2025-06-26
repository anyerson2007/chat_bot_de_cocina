🍳 Chatbot API experto en Cocina

Este proyecto es una API REST construida con FastAPI que funciona como un chatbot experto en cocina: responde preguntas sobre recetas, técnicas culinarias, sustituciones de ingredientes y más. Aprovecha el modelo Mistral vía OpenRouter (compatible con la API de OpenAI) para generar respuestas culinarias conversacionales.

🚀 Requisitos

Python 3.8 o superior (solo para ejecutar el backend)

Contar con una API Key de OpenRouter

Conexión a internet

🛠 Instalación

Clona este repositorio o descarga los archivos.

Crea un entorno virtual y actívalo:

python -m venv venv

# Activar entorno virtual
# Windows
venv\Scripts\activate
# macOS/Linux
source venv/bin/activate

Instala las dependencias:

pip install -r requirements.txt

Crea un archivo .env en la raíz del proyecto con:

API_KEY=tu_api_key_de_openrouter
BASE_URL=https://openrouter.ai/api/v1

▶ Ejecución

Inicia el servidor con:

uvicorn main:app --reload

API disponible en: http://127.0.0.1:8000

Documentación Swagger UI: http://127.0.0.1:8000/docs

📬 Ejemplo de uso

Petición POST a /chat:

{
  "pregunta": "¿Cómo preparo una salsa bechamel sin grumos?"
}

Respuesta esperada:

{
  "respuesta": "Para lograr una bechamel lisa, comienza derritiendo mantequilla, añade la harina y cocina el roux durante 2 minutos..."
}

📁 Estructura del proyecto

chatbot-ia_cocina/
├── main.py           # API con FastAPI
├── config.py         # Contiene el PROMPT_SISTEMA
├── .env              # Variables de entorno
├── requirements.txt  # Dependencias
├── Dockerfile        # Configuración para Docker
├── frontend/         # Interfaz web para el chatbot
│   ├── index.html    # Estructura HTML
│   ├── style.css     # Estilos modernos (Glassmorphism + tema culinario)
│   └── script.js     # Lógica de chat, efectos y temporizadores
└── README.md

💬 Interfaz Web del Chatbot

El proyecto incluye una interfaz web moderna para interactuar visualmente con la API.

✨ Funcionalidades del frontend

💎 Diseño Glassmorphism: fondo translúcido con desenfoque y bordes redondeados.

🎨 Tema Culinario: paleta de colores inspirada en tonos crema, rojo tomate y verde albahaca.

⌨️ Tipografía técnica: uso de Fira Code para un toque “dev”, combinada con una serif elegante para títulos.

💬 Mensajes organizados: estilo chat con diferenciación clara entre el usuario y el bot.

🕒 Temporizadores de inactividad

A los 2 min sin interacción se muestra una alerta.

A los 5 min el chat se limpia automáticamente.

✍️ Efecto “escribiendo…”: simula la respuesta del bot en tiempo real.

🔄 Soporte CORS habilitado para comunicación frontend–backend.

▶ Cómo usarlo

Asegúrate de que el backend esté en ejecución (uvicorn main:app --reload).

Abre frontend/index.html en tu navegador.

¡Pregunta lo que quieras sobre cocina! 😄

👤 Autor
Anyerson Contreras