
# PostgreSQL Installation

1. __Download PostgreSQL__ - Click the link below and download Postgre that apply to your operating system
[https://www.enterprisedb.com/downloads/postgres-postgresql-downloads](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads)

2. __Install PostgreSQL__ - Double click the downloaded content to install PostgreSQL to your device. Setup wizard will prompt you for next few actionable items. Some of the action items are listed below and most are best left with the default values which comes with the installation wizard. The only item you should care here is password, which is described below.
	```
	a) Installation Directory
	leave the default

	b) Password:
	- this is important, you will need this password from time to time
	- make it simple to remember since this is a learning database strong password is not necessary
	- use 'root' for your password as shown below:
		password: root
		retype password: root

	b) Leave everything else to default values until you see the next selection

	c) Uncheck 'Stack Builder' that asks you to install additional tools and click finish
	```
3. __Run pgAdmin and Create new Database__  - pgAdmin is a graphical user interface for PostgreSQL database engine
- in your computer locate pgAdmin application, which is installed with PostgreSQL engine during the installation and start it
- provide the password that you created in the installation
- navigate to databases view in pgAdmin and right click on it, then click create to create a new database
- give the name `dvdrental` for database name and click create

4. __Loading data__ to `dvdrental` database (a fictitious database for a DVD rental store)
- go to this link to get sample database: [https://www.postgresqltutorial.com/postgresql-sample-database/](https://www.postgresqltutorial.com/postgresql-sample-database/)
- at the bottom of the screen click on the red button, labeled "Download DVD Rental Sample Database"
- go to download folder and extract the content of the sample database
- go to command prompt or terminal and locate the `bin` directory of PostgreSQL installation folder
- in windows machine this is located here `C:\Program Files\PostgreSQL\12\bin`
- run `pg_restore` command to load data to `dvdrental` database as shown below
	```
	C:\Program Files\PostgreSQL\12\bin>pg_restore -U postgres -d dvdrental D:\dev\projects\lessons-postgresql\dvdrental.tar
	```
- go to databases in pgAdmin and right click and refresh - you will see all the data loaded

5. Installation completed!