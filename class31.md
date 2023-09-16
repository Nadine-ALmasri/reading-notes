# Razor Pages
## Introduction to Razor Pages

Razor Pages are introduced as a new way to build web applications in ASP.NET Core 2. They are sometimes seen as a revival of an old concept called WebMatrix.
## Why Razor Pages?

Razor Pages are presented as a more beginner-friendly and lightweight alternative to MVC for web development.
They are considered suitable for smaller projects where the complexity of controllers and models is not necessary.
## Creating Razor Pages Application

Visual Studio 2017 Preview 2 provides a template for creating Razor Pages applications.
The application structure resembles MVC but lacks separate folders for controllers and views.
## Application Structure

The project structure includes a "Pages" folder containing Razor views, referred to as "pages."
Razor Pages share the same Program and Startup classes as MVC applications.
## Separation of Logic and Presentation

Razor Pages allow for code-behind files named as "PageName.cshtml.cs," where the class is called the "page model."
This separation enables developers to maintain logic separately from the presentation.
## Exploring a Razor Page

A Razor page includes a @page directive to identify it as a Razor page.
Developers can specify a model, similar to a view model, which blends controller and model concepts.
Handler methods like OnGet() are used for GET requests and have asynchronous counterparts.
## Razor Page with No Code-Behind

Demonstrates how a Razor page can function without a separate code-behind file.
In this case, methods and properties are defined within the @functions section within the page itself.
## Wrapping Up

Reflects on the usage of Razor Pages as a lightweight option for beginners and simple in-house web projects.
Questions whether Razor Pages will have distinct use-cases compared to the well-established MVC framework.
## comparison between MVC and Razor Pages

 ### MVC:

- Handling Requests: MVC relies on routing, which can be configured to map requests to specific controller actions using a combination of controller and action names (e.g., /staff/index maps to the Index action in the StaffController).

- Code Placement: In MVC, application logic is primarily placed within controller actions. This is where request validation, business logic, and service calls are typically handled.

- Presentation Code (Markup): MVC actions usually return views, and the HTML markup is placed within these views. MVC follows a convention for locating views based on controller and action names.

- Data Display: To display data in views, you can create ViewModels, which are separate classes with properties for the data you want to present. These ViewModels are passed from controller actions to views.

- Folder Structure: MVC applications conventionally organize code into separate folders for controllers, views, and view models.

## Razor Pages:

- Handling Requests: Razor Pages use a simpler routing mechanism. Requests are directly mapped to Razor Pages within the "Pages" folder. For example, a request to /contact is mapped to Contact.cshtml in the "Pages" folder.

- Code Placement: In Razor Pages, application logic resides within Page Models. These Page Models are associated with Razor Pages and handle HTTP verbs like GET and POST.

- Presentation Code (Markup): Markup for Razor Pages is included within the .cshtml files themselves. There's no need to locate separate views because the Razor Page handles both the code and markup.

- Data Display: Data for Razor Pages can be directly added to the Page Model as properties. You set these properties within the Page Model's methods (e.g., OnGet). There's no need for separate ViewModels.

- Folder Structure: Razor Pages are organized within the "Pages" folder, and each Razor Page consists of both the .cshtml file (for markup) and a corresponding .cs file (acting as a controller).

This comparison highlights the differences between MVC and Razor Pages, including how they handle requests, where code is placed, where markup resides, how data is displayed, and their respective folder structures. It's essential to consider these distinctions when choosing the appropriate framework for your ASP.NET Core project.