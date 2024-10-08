# Manual Completo de Markdown

Markdown es un lenguaje de marcado ligero diseñado para formatear texto de manera sencilla. A continuación, se presenta un manual detallado de Markdown que cubre desde los conceptos básicos hasta las características avanzadas.

## 1. Encabezados

   Los encabezados se crean utilizando uno o más signos de ``#``. Los niveles van del 1 al 6.

   - Codigo

      ```markdown
      # Encabezado 1
      ## Encabezado 2
      ### Encabezado 3
      #### Encabezado 4
      ##### Encabezado 5
      ###### Encabezado 6
      ```

   - Vista

      # Encabezado 1
      ## Encabezado 2
      ### Encabezado 3
      #### Encabezado 4
      ##### Encabezado 5
      ###### Encabezado 6
   ---

## 2. Enfasis

   - **Negrita**<br>
   Se puede hacer texto en negrita usando dos asteriscos ``**`` o dos guiones bajos ``__``.

      - Codigo

         ````markdown
            **Texto en negrita**
            __Texto en negrita__
         ````

      - Vista

         **Texto en negrita**<br>
         __Texto en negrita__

   - **Cursiva**<br>
      Para cursiva, usa un asterisco ``*`` o un guion bajo ``_``.

      - Codigo

         ````markdown
            *Texto en cursiva*
            _Texto en cursiva_
         ````

      - Vista

         *Texto en cursiva*<br>
         _Texto en cursiva_

   - **Negrita y Cursiva**<br>
      Para combinar ambos, usa tres asteriscos `***` o tres guiones bajos ``___``.

      - Codigo

         ````markdown
            ***Texto en negrita y cursiva***
            ___Texto en negrita y cursiva___
         ````

      - Vista

         ***Texto en negrita y cursiva***<br>
         ___Texto en negrita y cursiva___
---      

## 3. Lista

   - Lista Desordenada<br>
   Usa asteriscos ``*``, signos más ``+``, o guiones ``-``.
      
      - Codigo

         ````markdown
            - Elemento 1
               - Subelemento 1
               - Subelemento 2
            - Elemento 2
         ````

         ````markdown
            * Elemento 1
               * Subelemento 1
               * Subelemento 2
            * Elemento 2
         ````

         ````markdown
            + Elemento 1
               + Subelemento 1
               + Subelemento 2
            + Elemento 2
         ````

      - Vista

         - Elemento 1
            - Subelemento 1
            - Subelemento 2
         - Elemento 2

   - Listas Ordenadas<br>
   Usa números seguidos de un punto ``.``.

      - Codigo

         ````markdown
            1. Primer elemento
               1. Subelemento 1
               2. Subelemento 2
            2. Segundo elemento
         ````
      - Vista

         1. Primer elemento
            1. Subelemento 1
            2. Subelemento 2
         2. Segundo elemento

   - Listas de Tareas<br>
   Crea listas de tareas con corchetes ``[]``.

      - Codigo

         ````markdown
            - [ ] Tarea pendiente
            - [x] Tarea completada
         ````
      - Vista
         
         - [ ] Tarea pendiente
         - [x] Tarea completada
---

## 4. Citas

   - Para citar texto, usa el símbolo ``>``.

      - Codigo
         `````markdown
         > Este es un bloque de cita.
         > 
         > Este es un bloque de cita extendido con una línea de separación.
         

      - Vista

         > Este es un bloque de cita.
         > 
         > Este es un bloque de cita extendido con una línea de separación.

   - Puedes anidar citas usando múltiples ``>``.

      - Codigo

         `````markdown
         > Cita de primer nivel
         >> Cita de segundo nivel
         

      - Vista   

         > Cita de primer nivel
         >> Cita de segundo nivel
---

## 5. Enlaces
   
   - Enlaces Básicos<br>
   Usa corchetes ``[]`` para el texto y paréntesis ``()`` para la URL.

      - Codigo

         ````markdow
         [Texto del enlace](http://www.ejemplo.com)
         ````
      
      - Vista
         
         [Texto del enlace](http://www.ejemplo.com)

   - Enlaces con Texto Alternativo<br>
   Puedes proporcionar un texto alternativo dentro de corchetes ``[]`` antes de la URL.

      - Codigo 
      - Vista
   
   - Enlaces Automáticos<br>
   Markdown también permite enlaces automáticos utilizando ángulos ``<>``.

      - Codigo 
      - Vista
---

## 6. Imágenes

   - Imágenes Básicas<br>
   Similar a los enlaces, pero precedido por un signo de exclamación ``!``.

      - Codigo 
      - Vista
   
   - Imágenes con Texto Alternativo

      - Codigo 
      - Vista
---

## 7. Codigo

   - Codigo en Linea<br>
   Para código en línea, usa una comilla invertida `````.
      
      - Codigo 
      - Vista
   
   - Bloques de Código<br>
   Para bloques de código, usa tres comillas invertidas ```````. Puedes especificar el lenguaje para el resaltado de sintaxis.
      
      - Codigo 
      - Vista
---

## 8. Tablas<br>
   Las tablas se crean usando barras verticales ``|`` y guiones ``-``.

   - Tablas Basicas

      - Codigo

         `````markdown
            | Columna 1 | Columna 2 |
            |-----------|-----------|
            | Fila 1, Celda 1 | Fila 1, Celda 2 |
            | Fila 2, Celda 1 | Fila 2, Celda 2 |
         

      - Vista

         | Columna 1 | Columna 2 |
         |-----------|-----------|
         | Fila 1, Celda 1 | Fila 1, Celda 2 |
         | Fila 2, Celda 1 | Fila 2, Celda 2 |


   - Alineación de Texto en Tablas<br>
   Puedes alinear el texto en las columnas usando dos puntos ``:``.
      
      - Alineación a la izquierda:

         - Codigo 
         - Vista

      - Alineación al centro:
      
         - Codigo 
         - Vista

      - Alineación a la derecha:
      
         - Codigo 
         - Vista
---

## 9. Líneas Horizontales<br>
   Crea líneas horizontales usando tres o más guiones ---, asteriscos ***, o guiones bajos ___.

   - Codigo 
   - Vista
---

## 10. HTML<br>
   Markdown permite incluir código HTML para elementos que no están cubiertos por Markdown.

   - Ejemplo HTML

      - Codigo 
      - Vista
---

## 11. Comentarios<br>
   Algunos sistemas permiten comentarios HTML que no se muestran en el documento renderizado.

   - Codigo 
   - Vista
---

## 12. Escapando Caracteres
   Para mostrar caracteres especiales, usa una barra invertida ``\``.

   - Codigo 
   - Vista
---

## 13. Otras Características

   - Subrayado<br>
   Markdown puro no soporta subrayado, pero algunos dialectos de Markdown y sistemas permiten usar HTML.

      - Codigo 
      - Vista

   - Definición de Listas<br>
   Para listas de definiciones, usa dos puntos ``:``.
      - Codigo 
      - Vista
---

## 14. Emoji

   - Lista de Emojis en Markdown<br>
   Estos son algunos de los emojis más comunes que puedes usar en Markdown. Para una lista completa, puedes consultar sitios como [Emoji Cheat Sheet](https://www.webfx.com/tools/emoji-cheat-sheet/) o utilizar cualquier herramienta de soporte de emojis dependiendo de la plataforma que utilices.

      - Caras

         - 😀 : `:grinning:`
         - 😃 : `:smiley:`
         - 😄 : `:smile:`
         - 😁 : `:grin:`
         - 😂 : `:joy:`
         - 🤣 : `:rofl:`
         - 😅 : `:sweat_smile:`
         - 😊 : `:blush:`
         - 😇 : `:innocent:`
         - 🙂 : `:slightly_smiling_face:`
         - 🙃 : `:upside_down_face:`
         - 😉 : `:wink:`
         - 😍 : `:heart_eyes:`
         - 😘 : `:kissing_heart:`
         - 😋 : `:yum:`
         - 😎 : `:sunglasses:`
         - 😤 : `:triumph:`
         - 😏 : `:smirk:`
         - 😒 : `:unamused:`
         - 😔 : `:pensive:`
         - 😖 : `:confounded:`
         - 😢 : `:cry:`
         - 😭 : `:sob:`
         - 😱 : `:scream:`
         - 😳 : `:flushed:`
         - 🤔 : `:thinking:`
         - 🤗 : `:hugs:`

      - Manos

         - 👍 : `:+1:` o `:thumbsup:`
         - 👎 : `:-1:` o `:thumbsdown:`
         - 👋 : `:wave:`
         - ✌️ : `:v:`
         - 👏 : `:clap:`
         - 🙌 : `:raised_hands:`
         - 🙏 : `:pray:`
         - 👊 : `:fist_oncoming:`
         - 🤞 : `:crossed_fingers:`
         - 🤙 : `:call_me_hand:`
         - 🖐️ : `:raised_hand_with_fingers_splayed:`
         - ✋ : `:raised_hand:`
         - 👈 : `:point_left:`
         - 👉 : `:point_right:`
         - 👇 : `:point_down:`
         - 👆 : `:point_up_2:`
         - 👌 : `:ok_hand:`

      - Corazones

         - ❤️ : `:heart:`
         - 💔 : `:broken_heart:`
         - 💖 : `:sparkling_heart:`
         - 💗 : `:heartpulse:`
         - 💙 : `:blue_heart:`
         - 💚 : `:green_heart:`
         - 💛 : `:yellow_heart:`
         - 💜 : `:purple_heart:`
         - 🖤 : `:black_heart:`
         - 💘 : `:cupid:`

      - Objetos

         - 📱 : `:iphone:`
         - 💻 : `:computer:`
         - ⌚ : `:watch:`
         - 📷 : `:camera:`
         - 🔍 : `:mag:`
         - 💡 : `:bulb:`
         - 🔧 : `:wrench:`
         - 🔒 : `:lock:`
         - 🛠 : `:hammer_and_wrench:`
         - 🧳 : `:luggage:`

      - Animales

         - 🐶 : `:dog:`
         - 🐱 : `:cat:`
         - 🦁 : `:lion:`
         - 🐻 : `:bear:`
         - 🐼 : `:panda_face:`
         - 🐨 : `:koala:`
         - 🐯 : `:tiger:`
         - 🦊 : `:fox_face:`
         - 🦋 : `:butterfly:`
         - 🐢 : `:turtle:`
         - 🐟 : `:fish:`
         - 🦄 : `:unicorn:`

      - Comida y bebida

         - 🍏 : `:green_apple:`
         - 🍎 : `:apple:`
         - 🍇 : `:grapes:`
         - 🍉 : `:watermelon:`
         - 🍓 : `:strawberry:`
         - 🍍 : `:pineapple:`
         - 🍔 : `:hamburger:`
         - 🍕 : `:pizza:`
         - 🍣 : `:sushi:`
         - 🍺 : `:beer:`
         - 🍷 : `:wine_glass:`
         - 🍸 : `:cocktail:`

      - Transporte

         - 🚗 : `:car:`
         - 🚕 : `:taxi:`
         - 🚙 : `:blue_car:`
         - 🚌 : `:bus:`
         - 🚎 : `:trolleybus:`
         - 🚑 : `:ambulance:`
         - 🚓 : `:police_car:`
         - 🚒 : `:fire_engine:`
         - 🚲 : `:bike:`
         - 🛴 : `:kick_scooter:`
         - ✈️ : `:airplane:`
         - 🚀 : `:rocket:`

      - Naturaleza

         - 🌞 : `:sun_with_face:`
         - 🌝 : `:full_moon_with_face:`
         - 🌚 : `:new_moon_with_face:`
         - 🌈 : `:rainbow:`
         - 🌊 : `:ocean:`
         - 🔥 : `:fire:`
         - 🌪️ : `:tornado:`
         - 🌟 : `:star2:`
         - ⭐ : `:star:`

      - Otros

         - 🎉 : `:tada:`
         - 🎂 : `:birthday:`
         - 🎁 : `:gift:`
         - 🎈 : `:balloon:`
         - 🏆 : `:trophy:`
         - 🎮 : `:video_game:`
         - 🕹️ : `:joystick:`
         - 🏅 : `:medal_sports:`
         - ⚽ : `:soccer:`
         - 🏀 : `:basketball:`
---

      
