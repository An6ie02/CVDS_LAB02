# CVDS - LABORATORIO 2 - PATTERNS

Angie Natalia Mojica Diaz\
Daniel Antonio Santanilla Arias

## SOBRE APACHE MAVEN

### ¿Cuál es su mayor utilidad?

### Fases de maven

### Ciclo de vida de la construcción

### Para qué sirven los plugins

### ¿Qué es y para qué sirve el repositorio central de maven?

## EJERCICIO DE LAS FIGURAS

### CREAR UNPROYECTO CON MAVEN

Buscarcómo se crea un proyecto maven con ayuda de los arquetipos(archetypes).
Busque cómo ejecutar desde línea de comandos el objetivo "generate" del plugin "archetype",con los siguientes
parámetros:\
Grupo: edu.eci.cvds\
Id del Artefacto: Patterns\
Paquete: edu.eci.cvds.patterns\
archetypeArtifactId: maven-archetype-quickstart

```console
mvn archetype:generate
```

![Comando](./images/image1.png)
![Parametros](./images/image2.png)
![Proyecto](./images/image3.png)
Para visualizar la estructura hacemos los comandos

```console
cd Patterns
tree /f
```

![Estructura](./images/image4.png)

### AJUSTAR ALGUNAS CONFIGURACIONES EN EL PROYECTO

Hay que cambiar la version delcompilador de Java a la versión 8, para ello, agregue la sección properties antes de la sección de
dependencias:\
![Configuraciones](./images/image5.png)

### COMPILAR Y EJECUTAR

Para compilar usar el comando

```console
mvn package
```

![Compilado1](./images/image6.png)
![Compilado2](./images/image7.png)

#### Objetivo del parametro package

Para ejecutar usar el comando

```console
mvn exec:java -Dexec.mainClass="edu.eci.cvds.patterns.App"
```

![Ejecutando](./images/image8.png)
Realice elcambio en la clase App.java para crear un saludo personalizado, basado en los parámetros de entrada a la aplicación.
![CambioApp](./images/image9.png)

Para mandar parametros al plugin "exec" se da de la siguiente manera

```console
mvn exec:java -Dexec.mainClass="edu.eci.cvds.patterns.App" -Dexec.args="'argument1' 'argument2'"
```

Ejecutar nuevamente la clase desde línea de comandos y verificar la salida: Hello World!
![Ejecutando](./images/image8.png)
Ejecutar la clase desde línea de comandos enviando su nombre como parámetro y verificar la salida. Ej: Hello Pepito!
![EjecutandoNombre](./images/image10.png)
Ejecutar la clase con su nombre y apellido como parámetro.¿Qué sucedió?
![EjecutandoNombreApellido1](./images/image11.png)
Verifique cómo enviar los parámetros de forma "compuesta" para que elsaludo se realice con nombre y apellido. Ejecutar nuevamente y verificar la salida en consola. Ej: Hello Pepito Perez!
![EjecutandoNombreApellido2](./images/image12.png)

### HACER EL ESQUELETO DE LA APLICACION

Hacer el esqueleto de la aplicacion de acuerdo a la guia de laboratorio.
![EqueletoApp](./images/image13.png)
Ejecute múltiples veces la clase ShapeMain, usando el plugin exec de maven con los siguientes parámetros y verifique la salida en consola para cada una:\
Sin parámetros
![ShapeMain1](./images/image14.png)
Parámetro: qwerty
![ShapeMain2](./images/image15.png)
Parámetro: pentagon
![ShapeMain3](./images/image16.png)
Parámetro: Hexagon
![ShapeMain4](./images/image17.png)

#### ¿Cuál(es) de las anterioresinstruccionesse ejecutan y funcionan correctamente y por qué?
