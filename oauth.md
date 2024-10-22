# OAuth
*Open Authorization* es un estandar abierto que permite flujos simples y
estandarizados de autorización para sitios web o aplicaciones. Es un método de
acceso delegado. OAuth nace impulsado por personal de twitter cuando
implementaban OpenID y se vuelve un estandar en la discusión abierta de la
**Internet Engineering Task Force (IETF)**

OAuth permite a un proveedor de servicio compartir el _acceso_ a su información
sin tener brindar credenciales a terceros actores. OAuth está diseñado para la
web, es decir para http, su funcionamiento más simple es que un tercero através
de un servidor de autenticación y con el token adecuado puede acceder al
servidor que contiene los recursos que necesita. Se le llama "3-legged OAuth".

<center>
    <p><a href="https://commons.wikimedia.org/wiki/File:Abstract-flow.png#/media/File:Abstract-flow.png"><img src="https://upload.wikimedia.org/wikipedia/commons/7/72/Abstract-flow.png" alt="A high-level overview of Oauth 2.0 authorization flow." height="603" width="835"></a><br>By <a href="//commons.wikimedia.org/w/index.php?title=User:Devansvd&amp;action=edit&amp;redlink=1" class="new" title="User:Devansvd (page does not exist)">Devansvd</a> - <span class="int-own-work" lang="en">Own work</span>, <a href="https://creativecommons.org/licenses/by-sa/4.0" title="Creative Commons Attribution-Share Alike 4.0">CC BY-SA 4.0</a>, <a href="https://commons.wikimedia.org/w/index.php?curid=109591026">Link</a></p>
</center>

OAuth 2.0 no es compatible con OAuth1. OAuth2 proporciona flujos de autorización
específicos para aplicaciones web, aplicaciones de escritorio, teléfonos móviles
y otros dispositibos.

## Fallos de seguridad
OAuth1(2009) tuvo un problema de fijación de sesión, esta vulnerabilida afectaba
al flujo de autorización de OAuth.

OAuth 2.0 ha sido objeto de análisis de seguridad, destacando amenazas como la
del "Open Redirector" y su variante "Covert Redirect", en el cual un servidor
malicioso puede confundir a los clientes para que envíen información sensible al
servidor incorrecto. Este problema llevó a la creación de un nuevo estándar de
seguridad para OAuth 2.0 que ha demostrado ser rebusto. 

En 2017, aproximadamente un millón de usuarios de Gmail fueron atacados mediante
phishing basado en OAuth. Los atacantes enviaban correos simulando ser contactos
conocidos, solicitando acceso a un supuesto documento en Google Docs, lo que en
realidad permitía a una aplicación maliciosa acceder a correos, contactos y
documentos. Google detuvo el ataque en aproximadamente una hora. En este caso el
ataque no fue explotando una vulnerabilidad del flujo de autenticación sino del
propio usuario.
