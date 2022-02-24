# Primer Examen XML

Este es el examen del día en que empieza la tercera guerra mundial (24-02-2022).

# Ejercicio 1: Dado el siguiente enunciado:

Los datos que vamos a transportar versan sobre los animales marinos pertenecientes a un zoológico.
De estos animales se va a almacenar el nombre, especie, familia, clase, alimentación, habitat y salinidad del agua.
Añadir que cada animal tiene un identificador que especifíca que son animales marinos y un identificador propio que los relaciona con su alimento.

    a. Dibuja la estructura del árbol XML.
    b. Elabora el documento XML.
    c. Introduce al menos los datos pertenecientes a dos animales en el documento XML.
    d. Elabora el documento DTD.

# Ejercicio 2: Elabora el documento DTD correspondiente a este XML:

```xml
<Alimentos>
    <Alimento>
        <InfoAlimento>
            <Nombre>Plancton</Nombre>
            <Tipo>Fitoplancton</Tipo>
            <Cantidad>50T</Cantidad>
        </InfoAlimento>
        <Consumidor>
            <Especie cod="05">Echinoidea</Especie>
            <CantidadIndividuo>50g</CantidadIndividuo>
            <NumIndividuos>5000<NumIndividuos>
        </Consumidor>
        <Consumidor>
            <Especie cod="07">Holothuroidea</Especie›\>
            <CantidadIndividuo>65g</CantidadIndividuo>
            <NumIndividuos>1000<NumIndividuos>
        </Consumidor>
    </Alimento>
    <Alimento>
        ...
    </Alimento>
<Alimentos>
```

# Ejercicio 3: Elabora el documento XML correspondiente a este DTD:

```dtd
<!ELEMENT habitat (características, turnos, zonas)>

    <!ELEMENT características (#PCDATA)>

    <!ELEMENT turnos (horario, empleados)>
        <! ELEMENT horario (#PCDATA)>
        <! ELEMENT empleados (limpiador, cuidador+)>
            <! ELEMENT limpiador EMPTY>
            <!ATTLIST limpiador identificador ID #REQUIRED>
            <! ELEMENT cuidador EMPTY>
            <!ATTLIST cuidador identificador ID #REQUIRED>

    <!ELEMENT zonas (zona)>
        <!ELEMENT zona (tamaño, individuo*)>
            <!ELEMENT tamaño (#PCDATA)>
            <!ELEMENT individuo (especie, edad, sexo)>
                <!ELEMENT especie (#PCDATA)>
                <!ATTLIST especie identificador NMTOKEN #REQUIRED>
                <!ELEMENT edad (#PCDATA)>
                <!ELEMENT sexo (#PCDATA)>
```