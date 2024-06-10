### Online-Job-Portal-using-Django

A job portal made using the python framework Django.

### Description
Django Job Portal is an open-source online platform designed to streamline the job search process for both job seekers and employers. Built with Django and utilizing SQLite for database management, this project offers a user-friendly interface for posting and applying to job listings.

Job portal is a web application where the candidates can register and search for suitable jobs and employers can register to post job vacancies at their company. The application provides job catalogue and information which helps the candidates decide which jobs to apply for.

The 3 user roles are Candidate , Employer and Admin

## Candidate
     * Can search for jobs based on different criterias ( Location , Role , Contract )
     * Apply for any number of jobs
     * View applied jobs in the dashboard

## Employer
    * Can add / update / delete jobs
    * Can view job applications ( Only for their jobs )

## Admin
    * Can add / remove employers
    * Can add / remove any user
    * Can add / update / delete jobs
    * Can view / delete any job applications

## Tech Stack:

# Django:
    - Powerful web framework for building web applications in Python.
# SQLite:
    - Lightweight, serverless database engine used for data storage.
# Bootsrtap:
    - Dsign the website with the help bootstrap
# HTML/CSS
    - create a template 

## Setup
   - https://github.com/virajcoder/jobportal.git

## Step 1: Python aur Django Instal
   1. Python Install karein:
      - [Python.org ]
   2. Django Install karein:
      - pip install django
     
## Step 2: Django Project Create 
  1. Project Start :
      * Django project start karne ke liye, command prompt ya terminal par yeh command run karein:
          - django-admin startproject myproject
          - cd myproject
      
## Step 3: Django App Create
  1. App Start:
        * Django app banane ke liye, aapko project directory ke andar rehkar yeh command run karni hogi:
            - python manage.py startapp myapp
      
## Step 4: Models Define karein
  1. Models Define karein:
      * myapp/models.py file ko open karein aur models define karein.
  2. Migrations Create aur Apply karein:
      - python manage.py makemigrations
      - python manage.py migrate
    
## Step 6: Views aur URLs Configure karein
  1. Views Define karein:
      * myapp/views.py file ko open karein aur views define karein.
          - from django.shortcuts import render
          - from .models import Post

          - def post_list(request):
             - posts = Post.objects.all()
             - return render(request, 'myapp/post_list.html', {'posts': posts})
 2. URLs Configure karein:
      * myapp ke liye ek urls.py file banayein aur usmein URLs define karein
            - from django.urls import path
            - from . import views

           - urlpatterns = [
             - path('', views.post_list, name='post_list'),]
      * Phir myproject/urls.py file ko update karein taaki myapp ke URLs include ho sakein:
            - from django.contrib import admin
            - from django.urls import path, include

          - urlpatterns = [
           - path('admin/', admin.site.urls),
           - path('', include('myapp.urls')),]


## Step 7: Templates Create karein
  1. Template Folder aur Files Banayein:
      * myapp directory ke andar templates folder aur uske andar myapp folder create karein.
      * myapp/templates/myapp/post_list.html file banayein
    
## Step 8: Development Server Start karein
   - python manage.py runserver




**************************************************** Thank You ***********************************************
