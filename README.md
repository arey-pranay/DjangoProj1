### [uv documentation](https://docs.astral.sh/uv/pip/environments/)

### [tutorial](https://www.youtube.com/playlist?list=PLu71SKxNbfoDOf-6vAcKmazT92uLnWAgy)

### [Django documentation](https://docs.djangoproject.com/en/5.2/)

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




