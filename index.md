#  Tarea para AW03 Markdow

## Borja Melo Ramos
Formatear un texto **puede** ser entretenido si prestas atención a *los videos de clase*.

<p>En Visual Studio Code, es más sencillo</p>

<ol>
  <li>Introducir un título.</li>
  <li>Hacer una lista númerada.</li>
  <li>Introducir una cita, como la que añado más abajo.</li>
  <li>Un enlace a una página web.</li>
  <li>Introducir una parte de código.</li>
  <li>Subir una imagen.</li>
  
</ol>

<p><a href="https://burela.org/gl">Pagina WEB principal de mi pueblo, Burela.</a> </p>


<p>Para introducir una cita con enlace:</p>
<blockquote>
  <p>Buscamos una noticia de interes y de actualidad.
  
  "Todos contra China en inteligencia artificial: la Comisión de Seguridad Nacional de EEUU pide una alianza con la UE para hacerles frente". </p>
  <footer>
    <cite><a href="https://www.xataka.com/pro/todos-china-inteligencia-artificial-comision-seguridad-nacional-eeuu-pide-alianza-ue-para-hacerles-frente">NOTICIA PABLO RODRÍGUEZ @Pabrodri -Xakata-
 </a></cite>
  </footer>
</blockquote>


<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <strong>Mi imagen de prueba:</strong>
  </head>
  <body>
    <img src="https://emeradiofm.com/wp-content/uploads/2019/11/burela.jpg" alt="Mi imagen de prueba">
  </body>
</html>
<br>
<br>
<br>

**EJEMPLO DE CODIGO python:** 
*El siguiente ejemplo muestra una implementación de cola FIFO en la que almacenamos valores enteros comprendidos entre 1 y 100 y posteriormente los leemos de forma secuencial. Funciona en cualquier versión de Python igual o superior a 3.5
Para realizar el programa solo tendrías que usar el siguiente código*


`from multiprocessing import Queue`
`import random`

`queue_time = Queue()`

`print("Saving elements at queue...")`
`for i in range (5):`
    `random_time = random.randint(1, 100)`
    `queue_time.put(random_time)`
    `print("%d added at queue" % random_time)`

`print("Reading elements from queue...")`
`while not queue_time.empty():`
    `time_read = queue_time.get()`
    `print("%d read from queue" % time_read)`
<br>
<br>
<br>

<p><a href="https://github.com/BorjaMeloRamos/BorjaMeloRamos.github.io/blob/a18867b703d44985a51505adddf329ee29f6ec7a/Referencias.md">Mi Página WEB Referencias.md.</a> </p>
