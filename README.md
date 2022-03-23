# example-airflow
Airflow is a platform to programmatically author, schedule and monitor workflows.


##  Initializing Environment
Before starting Airflow for the first time, You need to prepare your environment, i.e. create the necessary files, directories and initialize the database.

# Setting the right Airflow user
    mkdir -p ./dags ./logs ./plugins
    echo -e "AIRFLOW_UID=$(id -u)" > .env

## Initialize the database
On all operating systems, you need to run database migrations and create the first user account. To do it, run.

    docker-compose up airflow-init

After initialization is complete, you should see a message like below.

    airflow-init_1       | Upgrades done
    airflow-init_1       | Admin user airflow created
    airflow-init_1       | 2.2.4
    start_airflow-init_1 exited with code 0
The account created has the login airflow and the password airflow.

## Running Airflow
Now you can start all services:
    
    docker-compose up



## Scalable
airflow has a modular architecture and uses a message queue to orchestrate an arbitrary number of workers. Airflow is ready to scale to infinity.
## Dynamic
Airflow pipelines are defined in Python, allowing for dynamic pipeline generation. This allows for writing code that instantiates pipelines dynamically.
## Extensible
Easily define your own operators and extend libraries to fit the level of abstraction that suits your environment.S
## Elegant
Airflow pipelines are lean and explicit. Parametrization is built into its core using the powerful Jinja templating engine.
