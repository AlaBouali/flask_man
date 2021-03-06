# flask_man
Flask module to auto setup and manage the project and its configurations (app code, templates, databases...)

# Why should I use flask_man's framework?
<br>
<h2>flask_man will do most of the work for you ! ALL and KEEPING THE FLEXIBILITY AND SIMPLICITY OF FLASK !!</h2>
<ul>
<li>Create necessary codes, database, tables, files and folders when you initialize the project, leaving to you only editing the templates and adding some code to "template.py and "routes.py" when needed !</li>
<li>Add/Delete routes/templates to/from the project's files and code in "template.py and "routes.py"</li>
<li>Compatible with: SQLite, MySQL, MariaDB, PostgreSQL, Oracle SQL and MS SQL. You can switch between them with a single command any time.</li>
<li>Create/Delete models for/from the project.</li>
<li>Built-in functions ( in "utils.py" , "database.py" and "handlings.py") and decorators ( in "wrappers.py" ) to minimize the amount of code you write and maximize the security level of the projects.</li>
<li>Have customizable configurations at "settings.py" which most of them are loaded from "config.json" ( created on the project's creation ) which is also updated when the configurations are changed, every time the application starts.</li>
<li>Save files locally, filter them by their mimetypes and extensions, and serve them securily.</li>
<li>Upload files to firebase.</li>
<li>Users authentication and management with firebase ( create / update / delete / signup / signin / lookup / reset password ... ).</li>
<li>Send mail.</li>
<li>Send SMS ( you need an account <a href="https://identity.nexmo.com/">here</a> and get you API Key and Secret Key ) .</li>
<li>High level access control ( visitor , user , admin ) achieved with the decorators.</li>
<li>Secure the application from SQL-Injection by auto-escape: URL arguments, request's body's parameters and dynamic URIs.</li>
<li>Supports JWT-Authentication.</li>
<li>CSRF protection by: checking the referer header and/or CSRF token.</li>
<li>Supports rate-limit and google's Recaptcha.</li>
<li>Clickjacking protection.</li>
<li>XSS protection.</li>
<li>CORS's protection by validating the origin of the request.</li>
<li>Built-in functions to validate user's input against: SSRF and Path Traversal.</li>
<li>Ready to deploy directly on Heroku or shared Hosting site.</li>
<li>Create an instant backup for all your project's files.</li>
<li>Have a nice debug toolbar containing useful information for debugging.</li>
</ul>
<br>
The security in the this project is achieved via <a href="https://gitub.com/AlaBouali/sanitizy">sanitizy</a><br>


# Usage:
<div style="background: #f8f8f8; overflow:auto;width:auto;border:solid gray;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%">
Usage:

        flask_man [args...]

args:


        manager: to launch the web interface and manage the project from there


        examples: to show commands examples


        upgrade: to upgrade to the latest version of flask_man package


        init: to create "config.json" and python files that contains
              code and setup configurations, and to install required packages


        db: to choose database type to use ( sqlite or mysql or mariadb or postgresql or mssql or oracle )


        add_template: create a template file with that path in the
                      templates folder,add the name to the "config.json"
                      file and add necessary code to "templates.py"


        delete_template: delete the template file with that path from the
                         templates folder, remove the name from the
                         "config.json" file and delete the code from "templates.py"


        add_route: add the name to the "config.json" file and
                   add necessary code to "routes.py"


        delete_route: remove the name from the "config.json"
                      file and delete the code from "routes.py"


        add_model: add the name to the "config.json" file and
                   add necessary code to "models.py"


        delete_model: remove the name from the "config.json"
                      file and delete the code from "models.py"


        firebase_apikey: set the firebase APIKey


        firebase_bucket: set the firebase storage bucket


        firebase_configs: copy the firebase storage bucket's configs'
                          file to the local configs file


        pro: set project to production mode


        dev: set project to development mode
</pre></div>
# Manager
To use flask_man's manager run the following commands ( suppose we will call the project "flask_proj" ) :
<div style="background: #f8f8f8; overflow:auto;width:auto;border:solid gray;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%">

mkdir flask_proj

cd flask_proj

flask_man manager
</pre></div>
then open this link :
<br>
<br>
<a href='http://127.0.0.1:12345/'>http://127.0.0.1:12345/</a>
<br>
<br>
<img src='https://raw.githubusercontent.com/AlaBouali/flask_man/main/c1.png'>

<img src='https://raw.githubusercontent.com/AlaBouali/flask_man/main/2.png'>

<img src='https://raw.githubusercontent.com/AlaBouali/flask_man/main/3.png'>

<img src='https://raw.githubusercontent.com/AlaBouali/flask_man/main/4.png'>

# Running the application

<div style="background: #f8f8f8; overflow:auto;width:auto;border:solid gray;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%">
python app.py</pre></div>
or
<div style="background: #f8f8f8; overflow:auto;width:auto;border:solid gray;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%">
python3 app.py</pre></div>

# Commands examples:
You can also manage your project from the command line with the following commands ( just examples ) :
<div style="background: #f8f8f8; overflow:auto;width:auto;border:solid gray;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%">
** Launching the web interface:


Example:


        flask_man manager




** Upgrading the package:


Example:


        flask_man upgrade




** Creating a Project:


Example 1 (database: SQLite) :


        flask_man init config
        flask_man db sqlite
        flask_man init app
        flask_man init install


Example 2 (database: MySQL/MariaDB) :


        flask_man init config
        flask_man db mysql
        flask_man init app
        flask_man init install


Example 3 (database: PostgreSQL) :


        flask_man init config
        flask_man db postgresql
        flask_man init app
        flask_man init install


Example 4 (database: MS SQL) :


        flask_man init config
        flask_man db mssql
        flask_man init app
        flask_man init install


Example 5 (database: Oracle SQL) :


        flask_man init config
        flask_man db oracle
        flask_man init app
        flask_man init install




** Installing the requirements:


Example:


        flask_man init install




** Add a template to the project:


Example:


        flask_man add_template "admin/login.html"




** Remove a template from the project:


Example:


        flask_man delete_template "admin/login.html"




** Add a model to the project:


Example:


        flask_man add_model "user"




** Remove a model from the project:


Example:


        flask_man delete_model "user"




** Add a route to the project:


Example 1:


        flask_man add_route "admin/upload"


Example 2:


        flask_man add_route "/profile/<user_id>"




** Remove a route from the project:


Example 1:


        flask_man delete_route "admin/upload"


Example 2:


        flask_man delete_route "/profile/<user_id>"




** Set firebase APIKey:


Example :


        flask_man firebase_apikey "kjkhgyftrdfghjklkjhgfrdefg"




** Set firebase storage bucket:


Example :


        flask_man firebase_bucket "myfbbucket.appspot.com"




** Copy firebase storage bucket's config file to local config file:


Example 1 (Non-Windows):


        flask_man firebase_configs "/home/root/configs.json"


Example 2 (Windows):


        flask_man firebase_configs "C:\Users\user\Desktop\configs.json"




** Change Database type:


Example 1:


        flask_man db mysql


Example 2:


        flask_man db postgresql




** Go production:


Example :


        flask_man pro




** Go development:


Example :


        flask_man dev
</pre></div>
