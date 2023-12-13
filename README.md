# Análisis de sentimientos con Aprendizaje automatico

En este proyecto se lleva a cabo el análisis de sentimientos de la opinion publica acerca de los Republicanos (Partido politico de los Estados Unidos Americanos)  registrados en la plataforma de Reddit,
se implementan dos algoritmos, los dos se emplean para clasificar los datos segun si el comentario registrado fue positivo o negativo y se evaluaron con las metricas correspondientes conociendo así su performance.
Los datos se obtuvieron en la plataforma de ciencia de datos [Kaggle](https://www.kaggle.com/datasets/asaniczka/public-opinion-on-republicans-daily-updated)
Los campos que se encuentran en el dataset inicial corresponden a:

- comment_id: Unique identifier for each comment.
- score: Score or popularity of the comment
- self_text: The text content of the comment.
- subreddit: The subreddit where the comment was posted. 
- created_time:Timestamp of the comment's creation. 

Conociendo esta información se decidió trabajar con los comentarios que se encuentran en la columna self text llevando acabo una limpieza de los mismos, descubrimos diferentes elementos dentro de este campo, encontrando que en la
misma no solo se encontraban los posts de usuarios de la plataforma sino a que se encontraban tambien advertencias y anuncios creados por el BOT de Reddit.


![Screenshot of a comment on a GitHub issue showing an image, added in the Markdown, of an Octocat smiling and raising a tentacle.]([https://myoctocat.com/assets/images/base-octocat.svg](https://github.com/Ulimax/Analisis-de-sentimientos-mediante-SVM-y-RF/blob/main/randomForest1.png)https://github.com/Ulimax/Analisis-de-sentimientos-mediante-SVM-y-RF/blob/main/randomForest1.png)

