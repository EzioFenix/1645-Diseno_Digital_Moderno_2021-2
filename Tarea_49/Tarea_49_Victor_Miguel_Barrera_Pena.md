```json
{
    'nombre': 'Barrera Peña  Víctor Miguel',
    'tipo': 'Tarea',
    'no': '49',
    'grupo':  '6',
    'materia': '1645 Diseño Digital Moderno',
    'semestre': '2022-1',
    'enunciado': 'Como se implementa un tren de pulsos con un 555',
    'fecha': '30-10-22'
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


# Consideraciones de la siguiente tarea

- En lo personal, leí dos artículos y el siguiente me pareció excelentemente escrito, describe todo lo que hay que saber para usar el circuito, por lo cual la copiare textualmente.

## Como funciona el timer 555 en modo astable

El timer **555** es un circuito integrado, con el podemos realizar varias funciones, pero yo voy a explicarles la que creo desde mi punto de vista es la mas importante, Generar un tren de pulsos de una frecuencia determinada **[PWM o modulación por ancho de pulsos](https://www.electrontools.com/Home/WP/2016/03/09/pwm-modulacion-por-ancho-de-pulsos/)**

No es el objetivo del articulo explicar en detalle el circuito interno del integrado, solo voy a hacer unos comentarios generales al respecto para que no piensen que lo ocurre dentro de esta caja negra es arte de magia.

## Circuito interno

El integrado esta formado por un Flip Flop, una etapa de salida para controlar la corriente, transistores y dos comparadores de tensión, a estas configuraciones internas se le suma la red externa que dependiendo de el valor de sus componente obtenemos resultados diferentes.

![Circuito interno LM555](https://lh3.googleusercontent.com/-Gwn45BkGU4c/VZbs6n2b2GI/AAAAAAAAB0k/KGO3MNaxnNk/h300/CircuitoInterno55.png)

 

## Funcionamiento de cada uno de sus pines

- **Pin 1 (Gnd):** Es la referencia a tierra del circuito.

- **Pin 2 (Disparador o trigger):** Es la señal de entrada del comparador

- **Pin 3 (Salida):** Es por donde se obtiene la señal de salida esperada (el tren de pulsos)

- **Pin 4 (Reset):** Es el pin de reset, se controla mediante lógica negativa, es decir si quiero volver a iniciar el proceso debo enviar un cero a este pin, desde mi experiencia recomiendo conectar directamente este pin a VCC mediante una resistencia de pequeño valor, de esta manera evitamos que la salida se ponga a cero sin desearlo.

- **Pin 5 (Control de voltaje):** Este pin esta para producir la modulación por ancho de pulsos mediante la descarga del capacitador externo.

- **Pin 6 (Umbral):** Es la entrada de otro comparador, se compara a 2/3 de VCC contra la amplitud de la señal de disparo.

- **Pin 7 (Descarga):** Se descarga cuando el transistor se encuentra en saturación, se conecta a el divisor resistivo de la red de tiempo externa.

## Conexión básica para comportamiento astable (generador de tren de pulsos)

Utilizando esta simple configuración podemos general una señal cuadrada a la salida de la frecuencia que nosotros determinemos, la frecuencia y el ancho de los estados altos y bajos dependerá de la Red de tiempo, básicamente de los valores de los capacitares y resistencias que le pongamos.

![Como funciona el timer 555](https://lh3.googleusercontent.com/-hGYLJJSWSWY/VZb5WSRLF-I/AAAAAAAAB00/1gXs7pV_9m8/h400/555.gif)

Para controlar el ancho de cada estado del tren de pulsos debemos aplicar las siguientes formulas

![Ecuaciones ancho de pulsos 555](https://lh3.googleusercontent.com/-zT9jrJXdXw8/VZb7DrU1UvI/AAAAAAAAB1A/lz_ufjEYISY/h150/1%2B-%2B555.png)

**Ta** representa el tiempo en estado alto (H) y **Tb** representa el tiempo en estado bajo (L), modificando los valores R1 R2 y C1 podemos diseñar la señal a nuestro gusto, el periodo de la señal va a ser la suma del tiempo en alto mas el tiempo en bajo, y como ya sabemos ya frecuencia es la inversa del periodo.

## Forma de la señal de salida obtenida

La siguiente imagen muestra lo que veríamos en un osciloscopio, queda claro que podemos regular a nuestro gusto los tiempos de Ta y Tb modificando los valores de los elementos pasivos del circuito.

![Señal de salida PWM de 555 configurado como astable](https://lh3.googleusercontent.com/--m61dHYIdPU/VZb_bo7pQfI/AAAAAAAAB1U/w-RQy6Ik26s/h240/pwm%2B555.png)

## Ventajas de utilizar el circuito integrado 555

Fue uno de los primeros circuitos integrados en realizar darnos la posibilidad de generar un tren de pulsos a nuestro gusto, las ventajas se pueden enumerar aunque gracias al avance de la tecnología se puede obtener el mismo resultado de mucho mayor calidad con microprocesadores. Igualmente vale la pena mencionar algunas de las ventajas de utilizar el 555 para generar tren de pulsos.

- **Su bajo costo:** se consigue en cualquier casa de electrónica a muy buen precio.

- **No hay que programarlo:** como dijimos, este integrado no es un microprocesador y es por eso que no es necesario programar nada para obtener un tren de pulsos determinado.

- **Fácil de utilizar:** Es muy fácil de utilizar y es por eso que es ideal para enseñar en los colegios.



## Aplicaciones del integrado 555

Es un integrado muy versátil que se puede usar para gran cantidad de aplicaciones, eso dependerá de la imaginación del desarrollador. Las mas frecuentes aplicaciones son las siguientes.

- **Led intermitente:** es muy común utilizarlo como [temporizador](https://www.electrontools.com/Home/WP/2016/12/06/el-temporizador-555/) para hacer parpadear un led a una frecuencia determinada, generalmente para carteles luminosos.

- **Control de velocidad de un motor:** Se lo utiliza para generar una señal PWM para controlar la velocidad de un motor de corriente continua.

- **Alarmas:** dado el rango de frecuencias que maneja es muy común utilizarlo para hacer una alarma mediante de una circuiteria adicional

# Referencias

- Diapositivas Roberto Mandujano página 628,2022-1
- Veloso, C. (2019, 17 agosto). *Temporizador 555 – LM555 ⇨ GENERADOR DE PULSOS*. Tutoriales de Electrónica | Matemática y Física. https://www.electrontools.com/Home/WP/temporizador-lm555-electronica-analogica-digital/
