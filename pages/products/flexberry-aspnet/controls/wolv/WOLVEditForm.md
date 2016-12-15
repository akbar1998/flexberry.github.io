---
title: Варианты открытия формы редактирования при создании\редактировании объекта в WOLV
sidebar: flexberry-aspnet_sidebar
keywords: Flexberry ASP-NET
toc: true
permalink: ru/w-o-l-v-edit-form.html
folder: product--folder
lang: ru
---
Эта статья описывает часть информации о [WebObjectListView](web-object-list-view.html).

Данные способы настройки разработаны в замен [устаревшей](thick-box-click-in-row.html).

## Открытие web-формы редактирования

[Web-форма редактирования](web-edit-form.html) со списковой формы открывается в случае, когда необходимо:

* Создать новый объект.
* Создать новый объект на основе существующего.
* Отредактировать существующий объект.
* Открыть существующий объект на просмотр.

### Варианты открытия

Форма может открываться:

1. В текущем окне браузера.
2. В другом окне браузера:
3.
    * окно может быть в виде '''соседней вкладки''';
    * или в виде '''модального окна'''.

### Настройка открытия формы редактирования

Соответственно, для настройки открытия [web-формы редактирования](web-edit-form.html) необходимо:

1. Определиться, открывается ли [web-форма редактирования](web-edit-form.html) в текущем окне браузера или в новом
2. Если в новом, то будет ли это новая вкладка или модальное окно

Соответственно, после ответа на эти вопросы следует установить 2 настройки:

1. `WebObjectListView1.Operations.OpenEditorInNewWindow = true/false;`
2. `WebObjectListView1.[Operations](w-o-l-v-operations.html).OpenEditorInModalWindow = true/false;`

{% include note.html content='Обратите внимание, что при установленной `OpenEditorInNewWindow == false` вторая настройка не имеет смысла.' %}

## Открытие формы редактирования и режим Read-only

При открытии объекта одним пользователем, объект блокируется. В это время другие пользователи могут открывать объект только на чтение. 

Если объект, на [web-форму редактирования](web-edit-form.html) которого пытается зайти пользователь, заблокирован, то ему выдастся сообщение
"Объект заблокирован другим пользователем. Хотите открыть его только на чтение?" и варианты ответа "Да" и "Нет".

Соответственно, при выборе варианта "Да" пользователю откроется данная форма в режиме [только чтение](read-only-web.html).

Если пользователь выберет "Нет", то произойдет возврат на списковую форму.

Визуально возврат будет выглядеть по разному для разных вариантов открытия [web-формы редактирования](web-edit-form.html):

1. Если web-форма редактирования была открыта в том же окне браузера, произойдет перенаправление (redirect) на списковую форму.
2. Если web-форма редактирования была открыта в соседней вкладке, то вкладка закроется и произойдет переключение на вкладку со списком.
3. Если web-форма редактирования была открыта в модальном окне, произойдет закрытие модального окна.

Если пользователь не авторизован, то при открытии им объекта, он блокироваться не будет. 