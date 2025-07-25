# Clone o repositório
```
git clone https://github.com/faccin-eng/dj-commerce
```
# Crie e ative o ambiente virtual python
```
python -m venv .venv
.venv/Scripts/activate
```
# Ative o Django no debugger
Instale o Django no seu ambiente virtual
```
pip install django
```
Create a debugger launch profile
Alterne para a visualização de Execução no VS Code (usando a barra de atividades do lado esquerdo ou a tecla F5). Você poderá ver a mensagem "Para personalizar a Execução e a Depuração, crie um arquivo launch.json".
Isso significa que você ainda não possui um arquivo launch.json contendo configurações de depuração. O VS Code pode criá-lo para você clicando no link "Criar um arquivo launch.json":
Selecione o link e o VS Code solicitará uma configuração de depuração. Selecione Django no menu suspenso e o VS Code preencherá um novo arquivo launch.json com uma configuração de execução do Django.
O arquivo launch.json contém diversas configurações de depuração, cada uma das quais é um objeto JSON separado dentro do array de configuração.
Role para baixo e examine a configuração com o nome "Python: Django":
```
{
 "version": "0.2.0",
  "configurations": [
    {
      "name": "Python Debugger: Django",
      "type": "debugpy",
      "request": "launch",
      "program": "${workspaceFolder}\\manage.py",
      "args": ["runserver"],
      "django": true,
      "justMyCode": true
    }
  ]
}
```
Execute com ctrl + F5
