title:: SecDevOps Tema-6 (highlights)
author:: [[UNIR]]
full-title:: "SecDevOps Tema-6"
category:: #books

tags:: SecDevOps UNI

- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/d7095b61-4205-46b6-b02a-77b13111959c.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- ¿Qué se conoce como VNet? #flashcard
		  id:: 94571dfd-48d5-407d-a3cf-88671cc756ed
			- Azure Virtual Network (denominada también VNet) es una de las piezas esenciales para  la  infraestructura  de  red  privada  en  Azure  (Tullock,  2013).  VNet  permite  que muchos tipos de recursos de Azure, como las máquinas virtuales, se comuniquen de manera  segura  entre  sí,  con  Internet  y  con  las  redes  locales  on-premise.  VNet  es similar a la red tradicional de un centro de datos, pero tiene beneficios adicionales de la infraestructura nativa de nube, como la escalabilidad y alta disponibilidad.
		- (Page 5)
	- -
	- -
		- Algunos de los conceptos esenciales de VNet son:   Espacio de direcciones: al crear una red virtual, es necesario especificar un espacio de  direcciones  IP  privadas.  Azure  asigna  IP  de  este  espacio  a  los  recursos conectados a la red virtual. Por ejemplo, una VM desplegada en una red virtual con  espacio  de  direcciones  10.0.0.0/16  recibirá  una  IP  privada  dentro  de  esa subred, por ejemplo, 10.0.0.4.   Subredes: las subredes permiten segmentar la red virtual en una o más redes, y asignar una parte del espacio de direcciones de la red virtual a cada subred. Los recursos  podrán  desplegarse  en  la  subred  necesaria,  de  acuerdo  con  las necesidades de la arquitectura de los sistemas. Al igual que en una red tradicional, la segmentación de las subredes mejora la eficiencia de asignación de direcciones. #flashcard
		  id:: 3a708a9a-7d91-4f10-b3fb-9c96741c56a1
		- (Page 5)
	- -
	- -
		- Además, los recursos dentro de las subredes se pueden proteger utilizando grupos de seguridad de red.   Regiones: una región es un conjunto de centros de datos, implementados dentro de  un  perímetro  con  una  latencia  definida  y  conectados  a  través  de  una  red regional dedicada de baja latencia. Una VNet tiene un alcance para una sola región de Azure;  sin  embargo, se  pueden  conectar  varias  redes  virtuales  de diferentes regiones mediante el emparejamiento de redes virtuales.   Suscripción: una suscripción de Azure está vinculada a una sola cuenta, la que se utilizó  para  crear  la  suscripción  y  se  utiliza  para  fines  de  facturación  (es  un concepto similar al de cuenta en AWS). Los recursos se provisionan dentro de una suscripción.  Una  VNet  tiene  un  alcance  de  una  suscripción,  y  una  subscripción puede tener tantas VNets como sean necesarias. #flashcard
		  id:: c9078ff6-009a-4d08-9ef8-23ffddca0576
		- (Page 6)
	- -
	- -
		- Los recursos locales y las redes virtuales  en la nube se pueden  conectar mediante cualquier combinación de las siguientes opciones:   Red  privada  virtual  (VPN)  de  punto  a  sitio  (point-to-site):  en  este  caso,  cada equipo  de  la  red  local  que  necesite  conectarse  a  recursos  de  Azure  puede establecer una VPN. También se pueden denominar VPN de cliente. #flashcard
		  id:: fbc80026-7cfc-49c1-a116-d0d3e50900da
		- (Page 7)
	- -
	- -
		-   VPN de sitio a sitio (site-to-site): en este caso, un dispositivo VPN específico en la red local establece una conexión VPN con un Azure VPN Gateway. Este dispositivo VPN enruta el tráfico de las máquinas de la red local a la red virtual de Azure.   Azure  ExpressRoute:  esta  solución  establece  una  conexión  a  través  de  un colaborador de Azure. Al estilo de un servicio MPLS, este tráfico no se envía por Internet. #flashcard
		  id:: 9abffad2-38b0-4925-97ba-86ea57c25062
		- (Page 8)
	- -
	- -
		- Se pueden  definir  más  subredes  una  vez  creada  la  VNet  y,  como  se  ha  comentado previamente,  es  recomendable  mantener  un  espacio  de  direcciones  amplio  y segmentado para poder ampliar las subredes en el futuro #flashcard
		  id:: 3d327ed5-510a-4d10-be69-a7da0f26ae25
		- (Page 9)
	- -
	- -
		- Los  grupos  de  seguridad  de  aplicación  de  Azure,  o  application  security  groups, permiten  agrupar  máquinas  virtuales  e  interfaces  de  red  en  grupos  lógicos,  que pueden usarse en grupos de seguridad de red. Esto los convierte en una extensión natural de la estructura de la aplicación, ya que las reglas de los grupos de seguridad de red se pueden definir en base a objetos de la nube y no a IP específicas. #flashcard
		  id:: 975aebea-6c3b-450e-b32a-8d4968117782
		- (Page 10)
	- -
	- -
		- Los grupos de seguridad de red, o network security groups, funcionan como firewalls virtuales a nivel de interfaz de máquina virtual y de subred. Contienen listas de reglas definidas  a  partir  del  protocolo,  rango  de  IP  y  puertos  de  origen  y  rango  de  IP  y puertos de destino. Un mismo grupo de seguridad de red puede estar asociado a más de una interfaz y subred. #flashcard
		  id:: 2eaed3d5-5979-42ea-b723-1e260f7d3c36
		- (Page 11)
	- -
	- -
		- Un appliance se refiere a una máquina virtual que empaqueta el sistema operativo con un software específico. Se pueden distribuir como una imagen o plantilla lista para ser desplegada en un entorno de virtualización. #flashcard
		  id:: bb24a273-47e5-458e-880f-0109412b8908
		- (Page 17)
	- -
	- -
		- ¿Qué es un Juniper vSRX? #flashcard
		  id:: 0da37b02-e096-434e-9e6e-ed02471b9c12
			- El vSRX es un appliance virtual que ofrece servicios de seguridad y de red en entornos de  nube  pública  o  privada.  Se  conoce  como  firewall  de  nueva  generación,  o  next generation  firewall,  porque  no  solo  funciona  como  firewall  avanzado  (a  nivel  de paquetes  y  de  aplicación),  sino  también  como  rúter,  VPN,  NAT  o  IPS  (sistema  de detección y prevención de intrusiones).
		- (Page 18)
	- -
	- -
		- Las VPN de cliente sirven para dar acceso remoto a usuarios individuales. Son útiles, por ejemplo, para  usuarios itinerantes que necesitan acceder a los recursos de su organización, o para pequeñas oficinas en las que no merece la pena la inversión en un  dispositivo  de  VPN  corporativo,  y  prefieren  dar  acceso  individualmente  a  sus usuarios. #flashcard
		  id:: 987d1014-a645-4dce-a629-610aff636952
		- (Page 34)
	- -
	- -
		- Las VPN encapsulan el tráfico de la red origen en otros paquetes, y lo desencapsulan en  la  red  destino,  depositando  el  tráfico  como  si  ambas  redes  estuvieran interconectadas por un simple rúter. En el caso de la VPN de cliente, no hay red origen como tal. El cliente de VPN crea una interfaz de red virtual en el equipo del usuario. Cuando se establece la conexión, el cliente de VPN recibe una IP de la red destino, mediante el servidor DHCP de la VPN, y la configura en la interfaz virtual. A partir de ese momento, el tráfico que los procesos del equipo del usuario envíen a esa interfaz atravesará el túnel de la VPN y llegará a la red de destino. #flashcard
		  id:: 1acd545d-bbc8-4edd-b748-84c01cf55d83
		- (Page 34)
	- -