# payroll-repository
payroll-repository-descr

CRUD Examples GET/POST/PUT/DELETE
/**
*   Trying ::1...
* TCP_NODELAY set
* Connected to localhost (::1) port 8080 (#0)
*> GET /employees HTTP/1.1
*> Host: localhost:8080
*> User-Agent: curl/7.54.0
*> Accept: 
*>
*< HTTP/1.1 200
*< Content-Type: application/json;charset=UTF-8
*< Transfer-Encoding: chunked
*< Date: Thu, 09 Aug 2018 17:58:00 GMT
*<
* Connection #0 to host localhost left intact
*[{"id":1,"name":"Bilbo Baggins","role":"burglar"},{"id":2,"name":"Frodo Baggins","role":"thief"}] 
* 
*/

/**
*   Trying ::1...
* TCP_NODELAY set
* Connected to localhost (::1) port 8080 (#0)
*> GET /employees/99 HTTP/1.1
*> Host: localhost:8080
*> User-Agent: curl/7.54.0
*> Accept: /*
*>
*< HTTP/1.1 404
*< Content-Type: text/plain;charset=UTF-8
*< Content-Length: 26
*< Date: Thu, 09 Aug 2018 18:00:56 GMT
*<
* Connection #0 to host localhost left intact
*Could not find employee 99
*/

/**
 * 
 * $ curl -X POST localhost:8080/employees -H 'Content-type:application/json' -d 
 * '{"name": "Samwise Gamgee", "role": "gardener"}'
 * 
*/

/**
 * $ curl -X PUT localhost:8080/employees/3 -H 'Content-type:application/json' -d 
 * '{"name": "Samwise Gamgee", "role": "ring bearer"}'
 */

/**
 * 
 * $ curl -X DELETE localhost:8080/employees/3

	# Now if we look again, it's gone
	$ curl localhost:8080/employees/3
	Could not find employee 3
 * 
 */
