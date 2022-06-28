JsonPowerDB

What is JSON power DB ? JSON (JavaScript Object Notation) is a text-based standard for representing structured data that is based on JavaScript object syntax. It's a Rest API-based Multi-mode DBMS that's real-time, high-performance, lightweight, and simple to use. JsonPowerDB provides a ready-to-use API for Json document databases, RDBMS, Key-value databases, GeoSpatial databases, and Time Series databases. JPDB encourages and promotes the development of real serverless and pluggable APIs.

Benefits of using JsonPowerDB 1)Simplest way to retrieve data in a JSON format. 2)Schema-free, Simple to use, Nimble and In-Memory database. 3)It is built on top of one of the fastest and real-time data indexing engine - PowerIndeX. 4)It is low level (raw) form of data and is also human readable. 5)It helps developers in faster coding, in-turn reduces development cost. 6)Multiple Security Layers 7)A single instance - Million Indexes 8)Inbuilt support for querying multiple databases 9)Serverside Native NoSQL - best performance 10)Multi-mode database - One solution to a variety of data

History Release CODE FOR FORM

<title>Bootstrap Example</title> <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script> <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js"></script> <script src="http://login2explore.com/jpdb/resources/js/0.0.3/jpdb-commons.js"></script>
Vertical (basic) form
Employee ID:
Employee Name:
Email:
<script> function validateAndGetFormData() { var empIdVar = $("#empId").val(); if (empIdVar === "") { alert("Employee ID Required Value"); $("#empId").focus(); return ""; } var empNameVar = $("#empName").val(); if (empNameVar === "") { alert("Employee Name is Required Value"); $("#empName").focus(); return ""; } var empEmailVar = $("#empEmail").val(); if (empEmailVar === "") { alert("Employee Email is Required Value"); $("#empEmail").focus(); return ""; } var jsonStrObj = { empId: empIdVar, empName: empNameVar, empEmail: empEmailVar, }; return JSON.stringify(jsonStrObj); }
        function saveEmployee()
        {
            var jsonStr = validateAndGetFormData();
            if (jsonStr === "") {
                return;
            }
            var putReqStr = createPUTRequest("90939325|-31949287059960581|90939475",
                    jsonStr, "SAMPLE", "EMP-REL");
            alert(putReqStr);
            jQuery.ajaxSetup({async: false});
            var resultObj = executeCommandAtGivenBaseUrl(putReqStr,
                   "http://api.login2explore.com:5577", "/api/iml");
            alert(JSON.stringify(resultObj));
            jQuery.ajaxSetup({async: true});
            resetForm();
        }
       
    </script>
</body>
My Practice Code For All CRUD Operations

PUT:

{ "token": "90939325|-31949287059960581|90939475", "cmd": "PUT", "dbName": "Student", "rel": "Student-Rel", "jsonStr": { "id": "2", "name": "Abhishek", "email": "abhishek@gmail.com", "mobileno": "9967825671" } }

GET: { "token": "90939325|-31949287059960581|90939475", "dbName": "Student", "cmd": "GET_BY_KEY", "rel": "Student-Rel",

"jsonStr": {
    "name": "Abhishek"
}
}

UPDATE: { "token": "90939325|-31949287059960581|90939475", "dbName": "Student", "cmd": "UPDATE", "rel": "Student-Rel",

"jsonStr": {
  "1":{ "name":"Raj"
  },
  "2": { "name" :"Abhishek Kumar Pandey",
        "mobileno":"8420371974"           
       }
}
}

REMOVE: { "token": "90939325|-31949287059960581|90939475", "dbName": "Student", "cmd": "REMOVE", "rel": "Student-Rel",

"jsonStr": {
  "1":{ "name":"Raj"
  },
  "2": { "name" :"Abhishek Kumar Pandey",
        "mobileno":"8420371974"           
       }
}
}

IMAGES OF WORK:-) https://user-images.githubusercontent.com/90323573/176256712-64d19f1d-5e74-456e-be4b-bd344b504696.png https://user-images.githubusercontent.com/90323573/176256990-9bc52dbc-0fff-4a9b-8232-a3bc3c61f402.png https://user-images.githubusercontent.com/90323573/176257035-0763a9f8-030e-49dd-8cfc-748a9fca965a.png
