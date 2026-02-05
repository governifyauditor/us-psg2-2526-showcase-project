
# Auditar proyectos de PSG2-2526 con Bluejay.

Vídeo explicativo para hacer todos los pasos correctamente. SE RECOMIENDA VERLO COMPLETO Y DETENIDAMENTE. [Enlace](https://www.youtube.com/watch?v=Ygjj3RuBc4w)

## 0. Guía de cómo rellenar las X e Y
En los siguientes pasos se deberá sustituir las letras X e Y por un número correspondiente al grupo del trabajo. Aquí se explica cómo hacer esa sustitución:
- Cómo rellenar las X e Y.
  > Por ejemplo, el grupo 4 del Laboratorio 5:
  >
  > X = 5,
  > Y = 4
  >```yaml
  >name: 'PSG2-2526-G5-54'
  >owner: 'L5'
  >teamId: '54'
  >```
  > Por ejemplo, el grupo 1 del Laboratorio 2:
  >
  > X = 2,
  > Y = 1
  >```yaml
  >name: 'PSG2-2526-G2-21'
  >owner: 'L2'
  >teamId: '21'
  >```

## 1. Crear y configurar el repositorio

**Crear un repositorio en GitHub usando la actividad de GitHub Classroom correspondiente.**

- Actividad disponible en https://classroom.github.com/a/bBUMSf7j
- Selecciona tu UVUS.
- Selecciona tu grupo `GX-XY` o créalo si aún no existe (Sustituye X e Y siguiendo el paso 0).
- Acepta el assignment para poder acceder al repositorio de GitHub.

## 2. Crear el workspace en ZenHub
- Crea un nuevo workspace sobre el repositorio de GitHub abriendo la extensión de ZenHub y seleccionando la organización `gii-is-psg2`.
- Usa el nombre PSG2-2526-GX-XY (Sustituye X e Y siguiendo el paso 0) para el nuevo workspace.
- Configura el workspace como `private` y asigna el repositorio GitHub al workspace creado (asegúrate de seleccionar la organización `gii-is-psg2`).
- Añade todos los miembros del grupo al workspace (antes deben haber accedido a la actividad de GitHub Classroom).
- Añade también como miembro del workspace tanto a tu tutor (él/ella te indicará su usuario de GitHub) como al usuario `governifyauditor`
- Modifica los pipelines para que sigan la siguiente estructura **OBLIGATORIAMENTE:**
  - Elimina las pipelines denominadas `Icebox` y `Product Backlog`.
  - Renombra la pipeline `Sprint Backlog` a `Todo` (case sensitive).
  - Renombra la pipeline `Review/QA` a `In Review` (case sensitive).
- Como resultado tendremos un tablero donde las columnas principales que utilizaremos serán: `Todo, In Progress, In Review, Done` (case sensitive).

## 3. Modificar el archivo info.yml
En la rama main del repositorio modificar el archivo `info.yml`.

info.yml:
```yaml
project:
  name: 'PSG2-2526-GX-XY'
  owner: 'LX'
  teamId: 'XY'
  identities:
    zenhub:
      workspaceId: 'change_this_text_with_your_zenhub_workspace_id'
  notifications:
      email: 'josemgarcia@us.es,japarejo@us.es,iestrada@us.es,agarcia29@us.es,macuna@us.es,amarquez6@us.es'
  members:
    member1:
      name: 'José María'
      surname: 'García' 
      githubUsername: 'josemgarcia'
    member2:
      name: 'José Antonio'
      surname: 'Parejo'
      githubUsername: 'japarejo'
    member3:
      name: 'Bedilia'
      surname: 'Estrada'
      githubUsername: 'Adartse'
    member4:
      name: 'Alejandro'
      surname: 'García'
      githubUsername: 'Alex-GF'
    member5:
      name: 'Lola'
      surname: 'De Acuña'
      githubUsername: 'loladacuna'
    member6:
      name: 'Alfonso'
      surname: 'Márquez'
      githubUsername: 'alfedu'
```

- Sustituye X e Y siguiendo el paso 0.
- Sustituye los datos de cada memberN por los del miembro real.
- Si el número de miembros es menor de los que hay en la plantilla, elimina los últimos que sobren (por ejemplo, si son 5 miembros, eliminar el bloque completo de `member6`)
- Modifica la cadena de `notifications.email` para que contenga sólo los correos de todos los miembros separados por comas y sin espacios.
- Sustituye `workspaceId` por la id del workspace de zenhub (Necesario haber completado el paso 2). La id es una cadena de caracteres aleatorios que se encuentra en la url al acceder al tablero de ZenHub desde tu repositorio. Por ejemplo, si mi url al acceder al tablero es https://github.com/gii-is-psg2/psg2-2526-zenhub-test/issues#workspaces/psg2-2526-zenhub-test-695b53b8e17454001c0787b3/board, mi workspaceId sería **695b53b8e17454001c0787b3**. Siempre empezando tras el último guión y terminando antes de /board. Aquí tienes una imagen de ejemplo de cómo debería quedar el tablero de zenhub y de dónde se saca el workspaceId:
<img width="1872" height="989" alt="Tablero de ZenHub" src="https://github.com/user-attachments/assets/bf7b1cd0-ac2a-460e-ae30-aac27dba6d03" />


## 4. Unir el proyecto a la asignatura auditada por Bluejay

- Accede a [join.bluejay.governify.io](https://join.bluejay.governify.io).
- Añade la **URL del repositorio** de GitHub.
- Click en **CHECK**. Si ha dado error, revisa la [sintaxis](https://www.yamllint.com/) del info.yml.
- **Selecciona la clase** a la que te quieres unir (US-PSG2-2526) y especifica el código que te dará tu profesor.
- Click en **JOIN**.
- En caso de que haya algún otro problema al configurar Bluejay, el equipo de soporte está disponible en [un canal de Gitter dedicado](https://app.gitter.im/#/room/!VTAnLfNgxrEdydQgWd:gitter.im).


