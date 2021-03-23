# The site url availability check using Python
You can use the following python code to check whether your site is up or down. For this purpose we used requests module.
#### Script
```
import requests
urls = [
    'https://www.microsoft.com',
    'https://www.kernel.org',
    'https://www.unknown.unknown',
    'https://www.gnu.org',
    'https://www.facebook.com',
    'https://mail.google.com',
    'https://www.youtube.com'
]

for url in urls:
    
  try:
    
    response = requests.get(url)
    
    if response.status_code == requests.codes.OK:
        
      print('{:35} - up'.format(url))
    
    else:
    
      print('{:35} - Down'.format(url))
        
  except:
    
    print('{:35} - Error'.format(url))
```
#### output
https://www.microsoft.com           - up
