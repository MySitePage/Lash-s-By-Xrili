

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>lashesbyxrili | Elegant Lash Studio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;500;600;700&family=Playfair+Display:ital,wght@0,400;0,500;0,600;1,400&family=Poppins:wght@300;400;500&family=Montserrat:wght@400;500;600&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --soft-pink: #ffeef5;
            --light-pink: #fdd5e8;
            --medium-pink: #fbb6d9;
            --image-pink: #ffaad4;
            --dark-pink: #f98ec7;
            --soft-gray: #a9919c;
            --text-dark: #8c7a83;
            --cream: #fff9fc;
            --pale-peach: #ffeaf3;
        }

        body {
            font-family: 'Poppins', sans-serif;
            color: var(--text-dark);
            background-color: var(--soft-pink);
            line-height: 1.7;
            background-image: url('https://www.dropbox.com/scl/fi/ix4smsyipwuhgf5h3ywe9/IMG_7427.jpeg?rlkey=f5ebtpt12o16oebwee6wwbj8y&st=wwar5hf9&dl=1');
            background-size: cover;
            background-attachment: fixed;
            background-position: center;
            min-height: 100vh;
            position: relative;
        }

        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(rgba(255, 238, 245, 0.92), rgba(255, 249, 252, 0.95));
            z-index: -1;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        header {
            background-color: rgba(255, 255, 255, 0.97);
            box-shadow: 0 5px 25px rgba(255, 170, 212, 0.1);
            position: sticky;
            top: 0;
            z-index: 100;
            padding: 0.8rem 0;
            border-bottom: 1px solid rgba(251, 182, 217, 0.5);
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            flex-direction: column;
            align-items: flex-start;
        }

        .logo h1 {
            font-family: 'Dancing Script', cursive;
            font-size: 2.8rem;
            font-weight: 700;
            color: var(--image-pink);
            letter-spacing: 1px;
            line-height: 1;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.05);
        }

        .logo-subtitle {
            font-family: 'Playfair Display', serif;
            font-style: italic;
            font-size: 0.9rem;
            color: var(--soft-gray);
            letter-spacing: 1.5px;
            margin-top: 3px;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 2.2rem;
        }

        nav a {
            text-decoration: none;
            color: var(--text-dark);
            font-family: 'Playfair Display', serif;
            font-size: 1.15rem;
            font-weight: 500;
            padding: 0.5rem 0;
            position: relative;
            transition: color 0.3s ease;
        }

        nav a:hover, nav a.active {
            color: var(--image-pink);
        }

        nav a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            background: linear-gradient(to right, var(--image-pink), var(--dark-pink));
            bottom: 0;
            left: 0;
            transition: width 0.3s ease;
        }

        nav a:hover::after, nav a.active::after {
            width: 100%;
        }

        .header-cta {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .booking-btn {
            background: linear-gradient(to right, var(--image-pink), var(--dark-pink));
            color: white;
            border: none;
            padding: 10px 22px;
            font-size: 1rem;
            border-radius: 50px;
            cursor: pointer;
            font-weight: 500;
            transition: all 0.3s ease;
            font-family: 'Playfair Display', serif;
            text-decoration: none;
            display: inline-block;
            box-shadow: 0 4px 12px rgba(255, 170, 212, 0.2);
        }

        .booking-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 18px rgba(255, 170, 212, 0.3);
        }

        /* Hero Section */
        .hero {
            padding: 4rem 0 3rem;
            text-align: center;
            position: relative;
        }

        .hero-title {
            font-family: 'Dancing Script', cursive;
            font-size: 3.5rem;
            color: var(--image-pink);
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.05);
        }

        .hero-subtitle {
            font-family: 'Playfair Display', serif;
            font-size: 1.4rem;
            color: var(--soft-gray);
            margin-bottom: 2rem;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
            font-style: italic;
        }

        .hero-decoration {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .decoration-line {
            height: 1px;
            width: 80px;
            background: linear-gradient(to right, transparent, var(--image-pink), transparent);
        }

        .decoration-icon {
            color: var(--image-pink);
            font-size: 1.5rem;
        }

        /* Main Content */
        .main-content {
            padding: 1rem 0 4rem;
        }

        .page {
            display: none;
            animation: fadeIn 0.8s ease;
        }

        .page.active {
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Section Styling */
        .section-title {
            font-family: 'Dancing Script', cursive;
            font-size: 2.5rem;
            text-align: center;
            color: var(--image-pink);
            margin-bottom: 2.5rem;
            position: relative;
            display: inline-block;
            left: 50%;
            transform: translateX(-50%);
        }

        .section-title::after {
            content: '';
            position: absolute;
            width: 60%;
            height: 2px;
            background: linear-gradient(to right, transparent, var(--image-pink), transparent);
            bottom: -10px;
            left: 20%;
        }

        .card {
            background-color: rgba(255, 255, 255, 0.94);
            border-radius: 18px;
            padding: 2.2rem;
            margin-bottom: 2rem;
            box-shadow: 0 10px 30px rgba(255, 170, 212, 0.08);
            border: 1px solid rgba(251, 182, 217, 0.4);
            backdrop-filter: blur(5px);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(255, 170, 212, 0.12);
        }

        /* Home Page */
        .welcome-section {
            margin-bottom: 3rem;
        }

        .welcome-text {
            font-size: 1.1rem;
            text-align: center;
            max-width: 800px;
            margin: 0 auto 2.5rem;
            color: var(--text-dark);
            line-height: 1.8;
        }

        .highlight-box {
            background: linear-gradient(135deg, rgba(253, 213, 232, 0.3), rgba(255, 238, 245, 0.4));
            border-radius: 15px;
            padding: 1.8rem;
            margin: 2rem 0;
            border-left: 4px solid var(--image-pink);
        }

        .highlight-text {
            font-family: 'Playfair Display', serif;
            font-size: 1.3rem;
            color: var(--image-pink);
            text-align: center;
            font-style: italic;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2.2rem;
            margin: 3rem 0;
        }

        .feature-card {
            background-color: rgba(255, 255, 255, 0.94);
            border-radius: 15px;
            padding: 2rem;
            text-align: center;
            box-shadow: 0 8px 25px rgba(255, 170, 212, 0.08);
            border: 1px solid rgba(251, 182, 217, 0.4);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .feature-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(to right, var(--image-pink), var(--dark-pink));
        }

        .feature-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 15px 35px rgba(255, 170, 212, 0.15);
        }

        .feature-icon {
            font-size: 2.5rem;
            color: var(--image-pink);
            margin-bottom: 1.2rem;
            background: linear-gradient(to right, var(--image-pink), var(--dark-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .feature-title {
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
            color: var(--image-pink);
            margin-bottom: 1rem;
            font-weight: 600;
        }

        .owners-section {
            display: flex;
            align-items: center;
            gap: 3rem;
            margin: 4rem 0;
            background-color: rgba(255, 255, 255, 0.94);
            border-radius: 18px;
            padding: 2.5rem;
            box-shadow: 0 10px 30px rgba(255, 170, 212, 0.08);
            border: 1px solid rgba(251, 182, 217, 0.4);
        }

        .owners-photo {
            flex: 1;
            min-width: 300px;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }

        .owners-photo img {
            width: 100%;
            height: auto;
            display: block;
            transition: transform 0.5s ease;
        }

        .owners-photo:hover img {
            transform: scale(1.03);
        }

        .owners-info {
            flex: 1;
            min-width: 300px;
        }

        .owners-info h3 {
            font-family: 'Dancing Script', cursive;
            font-size: 2.5rem;
            color: var(--image-pink);
            margin-bottom: 1.2rem;
        }

        .owners-info p {
            margin-bottom: 1.5rem;
            font-size: 1.05rem;
            line-height: 1.8;
        }

        .instagram-handle {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            background: linear-gradient(to right, rgba(253, 213, 232, 0.3), rgba(255, 238, 245, 0.4));
            padding: 10px 20px;
            border-radius: 50px;
            color: var(--image-pink);
            font-weight: 500;
            text-decoration: none;
            transition: all 0.3s ease;
            border: 1px solid rgba(251, 182, 217, 0.5);
        }

        .instagram-handle:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(255, 170, 212, 0.1);
        }

        /* Portfolio Section */
        .portfolio-section {
            margin: 4rem 0;
        }

        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .portfolio-item {
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.08);
            transition: all 0.4s ease;
            position: relative;
            height: 300px;
        }

        .portfolio-item:hover {
            transform: translateY(-8px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.12);
        }

        .portfolio-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
            transition: transform 0.5s ease;
        }

        .portfolio-item:hover img {
            transform: scale(1.05);
        }

        .portfolio-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(to top, rgba(0, 0, 0, 0.7), transparent);
            color: white;
            padding: 1.5rem;
            transform: translateY(100%);
            transition: transform 0.3s ease;
        }

        .portfolio-item:hover .portfolio-overlay {
            transform: translateY(0);
        }

        /* Prices & Policy Page */
        .prices-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin: 2rem 0 3rem;
        }

        .price-card {
            background-color: rgba(255, 255, 255, 0.94);
            border-radius: 15px;
            padding: 2rem;
            text-align: center;
            box-shadow: 0 8px 25px rgba(255, 170, 212, 0.08);
            border: 1px solid rgba(251, 182, 217, 0.4);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .price-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(to right, var(--image-pink), var(--dark-pink));
        }

        .price-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 15px 35px rgba(255, 170, 212, 0.15);
        }

        .price-title {
            font-family: 'Montserrat', sans-serif;
            font-size: 1.5rem;
            color: var(--image-pink);
            margin-bottom: 1rem;
            font-weight: 600;
            letter-spacing: 0.5px;
        }

        .price-amount {
            font-family: 'Montserrat', sans-serif;
            font-size: 2.2rem;
            color: var(--text-dark);
            font-weight: 700;
            margin-bottom: 0.5rem;
        }

        .price-details {
            color: var(--soft-gray);
            font-size: 1rem;
            margin-bottom: 1rem;
            font-family: 'Poppins', sans-serif;
        }

        .price-note {
            font-size: 0.9rem;
            color: var(--soft-gray);
            font-style: italic;
            margin-top: 1rem;
            padding-top: 1rem;
            border-top: 1px dashed rgba(251, 182, 217, 0.8);
            font-family: 'Poppins', sans-serif;
        }

        .color-notice {
            background: linear-gradient(135deg, rgba(253, 213, 232, 0.3), rgba(255, 238, 245, 0.4));
            border-radius: 15px;
            padding: 1.5rem;
            margin: 2rem 0;
            text-align: center;
            border: 1px solid rgba(251, 182, 217, 0.5);
        }

        .color-notice h4 {
            font-family: 'Playfair Display', serif;
            font-size: 1.4rem;
            color: var(--image-pink);
            margin-bottom: 0.5rem;
        }

        .policy-list {
            list-style: none;
            padding-left: 0;
        }

        .policy-item {
            padding: 1.2rem 0;
            border-bottom: 1px solid rgba(251, 182, 217, 0.5);
            display: flex;
            align-items: flex-start;
        }

        .policy-item:last-child {
            border-bottom: none;
        }

        .policy-icon {
            color: var(--image-pink);
            margin-right: 15px;
            margin-top: 3px;
            font-size: 1.1rem;
            min-width: 20px;
        }

        /* Booking Page with Payment Method */
        .booking-section {
            max-width: 800px;
            margin: 0 auto;
        }

        .booking-form {
            background-color: rgba(255, 255, 255, 0.94);
            border-radius: 18px;
            padding: 2.5rem;
            box-shadow: 0 10px 30px rgba(255, 170, 212, 0.08);
            border: 1px solid rgba(251, 182, 217, 0.4);
        }

        .form-title {
            font-family: 'Dancing Script', cursive;
            font-size: 2.2rem;
            color: var(--image-pink);
            text-align: center;
            margin-bottom: 1.5rem;
        }

        .form-intro {
            text-align: center;
            margin-bottom: 2rem;
            color: var(--soft-gray);
            font-size: 1.05rem;
        }

        .form-group {
            margin-bottom: 1.8rem;
        }

        .form-label {
            display: block;
            margin-bottom: 0.5rem;
            color: var(--text-dark);
            font-weight: 500;
            font-family: 'Playfair Display', serif;
            font-size: 1.1rem;
        }

        .form-control {
            width: 100%;
            padding: 14px 18px;
            border: 1px solid rgba(251, 182, 217, 0.8);
            border-radius: 10px;
            font-size: 1rem;
            background-color: rgba(255, 255, 255, 0.9);
            color: var(--text-dark);
            transition: all 0.3s ease;
            font-family: 'Poppins', sans-serif;
        }

        .form-control:focus {
            outline: none;
            border-color: var(--image-pink);
            box-shadow: 0 0 0 3px rgba(255, 170, 212, 0.1);
        }

        textarea.form-control {
            min-height: 120px;
            resize: vertical;
        }

        /* Payment Methods Section */
        .payment-methods {
            background: linear-gradient(135deg, rgba(253, 213, 232, 0.2), rgba(255, 238, 245, 0.3));
            border-radius: 15px;
            padding: 1.8rem;
            margin: 2rem 0;
            border: 1px solid rgba(251, 182, 217, 0.5);
        }

        .payment-title {
            font-family: 'Playfair Display', serif;
            font-size: 1.4rem;
            color: var(--image-pink);
            margin-bottom: 1.2rem;
            text-align: center;
        }

        .payment-options {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 1.5rem;
            margin-top: 1.5rem;
        }

        .payment-option {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
            background-color: rgba(255, 255, 255, 0.9);
            padding: 1.2rem;
            border-radius: 12px;
            min-width: 120px;
            border: 1px solid rgba(251, 182, 217, 0.5);
            transition: all 0.3s ease;
        }

        .payment-option:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(255, 170, 212, 0.1);
        }

        .payment-icon {
            font-size: 2rem;
            color: var(--image-pink);
        }

        .payment-name {
            font-family: 'Montserrat', sans-serif;
            font-weight: 600;
            color: var(--text-dark);
            font-size: 0.95rem;
        }

        .submit-btn {
            background: linear-gradient(to right, var(--image-pink), var(--dark-pink));
            color: white;
            border: none;
            padding: 16px 35px;
            font-size: 1.1rem;
            border-radius: 50px;
            cursor: pointer;
            font-weight: 500;
            display: block;
            margin: 2.5rem auto 0;
            transition: all 0.3s ease;
            font-family: 'Playfair Display', serif;
            width: 100%;
            max-width: 300px;
            box-shadow: 0 5px 15px rgba(255, 170, 212, 0.2);
        }

        .submit-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(255, 170, 212, 0.3);
        }

        .form-footer {
            text-align: center;
            margin-top: 2rem;
            font-size: 0.9rem;
            color: var(--soft-gray);
            padding-top: 1.5rem;
            border-top: 1px solid rgba(251, 182, 217, 0.5);
        }

        /* Contact Section */
        .contact-section {
            margin: 4rem 0 2rem;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .contact-card {
            background-color: rgba(255, 255, 255, 0.94);
            border-radius: 15px;
            padding: 2rem;
            text-align: center;
            box-shadow: 0 8px 25px rgba(255, 170, 212, 0.08);
            border: 1px solid rgba(251, 182, 217, 0.4);
            transition: all 0.3s ease;
        }

        .contact-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 30px rgba(255, 170, 212, 0.12);
        }

        .contact-icon {
            width: 70px;
            height: 70px;
            background: linear-gradient(135deg, rgba(253, 213, 232, 0.3), rgba(255, 238, 245, 0.4));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 1.5rem;
            color: var(--image-pink);
            font-size: 1.8rem;
            border: 1px solid rgba(251, 182, 217, 0.5);
        }

        .contact-title {
            font-family: 'Playfair Display', serif;
            font-size: 1.4rem;
            color: var(--image-pink);
            margin-bottom: 0.8rem;
        }

        /* Footer */
        footer {
            padding: 3rem 0 2rem;
            margin-top: 3rem;
            background-color: rgba(255, 255, 255, 0.94);
            border-top: 1px solid rgba(251, 182, 217, 0.5);
        }

        .footer-content {
            text-align: center;
        }

        .footer-logo {
            font-family: 'Dancing Script', cursive;
            font-size: 2.5rem;
            color: var(--image-pink);
            margin-bottom: 1rem;
        }

        .footer-text {
            color: var(--soft-gray);
            font-size: 1rem;
            max-width: 600px;
            margin: 0 auto 2rem;
            line-height: 1.7;
        }

        .social-icons {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-bottom: 2rem;
        }

        .social-icon {
            width: 45px;
            height: 45px;
            background: linear-gradient(135deg, rgba(253, 213, 232, 0.3), rgba(255, 238, 245, 0.4));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--image-pink);
            font-size: 1.2rem;
            text-decoration: none;
            transition: all 0.3s ease;
            border: 1px solid rgba(251, 182, 217, 0.5);
        }

        .social-icon:hover {
            background: linear-gradient(to right, var(--image-pink), var(--dark-pink));
            color: white;
            transform: translateY(-5px);
            box-shadow: 0 8px 15px rgba(255, 170, 212, 0.2);
        }

        .copyright {
            color: var(--soft-gray);
            font-size: 0.9rem;
            margin-top: 1.5rem;
            padding-top: 1.5rem;
            border-top: 1px solid rgba(251, 182, 217, 0.5);
        }

        /* Responsive Design */
        @media (max-width: 992px) {
            .owners-section {
                flex-direction: column;
            }
            
            .owners-photo, .owners-info {
                min-width: 100%;
            }
        }

        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 1.2rem;
            }
            
            .logo {
                align-items: center;
                text-align: center;
            }
            
            .logo h1 {
                font-size: 2.5rem;
            }
            
            nav ul {
                gap: 1.5rem;
            }
            
            .hero-title {
                font-size: 2.8rem;
            }
            
            .hero-subtitle {
                font-size: 1.2rem;
            }
            
            .section-title {
                font-size: 2.2rem;
            }
            
            .features-grid, .prices-grid, .portfolio-grid, .contact-grid {
                grid-template-columns: 1fr;
            }
            
            .card, .booking-form {
                padding: 1.8rem;
            }
            
            .payment-options {
                flex-direction: column;
                align-items: center;
            }
            
            .payment-option {
                width: 100%;
                max-width: 250px;
            }
        }

        @media (max-width: 480px) {
            nav ul {
                flex-direction: column;
                align-items: center;
                gap: 1rem;
            }
            
            .logo h1 {
                font-size: 2.2rem;
            }
            
            .hero-title {
                font-size: 2.3rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
            
            .card, .booking-form, .owners-section {
                padding: 1.5rem;
            }
            
            .feature-card, .price-card, .contact-card {
                padding: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <h1>lashesbyxrili</h1>
                    <div class="logo-subtitle">Elegant Lash Studio</div>
                </div>
                <nav>
                    <ul>
                        <li><a href="#" class="nav-link active" data-page="home">Home & Policies</a></li>
                        <li><a href="#" class="nav-link" data-page="booking">Book Appointment</a></li>
                    </ul>
                </nav>
                <div class="header-cta">
                    <a href="#" class="booking-btn" data-page="booking">Book Now</a>
                </div>
            </div>
        </div>
    </header>

    <main class="main-content">
        <div class="container">
            <!-- Home & Policies Page -->
            <div class="page active" id="home-page">
                <section class="hero">
                    <h2 class="hero-title">Enhance Your Natural Beauty</h2>
                    <p class="hero-subtitle">Professional lash artistry in the comfort of our New Haven studio</p>
                    <div class="hero-decoration">
                        <div class="decoration-line"></div>
                        <i class="fas fa-star decoration-icon"></i>
                        <div class="decoration-line"></div>
                    </div>
                </section>

                <section class="welcome-section">
                    <div class="card">
                        <h3 class="section-title">Welcome</h3>
                        <p class="welcome-text">At lashesbyxrili, we believe that beauty lies in enhancing what you already have. Our home-based studio in New Haven, CT offers a personalized, comfortable experience where we create elegant lash sets that complement your unique features.</p>
                        
                        <div class="highlight-box">
                            <p class="highlight-text">"Currently offering beautiful black lash sets only - because classic is always in style"</p>
                        </div>
                        
                        <p class="welcome-text">Run by two passionate artists, we've perfected the art of creating lashes that look natural yet elevate your entire appearance. Each appointment is a relaxing experience tailored just for you.</p>
                    </div>
                </section>

                <section class="features-grid">
                    <div class="feature-card">
                        <div class="feature-icon">
                            <i class="fas fa-home"></i>
                        </div>
                        <h3 class="feature-title">Home Studio</h3>
                        <p>Experience personalized service in our comfortable, private studio located in New Haven, CT. A tranquil space designed for your relaxation.</p>
                    </div>
                    
                    <div class="feature-card">
                        <div class="feature-icon">
                            <i class="fas fa-users"></i>
                        </div>
                        <h3 class="feature-title">Dual Expertise</h3>
                        <p>Our studio is co-run by @wOr1al and @sweetestgirlyok, combining their skills to deliver exceptional results for every client.</p>
                    </div>
                    
                    <div class="feature-card">
                        <div class="feature-icon">
                            <i class="fas fa-heart"></i>
                        </div>
                        <h3 class="feature-title">Personalized Care</h3>
                        <p>Every lash set is customized to your eye shape, lifestyle, and personal style for a look that feels authentically you.</p>
                    </div>
                </section>

                <section class="owners-section">
                    <div class="owners-photo">
                        <img src="https://www.dropbox.com/scl/fi/3y8un450gw4b2gr464lxn/IMG_7423.jpeg?rlkey=gcztgl73shj8hciew3lbga8qg&st=7evqndjl&dl=1" alt="Owners of lashesbyxrili">
                    </div>
                    <div class="owners-info">
                        <h3>Meet Your Artists</h3>
                        <p>lashesbyxrili is a passion project brought to life by two talented friends: <strong>@wOr1al</strong> and <strong>@sweetestgirlyok</strong>. With complementary skills and a shared vision for beauty, we've created a studio where every client feels special and leaves feeling more confident.</p>
                        <p>We specialize in creating soft, elegant lash sets that enhance rather than overpower. Our approach focuses on precision, cleanliness, and creating a relaxing experience from start to finish.</p>
                        <a href="https://instagram.com/lashesbyxrili" target="_blank" class="instagram-handle">
                            <i class="fab fa-instagram"></i>
                            <span>@lashesbyxrili</span>
                        </a>
                    </div>
                </section>

                <section class="portfolio-section">
                    <h3 class="section-title">Our Work</h3>
                    <div class="portfolio-grid">
                        <div class="portfolio-item">
                            <img src="https://www.dropbox.com/scl/fi/gglztiejwzt4ftech3cnz/IMG_7426.jpeg?rlkey=x1ei1b7pxvfclok45go1vc59z&st=9e0jjjv6&dl=1" alt="Lash client result">
                            <div class="portfolio-overlay">
                                <p>Cat Eye Set</p>
                            </div>
                        </div>
                        <div class="portfolio-item">
                            <img src="https://i.postimg.cc/tCsrpT11/IMG-7425.jpg" alt="Lash client before and after">
                            <div class="portfolio-overlay">
                                <p>Natural Set</p>
                            </div>
                        </div>
                    </div>
                </section>

                <section class="prices-section">
                    <h3 class="section-title">Our Services</h3>
                    
                    <div class="color-notice">
                        <h4><i class="fas fa-palette"></i> Color Availability</h4>
                        <p>We currently specialize in beautiful black lash sets only. Black lashes provide the perfect contrast and definition for a classic, elegant look that suits every eye color and skin tone.</p>
                    </div>
                    
                    <div class="prices-grid">
                        <div class="price-card">
                            <h4 class="price-title">REGULAR SET</h4>
                            <div class="price-amount">$15</div>
                            <p class="price-details">+ $5 deposit required</p>
                            <p>Classic, beautiful black lash set perfect for everyday wear</p>
                            <p class="price-note">Our most popular choice</p>
                        </div>
                        
                        <div class="price-card">
                            <h4 class="price-title">CAT EYE SET</h4>
                            <div class="price-amount">$20</div>
                            <p class="price-details">+ $5 deposit required</p>
                            <p>Dramatic winged effect with black lashes that elongate and lift the eyes</p>
                            <p class="price-note">For a bold, glamorous look</p>
                        </div>
                        
                        <div class="price-card">
                            <h4 class="price-title">NATURAL SET</h4>
                            <div class="price-amount">$20</div>
                            <p class="price-details">+ $5 deposit required</p>
                            <p>Soft, subtle enhancement with black lashes for a barely-there effect</p>
                            <p class="price-note">Perfect for a minimal, everyday look</p>
                        </div>
                        
                        <div class="price-card">
                            <h4 class="price-title">WET SET</h4>
                            <div class="price-amount">$20</div>
                            <p class="price-details">+ $5 deposit required</p>
                            <p>Glossy, shiny finish with black lashes that create a wet look effect</p>
                            <p class="price-note">Trendy and eye-catching</p>
                        </div>
                    </div>
                    
                    <div class="card" style="text-align: center; margin-top: 2rem;">
                        <h4 style="font-family: 'Playfair Display', serif; color: var(--image-pink); font-size: 1.5rem; margin-bottom: 1rem;">Additional Service</h4>
                        <p style="font-size: 1.3rem; font-weight: 600; color: var(--text-dark); font-family: 'Montserrat', sans-serif;">LAYERING YOUR LASH: <span style="color: var(--image-pink);">$1</span></p>
                        <p style="margin-top: 0.5rem; color: var(--soft-gray);">Add dimension and fullness to your black lash set</p>
                    </div>
                </section>

                <section class="policy-section">
                    <h3 class="section-title">Our Policies</h3>
                    
                    <div class="card">
                        <ul class="policy-list">
                            <li class="policy-item">
                                <i class="fas fa-check-circle policy-icon"></i>
                                <div>
                                    <strong>Deposit Required</strong>
                                    <p>A $5 deposit is required to secure all appointments and will be applied to your total service cost. This deposit is non-refundable but can be transferred with 24 hours notice.</p>
                                </div>
                            </li>
                            <li class="policy-item">
                                <i class="fas fa-check-circle policy-icon"></i>
                                <div>
                                    <strong>Preparation</strong>
                                    <p>Please arrive with completely clean lashes free of any glue, mascara, or makeup. This ensures the best adhesion and longevity of your lash set.</p>
                                </div>
                            </li>
                            <li class="policy-item">
                                <i class="fas fa-check-circle policy-icon"></i>
                                <div>
                                    <strong>Payment Methods</strong>
                                    <p>We accept Cash, Cash App, and Apple Pay. Our lash clusters are priced at $10-15 and $15-20. The $5 deposit is required when booking.</p>
                                </div>
                            </li>
                            <li class="policy-item">
                                <i class="fas fa-check-circle policy-icon"></i>
                                <div>
                                    <strong>Booking Process</strong>
                                    <p>Please DM us on Instagram or use the booking form on our website to schedule your appointment. We'll confirm your appointment and provide deposit instructions.</p>
                                </div>
                            </li>
                            <li class="policy-item">
                                <i class="fas fa-check-circle policy-icon"></i>
                                <div>
                                    <strong>Photos</strong>
                                    <p>We may ask to take photos of your lashes after service for our portfolio, but only with your explicit permission. Your comfort and privacy are our priority.</p>
                                </div>
                            </li>
                            <li class="policy-item">
                                <i class="fas fa-check-circle policy-icon"></i>
                                <div>
                                    <strong>Special Requests</strong>
                                    <p>If you have any special requests, allergies, or questions, please let us know before your appointment so we can prepare and ensure your complete satisfaction.</p>
                                </div>
                            </li>
                        </ul>
                    </div>
                </section>

                <section class="contact-section">
                    <h3 class="section-title">Connect With Us</h3>
                    <div class="contact-grid">
                        <div class="contact-card">
                            <div class="contact-icon">
                                <i class="fab fa-instagram"></i>
                            </div>
                            <h4 class="contact-title">Instagram</h4>
                            <p>@lashesbyxrili</p>
                            <p style="font-size: 0.9rem; color: var(--soft-gray); margin-top: 0.5rem;">DM to book your appointment</p>
                        </div>
                        
                        <div class="contact-card">
                            <div class="contact-icon">
                                <i class="fas fa-envelope"></i>
                            </div>
                            <h4 class="contact-title">Email</h4>
                            <p>miharasvxma@gmail.com</p>
                            <p style="font-size: 0.9rem; color: var(--soft-gray); margin-top: 0.5rem;">For inquiries and questions</p>
                        </div>
                        
                        <div class="contact-card">
                            <div class="contact-icon">
                                <i class="fas fa-map-marker-alt"></i>
                            </div>
                            <h4 class="contact-title">Location</h4>
                            <p>New Haven, CT</p>
                            <p style="font-size: 0.9rem; color: var(--soft-gray); margin-top: 0.5rem;">Home Based Studio</p>
                        </div>
                    </div>
                </section>
            </div>

            <!-- Booking Page (Standalone) with Getform Integration -->
            <div class="page" id="booking-page">
                <section class="booking-section">
                    <div class="hero">
                        <h2 class="hero-title">Book Your Appointment</h2>
                        <p class="hero-subtitle">Secure your spot with a $5 deposit applied to your service total</p>
                        <div class="hero-decoration">
                            <div class="decoration-line"></div>
                            <i class="fas fa-calendar-alt decoration-icon"></i>
                            <div class="decoration-line"></div>
                        </div>
                    </div>
                    
                    <div class="booking-form">
                        <h3 class="form-title">Reservation Request</h3>
                        <p class="form-intro">Please fill out this form completely. We'll contact you within 24 hours to confirm your appointment details and provide deposit payment instructions.</p>
                        
                        <!-- Getform Integration - Form submission will go to your email -->
                        <form id="bookingForm" action="https://getform.io/f/apjxjdga" method="POST" enctype="multipart/form-data">
                            <input type="hidden" name="_gotcha" style="display:none !important">
                            
                            <div class="form-group">
                                <label class="form-label" for="clientName">Full Name *</label>
                                <input type="text" id="clientName" name="name" class="form-control" required placeholder="Your full name">
                            </div>
                            
                            <div class="form-group">
                                <label class="form-label" for="clientPhone">Phone Number *</label>
                                <input type="tel" id="clientPhone" name="phone" class="form-control" required placeholder="Phone number for confirmation">
                            </div>
                            
                            <div class="form-group">
                                <label class="form-label" for="clientEmail">Email Address</label>
                                <input type="email" id="clientEmail" name="email" class="form-control" placeholder="Optional, for appointment reminders">
                            </div>
                            
                            <div class="form-group">
                                <label class="form-label" for="serviceType">Service Requested *</label>
                                <select id="serviceType" name="service" class="form-control" required>
                                    <option value="">Select your desired lash set</option>
                                    <option value="regular">Regular Set - $15 + $5 deposit</option>
                                    <option value="cat-eye">Cat Eye Set - $20 + $5 deposit</option>
                                    <option value="natural">Natural Set - $20 + $5 deposit</option>
                                    <option value="wet">Wet Set - $20 + $5 deposit</option>
                                </select>
                            </div>
                            
                            <div class="form-group">
                                <label class="form-label" for="preferredDate">Preferred Date *</label>
                                <input type="date" id="preferredDate" name="date" class="form-control" required>
                            </div>
                            
                            <div class="form-group">
                                <label class="form-label" for="preferredTime">Preferred Time</label>
                                <select id="preferredTime" name="time" class="form-control">
                                    <option value="">Flexible</option>
                                    <option value="morning">Morning (9am-12pm)</option>
                                    <option value="afternoon">Afternoon (12pm-4pm)</option>
                                    <option value="evening">Evening (4pm-7pm)</option>
                                </select>
                            </div>
                            
                            <div class="form-group">
                                <label class="form-label" for="specialRequests">Special Requests or Questions</label>
                                <textarea id="specialRequests" name="requests" class="form-control" placeholder="Please let us know about any special requests, concerns, or questions before your appointment..."></textarea>
                            </div>
                            
                            <div class="form-group">
                                <label class="form-label" for="howHeard">How did you hear about us?</label>
                                <select id="howHeard" name="referral" class="form-control">
                                    <option value="">Select one</option>
                                    <option value="instagram">Instagram</option>
                                    <option value="friend">Friend Referral</option>
                                    <option value="previous">Previous Client</option>
                                    <option value="other">Other</option>
                                </select>
                            </div>
                            
                            <!-- Payment Methods Section -->
                            <div class="payment-methods">
                                <h4 class="payment-title">Accepted Payment Methods</h4>
                                <p style="text-align: center; color: var(--soft-gray); margin-bottom: 1rem;">We accept the following payment methods for deposits and service payments:</p>
                                
                                <div class="payment-options">
                                    <div class="payment-option">
                                        <i class="fas fa-money-bill-wave payment-icon"></i>
                                        <span class="payment-name">Cash</span>
                                    </div>
                                    <div class="payment-option">
                                        <i class="fas fa-mobile-alt payment-icon"></i>
                                        <span class="payment-name">Cash App</span>
                                    </div>
                                    <div class="payment-option">
                                        <i class="fab fa-apple payment-icon"></i>
                                        <span class="payment-name">Apple Pay</span>
                                    </div>
                                </div>
                                
                                <p style="text-align: center; margin-top: 1.5rem; font-size: 0.9rem; color: var(--soft-gray);">
                                    <i class="fas fa-info-circle"></i> A $5 deposit is required to secure your booking and will be applied to your total service cost.
                                </p>
                            </div>
                            
                            <button type="submit" class="submit-btn">Submit Booking Request</button>
                        </form>
                        
                        <div class="form-footer">
                            <p><i class="fas fa-info-circle" style="margin-right: 5px;"></i> After submitting, you'll be redirected to a confirmation page. We'll contact you within 24 hours to confirm availability and provide deposit payment instructions.</p>
                            <p style="margin-top: 1rem; font-size: 0.85rem;">Need immediate assistance? DM us on Instagram @lashesbyxrili</p>
                        </div>
                    </div>
                </section>
            </div>
        </div>
    </main>

    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-logo">lashesbyxrili</div>
                <p class="footer-text">A home-based lash studio in New Haven, CT specializing in elegant black lash sets that enhance your natural beauty. Currently serving over 12 satisfied clients with personalized attention and care.</p>
                
                <div class="social-icons">
                    <a href="https://instagram.com/lashesbyxrili" target="_blank" class="social-icon">
                        <i class="fab fa-instagram"></i>
                    </a>
                    <a href="mailto:miharasvxma@gmail.com" class="social-icon">
                        <i class="fas fa-envelope"></i>
                    </a>
                </div>
                
                <div class="copyright">
                    <p>&copy; 2023 lashesbyxrili. All rights reserved.</p>
                    <p style="margin-top: 8px;">I dm to book 🍀 | She/Her | Home Based | New Haven, CT | Currently specializing in black lash sets</p>
                </div>
            </div>
        </div>
    </footer>

    <script>
        // Navigation between pages
        document.addEventListener('DOMContentLoaded', function() {
            const navLinks = document.querySelectorAll('.nav-link');
            const bookingBtn = document.querySelector('.booking-btn');
            const pages = document.querySelectorAll('.page');
            
            // Function to switch pages
            function switchPage(pageId) {
                // Remove active class from all links and pages
                navLinks.forEach(l => l.classList.remove('active'));
                pages.forEach(page => page.classList.remove('active'));
                
                // Add active class to correct link
                document.querySelector(`[data-page="${pageId}"]`).classList.add('active');
                
                // Show corresponding page
                document.getElementById(pageId + '-page').classList.add('active');
                
                // Scroll to top of page
                window.scrollTo({ top: 0, behavior: 'smooth' });
            }
            
            // Navigation links
            navLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    const pageId = this.getAttribute('data-page');
                    switchPage(pageId);
                });
            });
            
            // Booking button
            if (bookingBtn) {
                bookingBtn.addEventListener('click', function(e) {
                    e.preventDefault();
                    switchPage('booking');
                });
            }
            
            // Set default date for booking forms
            function setDefaultDate() {
                const dateInput = document.getElementById('preferredDate');
                if (dateInput) {
                    const today = new Date();
                    const futureDate = new Date();
                    futureDate.setDate(today.getDate() + 3);
                    const futureDateStr = futureDate.toISOString().split('T')[0];
                    dateInput.setAttribute('min', today.toISOString().split('T')[0]);
                    dateInput.value = futureDateStr;
                }
            }
            
            // Initialize date pickers
            setDefaultDate();
        });
    </script>
</body>
</html>
