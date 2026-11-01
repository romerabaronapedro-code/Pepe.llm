<div align="center">

# Pepe LLM 🐸

**Tu cuaderno de estudio con IA — rápido, local y sin gastar tokens.**

[Características](#-características) · [Cómo funciona](#-cómo-funciona) · [Tecnología](#-tecnología) · [Desplegar](#-desplegarlo-tú-mismo)

</div>

---

## ¿Qué es Pepe LLM?

Pepe LLM es una aplicación web para estudiantes de **bachillerato y universidad** que reúne lo mejor de un cuaderno inteligente tipo NotebookLM, pero **sin depender de la nube ni quemar tokens**: casi todo el procesamiento (resúmenes, quizzes, tarjetas de repaso, plan de estudio) se hace **en tu propio navegador**, gratis y al instante.

Todo tu material de estudio se guarda **solo en tu navegador** (localStorage): no hace falta cuenta, no se sube nada a ningún servidor, y tus apuntes son 100 % tuyos.

## ✨ Características

| Sección | Qué hace |
|---|---|
| 📚 **Biblioteca** | Guarda tus apuntes, PDFs y documentos organizados por asignatura |
| 📝 **Estudiar** | Resúmenes, ideas clave y glosario generados al vuelo, sin IA externa |
| 🧠 **Practicar** | Quizzes y tarjetas de repaso (SRS — repetición espaciada) |
| 💬 **Chat** | Conversa con tus apuntes; la IA (Groq) es **opcional** y solo si tú la activas |
| 🔎 **Fuentes** | Busca y organiza fuentes de información para tus trabajos |
| 🗓️ **Planificador** | Organiza tu semana de estudio y sesiones Pomodoro integradas |
| 🧪 **Laboratorio** | Las funciones clásicas de la V1.4: OCR, PPTX/XLSX y mapa mental interactivo |

### Filosofía del proyecto

- **Rapidez primero**: procesamiento local (NLP en el navegador) en lugar de llamadas a modelos de pago.
- **Cero coste por uso**: la IA es opt-in; si nunca la activas, el coste es 0.
- **Privacidad total**: tus apuntes nunca salen de tu dispositivo.

## ⚙️ Cómo funciona

```
Apuntes → Procesamiento local (resumen · quiz · glosario · SRS) → Repaso
              ↓ (opcional)
           IA (Groq) solo cuando tú lo decides
```

- El procesamiento de texto vive en `src/lib/nlp.ts` y el algoritmo de repetición espaciada en `src/lib/srs.ts`.
- El estado de la app se guarda en el navegador vía `src/lib/store.ts`.
- La interfaz clásica V1.4 se sirve desde `public/legacy` en la ruta `/laboratorio`.

## 🛠️ Tecnología

- **React 19** + **TypeScript** + **Vite**
- **Tailwind CSS v4**
- **TanStack Router / Start**
- Procesamiento NLP propio en el cliente
- IA opcional vía Groq

## 🚀 Desplegarlo tú mismo

```bash
git clone https://github.com/TU-USUARIO/pepe-llm.git
cd pepe-llm
npm install
npm run dev
```

Abre `http://localhost:5173` y listo. No necesitas claves ni base de datos para el modo local; la IA de Groq solo requiere tu clave si la quieres activar.

## 📄 Licencia

MIT — usa, estudia y mejora Pepe LLM libremente.

---

<div align="center">
<b>Estudia · Organiza · Aprende — en local 🐸</b>
</div>
