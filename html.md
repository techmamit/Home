#HTML snippets

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
