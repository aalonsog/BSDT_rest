## Restaurants REST server

### Dependencies

- node.js
- npm

### How to install

<pre>
git clone https://github.com/aalonsog/BSDT_rest.git
cd BSDT_rest
npm install
</pre>

### How to configure

+ The server is configured to listen in port 8000. You can modify that folder using the env variable `PORT`
+ The server is configured to connect to database in `mongodb://localhost:27017/zips_small`. You can modify that folder using the env variable `DATABASE`

Example:
<pre>
export PORT=8081
</pre>

### How to run

<pre>
npm start
</pre>

### How to test

You can use any REST client to test the API. A test web page is also included in `http://localhost:<port>/webtest.html`

Examples using curl client:

#### Check server
	curl http://localhost:8000

#### List restaurants
	curl http://localhost:8000/restaurants
	
#### List restaurants including a query
	curl http://localhost:8000/restaurants?nombre=miRestaurante&calle=calle30

#### Get restaurant details
	curl http://localhost:8000/restaurants/2

#### Update restaurant details
	curl -H "Content-type:application/json" -X PUT -d '{"nombre":"Nuevo nombre"}' http://localhost:8000/restaurants/2

#### Create restaurant
	curl -H "Content-type:application/json" -X POST -d '{"nombre":"Mi restaurante"}' http://localhost:8000/restaurants

#### Delete restaurant
	curl -X DELETE http://localhost:8000/restaurants/3
