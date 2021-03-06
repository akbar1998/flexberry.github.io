---
title: Компоненты ember-flexberry
keywords: ember
sidebar: flexberry-ember_sidebar
toc: false
permalink: ru/fe_base-component.html
lang: ru
summary: Перечень компонентов, используемых в ember-flexberry
---

Компоненты — это семейство API, предназначенных для описания новых элементов DOM, подходящих для повторного использования. [Модуль `ember-flexberry`](ef_landing_page.html) включает в себя большое количество разнообразных компонентов, под разные виды задач.

## Базовый компонент ember-flexberry

Для удобства разработки и сопровождения, общая логика компонентов былы вынесена в базовый компонент ([`flexberry-base-component`](https://github.com/Flexberry/ember-flexberry/blob/develop/addon/components/flexberry-base-component.js)). Почти все компоненты [модуля `ember-flexberry`](ef_landing_page.html) наследуются от него.

### Список свойств базового компонента

Свойство | Описание | Дефолтное значение
:--------------|:-----------------------------------------------------------|:-------------
`readonly` | Флаг: указывает, доступен ли компонент только для чтения. | false
`required` | Флаг: указывает, требуется ли компонент. | false
`componentName` | Определяет, уникальное имя компонента. |
`dynamicProperties` | Определяет, динамические свойства компонента | null
`relatedModel` | Определяет модель, к которой относится значение текущего компонента. | null
`appConfigSettingsPath` | Определяет, путь к настройкам компонента в конфигурации приложения. | 'APP.components.flexberryBaseComponent'
`appConfig` | Определяет, конфигурацию приложения | null
`appConfigSettings` | Определяет, объект настроек компонента из конфигурации приложения  | null
`currentController` | Определяет, текущий контроллер. | null

### Использование базового компонента

Базовый компонент не является элементом управления и его нельзя определять в шаблонах. Он используется только в качестве "Родителя" для других компонентов.

Рекомендуется наследоваться от базового компонента в следующих случаях:

* При создании встраиваемого компонента (может быть определен [внутри ячеек списков с помощью `getCellComponent`](https://flexberry.github.io/ru/ef_object-list-view.html#%D0%B2%D1%8B%D1%87%D0%B8%D1%81%D0%BB%D0%B8%D0%BC%D1%8B%D0%B5-%D1%81%D0%B2%D0%BE%D0%B9%D1%81%D1%82%D0%B2%D0%B0-%D0%B2-getcellcomponent))
* При необходимости получения контроллера формы внутри компонента.

В остальных случаях использовать базовый компонент в качестве "Родителя" или нет зависит от конкретной ситуации.

## Список компонентов доступных в ember-flexberry

* Компоненты для работы и отображения данных
    * Списка объектов:
        * [flexberry-objectlistview](fe_object-list-view.html)
        * flexberry-simpleolv
        * [flexberry-groupedit](fe_groupedit.html)
    * Текстового поля:
        * [flexberry-textarea](fe_edit-form-components.html#flexberry-textarea)
        * [flexberry-textbox](fe_edit-form-components.html#flexberry-textbox)
        * [flexberry-field](fe_edit-form-components.html#flexberry-field)
    * Даты:
        * [flexberry-datepicker](fe_edit-form-components.html#flexberry-datepicker)
        * [flexberry-simpledatetime](fe_edit-form-components.html#flexberry-simpledatetime)
    * Мастерового поля:
        * [flexberry-lookup](fe_lookup-component.html)
    * Логичесого поля:
        * [flexberry-checkbox](fe_edit-form-components.html#flexberry-checkbox)
        * [flexberry-ddau-checkbox](fe_edit-form-components.html#flexberry-ddau-checkbox)
    * Файла:
        * [flexberry-file](ef_file.html)
    * Перечисления:
        * [flexberry-dropdown](fe_edit-form-components.html#flexberry-dropdown)
    * JSON:
        * [flexberry-jsonarea](fe_edit-form-components.html#flexberry-jsonarea)
        * flexberry-tree
* Компоненты для визуализации информации:
    * flexberry-validationmessage
    * flexberry-validationsummary
    * [ui-message](ef_ui-message.html)
    * flexberry-icon
    * [flexberry-error](ef_error.html)
    * flexberry-tab-bar
    * flexberry-menu
    * [flexberry-toggler](ef_flexberry-toggler.html)
    * flexberry-dialog
* Компоненты управления формами:
    * [flexberry-button](fe_edit-form-components.html#flexberry-button)
    * [flexberry-colorpicker](fe_edit-form-components.html#flexberry-colorpicker)
    * [flexberry-ddau-slider](fe_edit-form-components.html#flexberry-ddau-slider)
    * form-load-time-tracker
    * modal-dialog
