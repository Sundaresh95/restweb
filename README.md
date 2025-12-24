<img width="1918" height="1053" alt="440898697-d4ec0a2e-3a81-4409-9db6-9b63f3a79767" src="https://github.com/user-attachments/assets/bbb3689e-efb1-41eb-a349-2cb89bf96871" /># Ex.07 Restaurant Website
## Date:15/12/2025
## REf.No:25006077

## AIM:
To develop a static Restaurant website to display the food items and services provided by them.

## DESIGN STEPS:

### Step 1:
Requirement collection.

### Step 2:
Creating the layout using HTML and CSS.

### Step 3:
Updating the sample content.

### Step 4:
Choose the appropriate style and color scheme.

### Step 5:
Validate the layout in various browsers.

### Step 6:
Validate the HTML code.

### Step 7:
Publish the website in the given URL.

## PROGRAM:
~~~
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MARRIOTT MANOR | Home</title>
    <link rel="icon" href="{% static 'favicon.ico' %}">

    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">
    <style>
        body {
            margin: 0;
            font-family: 'Roboto', sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #f4f4f4, #eaeaea);
            box-sizing: border-box;
        }

        *, *::before, *::after {
            box-sizing: inherit;
        }

        header {
            background: linear-gradient(135deg, #2c3e50, #34495e);
            color: white;
            padding: 15px 20px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        header img {
            height: 50px;
        }

        header nav {
            display: flex;
            gap: 15px;
        }

        header nav a {
            text-decoration: none;
            color: white;
            font-weight: 500;
            font-size: 1rem;
            transition: color 0.3s ease;
        }

        header nav a:hover {
            color: #e67e22;
        }

        .banner {
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 40px 20px;
            background: url('banner-placeholder.jpg') no-repeat center center/cover;
            color: white;
            height: 300px;
            text-shadow: 0 4px 8px rgba(0, 0, 0, 0.7);
            text-align: center;
        }

        .banner-content {
            background: rgba(0, 0, 0, 0.5);
            padding: 20px 30px;
            border-radius: 10px;
        }

        .banner-content h1 {
            font-family: 'Playfair Display', serif;
            font-size: 2.5rem;
            margin-bottom: 10px;
            color: #f39c12;
        }

        .banner-content p {
            font-size: 1rem;
            margin-bottom: 15px;
            color: #ecf0f1;
        }

        .banner-content a {
            background: #e67e22;
            color: white;
            padding: 10px 20px;
            text-decoration: none;
            font-weight: bold;
            border-radius: 50px;
            transition: background 0.3s ease, transform 0.3s ease;
        }

        .banner-content a:hover {
            background: #d35400;
            transform: translateY(-3px);
        }

        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            padding: 30px 15px;
            background: #ffffff;
        }

        .feature {
            background: white;
            border-radius: 15px;
            padding: 15px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            text-align: center;
            transition: transform 0.3s ease;
        }

        .feature:hover {
            transform: translateY(-5px);
        }

        .feature img {
            width: 100%;
            border-radius: 10px;
            margin-bottom: 10px;
            transition: transform 0.3s ease;
        }

        .feature img:hover {
            transform: scale(1.05);
        }

        .feature h3 {
            font-size: 1.2rem;
            margin-bottom: 8px;
            color: #2c3e50;
            font-family: 'Playfair Display', serif;
        }

        .feature p {
            font-size: 0.9rem;
            color: #7f8c8d;
        }

        footer {
            background: linear-gradient(135deg, #2c3e50, #34495e);
            color: white;
            text-align: center;
            padding: 15px;
            margin-top: 30px;
        }

        footer a {
            color: #e67e22;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        footer a:hover {
            color: #ecf0f1;
        }

        @media (max-width: 768px) {
            header nav {
                flex-direction: column;
                align-items: center;
                gap: 10px;
            }

            .banner {
                height: auto;
                padding: 20px;
            }

            .banner-content h1 {
                font-size: 2rem;
            }

            .banner-content p {
                font-size: 0.9rem;
            }
        }

        @media (max-width: 480px) {
            .banner-content h1 {
                font-size: 1.8rem;
            }

            .banner-content p {
                font-size: 0.8rem;
            }

            .banner-content a {
                padding: 8px 15px;
                font-size: 0.9rem;
            }
        }
    </style>
</head>
<body>
  <header>
    <h1>MARRIOTT MANOR</h1>
        <nav>
            <a href="home.html">Home</a>
            <a href="menu.html">Menu</a>
            <a href="contact.html">Contact</a>
            <a href="admin.html">Admin</a>
        </nav>
    </header>

    <div class="banner">
        <div class="banner-content">
            <h1>Modern Muse</h1>
            <p>Serving You the Finest Cuisine</p>
            <a href="#features">Discover More</a>
        </div>
    </div>

    <section id="features" class="features">
        <div class="feature">
            <img src="foodpic.jpeg" alt="High quality dishes">
            <h3>High Quality Dishes</h3>
            <p>Savor exquisite culinary creations, meticulously prepared with the finest ingredients and world-class expertise.</p>
        </div>
    </section>
    <footer>
        <p>&copy; 2024 MARRIOTT MANOR. All rights reserved. | <a href="#">Privacy Policy</a></p>
    </footer>
</body>
</html>
~~~

## OUTPUT:
<img width="1918" height="1029" alt="440898640-8715e42e-6059-4ced-98e1-4dd01d3037ac" src="https://github.com/user-attachments/assets/e02ff9e0-f50d-4e58-bdeb-ffe8069e19a4" />
<img width="1918" height="1053" alt="440898697-d4ec0a2e-3a81-4409-9db6-9b63f3a79767" src="https://github.com/user-attachments/assets/949b6abc-69d0-4e50-9183-80afb2779e4f" />


<img width="1917" height="1055" alt="440898724-e2bb4278-a28e-477e-88a4-d3258d02518f" src="https://github.com/user-attachments/assets/25faa950-ad43-43a9-af3d-8aca25ae4701" />


## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
