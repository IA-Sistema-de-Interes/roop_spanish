Tome un video y reemplace la cara en él con una cara de su elección. Solo necesita una imagen de la cara deseada. Sin conjunto de datos, sin entrenamiento.

Puedes ver algunas demostraciones [here](https://drive.google.com/drive/folders/1KHv8n_rd3Lcr2v7jBq1yPSTWM554Gq8e?usp=sharing). También está disponible una extensión StableDiffusion, [here](https://github.com/s0md3v/sd-webui-roop).

![demo-gif](demo.gif)

## Descargo de responsabilidad
Este software está destinado a ser una contribución productiva a la industria de medios generados por IA en rápido crecimiento. Ayudará a los artistas con tareas como animar un personaje personalizado o usar el personaje como modelo para la ropa, etc.

Descargo de responsabilidad
Los desarrolladores de este software son conscientes de sus posibles aplicaciones no éticas y se comprometen a tomar medidas preventivas contra ellas. Tiene una verificación incorporada que evita que el programa funcione en medios inapropiados, incluidos, entre otros, desnudos, contenido gráfico, material sensible como imágenes de guerra, etc. Continuaremos desarrollando este proyecto en la dirección positiva mientras nos adherimos a la ley y la ética. Este proyecto puede cerrarse o incluir marcas de agua en la salida si así lo exige la ley.

Descargo de responsabilidad
Se espera que los usuarios de este software utilicen este software de manera responsable y respeten las leyes locales. Si se utiliza el rostro de una persona real, se sugiere a los usuarios que obtengan el consentimiento de la persona en cuestión y mencionen claramente que se trata de una falsificación profunda al publicar contenido en línea. Los desarrolladores de este software no serán responsables de las acciones de los usuarios finales.

## ¿Como lo instalo?

### Básico

Es más probable que funcione en su computadora, pero también será muy lento. Puede seguir las instrucciones para la instalación básica [here](https://github.com/s0md3v/roop/wiki/1.-Installation).

### Aceleración

Si tiene una buena GPU y está listo para resolver cualquier problema de software que pueda enfrentar, puede habilitar la GPU, que es mucho más rápida. Para hacer esto, primero siga las instrucciones básicas de instalación dadas anteriormente y luego siga las instrucciones específicas de la GPU. [here](https://github.com/s0md3v/roop/wiki/2.-Acceleration).

## ¿Como lo uso?

Ejecutar el comando `python run.py` abrirá esta ventana:

![gui-demo](gui-demo.png)

Elija una cara (imagen con la cara deseada) y la imagen/video de destino (imagen/video en el que desea reemplazar la cara) y haga clic en 'Iniciar'. Abra el explorador de archivos y navegue hasta el directorio en el que seleccione su salida. Encontrará un directorio llamado `<video_title>` donde puede ver los fotogramas que se intercambian en tiempo real. Una vez que se realiza el procesamiento, se creará el archivo de salida. Eso es todo.

A continuación se proporcionan argumentos de línea de comando adicionales. Para saber lo que hacen, consulte [this guide](https://github.com/s0md3v/roop/wiki/Advanced-Options).

```
options:
  -h, --help                                               show this help message and exit
  -s SOURCE_PATH, --source SOURCE_PATH                     select an source image
  -t TARGET_PATH, --target TARGET_PATH                     select an target image or video
  -o OUTPUT_PATH, --output OUTPUT_PATH                     select output file or directory
  --frame-processor FRAME_PROCESSOR [FRAME_PROCESSOR ...]  frame processors (choices: face_swapper, face_enhancer, ...)
  --keep-fps                                               keep target fps
  --keep-frames                                            keep temporary frames
  --skip-audio                                             skip target audio
  --many-faces                                             process every face
  --reference-face-position REFERENCE_FACE_POSITION        position of the reference face
  --reference-frame-number REFERENCE_FRAME_NUMBER          number of the reference frame
  --similar-face-distance SIMILAR_FACE_DISTANCE            face distance used for recognition
  --video-encoder {libx264,libx265,libvpx-vp9}             adjust output video encoder
  --video-quality [0-51]                                   adjust output video quality
  --max-memory MAX_MEMORY                                  maximum amount of RAM in GB
  --execution-provider {cpu} [{cpu} ...]                   available execution provider (choices: cpu, ...)
  --execution-threads EXECUTION_THREADS                    number of execution threads
  -v, --version                                            show program's version number and exit
```

¿Busca un modo CLI? El uso del argumento -s/--source hará que el programa se ejecute en modo cli.

## Créditos
- [henryruhs](https://github.com/henryruhs): por ser un colaborador insustituible del proyecto
- [ffmpeg](https://ffmpeg.org/): para facilitar las operaciones relacionadas con el vídeo
- [deepinsight](https://github.com/deepinsight): para ellos [insightface](https://github.com/deepinsight/insightface) proyecto que proporcionó una biblioteca y modelos bien hechos.
- y todos los desarrolladores detrás de las bibliotecas utilizadas en este proyecto.
