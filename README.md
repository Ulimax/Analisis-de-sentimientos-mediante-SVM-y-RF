# Análisis de sentimientos empleando Aprendizaje automático ML

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
misma no solo se encontraban los posts de usuarios de la plataforma sino a que se encontraban tambien advertencias y anuncios creados por el BOT de Reddit.Se quitaron estos comentarios y espacios vacios dentro de los mismos.

Ya que ahora tenemos un dataframe con puros comentarios se procedio a trabajar con una erramienta preentrenada de redes neuronales Conocida como Bert para conocer los sentimientos detras de cada comentario y en base a los mismos se procedio
a determinar que comentarios son considerados como negativos y positivos y agregandolos a nuestro dataset de comentarios como se muestra en la siguiente imagen.


![Screenshot of a comment on a GitHub issue showing an image, added in the Markdown, of an Octocat smiling and raising a tentacle.](https://github.com/Ulimax/Analisis-de-sentimientos-mediante-SVM-y-RF/blob/main/Captura%20de%20pantalla%20de%202023-12-13%2017-32-55.png)

Para el modelo de Random Forest se emplearon los hiperparametros n_estimators = 60, random_state=42, criterion = gini, con ello obtuvimos la siguiente matriz de confusión:

![Screenshot of a comment on a GitHub issue showing an image, added in the Markdown, of an Octocat smiling and raising a tentacle.](https://github.com/Ulimax/Analisis-de-sentimientos-mediante-SVM-y-RF/blob/main/randomForest1.png)

Y se calcularon las siguientes metricas para evaluar el performance del modelo.

- Accuracy = (40333+2943)/(40333+2944+510+8708)= 0.82439897
- Precision_clase_1 = 40333/(40333+8708) = 0.8224342896759853999714524581472645337574
-  Precision_clase_2 = 2943/(2943+510) = 0.8523023457862728062554300608166811468288
- Recall_clase_1 = 40333/(40333+510) = 0.9875131601498420782018950615772592610728
-  Recall_clase_2 = 2943/(2943+8708) = 0.2525963436614882842674448545189254141275

Para el modelo de SVM se emplearon los hiperparametros kernel =lineal
![Screenshot of a comment on a GitHub issue showing an image, added in the Markdown, of an Octocat smiling and raising a tentacle.](https://github.com/Ulimax/Analisis-de-sentimientos-mediante-SVM-y-RF/blob/main/Captura%20de%20pantalla%20de%202023-12-13%2017-59-29.png)
