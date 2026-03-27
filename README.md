🍽️ Asistente de reservas con IA para WhatsApp

n8n • WhatsApp API • AI Agent • Google Calendar


📖 Overview

Este proyecto implementa un asistente inteligente para la gestión de reservas a través de WhatsApp, capaz de automatizar completamente la interacción con clientes utilizando inteligencia artificial.
El sistema permite a los usuarios crear, modificar o cancelar reservas mediante mensajes de texto o audio, interpretando automáticamente la intención del usuario y gestionando las reservas en un calendario en tiempo real.
El workflow está desarrollado en n8n, integrando la API de WhatsApp, un agente de IA y un sistema de calendario para ofrecer una solución completa de automatización.


🚀 Features

Gestión automática de reservas desde WhatsApp
Interpretación de mensajes mediante IA
Soporte para mensajes de texto y audio
Transcripción automática de audios
Creación de eventos en calendario
Modificación de reservas existentes
Cancelación de reservas
Confirmaciones automáticas al cliente
Prevención de duplicados o errores
Notificaciones por email (opcional)


🏗️ System Architecture

User (WhatsApp)

      ↓
WhatsApp API

      ↓
n8n Workflow

      ↓
Message Processing (Text / Audio)

      ↓
Speech-to-Text (if audio)

      ↓
Data Normalization

      ↓
AI Agent (Intent Detection)

      ↓
Action Layer:
   → Create Reservation
   → Modify Reservation
   → Cancel Reservation
   
      ↓
Google Calendar Integration

      ↓
Response Generator

      ↓
WhatsApp Response


⚙️ Workflow Explanation

🔹 1. WhatsApp Trigger

El flujo comienza con la recepción de mensajes entrantes desde WhatsApp.

🔹 2. Duplicate / Loop Control

Se implementa un sistema para evitar mensajes duplicados o bucles en el flujo.

🔹 3. Message Processing

El sistema identifica el tipo de mensaje:
texto → se procesa directamente
audio → se descarga y transcribe

🔹 4. Data Normalization

El contenido del mensaje se convierte en un formato estándar para su análisis.

🔹 5. AI Agent (Intent Detection)

El agente de IA analiza el mensaje y determina la intención del usuario:
crear reserva
modificar reserva
cancelar reserva
También extrae información clave como:
fecha
hora
número de personas

🔹 6. Availability Check

El sistema consulta el calendario para verificar disponibilidad en el horario solicitado.

🔹 7. Reservation Handling

Dependiendo de la intención:
Crear reserva
verifica disponibilidad
crea evento en calendario
Modificar reserva
localiza evento existente
actualiza datos
Cancelar reserva
elimina el evento del calendario

🔹 8. Calendar Integration

Se utiliza Google Calendar como sistema de gestión de reservas en tiempo real.

🔹 9. Notification System (Optional)

Se pueden enviar notificaciones por correo electrónico con los detalles de la reserva.

🔹 10. Response Generation

El sistema responde al usuario en WhatsApp confirmando la acción realizada.


🛠️ Technologies Used

n8n — automatización de workflows
WhatsApp Business API — comunicación con usuarios
Google Calendar API — gestión de reservas
AI Agent (LLM) — interpretación de mensajes
Speech-to-Text — transcripción de audio
Email Service — notificaciones


▶️ Setup & Installation

Requisitos
Instancia de n8n (self-hosted o cloud)
Acceso a WhatsApp Business API
Cuenta de Google (Calendar API)
API de inteligencia artificial (OpenAI / Gemini)
Servicio de transcripción de audio (opcional)
Pasos
1. Importar el workflow en n8n
2. Configurar credenciales de WhatsApp API
3. Configurar Google Calendar
4. Configurar API de IA
5. Configurar servicio de transcripción (opcional)
6. Activar el workflow

   
📌 Use Cases

Restaurantes
Cafeterías
Clínicas y consultas
Peluquerías y centros de estética
Hoteles y alojamientos
Negocios con gestión de citas


📈 Future Improvements

Integración con sistema de pagos
Recordatorios automáticos de reservas
Gestión de usuarios (base de datos)
Panel de administración de reservas
Integración con CRM
Soporte multi-idioma


🧩 Key Highlights

Este proyecto demuestra:
Automatización de procesos de negocio en tiempo real
Uso de IA para interpretación de lenguaje natural
Integración de múltiples sistemas (WhatsApp + Calendar + AI)
Diseño de asistentes conversacionales funcionales
Aplicación directa en entornos empresariales
📄 License
Uso educativo y demostrativo. Adaptable a entornos empresariales.
