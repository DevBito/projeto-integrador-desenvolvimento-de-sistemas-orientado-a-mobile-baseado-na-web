
# 🏥 App Saúde - Sistema de Agendamento Hospitalar

Este projeto desenvolve um sistema simples de agendamento de consultas em hospitais, utilizando Flask no backend e HTML, CSS e JavaScript puro no frontend.

## 🚀 Tecnologias Usadas

**Backend:** 
- Python 3
- Flask
- Flask-SQLAlchemy
- SQLite.
  
**Frontend:** 
- HTML
- CSS
- JavaScript puro.


## Passo a Passo

1. **Configuração e Modelos:**
   - 🔧 Criamos o ambiente Flask e configuramos o banco de dados SQLite.
   - ⚙️ As configurações principais estão no arquivo config.py.
   - 🏗️ O SQLAlchemy é inicializado em database.py para gerenciar o banco de dados.

3. **Modularização das Rotas:**
   - As rotas foram divididas em blueprints na pasta `routes/`. Temos rotas para a área pública, para o admin e para o paciente.

4. **Templates HTML:**
   - Utilizamos Jinja2 para criar os templates, com um `base.html` que é estendido por todas as outras páginas.
   - As páginas incluem home, login, registro, área do paciente, agendamento e painel admin.

5. **Estilização e Responsividade:**
   - O CSS (em `static/css/style.css`) usa media queries para ser responsivo, garantindo boa aparência em dispositivos móveis.
   - O template `base.html` inclui a tag meta viewport para responsividade.

6. **Funcionalidades do Sistema:**
   - **Paciente:** Pode se registrar, fazer login, atualizar perfil e agendar consultas.
   - **Admin:** Pode se autenticar, gerenciar usuários, hospitais, especialidades e médicos.
   - **Agendamento:** O paciente escolhe hospital, especialidade, médico, data e hora. O sistema exibe confirmação e salva o agendamento.

7. **Interatividade com JavaScript:**
   - O JavaScript (em `static/js/main.js`) trata dos formulários de login e registro (via AJAX, se necessário) e inclui scripts para filtros e botões toggle nas páginas de admin.

## Como Executar

1. **Instale as Dependências:**
   - Crie um ambiente virtual e instale as bibliotecas necessárias (Flask, Flask-SQLAlchemy, etc.).
   - Exemplo:
     ```bash
     python -m venv venv
     venv\Scripts\activate      
     ```

2. **Crie o Banco de Dados:**
   - Ao iniciar o aplicativo, o SQLite cria o arquivo `db.sqlite3` automaticamente (se necessário, delete o antigo para recriar o esquema).

3. **Execute a Aplicação:**
   ```bash
   python app.py
   ```
   - Acesse `http://127.0.0.1:5000/` no navegador.

## Conclusão

Este aplicativo é um sistema básico de agendamento hospitalar utilizando Flask e tecnologias web simples. Desenvolvido de forma modular e responsiva, ele conta com diferentes áreas para pacientes e administradores.


