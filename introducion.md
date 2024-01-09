Nginx es un servidor web de alto rendimiento diseñado para servir aplicaciones escalables de alto rendimiento de manera eficiente y receptiva. Se puede utilizar para servir contenido estático, equilibrar la carga de solicitudes HTTP, proxy inverso FCGI/PSGI/USWGI y conexiones TCP arbitrarias. Dado esto, es importante poder configurar e implementar de forma segura las instalaciones de Nginx para proporcionar una interfaz web segura para tu aplicación y minimizar las superficies de ataque.

Fue creado para solucionar las principales limitaciones de rendimiento de Apache, por ejemplo el llamado problema c10k que se produce a partir de 10.000 conexiones simultáneas a una web.

## Funcionamiento
El funcionamiento base de Nginx es similar al de otros servidores web, en el que un usuario realiza una petición a través del navegador al servidor, y este le envía la información solicitada al navegador.

Lo que hace diferente a Nginx es su arquitectura a la hora de manejar procesos, ya que otros servidores web como Apache crean un hilo por cada solicitud.

Es decir, cada vez que un usuario haga una petición al servidor, por ejemplo entrando en la web, se creará un hilo nuevo.
Nginx funciona de una forma más eficiente gracias a la arquitectura asíncrona basada en eventos, en la que en vez de crear un hilo por cada petición, lo gestiona todo bajo el mismo proceso de trabajo donde se gestionan los diferentes hilos.

Este hilo o proceso de nginx contiene varios microprocesos o llamadas de trabajo. Esto se traduce en un mejor rendimiento de Nginx frente Apache sobre todo en consumo de memoria.
