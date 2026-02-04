
# Auditar proyectos de PSG2-2526 con Bluejay.

## 1. Crear y configurar el repositorio.

**1.1. Crear un repositorio en GitHub usando la actividad de GitHub Classroom correspondiente.**

- Actividad disponible en ENLACE
- Selecciona tu UVUS.
- Selecciona tu grupo `GX-XY` o créalo si aún no existe.
- Acepta el assignment para poder acceder al repositorio de GitHub.

## 2. Crear el workspace en ZenHub
- Crea un nuevo workspace sobre el repositorio de GitHub abriendo la extensión de ZenHub y seleccionando la organización `gii-is-psg2`.
- Usa el nombre PSG2-2526-GX-XY para el nuevo workspace, sustituyendo las X e Y igual que en pasos anteriores (por ejemplo: `PSG2-2425-G5-54`).
- Configura el workspace como `private` y asigna el repositorio GitHub al workspace creado (asegúrate de seleccionar la organización `gii-is-psg2`).
- Añade todos los miembros del grupo al workspace (antes deben haber accedido a la actividad de GitHub Classroom).
- Modificar los pipelines para que sigan la siguiente estructura **OBLIGATORIAMENTE:**
  - Elimina las pipelines denominadas `Icebox` y `Product Backlog`.
  - Renombra la pipeline `Sprint Backlog` a `Todo` (case sensitive).
  - Renombra la pipeline `Review/QA` a `In Review` (case sensitive).
- Como resultado tendremos un tablero donde las columnas principales que utilizaremos serán: `Todo, In Progress, In Review, Done` (case sensitive).

## 3. En la rama main modificar el archivo `info.yml`.
Vídeo explicativo para hacer los pasos 3 y 4 correctamente. Se recomienda verlo completo y detenidamente. [Enlace]()

info.yml:
```yaml
project:
  name: 'PSG2-2526-GX-XY'
  owner: 'LX'
  teamId: 'XY'
  identities:
    zenhub:
      workspaceId: "remplaza_este_texto_por_la_id_de_tu_workspace_de_zenhub"
  notifications:
    email: 'josemgarcia@us.es,japarejo@us.es,aruiz@us.es,cmuller@us.es,macuna@us.es,amarquez6@us.es'
  members:
    member1:
      name: 'José María'
      surname: 'García' 
      githubUsername: 'josemgarcia'
    member2:
      name: 'Jose Antonio'
      surname: 'Parejo'
      githubUsername: 'japarejo'
    member3:
      name: 'Antonio'
      surname: 'Ruiz'
      githubUsername: 'antonioruizcortes'
    member4:
      name: 'Carlos'
      surname: 'Müller'
      githubUsername: 'cmullercejas'
    member5:
      name: 'Lola'
      surname: 'De Acuña'
      githubUsername: 'loladacuna'
    member6:
      name: 'Alfonso'
      surname: 'Márquez'
      githubUsername: 'alfedu'
```

- Rellenar las X,Y.
    > Por ejemplo, el grupo 54 del Laboratorio 5:
    >```yaml
    >name: 'PSG2-2526-G5-54'
    >owner: 'L5'
    >teamId: '54'
    >```

- Sustituir los datos de cada memberN por los del miembro real.
- Si el número de miembros es menor de los que hay en la plantilla, eliminar los últimos que sobren (por ejemplo, si son 5 miembros, eliminar el bloque completo de `member6`)
- Modificar la cadena de `notifications.email` para que contengan sólo los correos de todos los miembros separados por comas y sin espacios.
- Sustituir workspaceId por la id del workspace de zenhub (Necesario haber completado el paso 2). La id es una cadena de caracteres aleatorios que se encuentra en la url al acceder al tablero de zenhub desde tu repositorio. Por ejemplo si mi url al acceder al tablero es https://github.com/gii-is-psg2/psg2-2526-zenhub-test/issues#workspaces/psg2-2526-zenhub-test-695b53b8e17454001c0787b3/board, mi workspaceId sería **695b53b8e17454001c0787b3**. Siempre empezando tras el último guión y terminando antes de /board. Imágen de ejemplo de como debería quedar el tablero de zenhub y de donde se saca el workspaceId:
<img width="1872" height="989" alt="Tablero de ZenHub" src="https://github.com/user-attachments/assets/bf7b1cd0-ac2a-460e-ae30-aac27dba6d03" />


## 3. Unir el proyecto a la asignatura auditada por Bluejay

- Accede a [join.bluejay.governify.io](https://join.bluejay.governify.io).
- Añade la **URL del repositorio** de GitHub.
- Click en **CHECK**. Si ha dado error revisa la [sintaxis](https://www.yamllint.com/) del info.yml.
- **Selecciona la clase** a la que te quieres unir (US-PSG2-2526) y especifica el código que te dará tu profesor.
- Click en **JOIN**.
- En caso de que haya algún otro problema al configurar Bluejay, el equipo de soporte está disponible en [un canal de Gitter dedicado](https://app.gitter.im/#/room/!VTAnLfNgxrEdydQgWd:gitter.im).


