# naviance
Search colleges with one-time login

### Magic Code
- navigate to `https://connection.naviance.com/family-connection/auth/login?hsid=<high school id>`
``` javascript
$.ajax({ url: '/family-connection/auth/login/authenticate', type: 'post', dataType: 'json', data: { username: '<username>', password: '<password>', is_ajax: true }, success: function(d) { console.log(d); }});
```
- cookie `sess` (Session ID) set by Naviance even if not present
- navigate to `d.url` (expected `/main` if correct or `/auth/login` if not)

### Ideas
- CI possible
- Single login: school id, username, password -> cookies stored
- All college data, analytics, etc. then accessible
