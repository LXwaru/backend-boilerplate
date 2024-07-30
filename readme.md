# This is a backend boiler plate using FastAPI and PostgreSQL
<li>create users</li>
<li>secure login using JWT token exchange</li>
<li>create/read items specific for each user</li>

## To use this boilerplate, follow these directions:
TC = terminal command <br>
<hr />

### create a virtual environment: 


TC: `python -m venv .venv`<br>
TC: `source .venv/bin/activate`
<hr />

### download dependencies
TC: `pip install fastapi` <br>
TC: `pip install sqlalchemy` <br>
TC: `pip install alembic` <br>
TC: `pip install pyjwt` <br>
TC: `pip install "passlib[bcrypt]"` <br>
TC: `pip install dotenv` <br>
TC: `pip install dotenv` <br>
TC: `pip install psycopg2` <br>

<hr>

### download/setup postgreSQL
There are a few ways to do this. [Click here for the PostgreSQL documentation](https://www.postgresql.org/) 

<hr>

### migrations

migrate down: <br>
TC: `alembic downgrade base` <br>
migrate up: <br>
TC: `alembic revision` <br>

<hr>

### setup an .env file

create a secret key for the security protocol
TC: `openssl rand -hex 32` <br>
copy the string and paste it in the .env as: <br>
SECRET_KEY={your secret key} <br>

after you've created a postgreSQL database, put the following code into the .env file:
`DATABASE_URL=postgresql://{username}:{password}@localhost/{dbname}`


<hr>

### open DEV environment on localhost:8000/docs

TC: `fastapi dev app/api/main.py`
