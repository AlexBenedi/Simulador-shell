Implementacion de un simulador de shell sin persisntencia de almacenarmiento ( una vez terminada la ejeucion del programa  se pierda la informacion)

A continuacion se detallan algunos de los comandos que se pueden ejecutar dentro del simulador:

+ pwd()

    - Devuelve la ruta completa de forma textual, con todos los nombres de los directorios desde la raíz hasta el directorio actual concatenados y separados por el separador '/'.


* ls()
    - Devuelve un listado con el nombre de todos los nodos contenidos en la ruta actual, uno por línea.
  
* du()
    - Devuelve un listado con el nombre y el tamaño de todos los nodos contenidos en la ruta actual, uno por línea.
  
* vi(string name, int size)
    - Edita el fichero de nombre 'name' (en el directorio actual). Para simular la edición, simplemente se cambia el tamaño del fichero al valor especificado como parámetro.
    - Si el fichero no existe, se debe crear con el nombre y tamaño especificados.
  
* mkdir(string name)
    - Crea un directorio de nombre 'name' en el directorio activo.
  
* cd(string path)
    - Hace que la ruta activa pase a referenciar a otro directorio.
    - La nueva ruta activa definida en 'path' debe referenciar un directorio o un enlace a un directorio.
  
* ln(string path, string name)
    - Crea en el directorio actual un enlace simbólico de nombre 'name' que apunta al elemento identificado mediante la ruta especificada en 'path', que puede ser de cualquier tipo.
    - El nombre 'name' es un nombre simple de nodo (se creará en el directorio activo), por lo que no puede contener una ruta completa.
    - La ruta definida en 'path' sí, de tal modo que se puede crear un enlace a un elemento en otro directorio del árbol, que debe existir previamente.
  
* stat(string path)
    - Devuelve el tamaño del nodo que referencia el path.
  
* rm(string path)
    - Elimina un nodo. Si es un fichero, es simplemente eliminado. Si es un enlace, elimina el enlace pero no el nodo referenciado.
    - Si es un directorio, elimina el directorio y todo su contenido. Si existen enlaces al elemento borrado, ese elemento sigue siendo accesible a traves del enlace (todavía existe), pero no a través de su ubicación original (que ha sido eliminada).
