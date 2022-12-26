title:: Implementación Del Enrutamiento Del Tráfico De Redes Virtuales (highlights)
deck:: [[Across-the-Net]]
author:: [[wwlpublish]]
full-title:: "Implementación Del Enrutamiento Del Tráfico De Redes Virtuales"
category:: #articles
url:: https://learn.microsoft.com/es-es/training/modules/introduction-to-azure-virtual-networks/9-implement-virtual-network-traffic-routing

- Highlights first synced by [[Readwise]] [[Monday, 26-12-2022]]
	- -
		- Acerca de cómo funcionan los endpoints privados en Azure #flashcard
			- Protección de una red virtual mediante la tunelización forzada
			  
			  La tunelización forzada permite redirigir o forzar todo el tráfico vinculado a Internet de vuelta a su ubicación local a través de un túnel VPN de sitio a sitio con fines de inspección y auditoría. Se trata de un requisito de seguridad crítico en la mayoría de las directivas de las empresas de TI. Si no configura la tunelización forzada, el tráfico de Internet desde las máquinas virtuales de Azure siempre va desde la infraestructura de red de Azure directamente a Internet, sin la opción que permite inspeccionarlo o auditarlo. Un acceso no autorizado a Internet puede provocar la divulgación de información u otros tipos de infracciones de seguridad. La tunelización forzada puede configurarse mediante Azure PowerShell. No se puede configurar con Azure Portal.
			  
			  En el ejemplo siguiente, la subred de front-end no usa la tunelización forzada. Las cargas de trabajo de la subred Frontend pueden continuar para aceptar y responder a las solicitudes de los clientes directamente desde Internet. Las subredes Mid-tier y Backend usan la tunelización forzada. Las conexiones salientes desde estas dos subredes a Internet se fuerzan o redirigen a un sitio local a través de uno de los túneles VPN de sitio a sitio (S2S).
			  
			  ![Subredes de back-end y de nivel intermedio con tunelización forzada a través de V P N S 25. Subredes de front-end enrutadas directamente a Internet.](https://learn.microsoft.com/es-es/training/modules/introduction-to-azure-virtual-networks/8-exercise-connect-two-azure-virtual-networks-global/../../wwl-azure/introduction-to-azure-virtual-networks/media/forced-tunnel-ba8d30e6.png)
		- ([View Highlight](https://read.readwise.io/read/01gn7576zvekey6f0ndn3h9c3m))
	- -