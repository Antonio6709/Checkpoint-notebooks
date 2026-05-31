\# ¿Qué notebook ejecutar primero?

Si quieres revisar la evolución lógica del proyecto, te recomiendo abrir primero \*\*`exercises/EX\_05\_Vectorstores\_Retrieval.ipynb`\*\*. Al ejecutar sus celdas, verás cómo un texto plano se divide en \*chunks\*, se transforma en embeddings usando \*SentenceTransformers\* y se recupera correctamente usando un índice de \*FAISS\*.



\## Demo End-to-End (1 sola celda)

Para comprobar que el flujo técnico más avanzado de este checkpoint (el reordenamiento post-retrieval) funciona correctamente, abre el cuaderno \*\*`exercises/EX\_07\_Reranking\_Optimizacion.ipynb`\*\*.



\*\*Pasos para la demo:\*\*

1\. Abre el cuaderno `EX\_07\_Reranking\_Optimizacion.ipynb`.

2\. Ve a la \*\*Actividad 1\*\*.

3\. Ejecuta directamente esa celda de código (Shift + Enter).



\*\*¿Qué hace y qué debes observar?\*\*

La celda coge una lista simulada de documentos recuperados por un \*Bi-Encoder\* (búsqueda inicial rápida). Selecciona los 4 mejores y, usando un algoritmo de ordenación con \*NumPy\*, les aplica los scores precisos de un \*Cross-Encoder\*. 



En el output de la celda verás que se imprime el \*\*Ranking Final Optimizado\*\*. Comprobarás que el orden inicial ha cambiado (el Documento 1, que tiene un score de cross-encoder altísimo, sube al primer puesto). Esto demuestra que la lógica matemática del \*Two-Stage Reranking\* está correctamente implementada y lista para integrarse en el chatbot final.

