## Description
This is an API that provides information on the courses offered at the University of Manitoba. Users can use it to find relevant course information including prerequisites, course name or terms they are generally offered in. Users can also find lists of courses based on a professor or year level.


## Endpoints
1. /courses/{course_number}/prereqs
2. /courses/{year}/list
3. /courses/{professor}/list
4. /terms/{course_number}/list

## Resources
1. You can get a list of courses that are prerequisites for the course number you enter (e.g. COMP2140):
{"results":["COMP1020"],"status":"success"}

2. You can get a list of courses based on what year level they are (e.g. 2000 level courses):
{"results":["COMP2140","COMP2160","COMP2150",etc...],"status":"success"}

3. You can get a list of courses taught by the specified professor (e.g "John Anderson")
{"results":["COMP3190"],"status":"success"}

4. You can get a list of terms the course number you entered is offered (e.g. "COMP2140")
{"results":["Fall 2021","Winter 2022"],"status":"success"}

## Samples Requests
1. Get a list of courses that are prerequisites for COMP2140:
Request: /courses/COMP2140/prereqs
Response: {"results":["COMP1020"],"status":"success"}

2. Get a list of courses at the 2000 level:
Request: /courses/2000/list
Response: {"results":["COMP2140","COMP2160","COMP2150",etc...],"status":"success"}

3. Get a list of courses taught by John Anderson:
Request: /courses/John_Anderson/list
Response: {"results":["COMP3190"],"status":"success"}

4. Get the list of terms in which course COMP 2140 is taught:
Request:/terms/COMP2140/list
Response:{"results":["Fall 2021","Winter 2022"],"status":"success"}
