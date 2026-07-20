<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>MR's Momos | Fresh Hot Delicious</title>

<style>

body{
margin:0;
font-family:Arial, sans-serif;
background:#fff7f2;
color:#333;
}

header{
background:#c1121f;
color:white;
text-align:center;
padding:30px;
}

header h1{
font-size:40px;
margin:0;
}

header p{
font-size:18px;
}


.container{
width:90%;
max-width:1100px;
margin:auto;
padding:20px;
}


.menu{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(230px,1fr));
gap:20px;
}


.card{
background:white;
border-radius:12px;
padding:15px;
box-shadow:0 3px 10px #ddd;
}


.card h3{
margin-top:5px;
}


.price{
color:#c1121f;
font-size:20px;
font-weight:bold;
}


button{
background:#c1121f;
color:white;
border:none;
padding:12px;
border-radius:8px;
width:100%;
cursor:pointer;
}


button:hover{
background:#8d0801;
}


.order-box{
background:white;
padding:20px;
border-radius:12px;
box-shadow:0 3px 10px #ddd;
margin-top:30px;
}


input,select,textarea{

width:100%;
padding:12px;
margin:8px 0 15px;
border-radius:8px;
border:1px solid #ccc;

}


.whatsapp{

background:#25D366;

}


.review{

background:white;
padding:15px;
border-radius:10px;
margin:10px 0;
box-shadow:0 2px 5px #ddd;

}


footer{

background:#222;
color:white;
text-align:center;
padding:20px;
margin-top:30px;

}

</style>

</head>


<body>


<header>

<h1>🥟 MR's Momos</h1>

<p>Fresh • Hot • Delicious</p>

<p>Pickup Orders Available</p>

</header>



<div class="container">


<h2>Our Menu</h2>


<div class="menu">


<script>

let menu=[

["Veg Steamed Momos","$9.99"],
["Chicken Steamed Momos","$10.99"],
["Paneer Momos","$10.99"],
["Veg Fried Momos","$10.99"],
["Chicken Fried Momos","$11.99"],
["Tandoori Veg Momos","$12.99"],
["Tandoori Chicken Momos","$13.99"],
["Chilli Momos","$12.99"],
["Masala Fries","$5.99"],
["Cold Drink","$2.49"]

];


menu.forEach(function(item){

document.write(`

<div class="card">

<h3>${item[0]}</h3>

<p class="price">${item[1]}</p>

<button onclick="addCart('${item[0]} ${item[1]}')">
Add To Cart
</button>

</div>

`);

});


</script>


</div>



<div class="order-box">


<h2>Your Order</h2>


<ul id="cart"></ul>



<h3>Customer Details</h3>


<label>Name</label>

<input id="name" placeholder="Your Name">



<label>Phone</label>

<input id="phone" placeholder="Phone Number">



<label>Pickup Date</label>

<input type="date" id="date">



<label>Pickup Time</label>

<input type="time" id="time">



<label>Special Request</label>

<textarea id="note" placeholder="Extra chutney, spicy, etc."></textarea>



<button class="whatsapp" onclick="sendOrder()">

Order On WhatsApp

</button>



</div>



<h2>Customer Reviews</h2>


<div class="review">
⭐⭐⭐⭐⭐ Amazing momos and great taste!
</div>


<div class="review">
⭐⭐⭐⭐⭐ Fast pickup and friendly service.
</div>


<div class="review">
⭐⭐⭐⭐⭐ Best momos in town.
</div>



</div>



<footer>

© 2026 MR's Momos

</footer>




<script>


let cart=[];


function addCart(item){

cart.push(item);

document.getElementById("cart").innerHTML=

cart.map(x=>"<li>"+x+"</li>").join("");

}



function sendOrder(){


let message=

`🥟 MR's MOMOS ORDER

Name:
${document.getElementById("name").value}

Phone:
${document.getElementById("phone").value}

Pickup Date:
${document.getElementById("date").value}

Pickup Time:
${document.getElementById("time").value}


Items:

${cart.join("\n")}


Notes:

${document.getElementById("note").value}

`;



let whatsapp="18252505474";


window.open(

"https://wa.me/"+whatsapp+"?text="+encodeURIComponent(message),

"_blank"

);


}


</script>



</body>
</html>
