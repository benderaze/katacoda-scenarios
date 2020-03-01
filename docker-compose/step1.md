
Afin de lancer une stack vous devez définir les différents services via un fichier de configuration `docker-compose.yml`.

Example de docker-compose.yml
<pre class="file">
version "3.7"
Services:
	service-name-1:
		image: <image_name>
		ports:
		  - 80:80
		volumes:
		  - ./service.conf:/etc/service/service.conf
	whoami
		image: <image_name_2>
		build: ./path/to/dockerfile
		depends_on:
		  - service-name-1
		environment:
		  - MY_ENV_VAR=environment

</pre>

Afin de lancer votre stack, vous pouvez lancer la commande `docker-compose up` dans le répertoire contenant votre fichier de description.

Créez une stack PHP myadmin avec une base mySql et un conteneur PHP (`phpmyadmin/phpmyadmin`).
