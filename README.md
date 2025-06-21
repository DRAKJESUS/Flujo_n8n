🧠 TwoMor3Bot - Workflow en n8n
Este flujo de trabajo automatiza las respuestas de un bot de Telegram, que actúa como asistente multifuncional para procesamiento de imágenes médicas, reconocimiento de emociones y análisis de marketing.

🚀 Funcionalidades
1. Comandos disponibles:
/start: Muestra un mensaje de bienvenida y guía de comandos.

/tumor: Solicita una imagen MRI con pie de foto “/tumor” para análisis médico.

/emocion: Solicita una imagen de rostro con pie de foto “/emocion” para análisis emocional.

/dataframes: Descarga y envía un archivo PDF con los dataframes.

/graphs: Descarga y envía un archivo PDF con gráficas de marketing.

🧩 Componentes del flujo
🔹 Telegram Trigger
Escucha los mensajes entrantes desde el bot y los dirige al Router Principal.

🔹 Router Principal (Switch)
Redirecciona los comandos /start, /tumor, /emocion, /dataframes, /graphs, y los mensajes con imágenes.

🔹 Flujo para /tumor:
Verifica que el mensaje tenga imagen con caption /tumor.

Descarga la imagen.

La envía vía HTTP POST a la API

Devuelve el PDF con los resultados al usuario por Telegram.

🔹 Flujo para /emocion:


Descarga la imagen.



Devuelve el PDF con el análisis emocional.

🔹 Flujo para /dataframes:


Envía el archivo resultante como documento PDF al usuario.

🔹 Flujo para /graphs:


Envía las gráficas como archivo PDF por Telegram.

🔐 Credenciales necesarias
Telegram Bot Token (almacenado como Telegram account 3 en n8n).

📦 API externas utilizadas
Detector de Tumores

Reconocimiento de Emociones

Plataforma de Marketing

👤 Usuario configurado
ID de Telegram usado para respuestas directas

