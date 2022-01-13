
```json
{
    'nombre': 'Barrera Peña  Víctor Miguel' ,
    'tipo': 'Tarea',
    'no': '24',
    'grupo':  '6',
    'materia': '1645 Diseño Digital Moderno',
    'semestre': '2022-1',
    'enunciado': 'nvestigar al menos 5 métodos de detección y corrección de errores (incluyendo mnp5)',
    'fecha': '28-09-2021'
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
    img{
       zoom:10%
    }
</style>


# Problema

Investigar al menos 5 métodos de detección y corrección de errores (incluyendo mnp5)

## Comprobación de paridad

Añadir un bit de paridad de cada bloque de paridad al final de cada bloque de datos de 7 bits.

$1110001 \longrightarrow$

Tenemos dos opciones:

- Paridad impar: si hay un numero par de 1's, entonces agregamos un 1 al final resultado en $1110001$ **1**.
  - Ahora "hay un número impar de 1's".
- Paridad par: si hay un numero impar de 1's, entonces agregamos un 1 al final, resultando en $1110001$ **0**.
  - Ahora "hay un número par de 1's".

## Comprobación de redundancia cíclica

Para este vamos a recordar un poco lo que pasa con aquellos polinomios que tienen un residuo, es posible obtener un dividendo que cumpla esta funcion

pensemos el siguiente ejemplo $m(x)=101$

necesitamos una función generadora llamada $g(x)=1x^1+0x^0 =10b$ 

al final de 101 se le agregará bits adiciones (con bits adicionales llamemosles $m_1$) que lograrán que  $m_1(x)/g(x)\%1=0$

Si quieres más profundidas:

- https://www.youtube.com/watch?v=_NkXZekQsQk ejemplo
- teoria suave https://www.youtube.com/watch?v=cZHuh-NEHwA
- explicación https://www.youtube.com/watch?v=7G1p2-VQEKQ&list=PLomN84AdULIBcoI8Rb98dnompliIktJk9&index=65
- Teoría pura y dura matemática
- pág 185-192 Stallings, W., Stallings, W., Tanenbaum, A., Fall, K. R., & Stevens, W. R. (2004). *Comunicaciones y Redes de Computadores, 6aedición*. Prentice-Hall. 7ma edición.

## Códigos de Hamming

En resumen si tu quieres trasmitir 4 bits de información vas a tener usar 3 bits para verificar que el código llegue bien  en este caso la configuración es (7:3), 7 bits de envió, de los cuales 3 son de comprobación, lo bueno de este método es que si por alguna razón se modifica 1 sólo bit de los datos,este método es capaz de corregir el error.

Los bits 1,2,4 van a ser bits de comprobación, los demás bits van a contener información, para resolverlo se hace de la siguiente manera se hace mediante iteraciones, si quieres ver como:

- Teoría: https://www.youtube.com/watch?v=gQK9nROFX20
- ejemplo :https://www.youtube.com/watch?v=KfunKv-3N3Q

## Redundancia

Si alguien dice un número y no lo escuchaste con claridad ¿Qué harías para asegurarte que lo comprendió correctamente. Lo más sencillo es repetir la información , ya se  en el mismo mensaje o en otro y verificando la información

## MNP5

<<La empresa Microcom desarrollo un protocolo llamado MNP (Microcom Networking Protocol) que se ha convertido en el estándar en modems>>.

- MNP tiende desde la versión 1 hasta la 7.
- <<incluye las características descriptas de las clases 3 y 4, pero usa además compresión de datos para mejorar la eficiencia. La mejora depende del tipo de datos, si se trata de textos de lectura la eficiencia puede llegar a duplicarse (mejora típica 85%), en datos y archivos ya comprimidos la mejora es ínfima. El método de compresión empleado hace dos cosas: primero, busca caracteres repetidos, cuando tres o más caracteres aparecen en sucesión los comprime; segundo, usa tabulación dinámica de caracteres repetidos, lo que le da habilidad de aprendizaje>>. 


# Referencias

- Bianchi, A. (s. f.). *Capítulo 3: Protección de los Datos:Control de Errores. Seguridad en Redes.* Protección de los Datos:Control de Errores. Seguridad en Redes. Recuperado 28 de septiembre de 2021, de http://www.geocities.ws/abianchi04/textoredes/c3.pdf

