# Poyecto_Mineria

# Clasificación de Emociones en Español con Embeddings y Modelos Transformers

Este proyecto implementa modelos de clasificación emocional en textos en español, utilizando RoBERTuito y técnicas modernas de NLP con `transformers`, `spaCy`, y `sentence-transformers`.

También se utilizaron tecnicas como fine tunning para generar embeddings mas precisos y ricos para la clasificación de texto emocional, al final obtuvimos una precisión del 95% en acurracy y f1 al evaluarse en el 20% del dataset.

## Estructura del Repositorio

Proyecto_Mineria

┣ PruebaFinal_v1.1.ipynb  
┣ Nuevo_Dataset_Patrones_Emocionales.csv  
┣ README.md  
┗ Screenshots.zip

## Requisitos

Antes de ejecutar el notebook en local, instala las siguientes dependencias:

```bash 
pip install pandas transformers sentence-transformers spacy language-tool-python
python -m spacy download es_core_news_sm.
```

Si estas en Collab ejecuta:
```bash
!sudo apt update
!sudo apt install openjdk-17-jdk -y
!update-alternatives --install /usr/bin/java java /usr/lib/jvm/java-17-openjdk-amd64/bin/java 1
!update-alternatives --set java /usr/lib/jvm/java-17-openjdk-amd64/bin/java
!pip install language-tool-python
!pip install -U spacy
!python -m spacy download es_core_news_sm
!pip install transformers sentence-transformers
!pip install transformers datasets evaluate
```

# Ejecución
## 1.- Clona el repo:

git clone [https://github.com/tu_usuario/NombreDelRepositorio.git](https://github.com/ALNM7/Poyecto_Mineria)

cd Proyecto_Mineria

## 2.-Abre el archivo PruebaFinal_v1.1.ipynb en Jupyter Notebook o Google Colab.

## 3.-Asegúrate de tener el archivo Nuevo_Dataset_Patrones_Emocionales.csv en el mismo directorio.

## 4.-Ejecuta todas las celdas del notebook 

# Funciones clave 

preprocesar_texto(texto)
Limpia, tokeniza y lematiza el texto de entrada en español utilizando spaCy.

generar_embeddings(textos)
Utiliza robertuito para obtener embeddings del texto.

entrenar_modelo(X, y)
Entrena un clasificador como por ejemplo SVM, KNN, etc. Sobre los embeddings.

evaluar_modelo(modelo, X_test, y_test)
Calcula la precisión, recall, F1 y matriz de confusión del modelo entrenado.


TrainingArguments (...)
Se colocan los argumentos para entrenar con fine tunning 
