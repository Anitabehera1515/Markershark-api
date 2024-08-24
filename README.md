1. Run the Spring Boot Application
> Start the Application:
   >> In Eclipse, right-click on your project and select Run As > Spring Boot App.
   >>The application will start, and the H2 database will be initialized in memory.
2.Prepare Postman for API Testing
> Open Postman:

  >>Launch Postman to set up your API requests.

> Create a New Request:

  >>Click on New > HTTP Request.

  >> Configure the request as follows:

    >>> Method: POST
    >>> URL: http://localhost:8080/api/supplier/query?location=India&natureOfBusiness=small_scale&manufacturingProcesses=3d_printing&page=0&size=10
    >>> Headers: Set Content-Type to application/json.
  >> Set Up the Request Body:

    >>> In the Body tab, choose raw and select JSON as the format.
    >>> Enter a JSON payload that matches your API's input parameters. For example:
         {
           "location": "India",
          "natureOfBusiness": "small_scale",
           "manufacturingProcesses": "3d_printing",
           "page": 0,
           "size": 10
         }
  >>Send the Request:

    Click Send in Postman to submit the request to your Spring Boot API.
3. Review the Response
   >>Inspect the Response:

    Postman will display the JSON response from the API. You should see a list of suppliers that match the criteria you provided.
   Example Response:
    {
    "content": [],
    "pageable": {
        "pageNumber": 0,
        "pageSize": 10,
        "sort": {
            "empty": true,
            "sorted": false,
            "unsorted": true
        },
        "offset": 0,
        "paged": true,
        "unpaged": false
    },
    "last": true,
    "totalPages": 0,
    "totalElements": 0,
    "size": 10,
    "number": 0,
    "sort": {
        "empty": true,
        "sorted": false,
        "unsorted": true
    },
    "numberOfElements": 0,
    "first": true,
    "empty": true
}
