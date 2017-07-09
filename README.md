# std_jsHive

Github -> Github Pages 북마클릿
https://gist.github.com/skratchdot/b1a00080e4b9a3afa61c

```js
javascript:(function(l){var h=l.hostname.split('.');var p=l.pathname.split('/');var user='';var proj='';if(h[1]==='github'&&h[2]==='io'){user=h[0]||'';proj=p[1]||'';l.href='https://github.com/'+user+'/'+proj}else if(h[0]==='github'&&h[1]==='com'){user=p[1]||'';proj=p[2]||'';l.href='https://'+user+'.github.io/'+proj}}(document.location))
```