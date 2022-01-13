Proyecto 1. Función Booleana con compuertas NAND y NOR

Alumno: 

- Barrera Peña Víctor Miguel

Grupo: 6

Ciudad universitaria, Ciudad de México



# Introducción

# Desarrollo

![image-20211010032050230](image-20211010032050230.png)

con nands y nors

## NAND

### Álgebra de Boole

Convertiremos al función original en una función únicamente compuesta sólo por NAND´S.

Forma objetivo $f=\overline{XY} = \overline{X} + \overline{Y}$
$$
\begin{aligned}
	f(A,B,C,D) &= (A+B)(C+\overline{D})\\
	f& =(\overline{\overline{(A+B)(C+\overline{D})}}) \\
	f&= \overline{\overline{(A+B)}+\overline{C+\overline{D}})} \\
	f&= \overline{(\overline{A} \cdot \overline{B})+(\overline{C} \cdot D)} \\
	\therefore f& =\overline{\overline{\overline{(\overline{A}\cdot \overline{B})} \cdot \overline{(\overline{C}\cdot D)}}}
\end{aligned}
$$



![image-20211010030155895](image-20211010030155895.png)

### Diagrama lógico

![image-20211010030228986](image-20211010030228986.png)

### Diagrama físico o patigrama

![image-20211010030319785](image-20211010030319785.png)



### Tabla de verdad

La función propuesta es la siguiente:
$$
f(A,B,C,D)= (A+B)(C+\overline{D})
$$

|  A   |  B   |  C   |  D   | $(A+B)(C+\overline{D})$ |      |
| :--: | :--: | :--: | :--: | ----------------------- | ---- |
|  0   |  0   |  0   |  0   | 0                       |      |
|  0   |  0   |  0   |  1   | 0                       |      |
|  0   |  0   |  1   |  0   | 0                       |      |
|  0   |  0   |  1   |  1   | 0                       |      |
|  0   |  1   |  0   |  0   | 1                       |      |
|  0   |  1   |  0   |  1   | 0                       |      |
|  0   |  1   |  1   |  0   | 1                       |      |
|  0   |  1   |  1   |  1   | 1                       |      |
|  1   |  0   |  0   |  0   | 1                       |      |
|  1   |  0   |  0   |  1   | 0                       |      |
|  1   |  0   |  1   |  0   | 1                       |      |
|  1   |  0   |  1   |  1   | 1                       |      |
|  1   |  1   |  0   |  0   | 1                       |      |
|  1   |  1   |  0   |  1   | 0                       |      |
|  1   |  1   |  1   |  0   | 1                       |      |
|  1   |  1   |  1   |  1   | 1                       |      |

![image-20211010030108925](image-20211010030108925.png)

![image-20211010030124605](image-20211010030124605.png)

## NOR


### Álgebra de Boole

![image-20211010030351363](image-20211010030351363.png)

Forma esperada $f=\overline{X+Y}$

## Boole

$$
\begin{aligned}
 f(A,B,C,D) &= (A+B) (C+\overline{D}) \\
 &=\overline{\overline{(A+B)(C+\overline{D})}} \\
 &= \overline{\overline{(A+B)}+ \overline{C+\overline{D}}}
\end{aligned}
$$





### Diagrama Lógico

![]( [nand.pdf](nand.pdf)

![image-20211010030444340](image-20211010030444340.png)

### Daigrama físico o patigrama

![image-20211010030510228](image-20211010030510228.png)

## Ensamblado Físico

Compuertas nand tfl 7400 (nand)

![image-20211010030551665](image-20211010030551665.png)

![image-20211010030609775](image-20211010030609775.png)

![image-20211010030619874](image-20211010030619874.png)

# Codigo Quartus

![image-20211010030755711](image-20211010030755711.png)

# Diagrama de bloques

![image-20211010030819158](image-20211010030819158.png)

### Conclusión

Barrera Peña Victor Miguel



## Anexo

## Pasar entre compuertas

<img src="image-20211010152743683.png" alt="image-20211010152743683" style="zoom:80%;" />

## Booleana NAND´s

![image-20211010144908699](image-20211010144908699.png)

### Reglas álgebra de Boole

![image-20211010030026172](image-20211010030026172.png)

