--- 
title: Start web application 
sidebar: guide-practical-guides_sidebar 
keywords: guide 
toc: true 
permalink: en/gpg_start-application.html 
lang: en 
autotranslated: true 
hash: c5e4650693d89816863f560d6c618c9c7a5fea8de5db6fa26aa00e54135afec2 
--- 

1.After generating the solution with the web application is successfully completed, it is necessary to run the project in `Visual Studio`: it is necessary to click right mouse button on stage and choose from the menu `ASP.NET` -> `C#` -> `Открыть in Visual Studio...`, or you can open a file with the extension `.sln` from the folder to which the generated solution (the folder was already open, if you have confirmed the opening of the directory with the generated solution). 

2.If you selected a menu item `ASP.NET` -> `C#` -> `Открыть in Visual Studio...`, you will be presented with a log of actions on opening of the file. To shut it down. 

3.The project opens in `Visual Studio`. 

![](/images/pages/guides/flexberry-aspnet/visual-studio.jpg) 

4.To run the web application without debugging: to do this, select the menu item `Debug` -> `Start Without Debugging` or just click `Ctrl F5`. 

![](/images/pages/guides/flexberry-aspnet/start-without-debugging.png) 

5.The web application appears in the selected toolbar browser ![](/images/pages/guides/flexberry-aspnet/browser.png). 

6.At startup, the web application will display the login form: 

![](/images/pages/guides/flexberry-aspnet/authentication-form.jpg) 

To log in to the app, you must enter the credentials previously generated by the user, that is `admin/admin`. 

7.After authentication, the main page appears in the web application: 

![](/images/pages/guides/flexberry-aspnet/application.png) 

The generated web application has a tree menu corresponding to the structure of containers specified when setting up a class with the stereotype `application` on the class diagram obtained when generating a prototype app in [Flexberry Designer]. 

In addition, the generated web application allows you to: 

* view a list of entity instances (objects) corresponding to classes of the source class diagram constructed during the analysis of the subject area (domain objects); 
* to perform operation insert/change/delete (CRUD operations) on objects subject области; 
* perform additional operations with lists of domain objects (filtering, configuring the display columns, export data to Microsoft Excel, etc.) 
* change theme (there are 4 ready to use themes); 
* for a user with the administrator role can access additional menu items that allow you to manage users, roles and their privileges, as well as to view the logs of the application. 

{% include note.html content="Start the web application only from Visual Studio.
All forms with Cyrillic names when generating transliterated. This is done to avoid errors associated with Cyrillic URL in the address bar." %} 

## Go 

* <i class="fa fa-arrow-left" aria-hidden="true"></i> [Generating web applications](gpg_generation-application.html) 
* [Enable ASP.NET State Service](gpg_asp-net-state-service.html) <i class="fa fa-arrow-right" aria-hidden="true"></i> 



{% include callout.html content="Переведено сервисом «Яндекс.Переводчик» <http://translate.yandex.ru>" type="info" %}