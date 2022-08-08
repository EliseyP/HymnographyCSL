# HymnographyCSL
Some instruments fo editing church-slavonic texts.

Working on the ODT documents **with styles** from templates from [csl_odt2tex](https://github.com/EliseyP/csl_odt2tex) project.

**Setting Running Header dialog**


![](Images/cslRunnHeaderB.png)  with this dialog `Running Header` can be obtained from `Title` and set for the document.

**Creating and Styles operation**

![](Images/cslNewFromTemplateB.png) - create new csl document from template [Гимнография 20 новый.ott](https://github.com/EliseyP/csl_odt2tex/blob/main/%D0%93%D0%B8%D0%BC%D0%BD%D0%BE%D0%B3%D1%80%D0%B0%D1%84%D0%B8%D1%8F%2020%20%D0%BD%D0%BE%D0%B2%D1%8B%D0%B9.ott)

![](Images/cslMakeBlackCopyB.png) - make black copy for red-colored csl document (in the same directory with `_BLACK.odt` suffix).

<img src="Images/docRed.png" width="30"> - apply red-colored styles.

<img src="Images/docBlack.png" width="30"> - apply black-colored styles.

**csl2pdf**

![Dialog](Images/Csl2Pdf_gui.png) - dialog running.  

![Red colored](Images/Csl2Pdf_red.png) - silent run (red-colored PDF).  

![Black colored](Images/Csl2Pdf_black.png) - silent run (black-colored PDF).

### Setting Running Header dialog

Запуск `gui`-диалога, позволяющего оперировать текстом колонтитула для документа с шаблоном `Гимнография 20 новый` из проекта [csl_odt2tex](https://github.com/EliseyP/csl_odt2tex).

Для запуска диалога есть своя кнопка ![](images/runnheader_16.png) на отдельной `toolbar`-панели, а также подменю в `Menu|Сервис|Addons`.

После запуска диалога в поле `Заглавие` автоматически помещается содержимое `user`-поля `TitleInText` (оно м.б. пустым, например, при создании документа).  
Также есть кнопка `Из текста`, для проведения этой операции **вручную**, при этом в поле помещается текст абзаца со стилем `Заглавие` (первый найденный).

У поля `Колонтитул` есть кнопка `Из Заглавия`, которая позволяет скопировать текст заглавия в поле колонтитула. Текст может редактироваться.

По нажатии кнопки `Обновить`, содержимое полей `Заглавие` и `Колонтитул` заносятся в `user`-поля `TitleInText` и `RunningHeader` соответственно. Содержимое поля `RunningHeader` при этом автоматически помещается в колонтитулы документа.

В данном примере укорочен текст Заглавия, слишком длинный для колонтитула.

<img src="Images/cslRHexample.jpeg" width="800" height="220">


### csl2pdf

Для работы расширения необходим скрипт `csl2tex.py` из проекта [csl_odt2tex](https://github.com/EliseyP/csl_odt2tex). 
Указать путь можно в **Параметрах** расширения. Меню `Сервис|Управление расширениями|CslHymnography.oxt`.  
**Note:** необходим весь каталог из этого проекта.

<img src="Images/OxtOptions.jpeg" width="1500" height="430">

`Pdf`-файл (а также промежуточный `.tex` файл) сохраняется в том же каталоге, что и открытый документ. Имя файла, если не изменено в диалоге, совпадает с именем открытого `odt`-документа (без расширения).  
