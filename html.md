# HTML snippets

### 1 Clear float

.group:before,
.group:after {
	content: "";
	display: table;
}

.group:after {
	clear: both;
}

.group {
	zoom: 1;
}


### 2 Navigation Bar

##### HTML
```
    <nav class="site-nav">
      <ul class="group">
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Portfolio</a></li>
        <li><a href="#">Contact Us</a></li>
      </ul>
    </nav>
 ```

##### CSS
```
.site-nav {
  margin-top: 20px;
}

.site-nav ul {
  margin: 0;
  padding: 0;
}

.site-nav li {
  list-style: none;
  float: left;
  margin-right: 5px;
}

.site-nav a {
  display: block;
  color: #617140;
  text-decoration: none;
  padding: 10px 20px;
  border: 3px solid #e5e9dc;
  border-bottom: none;
}

.site-nav a:hover {
  background-color: #e5e9dc;
}
```

### 3 Overlapping Image

##### html

```
      <div class="image-banner">
      
        <img src="https://learnwebcode.github.io/Web-Design-for-Beginners/squirrel.jpg">
        <div class="banner-description">
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
        </div>
        
      </div>

```
##### css
```
.image-banner{
  position: relative;
}

.banner-description{
  position: absolute;
  bottom: 0;
  left:0;
  color: white;
  padding: 4px 4px;
  background-color: rgba(0,0,0,.5)
}
```
### 4 Table
```
      <table>
        <thead>
          <tr>
            <th class="item-description">Item Name</th>
            <th class="quantity">Quantity</th>
            <th class="price">Price</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>Oranges</td>
            <td>5</td>
            <td>$3.00</td>
          </tr>
          <tr>
            <td>Celery</td>
            <td>2</td>
            <td>$2.50</td>
          </tr>
          <tr>
            <td>Garlic</td>
            <td>2</td>
            <td>$1.90</td>
          </tr>
          <tr>
            <td>Bananas</td>
            <td>6</td>
            <td>$2.99</td>
          </tr>
          <tr>
            <td>Onions</td>
            <td>4</td>
            <td>$3.00</td>
          </tr>
          <tr>
            <td>Very long awkwardly named yet still delicious item here</td>
            <td>4</td>
            <td>$3.00</td>
          </tr>
          <tr>
            <td>Carrots</td>
            <td>12</td>
            <td>$2.99</td>
          </tr>
        </tbody>
      </table>
 ```
 
 ##### CSS
 
 ```
 
 table{
  width: 100%;
  border-spacing: 0;
  border-collapse:collapse;
}

table th {
  text-align: left;
  background-color:#869960;
  border: 1px solid #869960;
  color: white;
}

table th, td{
  border: 1px solid #e5e9dc;
  padding: 8px;
  vertical-align: top;
}

table tbody tr:nth-child(even){
  background-color: #e5e9dc;
}

table tr td:nth-child(2),
table tr td:nth-child(3){
  text-align: right;
}

.item-description{
  width: 60%;
}

.quantity, .price{
  width: 20%;
}
 
 ```
 
### 5 Forms

##### html
<form>

        <label class="hidden-labels" for="email">Email</label>
        <input type="email" name="email" id="email" placeholder="Email">

        <label class="hidden-labels"  for="password">Password</label>
        <input type="password" name="password" id="password" placeholder="Password">

        <select>
          <option>Initially view...</option>
          <option>My Profile</option>
          <option>Inbox</option>
          <option>Account Settings</option>
        </select>

        <input type="submit" value="Sign In">

        <label>
          <input type="checkbox" name="remember" checked="checked" value="yes">
          <span class="checkbox-text">Stay signed in</span>
        </label>

      </form>

##### css
```
form{
  background-color: #e8e8e8;
    padding:40px;
}

input,
select{
  font-family: Tahoma, sans-serif;
  font-size: 100%;


}

input[type="email"],
input[type="password"],
input[type="submit"],
select{
  width: 100%;
  padding: 10px;
  height: 40px;
  box-sizing: border-box;
  margin-bottom: 10px;
}

input[type="email"]:focus,
input[type="password"]:focus,
select {
border: 1px solid #869960;
box-shadow: inset 2px 2px 2px rgba(0,0,0,.2);
}

.hidden-labels{
  position: absolute;
  height: 0;
  width:0;
  overflow: hidden;
  visibility: hidden;
   
}


input[type="submit"]{
  display:block;
  color: white;
  background-color: #869960;
  border: 1px solid #798a57;
  border-radius: 3px;
  
}

input[type="submit"]:focus,
input[type="submit"]:hover{
  background-color: #798a57;
  border: 1px solid #535e38;
  
}

.checkbox-text{
  font-size: 85%;
  color: #888
}
```
