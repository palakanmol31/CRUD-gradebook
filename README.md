# CRUD-gradebook

## How to run the code
1. git clone https://github.com/palakanmol31/CRUD-gradebook
2. Import the zip file on Netbeans. 
3. Clean and build and run the server .
4. Clean and build and run the client. 
5. Make sure student id is in string. Student id and task is required to do crud operations around the resource.


## Test Cases 

1.  Create – Select Instructor and tap create radio button. 
1) 201 , CREATED -  Add id and select a work task,then tap submit . 
2) 409 , CONFLICT – add a work task and student id that already exists and tap submit.
3) 400, BAD REQUEST – Do not add any work task or student name. 
4) 500, INTERNAL SERVER ERROR – Any runtime exception. 

2. Read – Select instructor or student and tap read radio button.
1) 410, GONE –  without creating or after deleting all ids, try reading an id. 
2) 200 , OK –  add a valid id and work task and tap submit
3) 404, NOT FOUND – add any random id that does not exists 
     
3.  Update – Select instructor and tap update button.
1) 200 , Ok – add a valid id and work task that exists, update the details and then tap submit .
2) 409 , CONFLICT –add an id or work task that does not exists
3) 400, BAD REQUEST – Do not add any work task or student name. 
4) 500, INTERNAL SERVER ERROR – Any runtime exception. 

4. Delete – Select instructor and tap delete radio button
1) 204 – NO Content – add id and work task that exists in the database
2) 404, NOT FOUND – add any random id that does not exists 
3) 410, GONE –  without creating or after deleting all ids, try reading an id. 

5. Appeal – Select student and tap appeal radio button
1)  200 , Ok – add a valid id that exists and also a task and tap submit. An appeal will be filed.
2) 409 , CONFLICT –add an id and work task that does not exists
3) 400, BAD REQUEST – Do not add any work task or student name. 
4) 500, INTERNAL SERVER ERROR – Any runtime exception. 


