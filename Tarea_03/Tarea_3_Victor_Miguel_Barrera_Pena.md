```json
{
    'nombre': 'Barrera Peña  Víctor Miguel',
    'tipo': 'Tarea',
    'no': '03',
    'grupo':  '6',
    'materia': '1645 Diseño Digital Moderno',
    'semestre': '2022-1',
    'enunciado': 'Realizar una  investigación sobre ¿Qué es la computación cuántica?',
    'fecha': '11-09-2021'
}
```



## Origen

<<A principios del siglo XX, Planck y Einstein proponen que la luz no es una onda continua (como las ondas de un estanque) sino que está dividida en pequeños paquetes o **cuantos**. Esta idea, en apariencia simple, servía para resolver un problema llamado la "catástrofe ultravioleta". Pero a lo largo de los años otros físicos fueron desarrollándola y llegando a conclusiones sorprendentes sobre la materia, de las cuales a nosotros nos interesarán dos: **la superposición de estados y el entrelazamiento**>>(Julián, 2019).

Lo resumiré de una forma abismalmente corta, pensemos lo que hace  una computadora y como representa toda información que maneja una computadora. Después de pensar podriamos simplificar el comportamiento de una computadora usando un automata, que guarda las cantidades 1 y 0, las lee, hace asignaciones y con ello  puede hacer todas las operaciones que conocemos en los algoritmos.

Subamos una capa de abstracción, ahora implementada con circuitos, si tengo almacenado una  ligera cantidad de voltaje decimos que es 1, si no la tengo es 0. Si quiero que a partir de los dos primeros obtengamos un siguiente resultado, por ejemplo, un `or`, usariamos compuertas eléctricas. A partir de la union de muchas compuertas  puedo hacer algoritmos (fisicamente implementados). Podemos observar que de los datos iniciales  se generan y se generan resultados hasta llegar al resultado esperado, los datos iniciales solo pueden almacenar un estado, por ejemplo, 1 o 0; ahora bien si cambiamos ese comportamiento por algo que puede generar los dos estados  vemos que es el doble de rapido con un estado, pero si agregamos otro estado sería $2 \cdot 2=4$ .

Puede generar 4 resultados, mientras que en un sistema tradicional tendría que generar cada uno de ellos a la vez. A estos estados de la memoria los llamamos bits en las computadoras tradicionales, pero en las computadoras cuanticas les llamamos `QBits`. Los Qbits pueden generar los $2^n$ al mismo tiempo. 

A primera vista uno podría pensar ¿Si los Qbits son mejores,  por qué no empezamos a trabajar con ellos de inmediato ? Sencillas razones que enlisto a continuación:

1. La falta de algoritmos, si bien los programas escritos con bits es posible simularlo con Qbits, ello no es una buena idea, ya que las computadoras clásicas siguen siendo más rápidas para ello actualmente.
2. Las condiciones para manterner una computadora cuántica en funcionamiento es muy cara todavia y no es muy estable.
3. Los Qbits pueden generar todos los posibles estados, pero ello tiene una probabilidad de error  asociada a todos los resultados generados. Es muy rapida para generarlos, pero al leerlos , se hace de manera secuencial y pudes corromper los datos ya que estas percibiendo el fenómeno, reucerda el experimento de la doble rendija.

Los sistemas cuánticos pueden ser el futuro, o posiblemente no , pero en lo que estamso de acuerdo, es en el potencial  pueden proporcionar de solucionar los porblemas asociados con este tipo de sistemas. En lo personal, yo creo que  el siguiente paso de la evolución computacional es una computadora biológico, que se piensa que si bien no fuera mucho más rapida a semejanza con la cuaántica, si sería más eficiente, portatil y brindando un rendimiento superior a la computación actual. Su punto fuerte es la eficiencia, imaginate una camara de seguridad que consuma menos de 1 watt, sería increible  o tu mega computadora actual , funcionando con 20 watts y siendo bastante pequeña, y calentandose casi nada.

Lo que creo es adecuado, es computación biológica para el usuario promedio y cuántica para  proyectos grandes, creo que eso sería el futuro que yo me esperaría.

# Referencias

- Julián, G. (2019, 1 marzo). *Computación cuántica: qué es, de dónde viene y qué ha conseguido*. Xataka. https://www.xataka.com/ordenadores/computacion-cuantica-que-es-de-donde-viene-y-que-ha-conseguido
