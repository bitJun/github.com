# 字符串转json格式的三种方式

## 1、eval方式解析，恐怕这是最早的解析方式了
function strToJson(str){ 
var json = eval('(' + str + ')'); 
return json; 
} 

## 2、new Function形式
function strToJson(str){ 
var json = (new Function("return " + str))(); 
return json; 
} 

## 3、使用全局的JSON对象
function strToJson(str){ 
return JSON.parse(str); 
} 
