# Trabajando con GitHub

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

