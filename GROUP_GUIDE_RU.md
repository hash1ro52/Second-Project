# Как разобраться с проектом вчетвером

Это форма регистрации для Alcohol Ranking Collection, связанная с вашей идеей каталога и отзывов. Весь сайт на английском. Для просмотра откройте `index.html` в браузере, а папку проекта - в VS Code.

Ниже предложено распределение подготовки к объяснению. Укажите реальные имена и фактический вклад участников перед сдачей.

## Участник 1 - HTML и структура

Разберитесь с `header`, `nav`, `main`, `form`, `fieldset`, `legend` и `footer` в `index.html`. Объясните, почему форма разделена на аккаунт, профиль и предпочтения. Покажите, как `for` у label связан с `id` поля.

Можно сказать:

> The form has three sections: account details, profile information and preferences. Fieldsets group related inputs. Labels explain what the user should enter and make the controls easier to use.

## Участник 2 - CSS и оформление

Посмотрите начало `style.css`, затем `.form-card`, `.form-grid`, `.choice` и `.submit-button`. Две колонки сделаны через Grid. Варианты выбора располагаются через Flexbox. Цвета, отступы и шрифты задаются обычными CSS-свойствами.

Можно сказать:

> We use a burgundy colour with a light background. The layout is simple and consistent. Short fields are placed in two columns, while longer fields take the full width.

## Участник 3 - телефон и доступность

В конце `style.css` найдите `@media (max-width: 650px)`: на узком экране колонки становятся одной. Покажите `:focus-visible`, ссылку Skip to content, `aria-describedby` и большие области нажатия у вариантов выбора.

Проверьте форму через Tab и Shift+Tab. Радиокнопки переключаются стрелками, флажки - пробелом. Ползунок тоже работает стрелками.

Можно сказать:

> On a small screen, the fields are stacked in one column. Users can navigate with a keyboard. Focus is visible, and the hints are connected to the relevant inputs.

## Участник 4 - проверка и оценка удобства

В HTML найдите `required`, `type="email"`, `pattern`, `min`, `max`, `step` и `maxlength`. В CSS найдите `:user-invalid`. Браузер проверяет поля, а CSS показывает оформление ошибки. `complete.html` показывает результат проверки, но не создаёт настоящий аккаунт.

Оценка и фактически выполненные проверки описаны в `docs/evaluation.md`. В ней нет выдуманных интервью с пользователями. Перед сдачей всей группе полезно самостоятельно повторить проверки и уточнить текст по своим наблюдениям.

Можно сказать:

> Validation uses HTML attributes instead of JavaScript. The browser checks the values before opening the confirmation page. The evaluation covered clear labels, error feedback, keyboard navigation and the mobile layout.

## Что стоит знать каждому

- `index.html` - структура и содержимое.
- `style.css` - внешний вид и адаптация.
- `complete.html` - демонстрационная страница завершения.
- `action` у form задаёт страницу перехода после успешной проверки.
- У личных полей нет `name`, чтобы демоверсия не передавала их в URL. Одна группа radio имеет общее имя для правильного переключения.
- `accept` у файла только подсказывает типы в окне выбора. Файл никуда не загружается.
- Дата для 18+ зафиксирована на день подготовки; без JavaScript она не обновляется автоматически.
- Проверка в браузере не заменяет сервер. Для учебного задания достаточно показать форму; настоящая регистрация потребовала бы отдельной серверной части.

## Перед сдачей

1. Всем открыть сайт и попробовать заполнить форму.
2. Внести свои имена в `docs/submission.pdf`.
3. Проверить файлы в `hash1ro52/Second-Project` и настройки GitHub Pages.
4. Проверить реальную ссылку сайта и вставить её в PDF.
5. Отправить в itslearning PDF с работающей ссылкой, макетами и оценкой удобства.

