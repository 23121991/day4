# day4
ques1.

how to compare to JSON have the same properties without order?

var obj1 = { name: 'person1', age: 5 };
var obj2 = { age: 5, name: 'person 1' };
ans1.
var obj1  = { 
  name: 'person1',
age: 5
};
var obj2 = { 
  age: 5,
  name: 'person 1' 
  };
    
//JSON.stringify(obj1) ===JSON.stringify(obj2)
false
//JSON.stringify(obj1=obj2)
true
console.log(obj1=obj2);
console.log (obj===obj2);


QUES.2
use the same rest countries print all the countries,region,subregion and population ?
ANS:

intex.html FORMAT:

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta http-equiv="X-UA-Compatible" content="IE=edge">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Document</title>
</head>
<body>
	<script src="script.js"><scriptsrc>
</body>
</html>



script.js FORMAT:

var request=new XMLHttpRequest();
request.open("GET","https://raw.githubusercontent.com/rvsp/restcountries-json-data/master/res-countries.json");
request.send();
request.onload=function(){
    var result=JSON.parse(request.response);
    for(let i=0;i<result.length;i++)
    console.log(result[i].names);
    for(let i=0;i<result.length;i++)
    console.log(result[i].region);
    for(let i=0;i<result.length;i++)
    console.log(result[i].subregion);
    for(let i=0;i<result.length;i++)
    console.log(result[i].population);
}


QUES3:
use the same rest countries api to display all the countries flag?
ANS:

script.js FORMAT:

var request=new XMLHttpRequest();
request.open("GET","https://raw.githubusercontent.com/rvsp/restcountries-json-data/master/res-countries.json");
request.send();
request.onload=function(){
    var result=JSON.parse(request.response);
    for(let i=0;i<result.length;i++)
    console.log(result[i].flag);

}
