# Web Page for Mathematical Calculations

## AIM:

To design a static website with validation to perform mathematical calculations in client side.

## DESIGN STEPS:

### Step 1:

Requirement collection.

### Step 2:

Creating the layout using HTML and CSS.

### Step 3:

Write javascript to perform the calculations.

### Step 4:

Include regularexpression based input validation.

### Step 5:

Validate the layout in various browsers.

### Step 6:

Validate the HTML code.

### Step 6:

Publish the website in the given URL.

## PROGRAM :

### index html:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Volume</title>
    <h1>MATHEMATICAL CALCULATIONS</h1>
    <style>
        * {
  box-sizing: border-box;
  font-family: Arial, Helvetica, sans-serif;
}
body {
  background-color:rgb(189, 192, 202);
}
.container {
  width: 1000px;
  margin-left: auto;
  margin-right: auto;
  
}
.content {
    display: block;
    width: 100%;
    background-color: #ff0728;
    max-height: 300px;
    max-width: 750px;
    margin-left: auto;
    margin-right: auto;
} 
.content2{
    display: block;
    width: 100%;
    background-color: #ff0728;
    max-width: 750px;
    margin-left: auto;
    margin-right: auto;
}
h1{
    text-align: center;
    font-size: 30px;
    color: black;
}
h2{
    text-align: center;
    font-size: 28px;
    padding-top: 10px;
    color: rgb(36, 23, 23);
}
.formelement{
    text-align: center;
    font-size:20px;

}
.footer{
    display:block;
    width:100%;
    height:44r4r0px;
    background-color:lightcyan;
    text-align:center;
    margin:0px 0px 0px 0px;
    color:#000000;
    font-size:30px;
}
    </style>
</head>
<body>

    <div class="container">
        <div class="content">
            <h2>AREA OF RECTANGLE</h2>
            <form>
                <div class=formelement>
                    <lable for="aedit">Length:</lable>
                    <input type="text" id="aedit" value="0"/>
                </div><br>
                <div class=formelement>
                    <lable for="bedit">Width:</lable>
                    <input type="text" id="bedit" value="0"/>
                </div><br>
                <div class=formelement>
                    <input type="button" value="AREA" id="calbutton"/>
                </div><br>
                <div class=formelement>
                    <lable for="cedit">Area:</lable>
                    <input type="text" id="cedit" readonly="0"/>
                </div><br>
                <div class=formelement>
                    Formula is LENGTH*WIDTH
                </div>
            </form>
        </div>
        <script type="text/javascript">
            var button;
            button=document.querySelector("#calbutton");
            button.addEventListener("click",function(){
                var atext,btext,ctext;
                var aval,bval,cval;
                var r1,r2,regexp;

                atext=document.querySelector("#aedit");
                btext=document.querySelector("#bedit");
                ctext=document.querySelector("#cedit");

                regexp=new RegExp("^[1-9]+[0-9]*$");

                aval=parseInt(atext.value);
                r1=aval.match(regexp);
                bval=parseInt(btext.value);
                r2=bval.match(regexp);


                if(r1==null)
               {
                alert("Please Enter positive INTEGERS ")
               }
               if(r2==null)
               {
                alert("Please Enter positive INTEGERS ")  
               }
                

                cval=aval*bval
                ctext.value=""+cval;
            });
        </script>
        <div class="content2">
            <h2>VOLUME OF RECTANGLE</h2>
            <form>
                <div class="formelement">
                  <lable for="radiusedit">Length:</lable>
                  <input type="text" id="lengthedit" value=" "/>
                </div><br>
                <div class="formelement">
                  <lable for="heightedit">Height:</lable>
                  <input type="text" id="heightedit" value=" "/>
                </div><br>
                <div class="formelement">
                  <lable for="heightedit">Width:</lable>
                  <input type="text" id="widthedit" value=" "/>
                </div><br>
                <div class="formelement">
                  <input type="button" value="Volume" id="valbutton"/>
                </div><br>
                <div class="formelement">
                  <lable for="volumeedit">VOLUME:</lable>
                  <input type="text" id="volumeedit" readonly="0"/>
                </div><br>
                <div class="formelement">
                Formula is:Length*Width*Height
                </div><br>
                
            </form>
    
            </div>
            
        </div>
        <script type="text/javascript">
          var button;
          button=document.querySelector("#valbutton");
          button.addEventListener("click",function(){
            
              var lengthtext,heighttext,widthtext,volumetext;
              var lval,hval,wval,vval;
              var r3,r4,r5,regexp;
    
              lengthtext=document.querySelector("#lengthedit");
              heighttext=document.querySelector("#heightedit");
              widthtext=document.querySelector("#widthedit");
              volumetext=document.querySelector("#volumeedit");

              regexp=new RegExp("^[1-9]+[0-9]*$");
      
              lval=parseFloat(lengthtext.value)
              r3=lval.match(regexp);
              hval=parseFloat(heighttext.value)
              r4=hval.match(regexp);
              wval=parseFloat(widthtext.value)
              r5=wval.match(regexp);

              if(r3==null)
              {
                alert("Please Enter positive INTEGERS ")
              }
              if(r4==null)
              {
                alert("Please Enter positive INTEGERS ")  
              }
              if(r5==null)
              {
                alert("please Enter positive INTEGERS ")
              }
              vval=lval*hval*wval
              volumetext.value=""+vval;
        
      
            });
      
        </script>     
        <div class="footer">Developed by Haridharshini.S</div>
    
</body>
</html>
```

## OUTPUT:

![output](./output.png)

## Result:

Thus a website is designed to perform mathematical calculations in the client side.
