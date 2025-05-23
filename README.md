# KwMathConsult FastAPI
- [KwMathConsult FastAPI](#kwmathconsult-fastapi)
  - [Read changelog HERE](#read-changelog-here)
  - [Development](#development)
  - [Production](#production)
  - [Author(s)](#authors)

## Read changelog [HERE](/CHANGELOG.md)

## Development

1. Read [this](./pyodbc.md) for things to do before installing pyodbc with pip. That is the backup Markdown file I copied from [here](https://github.com/mkleehammer/pyodbc/wiki/Install)
   
2. Download MS ODBC Driver 18 for [Windows](https://learn.microsoft.com/en-us/sql/connect/odbc/download-odbc-driver-for-sql-server?view=sql-server-ver16#download-for-windows)  or [Linux](https://learn.microsoft.com/en-us/sql/connect/odbc/linux-mac/installing-the-microsoft-odbc-driver-for-sql-server?view=sql-server-ver16&tabs=alpine18-install%2Calpine17-install%2Cdebian8-install%2Credhat7-13-install%2Crhel7-offline#18)
3. Fill out server details in the .env file
4.  Create a virtual environment using the `requirements.txt` in this repo, using [VSCode](https://code.visualstudio.com/docs/python/environments#_creating-environments) or [PyCharm](https://www.jetbrains.com/help/pycharm/creating-virtual-environment.html) or manually:
  
```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt

# and for when you want to exit the venv:
deactivate
```

5. Run Dev Server by typing `fastapi dev src/main.py` 

6. **READ THE DOCUMENTATION!** *All classes and functions have docstrings and/or comments.* If you wish to know how this code works, start with `main.py` in the `src` folder

## Production

1. Run `npm run build` in `/frontend` folder to export files to `/backend/public folder` 
2. Fill out server details in .env.production file
3. `sudo chmod +x run.sh`
4. `./run.sh` The script will install all prerequisites, install the server as systemd service and start it.
 
 
## Author(s)
Johnny (Lost) - jmlin0101@gmail.com