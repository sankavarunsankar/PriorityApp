# PriorityApp
Allotment of different priorities
Problem Statement:
**Description:** 
There are 4 areas that a user can allot different priorities to. 
1. Connection
2. Relationships
3. Career
4. Wealth

Along with priority, he/she needs to rate the satisfaction for all the above areas on a scale of 1 to 5.
Company admin/creator should have the ability to add more areas in the backend later if needed. 

**Task:**
Create REST APIs that 

- Returns a list of all the priority areas from the database
- Accepts the order of priority along with the satisfaction rating for each area for a user and stores it in the database

**Maven Dependencies Used**
	Restful WebService- Spring Web,
	Spring Boot,
	H2 DataBase,
	ORM- JPA
	
**Created 4 APIs**
1.GET - Priorities list
http://localhost:8080/Priorities

2.POST - Add Priority to Priorities
http://localhost:8080/Priorities
RequestBody
	{
        "id":"",
        "name": "new_priority"
    }
    
3.GET - Priorities of a User
http://localhost:8080/Priorities/104

4.POST - Update/Add Priorities of a User- If User not present add User
http://localhost:8080/addPriorities
RequestBody
	[
	    {
	        "userName": "ABCd",
	        "priorityId":1,
	        "rank": 1,
	        "satisfactionRating": 4
	    },
	    {
	        "userName": "ABCd",
	        "priorityId":2,
	        "rank": 2,
	        "satisfactionRating": 5
	    },
	    {
	        "userName": "ABCd",
	        "priorityId":3,
	        "rank": 3,
	        "satisfactionRating": 5
	    },
	    {
	        "userName": "ABCd",
	        "priorityId":4,
	        "rank": 4,
	        "satisfactionRating": 3
	    }
	]

# Execute /Priority/src/main/resources/schema.sql after starting the Application at H2 
	http://localhost:8080/h2-console
	JDBC URL: jdbc:h2:mem:Varun
	UserName:sa
