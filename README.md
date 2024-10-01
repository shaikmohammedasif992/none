<!DOCTYPE html>
{% load static %}
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equip="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">

    <link rel="stylesheet" href="{% static 'app/css/owl.carsousel.min.css' %}">
    <link rel="stylesheet" href="{% static 'app/css/all.min.css' %}">
    <link rel="stylesheet" href="{% static 'app/css/style.css' %}">

  <title>Dairy Products | {% block title %}{% endblock title %} Document</title>
</head>
<body>

  <nav class="navbar navbar-expand-lg navbar-dark bg-success">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">
        <img src="{% static "app/images/neel.png" %}" width="70" height="70" />
      </a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <a class="nav-link active" aria-current="page" href=" / ">Home</a>
          </li>

          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
              Products
            </a>
            <ul class="dropdown-menu">
              <li><a class="dropdown-item" href=" {% url 'category' 'ML' %}">Milk</a></li>
              <li><a class="dropdown-item" href=" {% url 'category' 'CR' %}">Curd</a></li>
              <li><a class="dropdown-item" href=" {% url 'category' 'MS' %}">Milkshake</a></li>
              <li><a class="dropdown-item" href=" {% url 'category' 'LS' %}">Lassi</a></li>
              <li><a class="dropdown-item" href=" {% url 'category' 'GH' %}">Ghee</a></li>
              <li><a class="dropdown-item" href=" {% url 'category' 'PN' %}">Paneer</a></li>
              <li><a class="dropdown-item" href=" {% url 'category' 'CZ' %}">Cheese</a></li>
              <li><a class="dropdown-item" href=" {% url 'category' 'IC' %}">Ice-Creams</a></li>
            </ul>
          </li>

          <li class="nav-item">
            <a class="nav-link text-white" href="{% url 'about' %}">About Us</a>
          </li>
          
          <li class="nav-item">
            <a class="nav-link text-white" href="{% url 'contact' %}">Contact Us</a>
          </li>
        </ul>
        <form class="d-flex" role="search">
          <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
          <button class="btn btn-outline-success" type="submit">Search</button>
        </form>
      </div>
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item dropdown mx-2">
          <a class="nav-link dropdown-toggle text-white" href="#" id="profileDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">Infity</a>
        <ul class="dropdown-menu" aria-labelledy="profileDropdown">
        <li><a class="dropdown-item" href="{% url 'profile' %}">Profile</a></li>
        <li><a class="dropdown-item" href="#">Orders</a></li>
        <li><a class="dropdown-item" href="{% url 'passwordchange' %}">Change Password</a></li>
        <li><a class="dropdown-item" href="{% url 'logout' %}">Logout</a></li>
        </ul>
        </li> 
            <li class="nav-item mx-2">
              <a href="{% url 'login' %}" class="nav-link text-white">Login</a>
              </li>  
              <li class="nav-item mx-2">
                 <a href="{% url 'customerregistration' %}" class="nav-link text-white">Registration</a>
              </li>  
      </ul>
    </div>
  </nav>  

  {% block banner-slider %}{% endblock banner-slider %}
  {% block information %}{% endblock information %}
  {% block main-content %}{% endblock main-content %}
  {% block payment-gateway %}{% endblock payment-gateway %}

  <footer class="container-fluid fixed-bottom bg-success text-center p-2 mt-5">
    Copyrights@2024 || Develop by Infity Software Solutions Pvt Ltd...
  </footer>

<script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.11.8/dist/umd/popper.min.js" integrity="sha384-I7E8VVD/ismYTF4hNIPjVp/Zjvgyol6VFvRkX/vR+Vc4jQkC+hVqc2pM8ODewa9r" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.min.js" integrity="sha384-0pUGZvbkm6XF6gxjEnlmuGrJXVbNuzT9qBBavbLwCsOGabYfZo0T0to5eqruptLy" crossorigin="anonymous"></script>

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.6.1/jquery.min.js"></script>

<script src="{% static 'app/js/owl.carsousel.min.js' %}"></script>
<script src="{% static 'app/js/all.min.js' %}" ></script>
<script src="{% static 'app/js/myscript.js' %}" ></script>

</body>
</html>
