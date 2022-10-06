title:: Entornos_de_Integracion_y_Entrega_Continua Tema-4 (highlights)
author:: [[UNIR]]
full-title:: "Entornos_de_Integracion_y_Entrega_Continua Tema-4"
category:: #books

tags:: #[[Entornos-CI-CD]] #[[UNI]]

- #tags #[[Entornos-CI-CD]] #[[UNI]]
- ![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_22942/b0518fce-a66f-4dbf-a68e-f7dfff19cbad.jpg)
- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- -
	- Figura 2. Pasos de la fase de commit. Fuente: elaboración propia. #ñspace
		- (Page 16)
	- -
	- -
	- artifacts,  este  concepto  se  refiere  a  cualquier elemento producido en una fase del pipeline que requiere ser persistido: los binarios compilados,  las  imágenes  de  docker  o  de  VM  y  los  informes  de  resultados  de  las pruebas  también  se  incluyen  en  esta  categoría.  Estos  se  suelen  almacenar  en repositorios  específicos  con  una  referencia  al  commit  a  partir  del  cual  se  han generado, pero siempre separados del sistema de control de cambios. Idealmente, deben  ser  exactamente  reproducibles  a  partir  de  ese  mismo  commit  si  fuera necesario. #ñspace
		- (Page 16)
	- -
	- -
	- Las fases habituales son:   Fase de commit, en la que se compila y empaqueta el código, se ejecutan pruebas unitarias y se analiza el código en cuanto a complejidad, estilo, etc.   Fase de pruebas de validación automáticas, en las que se prueba la funcionalidad del software de una manera más intensiva que en una prueba unitaria.   Fase  de  pruebas  de  validación  de  usuario,  que  puede  no  ser  totalmente automática y en la que hay involucrados equipos de probadores.   Fase de despliegue, que será totalmente automática. #ñspace
		- (Page 24)
	- -