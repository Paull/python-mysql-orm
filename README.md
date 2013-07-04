this a python mysql query builder module in codeIgniter active record style

version 0.1 of this module has been tested in production environment for several days

if you found any bugs or have any suggestions, don not hesitate to let me know, I will do my best to fix them. And you are welcome to make it better!

---

# Python Mysql Active Record

This is an activerecord module inspired from CodeIgniter activerecord and database driver library.

Use it to integrate a activerecord mysql database into your python application.

You can interact with the database using many of the active record functions that CodeIgniter provides.

##Dependency
* Python 2.7 enviroment. get it from[http://www.python.org/getit/]
* MySQL for Python. get it from[http://sourceforge.net/projects/mysql-python/files/mysql-python/1.2.3/]

##Usage
run as a console or import it as a module

* 1.first of all, you have to configure your database in config.py
* 2.1 import the database module then follow the step3 and step4
* 2.2 or just run database.py as a console then follow step4
* 3.make a instance of the class to initialize a database connection: db = Database()
* 4.call functions just like we do in codeigniter

##Notice
the function from() in ci is renamed to table() for avoiding compatible problem , it is a key word in python

##Examples
you can put them in your py codes or type them in the console(run database.py directly)

	dating_target = db.table('employee').select('firstname, lastname, email, mobile').where('age <', 25).where('gender', 'female').order_by('age', 'asc').limit(10, 20).get().reulst()
	print dating_target
	
or like this

	db.talbe('employee')
	db.where({'firstname':'Paul', 'age >': 28, })
	db.get()
	print db.row()

##More Help
The CodeIgniter activerecord user guide please visit [http://ellislab.com/codeigniter/user-guide/database/active_record.html]
