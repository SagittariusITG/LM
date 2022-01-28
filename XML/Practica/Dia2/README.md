## DTD

DTD (Definiciones de Tipo de Documento) -> Este especifica la estructura del documento XML.

* Este incluye elementos que pueden aparecer.
* Dónde pueden aparecer.
* El contenido y los atributos.

## Elementos

Los elementos también llamados etiquetas.

Estos se declaran con la etiqueta <!ELEMENT>.

### Elementos terminales

* ANY → Cualquier cosa.
* EMPTY → Vacío.
* #PCDATA → Texto.

### Elementos no terminales

* (?) al final de un atributo implica que no es un campo requerido.
* (+) en una etiqueta es que al menos debe haber un campo (en este caso debe hacer al menos una asignatura).
* (*) en una etiqueta es que puede haber 1 o más campo (en este caso permite que haya una o más asignatura).
    * Si ponemos * en dos etiquetas, deberá haber el mismo número de etiquetas, es decir, si hay 2 etiquetas que se llamen "horas" deberá haber 2 etiquetas "nombre".

## Atributos

Los atributos de los elementos.

Estos se declaran con la etiqueta <!ATTLIST>

### Elementos para los atributos

* ENUM → Es decir, no se puede poner ningún otro tipo de dato que no sea el introducido.
    * <!ATTLIST asignatura nom (hulio|miguel|anuel)>
    * Solo se podrá poner uno de esos 3 nombres como atributo.
* CDATA → Define que lo que se guarda es una string.
* ID → Para definir como identificador un atributo.
* IDREF → Hace referencia a un id que se llame igual.
    ```xml
    * <elemento nombre="hola"> (nombre id)
    * <elemento panceta="hola"> (panceta idref)
    ```
* NMTOKEN → Solamente le podemos pasar una única palabra.
* #REQUIRED → Obliga que el campo sea obligatorio.
* #IMPLIED → Define que el atributo es opcional.
* #FIXED → Define que no puede variar.