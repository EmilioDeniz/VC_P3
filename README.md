# VC_P3

El objetivo de la practicas es la extracción de características geometricas para el uso de detección de objetos específicos usando la librería openCV.

- En el primer ejercicio se nos propone fotografiar una imagen con varias monedas y algún objeto que no sea una moneda y luego hacer un filtrado para hacer un conteo de las monedas
  y no tener en cuenta el objeto que no lo es, hicimos uso de la función cv2.findContours() de openCV para detectar todos los contornos y filtramos en base al area y al perimetro para
  resolver con éxito esta tarea.
  
- En el segundo ejericio nos piden que fotografiemos una imagen con varias monedas solapadas y otra con monedas no solapadas y luego que seleccionemos por ejemplo una moneda y a partir de esa moneda
  que el programa devuelva el valor total del dinero que se encuentra en la imagen, para hacer esto hicimos uso de cv2.HoughCircles() ya que nos da fácilmente el radio del contorno y además nos
  serviría para la imagen con monedas solapadas. Los mayores problemas que encontramos fue a la hora de generar la imagen ya que las sombras o ligeros angulos hacen que el código pueda fallar y además el
  código no funciona en la imagen con la monedas solapadas por los problemas anterior aun usando la función de cv2.HoughCircles() que nos da una aproximación de los contornos no visibles.

- En el tercer ejercicio tenemos que hacer un clasificador de microplásticos y generar la matriz de confusión, para resolver esta tarea primero hicimos una función donde guardamos todas la caracteristicas
  geométricas de los 3 microplásticos en listas diferentes y a partir de esas listas creamos otras 3 listas con los máximos, minimos y medias para ayudarnos a crear una función de clasificación. En esta
  función fuimos probando combinaciones de caracteristicas distintas para obtener una  clasificación más precisa hasta que estemos satisfechos con nuestra matriz de confusión.




- Fuentes
  https://ieeexplore.ieee.org/document/8976153 - Proporcionado en el guión de practicas para estudiar formas de clasificar microplásticos.

  https://www.carm.es/web/pagina?IDCONTENIDO=718&IDTIPO=100&RASTRO=c285$m - Utilizado para obtener los diametros de las monedas del euro.
