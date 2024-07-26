# django_school_api
 *PT - BR*
Django REST API desenvolvida junto ao curso Alura: 'Django REST Framework: construindo APIs RESTful do Zero'.

 *ENGLISH*
Django Rest API developed with the 'Alura' course 'Django REST Framework: construindo APIs RESTful do Zero'. ('Django REST Framework: Developing RESTful APIs from scratch')
English explanation is after the Portuguese below:

# PORTUGUESE
#  Sistema de Gerenciamento Escolar
Visão Geral

O Sistema de Gerenciamento Escolar é uma aplicação baseada em Django projetada para gerenciar alunos (Estudante), cursos (Curso) e matrículas (Matricula). A aplicação utiliza o Django REST Framework (DRF) para fornecer uma API robusta para interagir com esses modelos. Também inclui uma interface administrativa para gerenciar os dados de forma eficiente.
Recursos

    Gerenciamento de Alunos: Crie, leia, atualize e exclua registros de alunos.
    Gerenciamento de Cursos: Gerencie detalhes dos cursos, incluindo código, descrição e nível.
    Gerenciamento de Matrículas: Acompanhe quais alunos estão matriculados em quais cursos e seu período de matrícula.
    Endpoints da API: Endpoints RESTful para gerenciar e consultar alunos, cursos e matrículas.
    Interface Administrativa: Interface administrativa do Django para gerenciar alunos, cursos e matrículas diretamente.

Instalação

Para configurar o projeto localmente, siga estes passos:

1 - Clone o Repositório

2 - Instale as Dependências

   'pip install -r requirements.txt'

3 - Aplique as Migrações

   'python manage.py migrate'

4 - Crie um Superusuário

   'python manage.py createsuperuser'

5 - Execute o Servidor de Desenvolvimento

   'python manage.py runserver'

# Endpoints da API
Alunos

    Listar Alunos: GET /api/estudantes/
    Obter Aluno: GET /api/estudantes/{id}/
    Criar Aluno: POST /api/estudantes/
    Atualizar Aluno: PUT /api/estudantes/{id}/
    Excluir Aluno: DELETE /api/estudantes/{id}/

Cursos

    Listar Cursos: GET /api/cursos/
    Obter Curso: GET /api/cursos/{id}/
    Criar Curso: POST /api/cursos/
    Atualizar Curso: PUT /api/cursos/{id}/
    Excluir Curso: DELETE /api/cursos/{id}/

Matrículas

    Listar Matrículas: GET /api/matriculas/
    Obter Matrícula: GET /api/matriculas/{id}/
    Criar Matrícula: POST /api/matriculas/
    Atualizar Matrícula: PUT /api/matriculas/{id}/
    Excluir Matrícula: DELETE /api/matriculas/{id}/

Matrículas por Aluno

    Listar Matrículas por Aluno: GET /api/matriculas/estudante/{pk}/

Matrículas por Curso

    Listar Matrículas por Curso: GET /api/matriculas/curso/{pk}/

Interface Administrativa

Você pode gerenciar os dados através da interface administrativa do Django em http://localhost:8000/admin/. Faça login usando a conta de superusuário criada durante a configuração.
Modelos

    Estudante: Representa um aluno com campos como nome, email, cpf, data_nascimento e celular.
    Curso: Representa um curso com campos como codigo, descricao e nivel.
    Matricula: Representa uma matrícula que liga um aluno a um curso com campos para estudante, curso e periodo.


    # ENGLISH

    # Overview

The Escola Management System is a Django-based application designed to manage students (Estudante), courses (Curso), and enrollments (Matricula). The application uses Django REST Framework (DRF) to provide a robust API for interacting with these models. It also includes an administrative interface to manage the data efficiently.
Features

    Student Management: Create, read, update, and delete student records.
    Course Management: Handle course details including code, description, and level.
    Enrollment Management: Track which students are enrolled in which courses and their enrollment period.
    API Endpoints: RESTful API endpoints for managing and querying students, courses, and enrollments.
    Admin Interface: Django admin interface to manage students, courses, and enrollments directly.

    Installation:
Para configurar o projeto localmente, siga estes passos:

1 - Clone the repository

2 - Install all dependencies

   'pip install -r requirements.txt'

3 - Apply migrations

   'python manage.py migrate'

4 - Create Superuser

   'python manage.py createsuperuser'

5 - Run the server

   'python manage.py runserver'


    API Endpoints
Students

    List Students: GET /api/estudantes/
    Retrieve Student: GET /api/estudantes/{id}/
    Create Student: POST /api/estudantes/
    Update Student: PUT /api/estudantes/{id}/
    Delete Student: DELETE /api/estudantes/{id}/

Courses

    List Courses: GET /api/cursos/
    Retrieve Course: GET /api/cursos/{id}/
    Create Course: POST /api/cursos/
    Update Course: PUT /api/cursos/{id}/
    Delete Course: DELETE /api/cursos/{id}/

Enrollments

    List Enrollments: GET /api/matriculas/
    Retrieve Enrollment: GET /api/matriculas/{id}/
    Create Enrollment: POST /api/matriculas/
    Update Enrollment: PUT /api/matriculas/{id}/
    Delete Enrollment: DELETE /api/matriculas/{id}/

Enrollment by Student

    List Enrollments for Student: GET /api/matriculas/estudante/{pk}/

Enrollment by Course

    List Enrollments for Course: GET /api/matriculas/curso/{pk}/

Admin Interface

You can manage the data via Django's built-in admin interface at http://localhost:8000/admin/. Log in using the superuser account created during setup.
Models

    Estudante: Represents a student with fields like nome, email, cpf, data_nascimento, and celular.
    Curso: Represents a course with fields such as codigo, descricao, and nivel.
    Matricula: Represents an enrollment linking a student to a course with fields for estudante, curso, and periodo.
