# Day04

Q1. How to compare two JSON have the same properties without order?
var obj1 = { name: "Person 1", age:5 };
var obj2 = { age:5, name: "Person 1" };


Q2. Use the rest countries API url -> https://restcountries.eu/rest/v2/all and display all the country flags in console

Ans-

Below is the javascript code to display all the country flags with country name-

//task.js

    var request=new XMLHttpRequest();
    request.open("GET","https://raw.githubusercontent.com/rvsp/restcountries-json-data/master/res-countries.json");
    request.send();
    request.onload=function(){
      var result=JSON.parse(request.response); 

       for(var i in result)
       {
            console.log("Country-"+result[i].name+" "+"Flag-"+result[i].flag);
       }
    }

To display it in console we need html code as given below-
//index.html

      <!DOCTYPE html>
      <html lang="en">
      <head>
          <meta charset="UTF-8">
          <meta http-equiv="X-UA-Compatible" content="IE=edge">
          <meta name="viewport" content="width=device-width, initial-scale=1.0">
          <title>Document</title>
      </head>
      <body>
          <script src="task.js"></script>
      </body>
      </html>


Q3. Use the same rest countries and print all countries name, region, sub region and population

Ans-

Below is the javascript code to display all the country names,region,subregion and it's population-

//task.js

    var request=new XMLHttpRequest();
    request.open("GET","https://raw.githubusercontent.com/rvsp/restcountries-json-data/master/res-countries.json");
    request.send();
    request.onload=function(){
      var result=JSON.parse(request.response); 

       for(var i in result)
       {
            console.log("Country-"+result[i].name+" "+"Region- "+result[i].region+" "+"Subregion-"+result[i].region+" "+"Population- "+result[i].population);

       }
    }

To display it in console we need html code as given below-
//index.html

      <!DOCTYPE html>
      <html lang="en">
      <head>
          <meta charset="UTF-8">
          <meta http-equiv="X-UA-Compatible" content="IE=edge">
          <meta name="viewport" content="width=device-width, initial-scale=1.0">
          <title>Document</title>
      </head>
      <body>
          <script src="task.js"></script>
      </body>
      </html>


