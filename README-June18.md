### WE got little grap over the  async javascript function ,little about the promises  etc.

#### Here we created  a function which return the promise and when it is resolve it fetch the weather data from weatherapi and return it as a object. 

```javascript  
function fetchData(){
 	return new Promisefunction (reslove ,reject){ 	
        	fetch ("https://api.weatherapi.com/v1/current.json?key=1650213131b14dca81c30209241806&q=london")
	.then(response=> response.json())
		.then(data=> console.log(data))	}}
```
#### Here we are using the async/await syntax to fetch the data from weatherapi and return it, it is minified version of the above code,its eaiser to use await over then to resolve the promises.

 ```javascript
  async function getData(){
	const data = await fetch ("https://api.weatherapi.com/v1/current.json?key=1650213131b14dca81c30209241806&q=london")
 var result = await data.json()
	console.log(result)	} 
 ```
