title:: Cloud Computing and DevOps Culture Tema-5 (highlights)
author:: [[UNIR]]
full-title:: "Cloud Computing and DevOps Culture Tema-5"
category:: #books

tags:: #[[Cloud-Computing-and-DevOps-Culture]] #[[UNI]]

- #tags #[[Cloud-Computing-and-DevOps-Culture]] #[[UNI]]
- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/531d5576-c016-4406-9071-e6f73b67516f.jpg)
- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- -
	- El primer caso de uso de la virtualización suele ser la consolidación de servidores. Esta se refiere a tomar instancias separadas del servidor y migrarlas a máquinas virtuales que se ejecutan en un único servidor. Pero además de ello, la consolidación de #car
	  id:: 634014fd-3e61-42aa-ac1c-636c2a7c3ede
		- servidores también puede ser entendida como el acto de coger numerosos servidores separados  y  migrarlos  a  menos  servidores,  con  múltiples  máquinas  virtuales ejecutadas en cada servidor. Las  empresas  que  implementan  la  consolidación  de  servidores  experimentan  una profunda  transformación:  pasan  de  ejecutar  150  servidores  físicos  a  ejecutar  150 máquinas  virtuales  en  solo  quince  servidores,  lo  que  redunda  en  una  enorme reducción  de  costes  e  inversión  de  hardware,  energía  y  refrigeración,  empleados, tiempo  y,  en  muchos  casos,  costes  de  licencias  de  software.  Por  tanto,  podemos afirmar que la consolidación de servidores puede llegar a ofrecer un 60 % u 80 % de mejora de utilización de recursos.
		- (Page 5)
	- -
	- -
	- Acerca de la virtualización en la nube privada #car
	  id:: 634014fd-812e-499d-9d0f-aee90a8173d4
		- En  pocas  palabras,  la  computación  en  la  nube  es  un  medio  para  proporcionar servicios de tecnología bajo demanda a través de Internet. Una nube privada es un entorno  donde  estos  servicios  operan  para  una  única  organización.  Numerosas organizaciones  de  TI  están  explorando  cómo  construir  sus  propias  nubes  privadas para aumentar la agilidad y reducir sus costes. La virtualización es un componente clave  de  las  nubes  privadas  porque  permite  un  rápido  aprovisionamiento  y desaprovisionamiento de servicios bajo demanda.
		- (Page 6)
	- -
	- -
	- ¿Cómo funciona la alta disponiblidad? #car
	  id:: 634014fd-08c2-4fc1-85f8-9c0bdb06eb8d
		- ¿Cómo es posible que un hipervisor, en un servidor físico, inicie una máquina virtual en  otro  hipervisor?  La  respuesta  es  clara:  no  es  posible.  No  puede.  La  alta disponibilidad  se  basa  en  un  software  de  virtualización  global  que  coordina  los esfuerzos de múltiples hipervisores. Cuando una máquina virtual en un servidor de hardware falla, el software de coordinación inicia una nueva máquina virtual en un servidor de hardware separado. En  realidad,  es  un  poco  más  complejo  que  eso.  El  software  de  coordinación  de virtualización  monitoriza  constantemente  todos  los  hipervisores  y  sus  máquinas virtuales.  Si  el  software de  coordinación  ve que el hipervisor en  un  servidor  ya no responde,  reinicia  las  máquinas  virtuales  del  hardware  que  ha  fallado  en  otro hardware.  Por  lo  tanto,  la  alta  disponibilidad  aborda  el  problema  del  fallo  del hardware  mediante  el  uso  de  un  software  de  virtualización  de  mayor  nivel  para coordinar los hipervisores en dos o más máquinas, a través de la monitorización continua y el reinicio de máquinas virtuales en otras máquinas si es necesario.
		- (Page 7)
	- -
	- -
	- Acerca del clustering #car
	  id:: 634014fd-d429-4f4e-946b-f17775ca0753
		- El agrupamiento está diseñado para garantizar que no se pierdan datos en caso de que  haya  un  fallo  de  software  o  de  hardware.  El  clustering  ha  sido  ofrecido, históricamente,  por  los  proveedores  de  aplicaciones  como  complemento  de  otros productos,  pero  con  algunos  inconvenientes  relacionados:  gastos  adicionales, soluciones  redundantes  e  infraestructura  compleja.  El  gasto  extra,  o  adicional,  se produce por la necesidad de contar con hardware adicional, con el sistema en espejo en  espera  (en  modo  standby),  listo  para  asumir  el  control  si  fallase
		- (Page 8)
	- -
	- -
	- Acerca de la réplica de datos #car
	  id:: 634014fd-5cdd-4f78-8d60-2afa614e781c
		- La replicación es otro servicio orientado a mejorar la calidad del servicio de datos. A diferencia de la duplicación (data mirroring) que se enfoca en cómo mantener copias de  datos  consistentes  en  tiempo  real,  la  replicación  aborda  la  necesidad  de mantener  copias  completas  de  los  datos  para  que  puedan  ser  utilizados  en  la reconstrucción  del  sistema.  Esto  se logra  enviando  copias  de  datos  a  un almacenamiento centralizado, lo que permite a una organización tener la seguridad de que en caso de que necesite acceder a los datos críticos por algún motivo, estos están almacenados de forma segura y disponibles en caso de ser necesarios.
		- (Page 10)
	- -
	- -
	- ¿Qué significa ser "ágil"? #car
		- Las organizaciones de TI deben estar preparadas para responder ante los cambios y las condiciones de negocio. Es por ello por lo que no hay mejor palabra para definir esta  cualidad  que  el  adjetivo  «ágil».  Cuando  pensamos  en  un  atleta  ágil, probablemente  imaginamos  a  alguien  que  puede  cambiar  de  rumbo  rápidamente, detenerse o cambiar la dirección para adaptarse a lo que sucede en el entorno que le rodea. actualidad: Como  es  sabido,  estos  son  los  requisitos  para  las  organizaciones  de  TI  en  la   Deben ser lo suficientemente flexibles como para aumentar o reducir los recursos informáticos que dedican al desarrollo de sus aplicaciones.   Deben  implementar  infraestructura  y  procesos  que  reduzcan  la  cantidad  de trabajo manual para cambiar los recursos informáticos que utilizan. En resumen, la organización de TI actual debe estar lista para moverse rápidamente en  cualquier  dirección  a  fin  de  responder  a  los  cambios  internos  o  externos  del entorno.
		- (Page 11)
	- -
	- -
	- Acerca de un pool de servidores virtualizados #car
	  id:: 634014fd-cf8f-44c7-b7ae-b9ae9749fee1
		- Con  la  agrupación  de  servidores,  el  software  de  virtualización  gestiona  un  grupo (pool)  de  servidores  virtualizados.  En  lugar  de  instalar  una  VM  en  un  servidor  en particular, simplemente se apunta el software de virtualización a la imagen de la VM y este software determina qué servidor físico es el más adecuado para ejecutar la VM. El software del pool de servidores también realiza un seguimiento de cada VM y  servidor  para  determinar  cómo  se  asignan  los  recursos.  Si  una  VM  necesita  ser reubicada para utilizar mejor los recursos disponibles, el software de virtualización automáticamente migra la VM a un servidor más adecuado. El pool se gestiona a través de una consola de administración y, si se advierte que este  está  alcanzando  su  tasa  de  utilización  máxima,  se  puede  agregar  de  forma transparente  otro  servidor  adicional  al  grupo.  A  continuación,  el  software  de virtualización  reequilibra  las  cargas  para  que  el  uso  de  todos  los  recursos  de  los servidores sea lo más efectivo posible. Debido a que no se puede saber qué servidor físico ejecutará la máquina virtual, el almacenamiento debe estar conectado en red para que una VM en cualquier servidor pueda acceder a los datos. Sin lugar a duda,  aquí está la semilla del futuro de la virtualización. En un futuro próximo, los departamentos de TI dejarán a un lado la instalación manual sistemas operativos en servidores individuales, o incluso en la gestión de clústers de máquinas virtuales en servidores individuales, debido a que son prácticas ineficientes.
		- (Page 13)
	- -
	- -
	- Sobre las cosas 'cool' en el trabajo #car
	  id:: 634014fd-af82-451a-9a65-c0dcc5bf690d
		-   No evites hacer el trabajo que consideras aburrido. Es divertido instalar software y  ver  surgir  cosas  nuevas.  No  es  tan  divertido  utilizar  entrevistas  de  casos  o revisiones técnicas. Pero ten en cuenta que esas tareas «aburridas» hacen posibles a las cosas divertidas. De hecho, a menos que completes estas tareas aburridas, probablemente  no  obtendrás  el  visto  bueno  para  avanzar  con  el  proyecto  y divertirte haciendo las cosas interesantes.
		- (Page 27)
	- -