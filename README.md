# Seleccion-RH
Selección de candidatos para empresas
# 📄 Evaluador de CVs - Gerente de Capital Humano

Este proyecto es una aplicación web que permite analizar CVs para el puesto de Gerente de Capital Humano usando inteligencia artificial (GPT-4). Se pueden subir uno o varios archivos PDF o Word y se genera un informe descargable por cada CV.

---

## 🧱 Estructura del Proyecto

```
Seleccion-RH/
├── backend/         # API Express para procesar y analizar CVs
├── frontend/        # Aplicación React para cargar archivos y mostrar resultados
├── README.md
```

---

## 🚀 Despliegue

### 1. Backend en Render

1. Ve a [https://render.com](https://render.com) y crea una cuenta.
2. Crea un nuevo Web Service y conecta el repo de GitHub.
3. Configura:

   * **Build Command:** `npm install`
   * **Start Command:** `node index.js`
   * **Runtime:** Node.js
   * **Environment Variables:**

     ```
     OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
     ```
4. Espera que Render lo despliegue. Copia la URL pública (ej: `https://backend-cv.onrender.com`).

### 2. Frontend en Vercel

1. Ve a [https://vercel.com](https://vercel.com).
2. Haz clic en **Import Project** y selecciona la carpeta `frontend`.
3. Asegúrate de que use React o Next.js correctamente detectado.
4. En el código fuente, reemplaza:

   ```js
   fetch("http://localhost:4000/api/analizar-cvs")
   ```

   por la URL de Render:

   ```js
   fetch("https://backend-cv.onrender.com/api/analizar-cvs")
   ```
5. Haz commit y Vercel desplegará automáticamente.

---

## 💻 Uso local

### Requisitos

* Node.js 18+

### Backend

```bash
cd backend
npm install
cp .env.example .env # Agrega tu OPENAI_API_KEY
node index.js
```

### Frontend

```bash
cd frontend
npm install
npm run dev
```

---

## 📂 Variables de entorno necesarias

**En `backend/.env`**:

```
OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

---

## 🧠 Tecnologías usadas

* React + TailwindCSS (frontend)
* Express + Multer + OpenAI API (backend)
* jsPDF (descarga de informes)

---

## 🖼️ Logo

Asegúrate de tener el logo en: `frontend/src/assets/logo.png` para que aparezca en los informes PDF.

---

## 📋 Estado actual

* ✅ Subida múltiple de archivos
* ✅ Análisis vía GPT-4
* ✅ Generación de informe descargable PDF con logo
* 🔜 Autenticación para terceros (opcional)

---

## 🙋‍♂️ Autor

Desarrollado por [jnovoar-coder207](https://github.com/jnovoar-coder207)
