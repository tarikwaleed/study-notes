[Guide](https://www.youtube.com/watch?v=xtnUwvjOThg)
- [ ] clone your project in $HOME
- [ ] run
```shell
mkvirtualenv --python=/usr/bin/python3.9 project_name
```
- [ ] run
```shell
pip install -r requirements.txt
```
- [ ] add new web app -> manula configurations -> python3.9
- [ ] in your web app add the virtualenv name
- [ ] alter WSGI configuration file 
- add the path of your project root
- ['DJANGO_SETTINGS_MODULE']='appname.settings'
- [ ] edit the path of the static files in web tab
- [ ]  put the domain name in the ALLOWED_HOSTS array


