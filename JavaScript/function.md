```javascript
const functionToReWrite = () => {
	return fetch('myapp/thingy.json')
  				.then(res => res.json())
  				.then(users => users[0])
          .then(user => fetch('myapp/users/' + user.user_name))
          .then(user => doMyThing(user.json))
          .catch(err => console.log(err))
}
```
```javascript
const rewrittenFunctionInES2017 = async () => {
  try {
  	const res = await fetch('myapp/thingy.json'); 
    const users = await res.json(); 
    const user = users[0];
    const userRes = await fetch('myapp/users/' + user.user_name);
    return doMyThing(userRes.json); 
  } catch (err) {
  	console.log(err);
  }
  return null
}
```
