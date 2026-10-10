### Причина проблеми
  Текст із поля "welcomeText" файлу config.json:4 виводиться всередині елемента <div id="text-wrapper">. У файлі index.html:34-37 для цього елемента задано CSS-властивість text-       
  transform: uppercase;, яка змушує браузер трансформувати весь текст у верхній регістр (великі літери) під час відображення:
    <div id="text-wrapper" style="top: 50%; left: 50%; position: absolute; color: #fff; transform: translate(-50%, -50%); text-align: center;
            text-transform: uppercase; font-family: Arial, Helvetica, sans-serif; font-weight: 400; line-height: 1.5em; font-size: large; white-space: nowrap;
            user-select: none; pointer-events: none;
        ">
  ──────
  ### Як зберегти оригінальний регістр символів
  #### Варіант 1: Видалити CSS-властивість (Рекомендовано)

  У файлі index.html:34-37 видаліть text-transform: uppercase; (або замініть на text-transform: none;):

    <div id="text-wrapper" style="top: 50%; left: 50%; position: absolute; color: #fff; transform: translate(-50%, -50%); text-align: center;
            font-family: Arial, Helvetica, sans-serif; font-weight: 400; line-height: 1.5em; font-size: large; white-space: nowrap;
            user-select: none; pointer-events: none;
        ">
