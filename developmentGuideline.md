### How to access db
(env) sreejabhattacharya@Sreejas-MacBook-Air ToDo-App % sqlite3 instance/test.db
SQLite version 3.37.0 2021-12-09 01:34:53
Enter ".help" for usage hints.
sqlite> .table
todo
sqlite> select * from table;
Error: in prepare, near "table": syntax error (1)
sqlite> select * from Todo;
sqlite> .help
sqlite> .exit
(env) sreejabhattacharya@Sreejas-MacBook-Air ToDo-App % 

### Create db before first request in app.py
@app.before_first_request
def create_tables():
    db.create_all()

### Creation of venv (virtual environment) with name "env"
pip3 install virtualenv
python3 -m venv env
source env/bin/activate