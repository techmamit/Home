# HTML snippets

#### Clear float

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


#### Navigation Bar

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
