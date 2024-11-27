# Clasificación de Imágenes: Perros y Gatos

Este proyecto permite crear un clasificador de imágenes para identificar si una imagen corresponde a un perro o un gato. Utiliza Python, TensorFlow y TensorFlow.js para entrenar el modelo de IA y luego ejecutarlo en un sitio web accesible desde cualquier navegador, incluyendo dispositivos móviles.

## Tecnologías utilizadas
- **Python**: para entrenar el modelo de clasificación.
- **TensorFlow**: para la creación y entrenamiento del modelo de IA.
- **TensorFlow.js**: para ejecutar el modelo en el navegador.
- **ngrok**: para crear un túnel HTTPS y permitir el acceso desde dispositivos móviles.

## Funcionalidad
El modelo de IA se entrena con imágenes de perros y gatos y luego se exporta en formatos `json` y `bin` para ser utilizados en un entorno web. Puedes usar este clasificador desde cualquier navegador web, o incluso en tu celular, simplemente apuntando la cámara a una imagen o a un animal real.

### ¿Cómo utilizarlo?

1. **Descargar el repositorio**
   - Clona o descarga el repositorio en tu computadora.

2. **Iniciar un servidor local**
   - Este proyecto utiliza un modelo de TensorFlow.js, por lo que necesita ser servido a través de HTTP o HTTPS.
   
   Para iniciar un servidor local:
   - Asegúrate de tener Python instalado.
   - Abre una terminal o línea de comandos.
   - Navega hasta la carpeta donde descargaste el repositorio.
   - Ejecuta el siguiente comando:
     ```bash
     python -m http.server 8000
     ```
   - Ahora abre tu navegador y ve a [http://localhost:8000](http://localhost:8000) para acceder a la aplicación.

3. **Utilizarlo en un celular**
   - Si deseas usar el clasificador desde un celular, necesitarás un túnel HTTPS ya que la cámara no funciona sin él.
   - Para ello, usa **ngrok**:
     - Descarga [ngrok](https://ngrok.com/) y descomprímelo.
     - Abre una terminal o línea de comandos.
     - Navega hasta la carpeta donde descargaste **ngrok**.
     - Ejecuta el siguiente comando para crear un túnel HTTPS:
       ```bash
       ngrok http 8000
       ```
     - Asegúrate de tener ambos: el servidor Python y el túnel de ngrok activos.
     - En la terminal de **ngrok**, aparecerá un enlace HTTPS que podrás abrir desde tu celular, no importa si no estás en la misma red local.

4. **Usar la cámara**
   - Abre el enlace HTTPS proporcionado por **ngrok** en tu celular.
   - Puedes cambiar entre la cámara delantera y trasera usando el botón "Cambiar cámara".
   - Apunta la cámara a un perro o gato y verás la predicción en la parte inferior de la pantalla.
   
   *Nota:* El modelo no es perfecto, así que si no clasifica correctamente, no te preocupes, es normal.

### Problemas comunes

- **Problema al acceder desde el celular:**
  Si no puedes acceder al proyecto desde tu celular, asegúrate de que el túnel de ngrok esté activo y funcionando correctamente. El túnel expira después de 2 horas, por lo que necesitarás reiniciarlo si eso sucede.

- **El modelo no clasifica bien:**
  Si el modelo no está clasificando correctamente las imágenes, ten en cuenta que es un modelo básico entrenado con un conjunto limitado de imágenes. Puedes entrenarlo con más datos o ajustar los parámetros para mejorar la precisión.

### Licencia

Este proyecto está bajo la licencia MIT.


# Clasificador_img-Tensorflow
