# solarofficeproject
<!---------------------------------------                         PUMP DESIGN.                   ----------------------------------------->
<P8>PUMP DESIGN</P8><br><br><br><br>
<p2>
Input the value of HEAD and DISCHARGE to get the size of the Pump<br>
in your project<br><br>
<br>
HEAD in meters<br><input type="text" id="head">
<br>
DISCHARGE in litres per day<br><input type="text" id="discharge">
<br>
LENGTH 	of pipe in meters<br><input type="text" id="length">
<br><br><br>
Input type of pipe<br><label>Select list</label>
             <select id = "pipe">
               <option value = "1">HDPE</option>
               <option value = "2">GI</option>
               <option value = "3">PVC</option>
             </select>
<br><br><br>
<button onclick="calculat()">calculate</button>
<br><br>
Size of PUMP required is <p10 id="insert1"></p10> HorsePower
<br><br>
Headloss in pipe is  <p11 id="insert3"></p11> meters
<br><br>
Diameter of pipe is <p12 id="insert4"></p12> millimeters

                       <script >
var x;
var y;
var z;
var w;
var a;
var b;
var c;
var d;
var e;
var f;
var g;
var h;
var i;
var j;
function calculat()
{
x= document.getElementById("head").value;
y= document.getElementById("discharge").value;
a= document.getElementById("length").value;
    if(pipe==1)
    	b=0.04;
    else if(pipe==2)
    	b=0.03;
    else
    	b=0.025;
c= y/(5*3600*1000);
d=Math.sqrt(c);
e=1.22*d;
f=8*b*a*c*c/(3.14*3.14*9.81*d*d*d*d*d);
g=x+e;
h=Math.floor(f);
i=1000*e;
j=Math.floor(i);
z =9.81*g*y/(0.65*1000*5*36000*0.746)+1;
w=Math.floor(z);
document.getElementById("insert1").innerHTML = w;
document.getElementById("insert3").innerHTML = h;
document.getElementById("insert4").innerHTML = j;
}
                      </script><br>

<br>
<br>
<br><br>
<!------------------------------------------                         HOMESYSTEM DESIGN.                      ------------------------------->
<P9>HOME SYSTEM DESIGN</P9><br><br><br><br>
<p3>
Input the number of APPLIANCES used in your home <br>
<br>
<br>
Lamps<br><input type="text" id="lamp">
<br>
tubelights<br><input type="text" id="tubelight">
<br>
colour TV<br><input type="text" id="colourTV">
<br>
LED TV<br><input type="text" id="LEDTV">
<br>
Fridge<br><input type="text" id="Fridge">
<br>
Ceiling Fan<br><input type="text" id="CeilingFan">
<br>
DesktopComputer<br><input type="text" id="DesktopsComputer">
<br>
HomeInternetRouter<br><input type="text" id="HomeInternetRouter">
<br>
LaptopComputer<br><input type="text" id="LaptopComputer">
<br>
<button onclick="calculate()">calculate</button>
<br>
Size of Solar Home System required is <p5 id="insert2"></p5> Watt

                            <script >
var a;   
var b;    
var c;    
var d;   
var e;    
var f;    
var g;     
var h;      
var i;     
var j;

function calculate()
{
a= document.getElementById("lamp").value;
b= document.getElementById("tubelight").value;
c= document.getElementById("colourTV").value;
d= document.getElementById("LEDTV").value;
e= document.getElementById("Fridge").value;
f= document.getElementById("CeilingFan").value;
g= document.getElementById("DesktopsComputer").value;
h= document.getElementById("HomeInternetRouter").value;
i= document.getElementById("LaptopComputer").value;
j =a*5+b*20+c*100*0.5+d*60*0.5+e*120+f*50+g*200*0.5+h*10+i*70*0.5;
document.getElementById("insert2").innerHTML = j;
}
                           </script><br>

</p3>
<br>
<br>
