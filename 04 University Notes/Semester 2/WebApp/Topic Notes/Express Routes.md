
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



### Routen Setup:

In `app.js`

![[Pasted image 20230723160307.png]]


Route definieren:

```js
var indexRouter = require("./routes/index");
var usersRouter = require("./routers/users");
```

Route einbinden:
```js
app.use('/', indexRouter);
app.use('/users', userRouter);
```


### Parameter in Routen

![[Pasted image 20230723160659.png]]


### Parameter auslesen

![[Pasted image 20230723160721.png]]