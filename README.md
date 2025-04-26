### [tutorial](https://www.youtube.com/playlist?list=PLu71SKxNbfoDOf-6vAcKmazT92uLnWAgy)

### [UV documentation](https://docs.astral.sh/uv/pip/environments/)
### [Django documentation](https://docs.djangoproject.com/en/5.2/)
### [Jinja documentation](https://jinja.palletsprojects.com/en/stable/)

### install uv
`powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"`

### create a project
`uv venv`

### activate virtual environment
`.venv\Scripts\activate`

### install Django
` uv pip install Django`

### start a Django Project
`django-admin startproject chaiaurDjango`
`cd chaiaurDjango`
`python manage.py runserver`

_ now you can check if all okay, by going to 127.0.0.1:8000 _

### File Structure till now
- Directory and venv are on the same level
- The project is inside directory
- The name of project and directoy is the same
![image](https://github.com/user-attachments/assets/ad0ff4af-e8d0-40da-8962-a0536347dffc)

### Overview of the Django System for Web Development
![image](https://github.com/user-attachments/assets/415b917e-13ca-4005-b9ae-7973437b073b)
Leftmost is User->Browser->Django and Rightmost is Model.py->DB

- Simpler Version ![image](https://github.com/user-attachments/assets/7658dc98-0c61-4d6b-8959-aa3af66b6e11)

### views.py

![image](https://github.com/user-attachments/assets/b516c91f-c5d9-4386-909e-6f92916c99dc)

### urls.py

![image](https://github.com/user-attachments/assets/2d893f2e-b203-485a-9cbc-488e21f72bdf)

- Create a templates folder in the Directory, same level as the project , add a website folder in it, and then add you index.html there
- Add this templates route in your settings.py (TEMPLATES.DIRS array) 'templates'

- Create a static folder in the Directory, same level as the project , add your styles.css in the.
- in the index.html, put the <link rel="stylesheet" href="{% static 'styles.css' %}" . Add {% load static %} . This enables us as templating engine.
-  Then finally go to settings.py, import os, after the STATIC_URL, add STATICFILES_DIRS = [os.path.join(BASE_DIR,'static')]

---

## Jinja (Lecture 4)

Variables are in {{ double curly braces }} , generally % .
Creating an app in Django Framweork - 
` python manage.py startapp chai `
Now add this app name in your settings.py file of your project, which would be in same level as the app. Add 'chai' in INSTALLED_APPS [] array.

Add django-html item and html value, in the Emmet: Include Languages, for VS Code Emmet.
In chai, create a templates folder, in that create a chai folder once more, and then your all_chai.html

Link this html page to your views.py of a subfolder. 
`def all_chai(request):
    return render(request, 'chai/all_chai.html') `

Now just like project's folder, add a urls.py by copying from there.
Then just link your project's urls.py to your chai app's urls.py, by importing include in the project urls.py

add path('chai/',include('chai.urls')) in the urlpatterns array then go to urls.py of your chai app
- remove the redundant routes, keep only one route, understand that the routes you define here, are as '/chai/[something]'

### Layout for re-usable, and for variable-based pages. Use block. Create a layout.html, inside templates, but outside website folder.


