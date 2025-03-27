<!DOCTYPE html><html lang="en">
<head>  
  <meta charset="UTF-8">  
    <meta name="viewport" content="width=device-width, initial-scale=1.0">   
     <meta http-equiv="X-UA-Compatible" content="ie=edge">  
       <title>Document</title> 
          <style>      
            table {         
               width: 500px;         
                  margin: 50px auto;         
                     border-collapse: collapse;           
                      border: 1px solid gray;      
                        }
        td {           
         border: 1px solid gray;            
         text-align: center;           
          line-height: 35px;        
          }   
           </style>
           </head>
<body>   
 姓名：<input type="text" id="txt-name">   
  年龄：<input type="text" id="txt-age">   
   <button onclick="show()">添加</button>
    <script>        
    var tab = document.createElement('table');       
     tab.createCaption().innerHTML = '宿舍信息表'; //标题        
     var tr = tab.insertRow();       
      tr.insertCell().innerHTML = '姓名';       
       tr.insertCell().innerHTML = "年龄";       
        tr.insertCell().innerHTML = '操作';

        //查找元素       
         var txtName=document.getElementById('txt-name');       
          var txtAge=document.getElementById('txt-age');       

        function show() {            
        //插入一行数据            
        var tr=tab.insertRow();            
        tr.insertCell().innerHTML=txtName.value;           
         tr.insertCell().innerHTML=txtAge.value;           
          tr.insertCell().innerHTML="<a href='#' onclick='del(this)'>删除</a>";            
            document.body.appendChild(tab);        
            }
        function del(obj){                        
        var t=obj.parentNode.parentNode;           
         t.parentNode.removeChild(t);        
         }
           </script>
           </body>
</html>
