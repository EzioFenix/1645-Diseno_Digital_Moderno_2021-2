```json
{
    'nombre': 'Barrera Peña  Víctor Miguel',
    'tipo': 'Tarea',
    'no': '45',
    'grupo':  '6',
    'materia': '1645 Diseño Digital Moderno',
    'semestre': '2022-1',
    'enunciado': 'Realizar una  investigación de CISC y RISC' ,
    'fecha': '23-10-2021'
}
```

<style>
    body{
  text-align: justify;
}
    h1{
        font-weight: bold;
        text-align:center;
    }
    p::first-letter{
  font-size: 1.3rem;
}
 a{
  text-decoration: none;
}
</style>


- RISC es más barato de producir, consume menos batería,es por ello que los dispositivos móviles los emplean, tiene que ver cuestiones de la arquitectura.

- La principal diferencia es que debido a que RISC tiene un conjunto de instrucciones reducido, acaba siendo necesario el uso de varias instrucciones más simples para ejecutar una más compleja, mientras que en el caso de una unidad CISC muchas instrucciones complejas se puedan realizar en una sola instrucción, por lo que las unidades CISC ahorran espacio en lo que a la cantidad de memoria se refiere.

- Una de las particularidades que tienen todas las CPUs desde principios de los años 90 es la segmentación, consistente en que en vez de esperar a que una instrucción se ejecute al completo en el procesador para dar paso a la siguiente, estas se van adelantando por cada etapa del ciclo de instrucción, la cual puede estar dividida en varias subetapas cada una de ellas.

  Dado que los procesadores RISC tienen una correlación directa entre la cantidad de instrucciones en el código binario y las que ejecuta la CPU es muy fácil segmentar las instrucciones en varias etapas. Pero **en un x86 es sumamente difícil**, ya que la segmentación se hace sobre las microinstrucciones generadas durante la etapa Decode, lo que supone aún más **circuitería adiciona**l funcionando y consumiendo energía de manera continua.

- Intel lo intento hace ya unos años con el fallido procesador Intel Medfield.

  Es más, una de las posibilidades que se han barajado es la creación de una **CPU mixta**, la cual consiste en un x86 que internamente decodifique sus instrucciones en instrucciones ARM y permita una total compatibilidad entre ambas ISAS, lo cual sería el procesador definitivo.

- Ahora la tendencia es hacer nucleos grandes (para potencia)  y núcleos pequeños para eficiencia https://www.youtube.com/watch?v=KgIgjHqchbk

![Por qué Intel y AMD no usan big.LITTLE en sus procesadores?](https://hardzone.es/app/uploads/2018/12/Foveros-8.jpg)

# Referencias

Roca, J. (2020, 12 noviembre). *¿Por qué no vemos procesadores x86 en dispositivos de muy bajo consumo?* HardZone. https://hardzone.es/tutoriales/rendimiento/x86-vs-arm-consumo-energetico/
