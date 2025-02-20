# 🖼️ Generador de Imágenes con Stable Diffusion

![Stable Diffusion](https://img.shields.io/badge/Stable%20Diffusion-v1.6-blue) ![Python](https://img.shields.io/badge/Python-3.10-blue) ![Streamlit](https://img.shields.io/badge/Streamlit-Web%20App-red)

## 📌 Descripción
Este proyecto es una aplicación web construida con **Streamlit** que permite generar imágenes a partir de descripciones de texto utilizando **Stable Diffusion Web UI**. La aplicación permite personalizar diversos parámetros como el tamaño de la imagen, el número de pasos de muestreo y la escala de orientación CFG.

## 🔍 Características Principales

✅ **Generación de imágenes basada en texto** mediante un modelo avanzado de IA.  
✅ **Personalización de parámetros** como resolución, pasos de muestreo y escala CFG.  
✅ **Descarga rápida de imágenes generadas** en formato PNG.  
✅ **Interfaz amigable y fácil de usar** desarrollada con Streamlit.

## 🌍 Modelo Utilizado
- **📚 Nombre del modelo**: `dreamshaper_8.safetensors`
- **🧠 Arquitectura**: Stable Diffusion
- **⚙️ Sampler recomendado**: `DPM++ 2M Karras`
- **📏 Parámetros clave**:
  - 📝 **Resolución recomendada**: `512x512`
  - ⏳ **Pasos de muestreo**: `20`
  - 🔄 **CFG Scale**: `7.0`

## ⚙️ Requisitos
Asegúrate de tener instalados los siguientes componentes:
- 💾 **Python 3.10+**
- 🤖 **Stable Diffusion Web UI (Automatic1111)**
- 📝 **Dependencias de Python**:
  ```sh
  pip install streamlit requests pillow
  ```

## 📝 Instalación y Ejecución
1. 🔄 **Clona el repositorio**:
   ```sh
   git clone https://github.com/usuario/proyecto-stable-diffusion.git
   cd proyecto-stable-diffusion
   ```
2. 💪 **Instala las dependencias necesarias**:
   ```sh
   pip install -r requirements.txt
   ```
3. 🚀 **Inicia Stable Diffusion Web UI**:
   ```sh
   python launch.py --api
   ```
4. 🌐 **Ejecuta la aplicación Streamlit**:
   ```sh
   streamlit run app.py
   ```

## 📺 Uso
1. ✏️ **Ingresa una descripción** en el campo de texto.
2. 🌐 **Ajusta los parámetros** según tus necesidades.
3. ✨ **Presiona "Generar Imagen"** y espera el resultado.
4. 💾 **Descarga la imagen generada** si lo deseas.

## 🌟 Capturas de Pantalla y Ejemplos de Imágenes
Ubica las siguientes imágenes en el repositorio:

- **📲 Capturas de la aplicación funcionando:**

  - 📁 Interfaz

  ![image](https://github.com/user-attachments/assets/8df3fde0-20dc-4266-8094-df2333d93a1f)
  
    
  - 📁 Resultado generado
 
    ![image](https://github.com/user-attachments/assets/09a6fd3d-1594-4b73-bc68-4d49a269d4d6)


- **🎨 Ejemplos de imágenes generadas:**
  - 📁 `generated_samples/sample1.png`

     ![sample1](https://github.com/user-attachments/assets/3f2a1f29-2bb5-40ac-a9cb-dff50b0eb161)

    
  - 📁 `generated_samples/sample2.png`

    ![sample2](https://github.com/user-attachments/assets/ec084144-cf04-405e-8e18-698fb532a559)


  - 📁 `generated_samples/sample3.png`

    ![sample3](https://github.com/user-attachments/assets/13dfc7f3-e8cc-4f5c-828d-a5d6546d9341)

    
  - 📁 `generated_samples/sample4.jpg`

    ![sample4](https://github.com/user-attachments/assets/4eb7f60c-5a43-4ec7-a703-3ad7e930af57)


## 👨‍💻 Autores
Desarrollado por **Carlos López Muñóz y Alejandro Fernández Barrionuevo** - 2025.



