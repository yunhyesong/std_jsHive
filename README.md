# std_jsHive

Github -> Github Pages 북마클릿

* https://gist.github.com/skratchdot/b1a00080e4b9a3afa61c 참고

```js
(function (l) {
  var h = l.hostname.split('.'),
      p = l.pathname.split('/'),
      user = '',
      proj = '';

  if (h[1] === 'github' && h[2] === 'io') {
    user = h[0] || '';
    proj = p[1] || '';
    l.href = 'https://github.com/' + user + '/' + proj;
  } else if (h[0] === 'github' && h[1] === 'com') {
    var filteredPath = p.filter(function(item) {
        return (item !== 'blob' && item !== 'gh-pages');
    });
    user = p[1] || '';
    proj = filteredPath.slice(2).join('/') || '';
    l.href = 'https://' + user + '.github.io/' + proj;
  }
}(document.location));
```

minify

```js
javascript:(function(l){var h=l.hostname.split('.'),p=l.pathname.split('/'),user='',proj='';if(h[1]==='github'&&h[2]==='io'){user=h[0]||'';proj=p[1]||'';l.href='https://github.com/'+user+'/'+proj}else if(h[0]==='github'&&h[1]==='com'){var filteredPath=p.filter(function(item){return(item!=='blob'&&item!=='gh-pages')});user=p[1]||'';proj=filteredPath.slice(2).join('/')||'';l.href='https://'+user+'.github.io/'+proj}}(document.location))
```