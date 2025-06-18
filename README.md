Proyecto de Similitud de Documentos con Modelo de Espacio Vectorial
📄 Descripción del Proyecto
Este proyecto demuestra la aplicación del Modelo de Espacio Vectorial (VSM) para medir la similitud entre un conjunto de documentos de texto. Utiliza la técnica TF-IDF (Frecuencia de Término - Frecuencia Inversa de Documento) para convertir los documentos en representaciones numéricas (vectores) y calcula la similitud del coseno entre ellos. Finalmente, visualiza las similitudes en una matriz de calor.

🎯 Objetivos
Representar documentos de texto como vectores numéricos utilizando TF-IDF.
Calcular la similitud semántica entre pares de documentos usando la similitud del coseno.
Visualizar la matriz de similitud para una comprensión intuitiva de las relaciones entre documentos.
🛠️ Tecnologías Utilizadas
Python 3.x
scikit-learn (sklearn): Para la vectorización TF-IDF y el cálculo de la similitud del coseno.
pandas: Para la manipulación y visualización de datos en formato tabular.
matplotlib: Para la creación de gráficos.
seaborn: Para la mejora estética de los gráficos, especialmente el mapa de calor.
numpy: Para operaciones numéricas básicas.
🚀 Cómo Ejecutar el Proyecto
Sigue estos pasos para poner en marcha el proyecto en tu entorno local:

1. Clona el Repositorio (si aplica)
Si tu proyecto está en un repositorio Git, clónalo:

2. Instala las Dependencias
Asegúrate de tener Python instalado. Luego, instala las librerías necesarias usando pip:

pip install scikit-learn pandas matplotlib seaborn numpy
3. Ejecuta el Script
Una vez instaladas las dependencias, simplemente ejecuta el script Python principal:

Bash

python nombre_de_tu_script.py
(Reemplaza nombre_de_tu_script.py con el nombre real de tu archivo Python, por ejemplo, similitud_documentos.py)

📁 Estructura del Proyecto
.
├── nombre_de_tu_script.py   # Script principal del programa
└── README.md                # Este archivo
📖 Detalles del Código
El script nombre_de_tu_script.py realiza las siguientes operaciones:

Definición de Documentos: Contiene un conjunto predefinido de 3 documentos de ejemplo.
Python

documentos = [
    "El veloz zorro marrón salta sobre el perro perezoso.",
    "Un perro marrón persiguió al zorro.",
    "El perro es perezoso."
]
Vectorización TF-IDF:
TfidfVectorizer de sklearn.feature_extraction.text se utiliza para transformar los documentos en una matriz TF-IDF. Cada fila de la matriz representa un documento y cada columna un término único, con su valor TF-IDF correspondiente.
Cálculo de Similitud Coseno:
cosine_similarity de sklearn.metrics.pairwise calcula la similitud coseno entre todos los pares de vectores de documentos generados por TF-IDF. Los valores cercanos a 1 indican alta similitud, mientras que los cercanos a 0 indican baja similitud.
Visualización:
La matriz de similitud se convierte en un DataFrame de pandas para una mejor manipulación y visualización.
seaborn.heatmap se emplea para crear un mapa de calor que representa visualmente la matriz de similitud, haciendo más fácil identificar las relaciones entre documentos.
📊 Resultados y Visualización
Al ejecutar el script, verás la matriz TF-IDF (en formato DataFrame), la matriz de similitud del coseno (también en DataFrame) y un análisis textual de las similitudes entre los documentos. Además, se generará y mostrará una gráfica de mapa de calor similar a la siguiente:

--- Matriz de Similitud del Coseno ---
        Doc1      Doc2      Doc3
Doc1  1.000000  0.413725  0.435777
Doc2  0.413725  1.000000  0.270529
Doc3  0.435777  0.270529  1.000000
Gráfico de la Matriz de Similitud del Coseno
(La imagen de arriba es un marcador de posición. Al ejecutar el script, se generará el mapa de calor real con los valores de similitud.)

En el mapa de calor:

Las celdas más claras (o más "cálidas", dependiendo del cmap) indican una mayor similitud.
Las celdas más oscuras (o más "frías") indican una menor similitud.
La diagonal siempre será 1.00, ya que un documento es idéntico a sí mismo.
🔮 Posibles Mejoras
Implementar preprocesamiento de texto más avanzado (lematización, eliminación de puntuación).
Permitir que el usuario ingrese sus propios documentos o cargue un corpus desde un archivo.
Añadir una función para buscar documentos relevantes dada una consulta del usuario.
Explorar otras métricas de similitud.
Integrar una interfaz de usuario web (por ejemplo, con Flask o Streamlit).
