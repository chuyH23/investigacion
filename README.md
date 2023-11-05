
# Pep8

 Que es?

La PEP8 es una guía que indica las convenciones estilísticas a seguir para escribir código Python. Se trata de un conjunto de recomendaciones cuyo objetivo es ayudar a escribir código más legible y abarca desde cómo nombrar variables, al número máximo de caracteres que una línea debe tener.

Dos mismos códigos pueden realizar lo mismo funcionalmente, pero si no se siguen unas directrices estilísticas, se puede acabar teniendo un código muy difícil de leer. Los problemas más frecuentes suelen ser:

-	Líneas demasiado largas.
-	Nombres de variables poco explicativos.
-	Código mal comentado.
-	Uso incorrecto de espacios y líneas en blanco.
-	Código mal identado.

Ejecutamos esto en terminal
```
$ pip install autopep8
Ejecutamos esto tambien
$ autopep8 script.py -v -i
Este codigo tiene errores
# script.py
def MiFuncionSuma(A, B, C, imprime = True):
    resultado=A+B+C
    if imprime != False:
        print(resultado)
    return resultado
a          = 4
variable_b = 5
var_c      = 10

MiFuncionSuma(a, variable_b, var_c)
```

Debería quedar asi:
```
# script.py
def mi_funcion_suma(a, b, c, imprime=True):
    resultado = a + b + a
    if imprime:
        print(resultado)
    return resultado


a = 4
variable_b = 5
var_c = 10

mi_funcion_suma(a, variable_b, var_c)
```
dentro de sus funciones esta:


- Indentación: Utiliza cuatro espacios para la indentación en lugar de tabulaciones. No mezcles espacios y tabulaciones para la indentación.

- Longitud de línea: Las líneas de código no deben exceder los 79 caracteres. Para documentación y comentarios, el límite es de 72 caracteres.

- Espacios en blanco en expresiones y declaraciones: Utiliza espacios en blanco de manera consistente para mejorar la legibilidad. Por ejemplo, coloca espacios alrededor de operadores, después de comas y dos puntos.

- Comentarios: Usa comentarios para explicar partes complejas del código. Los comentarios deben ser claros y concisos. Evita comentarios innecesarios.

- Nombres de variables y funciones: Elige nombres descriptivos para las variables, funciones y clases. Utiliza minúsculas con guiones bajos para las variables y minúsculas con mayúsculas iniciales para las funciones y métodos.



#  modulos y paquetes de pythin

que es?

Los módulos y los paquetes en Python son librerías adicionales al código base de Python que contienen funciones. Los módulos hacen referencia a archivos de Python que pueden contener una o varias funciones. El uso de módulos nos permite mantener el orden. Por otra parte, los paquetes son carpetas que contienen módulos y a su vez nos permiten mantener en orden proyectos que pueden ser demasiado grandes. En Python los paquetes deben contener un archivo de inicialización conocido como init. A lo que conocemos como librerías de Python son paquetes que han sido desarrollados por la comunidad para diferentes aplicaciones.

Funciones

La ventaja de utilizar módulos y paquetes es que te permiten dividir tu código en componentes más pequeños y manejables, lo que facilita su mantenimiento y reutilización. También ayuda a evitar conflictos de nombres al separar funcionalidades en diferentes espacios de nombres. En resumen, los módulos y paquetes son fundamentales para organizar y estructurar proyectos en Python de manera más ordenada y eficiente.

Ejemplo

Consideremos, por ejemplo, un archivo aritmetica.py que contenga las siguientes definiciones.

```
def sumar(a, b):
    return a + b

def restar(a, b):
    return a - b

def mult(a, b):
    return a * b

def div(a, b):
    return a / b
```

Podemos acceder a ellas desde otro archivo de Python ubicado en la misma ruta importando el módulo.

```
import aritmetica

print(aritmetica.sumar(7, 5))
Una sintaxis alternativa para importar objetos desde un módulo es la siguiente.
from aritmetica import sumar

print(sumar(7, 5))
Nótese que, en este segundo caso, no se prefija el nombre del módulo al invocar al objeto importado. Podemos importar varios objetos separándolos por comas.
from aritmetica import sumar, restar, mult, div

print(sumar(7, 5))
print(restar(7, 5))
print(mult(7, 5))
print(div(7, 5))
O bien, para importar todos los objetos dentro de un módulo:
from aritmetica import *

```


# los entornos virtuales en python

que es?

Un entorno virtual es un entorno Python en el que el intérprete Python, las bibliotecas y los scripts instalados en él están aislados de los instalados en otros entornos virtuales, y (por defecto) cualquier biblioteca instalada en un «sistema» Python, es decir, uno que esté instalado como parte de tu sistema operativo.
Un entorno virtual es un árbol de directorios que contiene archivos ejecutables de Python y otros archivos que indican que es un entorno virtual.


Cuando un entorno virtual está activo (es decir, el intérprete de Python del entorno virtual se está ejecutando), los atributos sys.prefix y sys.exec_prefix apuntan al directorio base del entorno virtual, mientras que sys.base_prefix y sys.base_exec_prefix apuntan a la instalación Python del entorno no virtual que se utilizó para crear el entorno virtual. Si un entorno virtual no está activo, entonces sys.prefix es lo mismo que sys.base_prefix y sys.exec_prefix es lo mismo que sys.base_exec_prefix (todos ellos apuntan a una instalación Python de entorno no virtual).
Cuando un entorno virtual está activo, cualquier opción que cambie la ruta de instalación será ignorada de todos los archivos de configuración de distutils para evitar que los proyectos se instalen inadvertidamente fuera del entorno virtual.

funcionalidad


- Los entornos virtuales en Python son una funcionalidad esencial que permite aislar y gestionar de manera eficiente las dependencias de tus proyectos. Aquí tienes algunas de las principales funcionalidades y ventajas de utilizar entornos virtuales en Python:

- Aislamiento de dependencias: Los entornos virtuales permiten crear un espacio aislado en el que puedes instalar y gestionar las dependencias específicas de un proyecto sin interferir con otras versiones de las mismas dependencias utilizadas en otros proyectos. Esto es crucial para evitar conflictos de versiones.

- Gestión de paquetes: Puedes usar herramientas como pip para instalar, actualizar y eliminar paquetes específicos en un entorno virtual sin afectar al sistema global de Python.

- Control de versiones de Python: Puedes seleccionar una versión específica de Python para tu entorno virtual, lo que te permite trabajar con proyectos que requieren versiones específicas de Python sin afectar la instalación global de Python en tu sistema.

- Reproducibilidad: Al utilizar entornos virtuales, puedes definir claramente las versiones de las dependencias utilizadas en un proyecto, lo que facilita la reproducibilidad de tu entorno de desarrollo en diferentes sistemas.

- Evitar conflictos de dependencias: Cuando trabajas en varios proyectos, es común que estos requieran diferentes versiones de las mismas dependencias. Los entornos virtuales permiten mantener separadas estas dependencias, evitando conflictos.

ejemplo

1. Abre tu terminal o línea de comandos.

2. Navega al directorio donde deseas crear tu entorno virtual o crea una nueva carpeta para tu proyecto si aún no lo has hecho.

3. Para crear un entorno virtual, ejecuta el siguiente comando:
```
python -m venv myenv
```
Esto creará un nuevo entorno virtual llamado "myenv" en el directorio actual.

4. Activa el entorno virtual. La forma en que lo actives depende del sistema operativo que estés utilizando:

```
source myenv/bin/activate
```
Notarás que el nombre de tu entorno virtual se agrega al inicio de tu línea de comandos, indicando que el entorno está activo.

Una vez que el entorno está activado, puedes instalar paquetes y trabajar en tu proyecto sin interferir con el sistema global de Python.

5. Para desactivar el entorno virtual cuando hayas terminado de trabajar en tu proyecto, simplemente ejecuta:
```
deactivate
```
Con este entorno virtual, puedes instalar y gestionar paquetes específicos para tu proyecto sin afectar otros proyectos o la instalación global de Python en tu sistema. Cuando actives este entorno, todas las operaciones de pip se realizarán en el ámbito de ese entorno, lo que facilita el aislamiento de dependencias y la gestión de tu proyecto


## Referencias

https://ellibrodepython.com/python-pep8

https://tutorial.recursospython.com/modulos-y-paquetes/