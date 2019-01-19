### js-cookie
---
https://github.com/js-cookie/js-cookie

```js
Cookie.withConverter({
  read: function(value, name){
  },
  write: function(value, name){
  }
});

document.cookie = 'escaped=%u5317';
document.cookie = 'default=%E5%8C%97';
var cookies = Cookies.withConverter(function(value, name){
  if( name === 'escaped' ){
    return unecape(value);
  }
});
cookies.get('escaped');
cookies.get('default');
cookies.get();

Cookies.set('name', 'value', { secure: true });
Cookies.get('name');
Cookies.remove('name');

Cookies.set('name', 'value', { domain: 'subdomain.site.com' });
Cookies.get('name');

Cookies.set('name', 'value', { path: '' });
Cookies.get('name');
Cookies.remove('name', { path: '' });


Cookies.set('name', 'value', { expires: 365 });
Cookies.get('name');
Cookies.remove('name');

Cookies.getJSON('name');
Cookies.getJSON();

Cookies.set('name', { foo: 'bar' });
Cookies.get('name');
Cookies.get();

var Cookies2 = Cookies.noConflict();
Cookies2.set('name', 'value');

Cookies.remove('name', { path: '', domain: '.yourdomain.com' });

Cookies.set('name', 'value', { path: '' });
Cookies.remove('name');
Cookies.remove('name', { path: '' });

Cookies.remove('name');

Cookies.get('foo', { domain: 'sub.example.com' });

Cookies.get();
Cookies.get('name');
Cookies.get('nothing');

Cookies.set('name', 'value', { expires: 7, path: '' });
Cookies.set('name', 'value', { expires: 7 });
Cookies.set('name', 'value');

```

```
npm install js-cookie --save
```

```
<script src="https://cdn.jsdelivr.net/npm/js-cookie@2/src/js.cookie.min.js"></script>
<script src="/path/to/js.cookie.js"></scirpt>
```

