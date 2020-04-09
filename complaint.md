<html>
<head>
    <title>helping hands</title>
    <link href="css/style2.css" rel="stylesheet" type="text/css">
    <link href="https://stackpath.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet" type="text/css">
    <!-- Latest compiled and minified CSS -->
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css">

<!-- jQuery library -->
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>

<!-- Latest compiled JavaScript -->
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js"></script>

<meta charset="utf-8">
<title>Untitled Document</title>
<script>
var stateObject = {
"India": { "Delhi": ["new Delhi", "North Delhi"],
"Kerala": ["Thiruvananthapuram", "Palakkad"],
"Goa": ["North Goa", "South Goa"],

},
"Australia": {
"South Australia": ["Dunstan", "Mitchell"],
"Victoria": ["Altona", "Euroa"]
}, "Canada": {
"Alberta": ["Acadia", "Bighorn"],
"Columbia": ["Washington", ""]
},
}
window.onload = function () {
var countySel = document.getElementById("countySel"),
stateSel = document.getElementById("stateSel"),
districtSel = document.getElementById("districtSel");
for (var country in stateObject) {
countySel.options[countySel.options.length] = new Option(country, country);
}
countySel.onchange = function () {
stateSel.length = 1; // remove all options bar first
districtSel.length = 1; // remove all options bar first
if (this.selectedIndex < 1) return; // done
for (var state in stateObject[this.value]) {
stateSel.options[stateSel.options.length] = new Option(state, state);
}
}
countySel.onchange(); // reset in case page is reloaded
stateSel.onchange = function () {
districtSel.length = 1; // remove all options bar first
if (this.selectedIndex < 1) return; // done
var district = stateObject[countySel.value][this.value];
for (var i = 0; i < district.length; i++) {
districtSel.options[districtSel.options.length] = new Option(district[i], district[i]);
}
}
}
</script>
</head>

</head>
<body>

<header>
    <div class="main"></div>
    <div class="logo">
        <img src=https://static1.squarespace.com/static/58a2668c9f74565dfa449d47/t/58bda1aaebbd1ad2e8ed6c8a/1581978075836/?format=1500w>        
        <nav>
            <ul>
                  <li> <a herf="index.html"><i class="fa fa-home"></i>Home</a>
                   
                  </li>
                  <li> <a herf="#">Services</a>
                        <div class="sub-menu"> <ul>
                             <li><a href="#">status</a></li>
                             <li><a href="#">complaint</a></li>
                         </ul>
                        </div>
                  </li>
                  <li> <a herf="#">Gallery</a></li>
                  <li> <a herf="#">About us</a></li>
                  <li> <a herf="#">Contact</a></li>

            </ul>
        </nav>
    </div>
    
    <div class="reg">
        <h1 style="color: white;text-align: center;font-style: italic;">OUR HANDS ARE READY TO <br>HELP YOU </h1>
            <form method="POST" id="reg" action="..php">
              <label for="full-name">Full Name</label><br>
              <input type="text" name="name" id="full-name" placeholder="First and Last Name" required=""><br>
              <label for="email-address">Email Address</label><br>
              <input type="email" name="_replyto" id="email-address" placeholder="email@domain.tld" required=""><br>
              <label for="telephone">Phone Number (+91)</label><br>
              <input type="telephone" name="telephone" id="telephone" placeholder=""><br>
              <label>Category</label><br>
              <input type="radio" name="gender" id="val" value="male" > <p style="color: #fff; display: inline;">Enquiry</p>
              <input type="radio" name="gender" id="val" value="female"> <p style="color: #fff; display: inline;">Complaint</p> <br>            
