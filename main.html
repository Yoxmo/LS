import requests, os, shutil , time , subprocess, glob
from bs4 import BeautifulSoup

name = input('[?] Enter github: ')
#Name for github / to get branch and do seprate live server.

print('''
▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒
▒▒▄▄▄▒▒▒█▒▒▒▒▄▒▒▒▒▒▒▒▒
▒█▀█▀█▒█▀█▒▒█▀█▒▄███▄▒
░█▀█▀█░█▀██░█▀█░█▄█▄█░
░█▀█▀█░█▀████▀█░█▄█▄█░
████████▀█████████████
''')
# City art ascii for console.

print(f'\n[*] Done your website is being made\nYou can access it here in a few seconds\n Link: Live-Server.{name}.repl.co\n\n\n\n')
# Printing live server link via the name.



# Creating the flask app server.
def addroutes():
  files = glob.glob(f"web/*")
  # Getting all the files in web for the naming and creating of diffrent routes/website direcions.


  init = f"""import flask , os
from flask import Flask, render_template , redirect , request

template_dir = os.path.abspath('web')
static_dir = os.path.abspath('web/assets')

app = Flask(__name__, template_folder=template_dir , static_folder=static_dir)

app.config['TEMPLATES_AUTO_RELOAD'] = True


@app.route('/')
def index():
  return render_template('index.html')
""" 
  
  open('app.py', 'w+').write(init)
  # Config and first index route for app server, using w+ to recreate the file for updates / future appends


  # Simple for loop to get all the html files in the web dir and removing all the extra stuff like .html and / from files. 
  for html in files:
    if html == f"web/index.html":
      pass
    else:
      if html.endswith('html'):
        html = html.strip('web').strip('.html').strip('/')
    
        cleanedr = f"""\n #==== New Route ====#
@app.route('/{html}')
def {html}():
  return render_template('{html}.html')
"""
        open('app.py', 'a+').write(cleanedr)

        # Creating the route and adding it to  app.py file. using a+ to append the file with cleaned code.
      pass

  
  print('[*] Added all routes...')

  last = f"""\nif '__main__' == __name__:
    app.run(host='0.0.0.0', port='5000', debug=True)
  """ 
    
  open('app.py', 'a+').write(last)
  # Creating the final part to run on all host (creating a live server from repl).


# Init cloneing for the web dir from github.
if len(glob.glob(f"web/*")) <= 0:
    os.system(f'git clone https://github.com/{name}/web.git')
else:
    shutil.rmtree('web')
    os.system(f'git clone https://github.com/{name}/web.git')

addroutes()
# Calling the addroutes before starting the app.py.
subprocess.Popen(('python3', 'app.py')) 

while True:
  
  # Entering the web dir for the .git info and then pulling newest branch from the {{names}} github and checking for output.
  result = subprocess.check_output(f"cd web && git pull https://github.com/{name}/web.git", shell=True)
  
  if str(result.decode()).strip('\n') != "Already up to date.":
    # If github returns up to date redo routes incase a new file is added / new html page
    addroutes()
  else:
    print('[*] No change...')
    # Sleep is just so repl dosen't max out cpu and boot offline.
    time.sleep(1)
