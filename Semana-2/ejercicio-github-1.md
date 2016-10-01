# Trabajando con GitHub

## Introducción (un poco larga !!)
Esta semana nos crearemos una cuenta en GitHub cada uno.
GitHub es una plataforma de desarrollo colaborativo de software para alojar proyectos 
utilizando el sistema de control de versiones Git. El código se almacena de forma pública, 
aunque también se puede hacer de forma privada, creando una cuenta de pago.

GitHub permite colaborar en un proyecto y mantener versiones distintas de un mismo proyecto.
Una de las grandes ventajas es que permite trabajar en "local" y luego sincronizar los cambios
en el repositorio en línea junto con los cambios de los demás colaboradores.

Al final de esta semana tendremos un repositorio GitHub que se parecerá al siguiente árbol:

```
enrique@raspberrypi:~ $ tree CursoHacker
CursoHacker
├── LICENSE
├── README.md
├── Semana-2
│   ├── ejercicio-linea-comando-1.md
│   ├── ejercicios-enrique
│   │   ├── passwd
│   │   ├── Resultado
│   │   ├── resultado.1
│   │   ├── resultado.10
│   │   ├── resultado.3
│   │   ├── resultado.4
│   │   ├── resultado.5
│   │   ├── resultado.6
│   │   ├── resultado.7
│   │   ├── resultado.8
│   │   └── resultado.9
│   └── temario.md
├── temario.md
└── Verano
    └── temario.md
```

Antes de empezar con git se recomienda inicializar dos variables de entorno que git necesita
para identificarte. Por ejemplo yo pondría:

``` bash
enrique@raspberrypi:~ $ git config --global user.name quiquee
enrique@raspberrypi:~ $ git config --global user.email enrique.melero@gmail.com
```

Para evitar tener que escribir estas órdenes de iniciación del entorno de git os recomiendo
que pongais las siguientes líneas al final del fichero .profile de vuestro directorio principal.

``` 
# This is .profile
...

# Inicializa el entorno git
# usad aquí vuestro nombre de usuario git y la dirección email que 
# usásteis al registraros

git config --global user.name quiquee
git config --global user.email enrique.melero@gmail.com

```

Las órdenes de git que aprenderemos hoy son las siguientes: clone, add y push

clone: copia un repositorio localmente 

add: añade un fichero o directorio al repositorio local

commit: confirma los cambios en el repositorio local

push: sube los cambios locales al repositorio remoto (GitHub)

``` bash
enrique@raspberrypi:~ $ git clone <repository_url>
enrique@raspberrypi:~ $ git add <directorio>
enrique@raspberrypi:~ $ git commit
enrique@raspberrypi:~ $ git push
```
Podéis encontrar una descripción de cada una de estas opciones en castellano en el fantástico libro sobre
git que existe en línea: https://git-scm.com/book/es/v1

Os aviso que usar git es complicado al principio, pero después de un tiempo no podréis vivir sin él y es 
una herramienta fundamental para poder programar eficientemente, en solitario o de forma colaborativa.

Ahora vamos con el ejercicio:

## El Ejercicio
Quiero que entendáis muy bien lo que vamos a hacer. Repetirlo dentro de vuestra cabeza un par de veces (o más si hace falta), porque es una secuancia de acciones que realizaremos muchas otras veces:

```
1 Replicaremos un repositorio con un proyecto en GitHub en nuestra estructura de ficheros local
2 Añadiremos ficheros o directorios al proyecto
3 Documentaremos el cambio que hemos realizado
4 Sincronizaremos los cambios con el proyecto en GitHub
````
Repítelo un par de veces, aunque suene un poco raro. Enseguida lo vais a entender. 

Aplicado a nuestro proyecto, lo que haremos esta semana será:
``` bash
1 Replicaremos el proyecto CursoHacker con url https://github.com/quiquee/CursoHacker.git localmente con 'clone'
2 Añadiremos el directorio Semana-2/ejercicios-<usuario> al proyecto con 'add'
3 Confirmaremos y documentaremos los cambios con 'commit'
4 Subiremos los cambios al proyecto en GitHub con 'push'
```
Y ahora podeis intentarlo hacer sin copiar y pegar, o podéis hacerlo copiando lo que yo he hecho. Recordar el objetivo
es guardar en el repositorio de GitHub el progreso de esta semana, que cada uno hemos realizado en nuestro directorio:

Replicar el proyecto localmente:
``` bash
enrique@raspberrypi:~ $ git clone https://github.com/quiquee/CursoHacker.git
Cloning into 'CursoHacker'...
remote: Counting objects: 55, done.
remote: Compressing objects: 100% (50/50), done.
remote: Total 55 (delta 23), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (55/55), done.
Checking connectivity... done.
```
Ahora tendréis una copia de CursoHacker en vuestro directorio local

Añadir al proyecto el directorio donde hemos hecho los ejercicios de la línea de comando. Lo haremos copiando
el directorio ejercicios-<usuario> en el directorio del proyecto local
``` bash
enrique@raspberrypi:~ $ cd CursoHacker/
enrique@raspberrypi:~/CursoHacker $ cp -R ../ejercicios-enrique Semana-2
enrique@raspberrypi:~/CursoHacker $ git add Semana-2/ejercicios-enrique
```
Documentar los cambios:
``` bash
enrique@raspberrypi:~/CursoHacker $ git commit
```
Y sincronizarlos con el repositorio remoto:
``` bash
enrique@raspberrypi:~/CursoHacker $ git push
```

Si todo ha ido bien podréis ir a ver en https://github.com/quiquee/CursoHacker/ que ahora está vuestro ejercicio con las
respuestas bajo un nuevo directorio que antes no existía. No es sencillo conceptualizar esto, así que si hay dudas o problemas no dejéis de decírmelo.

Suerte !!!
