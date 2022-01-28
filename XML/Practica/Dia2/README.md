## DTD

DTD (Definiciones de Tipo de Documento) -> Este especifica la estructura del documento XML.

* Este incluye elementos que pueden aparecer
* Dónde pueden aparecer
* El contenido y los atributos.

## Tipos

ANY -> Cualquier cosa
EMPTY -> Vacío
#PCDATA -> Texto

* (?) al final de un atributo implica que no es un campo requerido.
* (+) en una etiqueta es que al menos debe haber un campo (en este caso debe hacer al menos una asignatura).
* (*) en una etiqueta es que puede haber 1 o más campo (en este caso permite que haya una o más asignatura)
    * Si ponemos * en dos etiquetas, deberá haber el mismo número de etiquetas, es decir, si hay 2 etiquetas que se llamen "horas" deberá haber 2 etiquetas "nombre".