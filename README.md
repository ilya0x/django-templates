# <img src="./images/django-full-50.png" alt="Django">

Django is a high-level web framework for Python that simplifies web application
development. It includes a comprehensive set of features and tools, follows the
Model-View-Controller (MVC) architecture, prioritizes security and scalability,
and benefits from a thriving developer community and ecosystem of extensions.
This makes Django a powerful choice for building web applications efficiently
and securely.

- <b>Batteries-Included:</b> Django follows the "batteries-included" philosophy,
  offering a wide range of pre-built components and features for common web
  development tasks, like authentication, database management, and URL routing.

- <b>Model-View-Controller (MVC) Architecture:</b> Django follows the
  Model-View-Controller (MVC) architecture, which helps maintain a clean
  separation of concerns between data models (representing the database), views
  (handling user interface logic), and templates (defining the presentation).

- <b>Secure and Scalable:</b> Django emphasizes security best practices by
providing features like built-in protection against common web vulnerabilities
(Cross-Site Scripting, SQL Injection, etc.) and encourages us to write secure code.

<br>

## <img src="./images/template-20.png" alt="template"> Templates & Project Examples

<b>Standard File Structure Template</b> -<br>
<br>
<a href="https://github.com/ilya0x/crm-app"><b>CRM App</b></a> - A customer
relationship management (CRM) application with complete block and inline notes
on customization of variables.<br>
<br>
<a href="https://github.com/ilya0x/topfloor0x-marketplace">
<b>MerchantGuild.Shop Marketplace</b></a> - A complete functioning marketplace.
Live at merchantguild.shop<br>
<br>
<a href="https://github.com/ilya0x/rolld20-app"><b>RollD20 App</b></a> - A
tabletop gaming support app with video, voice and text chat integration. Live at
rolld20.online<br>
<br>
<a href="https://github.com/ilya0x/web-api"><b>Web API</b></a> - interactive
Web API using Django REST framework.

<br>

## <img src="./images/vscode-20.png" alt="Flask"> Visual Studio Code Extensions

<a href="https://marketplace.visualstudio.com/items?itemName=batisteo.vscode-django">
<b>Django</b></a> - Beautiful syntax and scoped snippets<br>
<br>
<a href="https://marketplace.visualstudio.com/items?itemName=thebarkman.vscode-djaneiro">
<b>Djaneiro - Django Snippets</b></a> - A collection of snippets for django
templates, models, views, fields & forms.<br>
<br>
<a href="https://marketplace.visualstudio.com/items?itemName=Emeric-Defay.django-factory">
<b>Django Factory</b></a> - Generating files (urls.py, serializer.py, app.html,
forms.py, admin.py, ...) based on views and models files from your apps.<br>

<br>

## 📝Notes

> These notes are updated on regular basis

<!--TODO: Table of Contents -->

<br>

### Project Setup

A step-by-step walkthrough of Django project setup:

1. It is recommended to work in a virtual environment. Python comes with virtual
   environment generator "venv".<br>
   Create a virtual environment by running: `$ python3 -m venv env`
2. Activate the virtual environment: `$ .\env\Scripts\Activate.ps1`
   - Deactivate with `$ deactivate`
3. Install Django: `$ pip install django`
4. Start Django project: `$ django-admin startproject name-of-project`
5. If using Git & GitHub, you can exclude the `env` by creating a `.gitignore`
   file in your project's root directory with entry for the folder you want to exclude:
   `/excluded_folder_name/`

<br>

> [Django Project – Code a CRM App Tutorial
](https://youtu.be/t10QcFx7d5k?si=nXjnBPtPB2htBcnh) has a section at beginning
on how to setup MySQL with Django.

<br>

### Function-Based Views

Function-Based Views (FBVs) in Django are a way to define the logic for handling
HTTP requests in a Django web application by using Python functions. They are a
fundamental concept in Django for building web applications and are an
alternative to Class-Based Views (CBVs). Here's an explanation of Function-Based
Views in Django:

**Basic Structure:** In a Function-Based View, you define a Python function to
handle a specific URL pattern or HTTP request. This function takes an HTTP
request object as its argument and returns an HTTP response object. The
function's name usually reflects the view's purpose, such as `my_view(request)`.

**Simplicity:** Function-Based Views are known for their simplicity and
straightforwardness. They are suitable for handling simple views or views that
perform a single action in response to an HTTP request. This simplicity can make
them easier to understand and maintain for small to moderately complex views.

**Decorators:** You can use Python decorators to add functionality to Function-Based
Views. Decorators allow you to perform tasks like authentication, permission
checks, and caching before or after the view function is executed. Django
provides built-in decorators like `@login_required` and `@permission_required` for
this purpose.

<br>

### Class-Based Views

Class-Based Views (CBVs) in Django are an alternative approach to defining the
logic for handling HTTP requests in a Django web application. Unlike
Function-Based Views (FBVs), which use functions to handle requests, CBVs use
Python classes to organize and encapsulate view behavior. Here's an explanation
of Class-Based Views in Django:

**Class Structure:** In Class-Based Views, views are defined as Python classes
rather than functions. Each view is represented as a class, and the HTTP methods
(GET, POST, etc.) are handled by class methods with specific names, such as
`get()`, `post()`, `put()`, and so on. The class name usually reflects the view's
purpose.

**Reusability:** One of the primary advantages of CBVs is their ability to promote
code reuse. You can create base view classes with common functionality and then
inherit from these base classes to create specific views. This encourages the
DRY (Don't Repeat Yourself) principle and makes it easier to maintain and extend
your views.

**Mixins:** Django provides a set of reusable view components called mixins, which
are classes that can be mixed into your view classes to add specific behavior.
For example, the `LoginRequiredMixin` mixin can be used to require user
authentication for a view. Mixins enhance the flexibility of CBVs.

**Decorators:** You can still use decorators with Class-Based Views to add
functionality, similar to Function-Based Views. Decorators are applied to class
methods rather than functions. For instance, you can use the `@login_required`
decorator to require authentication for specific HTTP methods.
