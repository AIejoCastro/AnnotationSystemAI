# Sistema de Reconocimiento Automático de Actividades Humanas

Sistema de inteligencia artificial para reconocer actividades humanas en tiempo real: caminar hacia la cámara, caminar de regreso, girar, sentarse y levantarse.


## Autores

- Daniel Escobar
- Juan Calderón  
- Alejandro Castro

Universidad ICESI - Inteligencia Artificial I - 2025-1

## Requisitos

- Python 3.8 - 3.11
- Jupyter Notebook o VSCode
- Webcam funcional
- Windows, macOS, o Linux

## Instalación

### 1. Clonar el repositorio
```bash
git clone <repo>
cd AnnotationSystemAI/Entrega-2/src
```

### 2. Instalar dependencias
```bash
pip install opencv-python==4.8.1.78
pip install mediapipe==0.10.8
pip install pandas==2.0.3
pip install numpy==1.24.3
pip install scikit-learn==1.3.0
pip install matplotlib==3.7.2
pip install seaborn==0.12.2
pip install joblib==1.3.2
pip install tqdm==4.65.0
```
(pip install -r requirements.txt)

### 3. Verificar estructura de carpetas
```
Entrega-2/
└── src/
    ├── motion_system.ipynb       # Sistema en tiempo real
    ├── model.ipynb               # Entrenamiento del modelo
    ├── process_data.ipynb        # Procesamiento de datos
    └── modelo_rf_output/         # Modelos entrenados
        ├── modelo_rf.pkl
        ├── scaler.pkl
        └── label_encoder.pkl
```

## Ejecución



### Entrenar el modelo (solo si quieres re-entrenar)
```bash
# Los modelos ya están entrenados en modelo_rf_output/
# Solo ejecuta esto si quieres entrenar desde cero:
jupyter notebook model.ipynb
```

### Ejecutar la aplicación 
```bash
# Opción 1: En Jupyter Notebook
jupyter notebook motion_system.ipynb
# Ejecutar todas las celdas

# Opción 2: En VSCode
# Abrir motion_system.ipynb y ejecutar todas las celdas
```


## Controles (en el sistema en tiempo real)

- **Q**: Salir del programa
- **A**: Mostrar/ocultar ángulos articulares

## Solución de problemas

### Error: Jupyter no está instalado
```bash
pip install jupyter
```

### Error: No se puede abrir la cámara
- Verificar que la webcam esté conectada
- Cerrar otras aplicaciones que usen la cámara


### Error: No se encuentra el modelo
- Verificar que la carpeta `modelo_rf_output/` contenga los archivos .pkl
- Ejecutar primero `model.ipynb` para generar los modelos
- Asegurarse de estar en la carpeta `src/`

### Error de dependencias
```bash
pip install --upgrade pip

```
