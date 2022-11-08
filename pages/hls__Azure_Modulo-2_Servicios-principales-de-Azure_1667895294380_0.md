file-path:: ../assets/Azure_Modulo-2_Servicios-principales-de-Azure_1667895294380_0.pdf

- ## 2.3 Servicios de computación
-
- Las {{cloze máquinas virtuales (Virtual Machines)}} son emulaciones de software de equipos físicos. Incluyen procesadores virtuales, memoria, almacenamiento y redes. Forma parte de la oferta de IaaS, lo que proporciona al usuario un control y personalización total. #flashcard
  hl-page:: 16
  ls-type:: annotation
  id:: 636a12a6-ac82-44a2-99e9-75c96f307016
  hl-color:: yellow
-
- El servicio de {{cloze aplicaciones de Azure (Azure App Services)}} es una plataforma totalmente administrada para crear, implementar y escalar aplicaciones web y API rápidamente. Forma parte de la oferta de PaaS, lo que permite al usuario abstraerse de la infraestructura subyacente y satisface requisitos de cumplimiento, seguridad y rendimiento de nivel empresarial. #flashcard
  hl-page:: 17
  ls-type:: annotation
  id:: 636a12b9-485c-4beb-bf97-58965d02339b
  hl-color:: yellow
-
- El servicio {{cloze de contenedores de Azure}} ofrece un entorno virtualizado ligero que no requiere administración del sistema operativo y puede responder a los cambios bajo demanda. #flashcard
  hl-page:: 18
  ls-type:: annotation
  id:: 636a12ca-9b33-401c-8407-29769435be99
  hl-color:: yellow
-
- Azure ofrece actualmente dos servicios de contenedores: #flashcard
  hl-page:: 18
  ls-type:: annotation
  id:: 636a12f3-658d-488e-aefb-8fe10650f831
  hl-color:: yellow
	-  **Azure Container Instances**: oferta de PaaS que ejecuta un contenedor en Azure sin la necesidad de administrar una máquina virtual o servicios adicionales.
	-  **Azure Kubernetes Service:** servicio de completo para la ejecución de contenedores con arquitecturas distribuidas y grandes volúmenes de contenedores.
	-
- El servicio {{cloze de escritorio virtual Windows (Windows Virtual Desktop)}} permite la virtualización de aplicaciones y escritorios Windows que se ejecutan en la nube. #flashcard
  hl-page:: 18
  ls-type:: annotation
  id:: 636a1319-9818-40c2-9c14-6436a4faa241
  hl-color:: yellow
-
- ## 2.4 Servicios de redes
-
- {{cloze Azure Virtual Network (VNet) que}} permite que los recursos de Azure se comuniquen entre sí, con Internet y con redes locales. #flashcard
  hl-page:: 19
  ls-type:: annotation
  id:: 636a136f-7e9a-44af-bb0b-e71f564f04d3
  hl-color:: yellow
-
- {{cloze Balanceador de carga (Azure Load Balancer) que}} permite habilitar alta disponibilidad y modular el rendimiento de red de las aplicaciones. #flashcard
  hl-page:: 20
  ls-type:: annotation
  id:: 636a137a-6fc6-4f9e-aa99-63d623851f3d
  hl-color:: yellow
-
- {{cloze Pasarela de aplicaciones/firewall de aplicaciones web (Application Gateway/WAF) que}} permite construir frontales web escalables y altamente disponibles. #flashcard
  hl-page:: 20
  ls-type:: annotation
  id:: 636a1380-df26-44e8-991e-36fbdadbe7b8
  hl-color:: yellow
-
- Protección contra ataques distribuidos de denegación de servicio (DDoS Protection) que permite proteger los recursos de Azure contra este tipo de ataques.
  hl-page:: 20
  ls-type:: annotation
  id:: 636a1384-bc4b-49d6-9813-c2784f6ab9f9
  hl-color:: yellow
-
- {{cloze Pasarela de red privada virtual (Virtual Private Network Gateway, VPN Gateway)}} que se usa para enviar tráfico cifrado entre una red virtual de Azure y una ubicación local a través de Internet público. #flashcard
  hl-page:: 20
  ls-type:: annotation
  id:: 636a138b-4801-4b9d-ae60-b32b02b280e9
  hl-color:: yellow
-
- {{cloze Azure Express Route (ER)}} que extiende las redes locales a Azure a través de una conexión privada que facilita un proveedor de conectividad. #flashcard
  hl-page:: 20
  ls-type:: annotation
  id:: 636a13a4-4cfa-4547-97e9-0901334b0808
  hl-color:: yellow
-
- Los servicios de almacenamiento de Azure proporcionan diferentes niveles de acceso que conviene conocer: #flashcard
  hl-page:: 22
  ls-type:: annotation
  id:: 636a14bf-e4d7-4abf-a494-7fc96e3596eb
  hl-color:: yellow
	-  **Frecuente**: Optimizado para almacenar datos a los que se accede con frecuencia.
	-  **Poco frecuente**: Optimizado para almacenar datos a los que se accede con poca frecuencia y se almacenan durante **al menos 30 días**.
	-  **Optimizado** para almacenar datos a los que rara vez se accede y se almacenan durante **al menos 180 días** con **requisitos de latencia flexibles**.
-
- El servicio {{cloze Instancia administrada de Azure SQL (Azure SQL Managed Instance)}} permite a los clientes de SQL Server subir y trasladar sus aplicaciones locales a la nube con cambios mínimos en las aplicaciones y en la base de datos. Presenta las características siguientes: #flashcard
  hl-page:: 24
  ls-type:: annotation
  id:: 636a151b-88a5-4f2c-b9de-73c7687de9ed
  hl-color:: yellow
	-  Plataforma como servicio (PaaS) totalmente administrada y permanentemente disponible.
	-  Conserva todas las capacidades de una PaaS (parches automáticos y actualizaciones de versiones, copias de seguridad automáticas y alta disponibilidad).
	-  El cliente puede intercambiar sus licencias existentes por tarifas con descuento en SQL Managed Instance mediante la ventaja híbrida de Azure.