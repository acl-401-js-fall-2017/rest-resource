HTTP REST API Resource
===

You will need to complete converting `simple-db` to promises and publish it to npm before you do this assignment 
(alternatively you can use the "classwork" published npm library).

## Directions

* Combine a vanilla NodeJS http server with your simple-db to create your first REST API
* Pick a "resource" - the entity you're saving and getting, like `unicorns`
* Implement:
    * `GET /<resource>` - returns array of all of the resources
    * `POST /<resource>` - inserts the supplied request body as a document into the resource collection
    * `GET /<resource>/:id` -
      * returns the single object specified by the id
      * returns 404 not found if no resource found with that id    
    * `DELETE /<resource>/:id` - removes the resource with that id. not an error if doesn't exist. 
      * return `{ removed: true }` or `{ removed: false }`)
* Use plural name in your url path (`/unicorns`, **not** `/unicorn`)
* You'll need to create a body parser like we did in class.

### Architecture and Design

* Use modules and project organization (files). Follow structure we covered in class.

## Testing

* Basic E2E with setup to manage db

## Bonus

* `PUT /<resource>/:id` - updates the resouce with supplied request body

* Add another resource type
  * SUPER BONUS: Generisize your first route handler into a general purpose
  handler by wrapping in a higher order function that takes a collection name

## Rubric

* Server, App, Project Organization: *1pt*
* Methods for Route
  * `GET` all: *1pt*
  * `POST`: *1pt*
  * `GET` by id: *1pt*
  * `DELETE` by id: *1pt*
* Tests
  * setup (with db setup) *1pts*
  * Tests
      * `GET` all (empty and with multiple): *1pt*
      * `POST`: *1pt*
      * `GET` by id (plus non-existant id): *1pt*
      * `DELETE` by id (plus non-existant id): *1pt*
