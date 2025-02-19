import streamlit as st
import requests
import base64
import json
from io import BytesIO
from PIL import Image

# Configuración de la API de Stable Diffusion Web UI
SD_API_URL = "http://127.0.0.1:7860/sdapi/v1/txt2img"  # Asegúrate de que este puerto es el correcto

# Título de la aplicación
st.title("Generador de Imágenes con Stable Diffusion")

# Entrada del usuario
prompt = st.text_area("Describe la imagen que quieres generar:", "A mystical ink-style mountain landscape")

# Opciones de configuración
width = st.slider("Ancho de la imagen", 512, 1024, 768, step=64)
height = st.slider("Alto de la imagen", 512, 1024, 768, step=64)
steps = st.slider("Número de pasos de muestreo", 10, 50, 25)
cfg_scale = st.slider("Escala de orientación del CFG", 1.0, 12.0, 7.0)

# Botón de generación
if st.button("Generar Imagen"):
    payload = {
        "prompt": f"{prompt}, <lora:Ink_scenery:1>",
        "negative_prompt": "low quality, worst quality, blurry",
        "sampler_name": "Euler a",
        "steps": steps,
        "cfg_scale": cfg_scale,
        "width": width,
        "height": height,
        "enable_hr": False,
        "denoising_strength": 0.5,
        "override_settings": {
            "sd_model_checkpoint": "dreamshaper_8.safetensors"
        }
    }

    # Enviar la solicitud a la API
    response = requests.post(SD_API_URL, json=payload)
    
    if response.status_code == 200:
        result = response.json()
        img_data = base64.b64decode(result["images"][0])
        
        # Mostrar imagen
        image = Image.open(BytesIO(img_data))
        st.image(image, caption="Imagen Generada", use_container_width=True)
        
        # Botón de descarga
        buf = BytesIO()
        image.save(buf, format="PNG")
        st.download_button(label="Descargar Imagen", data=buf.getvalue(), file_name="imagen_generada.png", mime="image/png")
    else:
        st.error(f"Error en la generación: {response.status_code}")
