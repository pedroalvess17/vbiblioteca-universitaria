# vbiblioteca-universitaria
um sistema basiquin usando Windows Server + IIS + Python + Flask. 
Este projeto implementa um site de Biblioteca Universitária usando IIS (Windows Server) para o frontend e Flask (Python) para o backend.
Instalação
Instalar Python
Instalar dependências:
pip install flask flask-cors


Copiar a pasta biblioteca_site para C:\.

Executar o Backend (Flask)

Manual:

python C:\biblioteca_site\flask_app.py


Automático (Task Scheduler):

Program/script:

C:\Users\Administrator\AppData\Local\Programs\Python\Python311\python.exe


Arguments:

C:\biblioteca_site\flask_app.py


Start in:

C:\biblioteca_site

Configuração do IIS

Criar novo site apontando para:

C:\biblioteca_site


Porta: 80

Liberar Directory Browsing em /pdfs (opcional)

Rotas da API

Listar PDFs:

GET /pdf_list


Listar PDFs por curso:

GET /pdf_list?course=Computacao


Registrar empréstimo:

POST /loan


Listar empréstimos:

GET /loans

Fluxo

IIS serve as páginas HTML e PDFs

JavaScript chama a API Flask

Flask retorna lista de PDFs e grava empréstimos no CSV

admin.html lê o CSV via Flask

Replicação

Para reproduzir o sistema:

Instalar Windows Server + IIS

Instalar Python

Copiar a pasta biblioteca_site

Criar site no IIS

Configurar Flask no Task Scheduler

Testar:

Site:

http://IP/catalogo.html


API:

http://localhost:5000/pdf_list
