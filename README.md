# Solar System API

## Goal


* Improve understanding of Flask & SQL Alchemy with repetition

Build a Solar System API. This API will store information about different planets.
Creating RESTful endpoints for CRUD operations.

## Project  
---  

Part I  

* Define a `Planet` class with the attributes `id`, `name`, and `description`, and one additional attribute
* Create a list of `Planet` instances  

Part II  

* Create an endpoint to get one existing `planet`, so that I can see the `id`, `name`, `description`, and `type` of the `planet`.
* ...such that trying to get one non-existing `planet` responds with get a `404` response, so that I know the `planet` resource was not found.
* ... such that trying to get one `planet` with an invalid `planet_id` responds with get a `400` response, so that I know the `planet_id` was invalid.  

Part III  

* Create the database `solar_system_development`
* Setup the `Planet` model with the attributes `id`, `name`, and `description`, and `type`.
* Create a migration to add a table for the `Planet` model and then apply it. 
    * *Confirm that the `planet` table has been created as expected in postgres*.
* Submit a POST request with new valid `planet` data and get a success response, so that I know the API saved the planet data
* Creat an endpoint to get all existing `planets`, so that I can see a list of planets, with their `id`, `name`, `description`, and other data of the `planet`.  

Part IV  
 
* Submit an UPDATE request with valid planet data to update one existing `planet` and get a success response, so that I know the API updated the `planet` data.
* Submit a request to delete one existing `planet` and get a success response, so that I know the API deleted the `planet` data..
    * Each of the above endpoints should respond with a `404` for non-existing planets and a `400` for invalid `planet_id`.  

Part V  

* Review the requirements for Wave 01 - 04  

    * Test the endpoints using postman
    * Complete or fix any incomplete or broken endpoints
    * Look for opportunities to refactor  

Part VI  

Complete the following requirements, with similar functionality to the Hello Books API:

1. Create a `.env` file.
1. Populate it with two environment variables: `SQLALCHEMY_DATABASE_URI` and `SQLALCHEMY_TEST_DATABASE_URI`. Set their values to the appropriate connection strings.
1. Create a test database with the correct, matching name.
1. Refactor the `create_app` method to:
   * Check for a configuration flag
   * Read the correct database location from the appropriate environment variables
1. Manually test that my development environment still works.
1. Create a `tests` folder with the files:
    -  `tests/__init__.py`
    -  `tests/conftest.py`
    -  `tests/test_routes.py`.
1. Populate `tests/conftest.py` with the recommended configuration.
1. Create a test to check `GET` `/planets` returns `200` and an empty array.
1. Confirm this test runs and passes.

## Writing Tests

Create test fixtures and unit tests for the following test cases:

1. `GET` `/planets/1` returns a response body that matches our fixture
2. `GET` `/planets/1` with no data in test database (no fixture) returns a `404`
3. `GET` `/planets` with valid test data (fixtures) returns a `200` with an array including appropriate test data
4. `POST` `/planets` with a JSON request body returns a `201`  


*Note: For this project, I will not expect to have high test coverage because I have not tested all of the CRUD routes. Still, it is helpful to practice checking coverage and reading reports of the code which detail the code that is tested, and the code that is not tested.*



