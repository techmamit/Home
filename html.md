# HTML snippets

1 Clear float

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


2 Navigation Bar

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

3 Overlapping Image

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
