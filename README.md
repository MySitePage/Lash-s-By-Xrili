
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>lashesbyxrili | Coming Soon</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;500;600;700&family=Poppins:wght@300;400;500&display=swap" rel="stylesheet">
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
            background: linear-gradient(135deg, var(--soft-pink) 0%, var(--light-pink) 100%);
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 20px;
            line-height: 1.6;
        }

        .container {
            max-width: 800px;
            width: 100%;
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            padding: 50px 40px;
            box-shadow: 0 20px 50px rgba(255, 170, 212, 0.15);
            border: 1px solid rgba(251, 182, 217, 0.4);
            margin: 20px 0;
            position: relative;
            overflow: hidden;
        }

        .container::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(to right, var(--image-pink), var(--dark-pink));
        }

        .logo {
            margin-bottom: 30px;
        }

        .logo h1 {
            font-family: 'Dancing Script', cursive;
            font-size: 3.5rem;
            font-weight: 700;
            color: var(--image-pink);
            letter-spacing: 1px;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.05);
            margin-bottom: 5px;
        }

        .logo-subtitle {
            font-size: 1.1rem;
            color: var(--soft-gray);
            letter-spacing: 2px;
            text-transform: uppercase;
            font-weight: 500;
        }

        .main-icon {
            font-size: 4rem;
            color: var(--image-pink);
            margin: 30px 0;
            background: linear-gradient(to right, var(--image-pink), var(--dark-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            display: inline-block;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }

        h2 {
            font-family: 'Dancing Script', cursive;
            font-size: 2.8rem;
            color: var(--image-pink);
            margin-bottom: 20px;
            line-height: 1.2;
        }

        .status-message {
            font-size: 1.2rem;
            color: var(--text-dark);
            margin-bottom: 25px;
            padding: 0 10px;
        }

        .notice-box {
            background: linear-gradient(135deg, rgba(253, 213, 232, 0.3), rgba(255, 238, 245, 0.4));
            border-radius: 15px;
            padding: 25px;
            margin: 30px 0;
            border: 1px solid rgba(251, 182, 217, 0.5);
            position: relative;
        }

        .notice-box h3 {
            font-family: 'Dancing Script', cursive;
            font-size: 1.8rem;
            color: var(--image-pink);
            margin-bottom: 15px;
        }

        .notice-box p {
            font-size: 1rem;
            color: var(--text-dark);
            margin-bottom: 10px;
        }

        .contact-info {
            margin: 30px 0;
            padding: 20px;
        }

        .contact-info h3 {
            font-family: 'Dancing Script', cursive;
            font-size: 2rem;
            color: var(--image-pink);
            margin-bottom: 20px;
        }

        .contact-method {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
            margin: 15px 0;
            padding: 12px 20px;
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 12px;
            border: 1px solid rgba(251, 182, 217, 0.5);
            transition: all 0.3s ease;
            max-width: 400px;
            margin-left: auto;
            margin-right: auto;
        }

        .contact-method:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(255, 170, 212, 0.1);
        }

        .contact-icon {
            color: var(--image-pink);
            font-size: 1.5rem;
            width: 40px;
            text-align: center;
        }

        .contact-details {
            text-align: left;
            flex: 1;
        }

        .contact-details strong {
            display: block;
            color: var(--text-dark);
            margin-bottom: 3px;
        }

        .contact-details span {
            font-size: 0.9rem;
            color: var(--soft-gray);
        }

        .countdown {
            margin: 40px 0;
            padding: 25px;
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 15px;
            border: 1px solid rgba(251, 182, 217, 0.5);
        }

        .countdown h3 {
            font-family: 'Dancing Script', cursive;
            font-size: 2rem;
            color: var(--image-pink);
            margin-bottom: 20px;
        }

        .countdown-timer {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }

        .time-unit {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .time-value {
            width: 80px;
            height: 80px;
            background: linear-gradient(to right, var(--image-pink), var(--dark-pink));
            color: white;
            font-size: 2.2rem;
            font-weight: 700;
            border-radius: 12px;
            display: flex;
            justify-content: center;
            align-items: center;
            margin-bottom: 8px;
            box-shadow: 0 5px 15px rgba(255, 170, 212, 0.2);
        }

        .time-label {
            font-size: 0.9rem;
            color: var(--soft-gray);
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .social-icons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 30px 0;
        }

        .social-icon {
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, rgba(253, 213, 232, 0.3), rgba(255, 238, 245, 0.4));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--image-pink);
            font-size: 1.4rem;
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

        .footer {
            margin-top: 30px;
            color: var(--soft-gray);
            font-size: 0.9rem;
            max-width: 800px;
            width: 100%;
            padding-top: 20px;
            border-top: 1px solid rgba(251, 182, 217, 0.5);
        }

        .highlight {
            color: var(--image-pink);
            font-weight: 600;
        }

        /* Responsive styles */
        @media (max-width: 768px) {
            .container {
                padding: 40px 25px;
            }
            
            .logo h1 {
                font-size: 2.8rem;
            }
            
            h2 {
                font-size: 2.2rem;
            }
            
            .countdown-timer {
                gap: 10px;
            }
            
            .time-value {
                width: 70px;
                height: 70px;
                font-size: 1.8rem;
            }
        }

        @media (max-width: 480px) {
            .container {
                padding: 30px 20px;
            }
            
            .logo h1 {
                font-size: 2.3rem;
            }
            
            h2 {
                font-size: 1.8rem;
            }
            
            .countdown-timer {
                flex-wrap: wrap;
                gap: 15px;
            }
            
            .time-value {
                width: 65px;
                height: 65px;
                font-size: 1.6rem;
            }
            
            .contact-method {
                flex-direction: column;
                text-align: center;
                padding: 15px;
            }
            
            .contact-details {
                text-align: center;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="logo">
            <h1>lashesbyxrili</h1>
            <div class="logo-subtitle">Elegant Lash Studio</div>
        </div>
        
        <div class="main-icon">
            <i class="fas fa-hourglass-half"></i>
        </div>
        
        <h2>Our Website is Coming Soon</h2>
        
        <p class="status-message">
            We're working hard to bring you a beautiful online experience. 
            <span class="highlight">Please check back soon!</span>
        </p>
        
        <div class="notice-box">
            <h3>Important Notice</h3>
            <p><i class="fas fa-info-circle" style="color: var(--image-pink); margin-right: 8px;"></i> 
                The full website design is complete and ready to launch. 
                We're awaiting final approvals to make it live.
            </p>
            <p><i class="fas fa-calendar-alt" style="color: var(--image-pink); margin-right: 8px;"></i> 
                Original launch date: <span class="highlight">6 days ago</span>
            </p>
        </div>
        
        <div class="contact-info">
            <h3>Contact Us</h3>
            
            <div class="contact-method">
                <div class="contact-icon">
                    <i class="fab fa-instagram"></i>
                </div>
                <div class="contact-details">
                    <strong>Instagram</strong>
                    <span>@lashesbyxrili</span>
                </div>
            </div>
            
            <div class="contact-method">
                <div class="contact-icon">
                    <i class="fas fa-envelope"></i>
                </div>
                <div class="contact-details">
                    <strong>Email</strong>
                    <span>londonpear12.34@gmail.com</span>
                </div>
            </div>
            
            <div class="contact-method">
                <div class="contact-icon">
                    <i class="fas fa-map-marker-alt"></i>
                </div>
                <div class="contact-details">
                    <strong>Location</strong>
                    <span>New Haven, CT • Home Based Studio</span>
                </div>
            </div>
        </div>
        
        <div class="countdown">
            <h3>Expected Launch</h3>
            <p>We expect to launch the full website within the next few days.</p>
            
            <div class="countdown-timer">
                <div class="time-unit">
                    <div class="time-value" id="days">--</div>
                    <div class="time-label">Days</div>
                </div>
                <div class="time-unit">
                    <div class="time-value" id="hours">--</div>
                    <div class="time-label">Hours</div>
                </div>
                <div class="time-unit">
                    <div class="time-value" id="minutes">--</div>
                    <div class="time-label">Minutes</div>
                </div>
                <div class="time-unit">
                    <div class="time-value" id="seconds">--</div>
                    <div class="time-label">Seconds</div>
                </div>
            </div>
        </div>
        
        <div class="social-icons">
            <a href="https://instagram.com/lashesbyxrili" target="_blank" class="social-icon">
                <i class="fab fa-instagram"></i>
            </a>
            <a href="mailto:londonpear12.34@gmail.com" class="social-icon">
                <i class="fas fa-envelope"></i>
            </a>
        </div>
    </div>
    
    <div class="footer">
        <p>&copy; 2023 lashesbyxrili. Website design completed. Launch pending.</p>
        <p style="margin-top: 10px;">I dm to book 🍀 | She/Her | Home Based | New Haven, CT</p>
    </div>

    <script>
        // Countdown timer - set to 7 days from original deadline
        function updateCountdown() {
            // Set the countdown date (7 days from original deadline)
            const countdownDate = new Date();
            countdownDate.setDate(countdownDate.getDate() + 7);
            
            const now = new Date().getTime();
            const distance = countdownDate - now;
            
            if (distance < 0) {
                // If countdown is over, reset to 1 day
                document.getElementById("days").innerHTML = "00";
                document.getElementById("hours").innerHTML = "00";
                document.getElementById("minutes").innerHTML = "00";
                document.getElementById("seconds").innerHTML = "00";
                return;
            }
            
            const days = Math.floor(distance / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);
            
            document.getElementById("days").innerHTML = days.toString().padStart(2, '0');
            document.getElementById("hours").innerHTML = hours.toString().padStart(2, '0');
            document.getElementById("minutes").innerHTML = minutes.toString().padStart(2, '0');
            document.getElementById("seconds").innerHTML = seconds.toString().padStart(2, '0');
        }
        
        // Update countdown every second
        updateCountdown();
        setInterval(updateCountdown, 1000);
        
        // Add a subtle animation to the notice box
        document.addEventListener('DOMContentLoaded', function() {
            const noticeBox = document.querySelector('.notice-box');
            noticeBox.style.transform = 'translateY(0)';
            noticeBox.style.opacity = '1';
            
            // Initial state for animation
            noticeBox.style.transform = 'translateY(20px)';
            noticeBox.style.opacity = '0';
            noticeBox.style.transition = 'transform 0.5s ease, opacity 0.5s ease';
            
            setTimeout(() => {
                noticeBox.style.transform = 'translateY(0)';
                noticeBox.style.opacity = '1';
            }, 300);
        });
    </script>
</body>
</html>
