al ser un servicio simple, lo hace un buen objetivo para atacar, algunos de los principales ataques que tiene son:

### DHCP Starvation
Gasta las direcciones para que los clientes legítimos no puedan conectarse

Hace un ataque DoS con el que inunda al servidor con DHCP Discover, usa también MAC Spoofing para hacerse pasar por otros dispositivos.

Su principal implicación está en la disponibilidad, ya que deja de dar servicio a clientes.

Esto pasa porque tiene que responder a todas las peticiones, con lo que no diferencia entre una petición maliciosa de una buena, agotando todas las direcciones posibles.

Se puede solucionar monitoreando DHCP Requests inusuales.

### Rogue: 
El atacante configura un servidor malicioso que asignte configuraciones (generalmente Gateway) con la que conseguir todo el tráfico.
Por ejemplo, un atacante crea un nuevo servidor DHCP que asigna como Gateway por defecto uno comprometido con el que puede acceder a todo el tráfico del cliente.

Este ataque afecta al principio de la confidencialidad, ya que tiene acceso a todo el tráfico del cliente.

Se puede implementar un DHCP Snooping que excluya los paquetes de los servidores DHCP no legítimos

### Replay
Reenvía mensajes DHCP  de clientes legítimos para suplantar su identidad.

Este ataque afecta tanto a Confidencialidad, ya que puede ganar acceso a la red, Integridad, porque ha manipulado paquetes de la red, como a Disponibilidad, ya que el cliente legítimo puede no tener acceso a la red.

Se pueden implementar opciones de autenticación de DHCP.


https://arxiv.org/html/2502.10646v1
