
Afin de créer une image Docker, il faut déclarer les commandes à effectuer dans un fichier nommé Dockerfile.

Example de Dockerfile
<pre class="file">
FROM alpine
ADD README.md /tmp/
</pre>

Les commandes principales sont:
* FROM
* ADD, COPY
* RUN
* CMD, ENTRYPOINT
   * ${ENTRYPOINT} ${CMD} (avec CMD surchargeable au lancement)
* EXPOSE, VOLUME

En partant le l’image `alpine`, créez un Dockerfile appelant ping et prenant en paramètre du conteneur le host (localhost par défaut).
