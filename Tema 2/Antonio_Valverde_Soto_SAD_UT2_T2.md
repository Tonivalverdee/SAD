
# Recopilación Pasiva de Información utilizando Google Hacking y Shodan

**Antonio Valverde Soto**  
2º ASIR

---

## Índice
- Enunciado de la tarea
- Resolución de la tarea
  - Ejercicio 1
  - Ejercicio 2
  - Ejercicio 3
  - Reflexión ética

---

## Enunciado de la tarea

**Tarea:** Recopilación Pasiva de Información utilizando Google Hacking y Shodan

**Objetivos:**

Aplicar los conocimientos teóricos sobre la recopilación pasiva de información en un ejercicio práctico.

Explorar y utilizar técnicas de Google Hacking para la obtención de información sensible y expuesta en Internet.

Aprender a usar Shodan para identificar dispositivos y servicios expuestos públicamente.

Reflexionar sobre las implicaciones éticas del uso de estas herramientas.

**Instrucciones:**

### Parte 1: Google Hacking

**Búsqueda en Google:**  
Elige una organización ficticia o real (para la cual tienes autorización). Utiliza los comandos avanzados de Google para recopilar información pasiva.

Realiza al menos 5 búsquedas avanzadas utilizando comandos como `site:`, `filetype:`, `intext:` y combinaciones de operadores booleanos como `OR` o `-`.

Documenta tus búsquedas y los resultados obtenidos en un informe.  
Nota: No utilices estas técnicas en sitios no autorizados (contenido para adultos, web del Centro, o páginas de contenido ilícito).

**Consulta con Google Dorks:**  
Accede a la Google Hacking Database (GHDB) en el sitio de Exploit DB.  
Selecciona 3 Google Dorks que te parezcan relevantes para obtener información sensible, como contraseñas, archivos de configuración, o datos expuestos en servicios como Trello o GitHub.

Realiza las búsquedas en Google y documenta los resultados, siempre garantizando la legalidad y la ética de las búsquedas.

### Parte 2: Shodan

**Exploración de Shodan:**  
Crea una cuenta gratuita en Shodan.io (si no la tienes ya).

Realiza 3 búsquedas avanzadas en Shodan, usando filtros como `port:`, `country:`, o `org:`, para identificar dispositivos o servicios expuestos en internet.

Por ejemplo, puedes buscar servidores FTP o cámaras IP expuestas.

Documenta las IPs encontradas, su ubicación geográfica y cualquier información adicional relevante.  
No intentes interactuar con los dispositivos que encuentres.

### Parte 3: Reflexión ética

Redacta un breve ensayo (máximo 500 palabras) reflexionando sobre los posibles riesgos y consecuencias de utilizar herramientas como Google Hacking y Shodan en sistemas no autorizados. ¿Cuáles son las responsabilidades éticas y legales de un hacker ético en este contexto?

---

## Resolución de la tarea

### Ejercicio 1

Voy a usar una organización llamada PcComponentes, para ello primero voy a buscar la página PcComponentes, por medio del comando site.

Al buscar de esta forma, únicamente me muestra resultado acerca de la página pccomponentes.com.

Ahora a continuación voy a mostrar los archivos pdf por ejemplo que tengan en PcComponentes.

Ahora he usado el comando filetype, y he especificado la extensión pdf, de tal manera que me va a mostrar únicamente los archivos pdf que tenga públicos la página PcComponentes.

Con esta búsqueda, al poner el comando intext le estoy diciendo, que dentro del dominio especificado, me muestre todas las páginas que contengan algo relacionado con Asus.

Al ponerle `site:linkedin.com “PcComponentes”`, me muestra perfiles de linkedin relacionados con PcComponentes, ya sea la cuenta de la misma empresa, o cuentas de trabajadores que trabajen en PcComponentes.

Ahora no he podido buscar a través de la página PcComponentes, ya que no muestra públicos archivos ini, por eso le he quitado el comando de site, pero al poner únicamente `filetype:ini “password” OR “user”`, estoy diciendo que me muestre los archivos ini que contentan esos parámetros.

Muchos de estos comandos se pueden combinar para obtener más información acerca de una página.

### Ejercicio 2

En la página Exploit DB, busco Google Hacking, y accedo a la base de datos de Google Hacking.

He elegida por ejemplo la primera línea de la base de datos, que es de un repositorio de GitHub.

Aquí en este repositorio de GitHub, podemos ver un rsa privado de ssh.

Este es otro Google Dork, también mostrado en la página ExploitDB

Y este de aquí es otro, Google Dork.

### Ejercicio 3

A continuación voy a utilizar el programa shodan, el cuál es muy potente para detectar vulnerabilidades de diferentes IPs o páginas web. En este caso he buscado con el comando country todas las IPs que tengan un puerto abierto, ya sea el 8080 (por defecto de internet) o cualquier otro.

Esta IP por ejemplo, tiene difentes vulnerabilidades, las cuales nos muestra shodan, la IP en cuestión es la 5.175.40.174.

Ahora filtro más la búsqueda, especificando el puerto al 443 con el comando port, este puerto es el puerto por defecto de HTTPS.

En este caso, esta IP tiene una cantidad grande de registros de vulnerabilidades, hay vulnerabilidades detectadas desde 2006.

Al ponerle org, estoy diciendo que sea de una organización, lo que significa que el dominio es .org.

Este es el primer resultado que me ha mostrado esta búsqueda, hay también vulnerabilidades registradas, tanto de 2024, como desde 2013 hasta 2007, sin contar 2010 ni 2008.

---

## Reflexión ética

Al buscar usando este tipo de filtros o comandos con herramientas como Google Hacking o Shodan, podemos acceder a sitios web a los cuales no estemos autorizados a entrar, lo cuál puede generar represalias para el buscador, hay recomendaciones si vas a entrar a sitios de ese tipo, como usar máquinas virtuales con adaptador NAT, utilizar navegadores como Tor, ya que pueden llegar a ocultar tu IP, no obstante hay que ser consciente de que siempre pueden llegar a rastrearte.

Pero no es lo que buscamos nosotros, ya que el ámbito del Hacking se basa en fines éticos, con autorización de las personas a las que se les van a realizar auditorías utilizando técnicas como Pentesting o similares, de lo contrario, ya sería algo ilegal y no son los principios del Hacking, ya que pasar a ser Cibercriminal o Ciberdelincuente, este tipo de actos, afectan mucho a los hackers, ya que manchan su nombre, debido a que la gente llama hacker a los crackers, cibercriminales, etc.

A día de hoy, un hacker es muy importante, ya que puede detectar vulnerabilidades que a simple vista, para una persona sin conocimientos, no piensa que pueda tener, también hay que saber que nunca somos completamente invulnerables, ya que siempre que estemos conectados a internet, podemos recibir algún tipo de ataque, ya sea por técnicas como Phishing, Ataques DDoS, Troyanos, etc. por ello y por mucho más, en un empresa es recomendable que sólo sea administrador una persona con los conocimientos suficien...
