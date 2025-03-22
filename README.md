# Pinecone y LangChain con OpenAI

Autora: Laura Sofía Gil Chaves

Este proyecto implementa un sistema de recuperación de información utilizando Pinecone como base de datos vectorial y LangChain para la generación de respuestas basadas en un modelo de lenguaje de OpenAI.

## Instalación

Se debe tener instalado los siguietes paquetes

```bash
  pip install pinecone-client langchain-pinecone
  pip install --upgrade langchain langchain-community
  pip install --upgrade langchain-openai
```
### Claves de API Necesarias

Antes de ejecutar el proyecto, asegúrate de tener configuradas las siguientes claves de API:

- **OPENAI_API_KEY**: Clave de API de OpenAI.
- **PINECONE_API_KEY**: Clave de API de Pinecone.
- **PINECONE_ENV**: Entorno de Pinecone (por ejemplo, `us-west1-gcp`).

---
### Digarma del proyecto

![image](https://github.com/user-attachments/assets/c6fcb323-fc07-4d71-93da-223903a641fb)

### Tecnologías Utilizadas

- LangChain: Framework para encadenar modelos de lenguaje con fuentes de datos externas.
- Pinecone: Base de datos vectorial para almacenamiento y búsqueda de embeddings.
- OpenAI: Modelos de lenguaje avanzados para generación de respuestas.
- BeautifulSoup: Para extraer contenido relevante de páginas web.

### Configuración del Proyecto

El script realiza las siguientes acciones:

1. Carga las Credenciales: Verifica y solicita las claves de API necesarias para OpenAI y Pinecone.
   
2. Configura Pinecone: Inicializa Pinecone y crea un índice si no existe.
   
3. Carga y Procesa Documentos: Obtiene datos de Wikipedia utilizando WebBaseLoader de LangChain y BeautifulSoup para extraer texto relevante.

4. Genera Embeddings: Convierte los textos en vectores utilizando OpenAIEmbeddings.

5. Crea la Base de Datos Vectorial: Almacena los embeddings en Pinecone para facilitar la búsqueda semántica.
   
6. Configura un Sistema de Recuperación de Información: Usa LangChain para interactuar con los documentos indexados.
   
7. Realiza Consultas:Permite hacer preguntas sobre el contenido almacenado.


### Uso

Ejecuta el script para realizar una consulta sobre el tema de interés. Por ejemplo:

```bash
  query = "Explain me who is BTS"
  result = qa_chain(query)

  print("Respuesta:", result["result"])
  print("Documentos fuente:", result["source_documents"])
```

Esto devolverá una respuesta generada por el modelo de lenguaje y los documentos utilizados como referencia.

### Evidenicas
![image](https://github.com/user-attachments/assets/f5777398-661a-4012-b9d3-a0c6899340b2)
![image](https://github.com/user-attachments/assets/71b7d45b-f9fa-4cfe-b41f-476cbe611358)
![image](https://github.com/user-attachments/assets/0e9d7b6a-99f6-4ad8-8783-0c9f81058f16)
![image](https://github.com/user-attachments/assets/13232aff-33c3-4a62-a44b-c85a761f2694)





###
