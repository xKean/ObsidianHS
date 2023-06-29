---
dg-publish: true
---
### Beispiel-Routes:

#### Get
```js
router.get('/suchen', function(req, res, next){
	console.log(req.query);
	res.render('formular', {title'Hallo'})
});
```


#### Post
```js
router.post('/suchen', function(req, res, next){
	console.log(req.body);
	res.send(req.body);
});
```


### Responses:
![[Pasted image 20230505123010.png]]