---
marp: true
theme: default
class:
    - invert
--- 

# **Proyecto Ataque Inyección SQL** 👨‍💻💉💻️
<!--    Notas para diapositivas
    ¿Qué es una inyección SQL?
    La inyección SQL, o SQLi, es un tipo de ataque a una web que permite a un atacante insertar sentencias SQL maliciosas, obteniendo potencialmente acceso a datos sensibles en la base de datos o destruyendo estos datos.
-->

```
select * 
from products 
where tag = 'pets' 
or 1=1 UNION SELECT * FROM users---
```

___
<!--COMIENZO DE LA PARTE 1-->
# **¿Por qué es necesario prevenir el inyección SQL?**
Una inyección SQL es un tipo de ataque a una web que permite a un atacante insertar sentencias SQL maliciosas, obteniendo potencialmente acceso a datos sensibles en la base de datos o destruyendo estos datos.

Si la entrada no se sanea correctamente, los hackers pueden usar estas áreas para inyectar comandos SQL maliciosos que engañen a la base de datos para que ejecute comandos no deseados.

Para el objetivo de un ataque de inyección de SQL exitoso, el impacto suele ser grave.






___
# **¿Qué impacto podría llegar a suponer éste tipo de ataque?**
<!--Yo, Si soy-->
Un ataque de inyección de SQL exitoso puede permitir a quien lo lleva a cabo:

- Extraer y divulgar información sensible.
- Eliminar el contenido de la base de datos.
- Manipular transacciones.
- Forzar la escalada de privilegios y convertirse en administrador del servidor de base de datos.   
- Modificar datos y archivos de las bases de datos.
- Intrusión en la página web.
- Robo de identidad.

___

 ## **¿Qué pasos seguirías para prevenir ataques de inyeccion SQLi?** 
 
 ### **Plan de formación para los desarrolladores** 

  
- **No confiar en ninguna entrada de usuario**
<!--Cualquier entrada de usuario que utiliza autentificación SQL representa un potencial riesgo de inyección SQL. 

Así que, es recomendable tratar a todas las entradas del usuario como si no fuesen de confianza.-->

- **Usa listas blancas, no listas negras**
<!--Filtrar las entradas de usuario mediante listas blancas en vez de listas negras.-->

- **Utiliza las últimas tecnologías**
<!--Muchas tecnologías de desarrollo web antiguas no cuentan con protección SQLi.-->

- **Emplear mecanismos verificados**
<!--Se debe evitar intentar construir protección SQLi desde cero.  
La mayoría de las tecnologías de desarrollo modernas te ofrecen mecanismos de protección contra ataques SQLi.--> 

- **Escaneos regulares**
    - Las SQLi pueden ser introducidas por los desarrolladores o a través de librerías externas



---
# **Vulnerabilidad** - **CVE-2022-27175**

## **Descripción de la vulnerabilidad**

DIAEnergie de la empresa Delta Electronics tiene una vulnerabilidad a partir del 29 de marzo de 2022. Las versiones afectadas son todas las anteriores a la 1.8.02.004.

**Métricas CVSS**

Overall: 9.8
Impacto: Completo

---

## **Tipo de vulnerabilidad**

- SQL Injection permite al atacante enviar o “inyectar” instrucciones SQL de forma maliciosa y malintencionada dentro del código SQL programado para la manipulación de bases de datos, de esta forma todos los datos almacenados estarían en peligro.

## **Tipo del exploit**

Es una blind SQLi la cuál existe en el parámetro GetCalcTagList. Esto significa que ese parámetro es inyectable pero que no daría señales de que esta funcione, es decir que si hacemos una inyección válida la respuesta en todos los casos será de error.

---

## **Efectos del exploit**

El exploit de esta vulnerabilidad permitirá al atacante inyectar secuencias SQL, recibir y modificar el contenido de la base de datos, y ejecutar comandos del sistema.

## **Solución o parche que se publicó.**

Delta Electronics ha arreglado las vulnerabilidades reportadas y recomienda a los usuarios a actualizar a la versión 1.9 o superior. También

- Minimice la exposición de la red para todos los dispositivos y/o sistemas de sistema de control, y asegúrese de que no sean accesibles desde Internet.
- Utilizar un firewall que pueda detectar ataques contra la debilidad de "Path Traversal" y "SQLi".
- Cuando se requiera acceso remoto, use métodos seguros, como VPN.
<!--Final de la parte 1-->

<!--Parte 2-->
---
<!--No tocar esta realizado-->
# 10 tipos de ataques informaticos mas habituales

1. ### **Virus**: 
El virus es un código que infecta los archivos del sistema mediante un código maligno, pero para que esto ocurra necesita que un usuario lo ejecute. Una vez que este entre en funcionamiento, se exparce por todo el sistema y todo elemento de nuestro ordenador y son capaces de propagarse a otros dispositivos de la red interna. Depende del tipo de virus sea es capaz de eliminar archivos del ordenador, hacerse con el completo crontol del dispositivo o sino molestar al usuario mostrandole imagenes por pantalla o bloqueando el sistema. Formas de solucionar o prevenir el problema Instala un software antivirus, mantener actualizado el antivirus y el sistema en versiones estables 

---
2. ### **Spyware**:
 Es un programa espía, cuyo objetivo principal es obtener información. Su fomra de actuar es de forma oculta, sin ser detectado, para que puedan recolectar información sobre nuestro equipo sin despertar nuestra preocupación, e incluso instalar otros programas sin que nos demos cuenta de ello. Formas de solucionar el problema es descargando algun antivirus sea capaz de detectar los sypware que tendramos instalado en nuestro ordenador y haciendo un analisis de sistema gradualmente y haciendo una limpieza de archivos basura

---
3. ### **Adware**:
La función principal del adware es la de mostrar publicidad de forma invasiva. Aunque su intención no es la de dañar equipos, es considerado por algunos una clase de spyware, ya que puede llegar a recopilar y transmitir datos, tambien existes algunos adware en formato de extension de navegador que se puede llegar a instalar de forma erronea. Formas de solucionarlo Hacemos un analisis completo del ordenador y con un antivirus hacemos un escaneo a ver si detectamos algun archivo extraño, lo mas probable que los adware sea alguna aplicaccion que haya instalado por eso deberiamos desinstalarla y configurar el navegador para que no nos instale extensiones desconocidas 

---
4. ### **Troyano**:
 Son similares a los virus, pero persiguiendo objetivos diferentes. Mientras que el virus es destructivo por sí mismo, el troyano lo que busca es abrir una puerta trasera para favorecer la entrada de otros programas maliciosos. pasar desapercibido e ingresar a los sistemas sin que sea detectado como una amenaza potencial. No se propagan a sí mismos y suelen estar integrados en archivos ejecutables aparentemente inofensivos. Formas de solucion tener un buen antivirus que analice cualquier fichero malicioso y que antes de ejecutar alguna fichero extraño sepamos de donde viene su origen.

 Solucion:

---
5. ### **Ransomware**:
 ransomware es un tipo de malware que impide a los usuarios acceder a su sistema o a sus archivos personales generalmente cifrándola, y solicitando un rescate a cambio de su liberación. forma de solucionarlo es haciendo copias de seguridad del archivo y teniendo configurado el cortafuego


---
<!--- 


Se han identificado y descrito los tipos de ataques mas comunes correctamente (5pt)

Se han analizado los tipos de ataque exponiendo el posible alcance y las posibles soluciones correctamente(5pt)



-->

6. ### **Doxing**: 
El doxing es el acto de revelar información personal de una persona tales como su nombre real, su dirección particular, su lugar de trabajo, su telefóno, datos financieros. El doxing puede ser hecho de varias formas, como por ejemplo ejecutar una búsqueda WHOIS en relación con un nombre de dominio, este es efectivo si la persona que compro el dominio no oculto su información privada en el momento de la compra, otra de estas es mediante "sniffing" el cual es el analisis de paquetes.  Esto podria conllevar a perjudicar la reputación del trabajador y la de sus compañeros.
Una de las formas de protegerse sería la de utilizar una VPN para proteger su dirección IP, usar contraseñas seguras, diferentes nombres de usuario en cada plataforma y revisar y utilizar la privacidad maxima posible en las redes sociales.

---
7. ### **Pishing**:  
Se trata de diversas técnicas de “Ingeniería social” como la suplantación de identidad. Esto puede conllevar a perdidas de fondos corporativos, exposición de información personal de clientes y de compañeros de trabajo y el robo o perdida del acceso a archivos confidenciales, todo esto influye en la perdida de reputación de la empresa.
Esto se puede evitar de varias formas, la primera es que evites acceder a páginas web a traves de enlaces, lo recomendado es que se ingrese la url manualmente, otra forma es asegurarte de que tu antivirus este actualizado y que tenga herraminetas antiphishing

---
8. ### **Denegacion de servicio(DDOS)**: 
Un DDoS(Distribute Denial of Service) es un tipo de ataque el cual se aprovecha de la limitación de capacidad que se tienen en cuanto los recursos de red. El ataque DDoS envia gran cantidad de solicitudes al recurso web atacado con el fin de superar la capacidad del sitio web para gestionar tantas solicitudes y evitando que  funcione correctamente. Esto afectara al servicio de la siguiente forma:
- La respuesta a las solicitudes será mucho más lenta de lo normal.
-  Posibilidad de que se ignoren algunas (o todas) las solicitudes de los usuarios.

Estas son las formas para protegerte en contra de estos ataques
- Ubicar el servidor web en una zona desmilitarizada (entre cortafuegos), también llamada DMZ, evitando así que un intruso pueda acceder a la red interna si vulnera el servidor web.
- Implementar un sistema de detección y prevención de intrusiones (IDS/IPS) que monitorizan las conexiones.

---
9. ### **Inyeccion SQL**: 
Una inyección SQL es un tipo de ataque a una web que permite a un atacante insertar sentencias SQL maliciosas, obteniendo potencialmente acceso a datos sensibles en la base de datos o destruyendo estos datos. Cuando este tipo de ataque tiene exito las siguientes cosas pueden ser posibles.

- Extracción y divulgación de información sensible.
- Eliminación del contenido de la base de datos.
- Manipulación de  transacciones.
  
- Modificar datos y archivos de las bases de datos.

Para evitarlo puedes intentar hacer las cosas que menciono a continuacion, puedes utilizar las últimas tecnologías, ya que algunas de las aplicaciones de desarrollo web antiguas estan desprotegidas ante ataques Sqli, esto tambien incluye el uso de mecanismos verificados ya que suelen estar protegidos ante esos ataques



---
10. ### **Gusano**: :worm:
El principal objetivo de los gusanos es propagarse y afectar al mayor número de dispositivos posible. Para ello, crean copias de sí mismos en el ordenador afectado, que distribuyen posteriormente a través de diferentes medios, como el correo electrónico o programas P2P entre otros.

Los gusanos suelen utilizar técnicas de ingeniería social para conseguir mayor efectividad. Para ello, los creadores de malware seleccionan un tema o un nombre atractivo con el que camuflar el archivo malicioso. Este virus suele ser creado con el objetivo de colapsar ordenadores y redes informaticas, la diferencia que tiene con un virus es que el gusano no infecta archivos.

Para protegerse de esto es igual que con los virus:
- Evita abrir mensajes y archivos adjuntos desconocidos
- No utilices páginas web no seguras

---
 
# **Fases de un Ciberataque**
Conocer cómo actúan los ciberdelincuentes es una buena manera de poder prevenir, detectar y en el peor de los casos, remediar sus ciberataques. Consta de 7 fases denominadas cyber kill chain. :chains:

A continuacion analizaremos cada una de la diferentes fases;

---
# **Fase 1 Reconocimiento** :mag:

El ciberdelincuente recopila información sobre la empresa o el sujeto en cuestión dichas acciones pueden ser buscar información pública sobre la empresa, observar que tipo de tecnología utiliza y buscar datos relevantes de empleados por las redes sociales.
 La mejor forma de prevenir es formando a tus empleados para que obtengan un verdadera conscincia de la importancia de sus datos y de la privacidad de estos en internet 

---
# **Fase 2 Preparacion** :stew:
 Una vez que el atacante ha recopilado toda la informacion relevante prepara el ataque sobre el objetivo. Por ejemplo un atacante podria crear un documento PDF e incluirlo en un correo electronico que suplante la identidad de una persona legitima con al que la empresa interactue normalmente (fishing) :fishing_pole_and_fish:
 
Una vez más, tener un plan de concienciación en ciberseguridad es el mejor mecanismo para frenar el ataque en esta fase.


---
# **Fase 3 Distribucion** :e-mail:
 En esta fase se produce la transmision del ataque tras la ejecucion de una accion por parte de la victima un ejemplo podria consistir en la la descarga de  un documento por parte de la victima.

 Ser consientes de la existenncia de este tipo de ataques y aprender a identificarlos sera nuestra primera linea de defensa.
 
---
 # **Fase 4 Explotación**  :volcano:
Esta etapa es en la que el atacante compromete el equipo infectado y su red. Esto implica la *"detonación"* :bomb: del ataque, que se suelen conseguir explotando una vulnerabilidad para la que lo más probable es que exista un parche de seguridad pero no esté operativo. Al no estar parcheada, se deja una *puerta abierta* y los equipos del exterior podrán entrar y efectuar el ciberataque. Es importante contar con soluciones de seguridad y mantener todos los sistemas, incluido el antivirus, actualizados a su última versión  para evitar quedar expuesto.

---
# **Fase 5 Instalación** :inbox_tray:
Fase en la que el atacante instala el malware en la víctima. Pero también hay circunstancia en las que no se requiera instalación, como en el robo de credenciales :fishing_pole_and_fish:. En cualquier caso, una correcta formacion en ciberseguridad será la mayor medida a tomar en esta fase, junto con medidas técnicas como la monitorización del estado de los sistemas, ya sea mediante infraestructura propia o a través de seguridad gestionada o subcontratando personal o servicios. 

---
# **Fase 6 Comando y control** :video_game:
Llegados a este punto el atacante cuenta con el control del sistema de la víctima, en el que podrá realizar o desde el que lanzar sus acciones maliciosas dirigidas desde un servidor central conocido como C&C (Command and Control), llevarse documentación confidencial, instalar otros programas, conocer cómo es la red del usuario, etc. 
Contar con medidas de control de acceso a la información (2FA) y una conciencia de la privacidad y del valor de los datos, es fundamental para reducir el alcance del ataque.

---
# **Fase 7 Acciones sobre los objetivos** :smiling_imp:
Esta es la fase final en la que el atacante se hace con los datos e intenta expandir su acción maliciosa hacia más objetivos. Esto explica por qué la kill chain no es lineal sino cíclica, ya que se volverían a ejecutar todas y cada una de sus fases de cara a infectar a más víctimas.

---
# **Concluciones**
Para poder romper la cadena y evitar que un ataque consiga sus objetivos es necesario estar verdaderamente comprometido con la ciberseguridad. Una organización que mantenga todos sus sistemas y equipos actualizados, utilice las soluciones de seguridad adecuadas, monitorice la actividad de sus comunicaciones y sus empleados cuenten con los conocimientos necesarios en ciberseguridad, aumenta considerablemente su capacidad para detectar y responder ante este tipo de incidentes de seguridad, poniéndoselo mucho más difícil a los adversarios y evitando que los sistemas y la información que en ellos se almacena se vean comprometidos.



 