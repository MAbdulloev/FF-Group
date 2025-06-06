<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FF Group - Фулфилмент для продавцов маркетплейсов</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700;800&family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #1a3b6c;
            --secondary: #ff6b00;
            --accent: #2ecc71;
            --light: #f5f7fa;
            --dark: #2c3e50;
            --gray: #7f8c8d;
            --transition: all 0.3s ease;
            --shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Roboto', sans-serif;
            color: var(--dark);
            line-height: 1.6;
            background-color: #ffffff;
            overflow-x: hidden;
        }
        
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Montserrat', sans-serif;
            font-weight: 700;
            line-height: 1.2;
            margin-bottom: 20px;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--secondary);
            color: white;
            padding: 14px 32px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: var(--transition);
            border: none;
            cursor: pointer;
            font-size: 16px;
            box-shadow: var(--shadow);
        }
        
        .btn:hover {
            background-color: #e55a00;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(255, 107, 0, 0.3);
        }
        
        .btn-outline {
            background: transparent;
            border: 2px solid var(--secondary);
            color: var(--secondary);
            box-shadow: none;
        }
        
        .btn-outline:hover {
            background: var(--secondary);
            color: white;
        }
        
        section {
            padding: 100px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 60px;
            position: relative;
        }
        
        .section-title:after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--secondary);
            border-radius: 2px;
        }
        
        /* Header Styles */
        header {
            background-color: white;
            box-shadow: 0 2px 15px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo-text {
            font-family: 'Montserrat', sans-serif;
            font-size: 28px;
            font-weight: 800;
            color: var(--primary);
        }
        
        .logo-highlight {
            color: var(--secondary);
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 30px;
        }
        
        nav ul li a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: var(--transition);
            position: relative;
            padding: 5px 0;
        }
        
        nav ul li a:after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--secondary);
            transition: var(--transition);
        }
        
        nav ul li a:hover {
            color: var(--secondary);
        }
        
        nav ul li a:hover:after {
            width: 100%;
        }
        
        .contact-info {
            display: flex;
            align-items: center;
        }
        
        .phone {
            font-weight: 600;
            color: var(--primary);
            margin-right: 20px;
            display: flex;
            align-items: center;
            white-space: nowrap;
        }
        
        .phone i {
            margin-right: 8px;
            color: var(--secondary);
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, rgba(26, 59, 108, 0.9) 0%, rgba(44, 62, 80, 0.9) 100%), url('https://images.unsplash.com/photo-1551836022-d5d88e9218df?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1920&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 200px 0 120px;
            text-align: center;
        }
        
        .hero-content {
            max-width: 900px;
            margin: 0 auto;
        }
        
        .hero h1 {
            font-size: 52px;
            margin-bottom: 25px;
            animation: fadeInDown 1s ease;
        }
        
        .hero p {
            font-size: 22px;
            margin-bottom: 40px;
            animation: fadeInUp 1s ease;
        }
        
        .hero-stats {
            display: flex;
            justify-content: center;
            gap: 40px;
            margin-top: 60px;
            flex-wrap: wrap;
        }
        
        .stat-item {
            background: rgba(255, 255, 255, 0.15);
            backdrop-filter: blur(10px);
            border-radius: 10px;
            padding: 25px;
            min-width: 200px;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .stat-number {
            font-size: 42px;
            font-weight: 800;
            margin-bottom: 10px;
            color: var(--secondary);
        }
        
        .stat-text {
            font-size: 18px;
        }
        
        /* Marketplace Section */
        .marketplace-section {
            background-color: var(--light);
            padding: 80px 0;
        }
        
        .marketplace-title {
            text-align: center;
            margin-bottom: 30px;
            font-size: 28px;
            color: var(--primary);
        }
        
        .marketplace-logos {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 40px;
            padding: 20px;
        }
        
        .marketplace-logo {
            height: 60px;
            opacity: 0.8;
            transition: var(--transition);
            filter: grayscale(100%);
        }
        
        .marketplace-logo:hover {
            opacity: 1;
            transform: translateY(-5px);
            filter: grayscale(0%);
        }
        
        /* Services Section */
        .services {
            background-color: white;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .service-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
            text-align: center;
            padding: 40px 30px;
            border: 1px solid rgba(0, 0, 0, 0.05);
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }
        
        .service-icon {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, var(--primary) 0%, var(--dark) 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 25px;
            color: white;
            font-size: 30px;
        }
        
        .service-card h3 {
            font-size: 24px;
            margin-bottom: 15px;
            color: var(--primary);
        }
        
        .service-card p {
            margin-bottom: 20px;
        }
        
        .service-highlight {
            background: rgba(255, 107, 0, 0.1);
            padding: 5px 15px;
            border-radius: 20px;
            display: inline-block;
            color: var(--secondary);
            font-weight: 600;
            font-size: 14px;
            margin-top: 10px;
        }
        
        /* Benefits Section */
        .benefits {
            background: linear-gradient(to bottom, #f8faff 0%, #ffffff 100%);
        }
        
        .benefits-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .benefit-card {
            display: flex;
            align-items: flex-start;
            padding: 30px;
            background: white;
            border-radius: 15px;
            box-shadow: var(--shadow);
            transition: var(--transition);
            border: 1px solid rgba(0, 0, 0, 0.05);
        }
        
        .benefit-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .benefit-icon {
            min-width: 70px;
            height: 70px;
            background: var(--light);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--secondary);
            font-size: 28px;
            margin-right: 25px;
        }
        
        .benefit-content h3 {
            margin-bottom: 15px;
            color: var(--primary);
        }
        
        /* Process Section */
        .process {
            background: linear-gradient(to right, var(--primary) 0%, var(--dark) 100%);
            color: white;
            position: relative;
            overflow: hidden;
        }
        
        .process:before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1519501025264-65ba15a82390?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1920&q=80');
            opacity: 0.1;
            background-size: cover;
            background-position: center;
        }
        
        .process-steps {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            position: relative;
            z-index: 2;
        }
        
        .step {
            flex: 0 0 calc(25% - 30px);
            text-align: center;
            padding: 30px;
            position: relative;
        }
        
        .step:not(:last-child):after {
            content: '';
            position: absolute;
            top: 50%;
            right: -30px;
            width: 60px;
            height: 2px;
            background: rgba(255, 255, 255, 0.3);
        }
        
        .step-number {
            width: 70px;
            height: 70px;
            background: var(--secondary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 28px;
            font-weight: 700;
            margin: 0 auto 25px;
            border: 3px solid rgba(255, 255, 255, 0.3);
        }
        
        .step h3 {
            margin-bottom: 15px;
            font-size: 22px;
        }
        
        /* Testimonials */
        .testimonials {
            background-color: white;
        }
        
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .testimonial-card {
            background: white;
            border-radius: 15px;
            padding: 30px;
            box-shadow: var(--shadow);
            border: 1px solid rgba(0, 0, 0, 0.05);
            position: relative;
        }
        
        .testimonial-card:before {
            content: '"';
            position: absolute;
            top: 20px;
            left: 20px;
            font-size: 80px;
            color: rgba(26, 59, 108, 0.1);
            font-family: serif;
            line-height: 1;
        }
        
        .testimonial-content {
            padding-top: 20px;
            margin-bottom: 20px;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
        }
        
        .author-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background-color: var(--primary);
            margin-right: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            font-size: 20px;
        }
        
        .author-info h4 {
            margin-bottom: 5px;
            font-size: 18px;
        }
        
        .author-role {
            color: var(--gray);
            font-size: 14px;
        }
        
        /* Contact Section */
        .contact {
            background: linear-gradient(to right, #f8faff 0%, #ffffff 100%);
        }
        
        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 50px;
        }
        
        .contact-info-box {
            background: white;
            border-radius: 15px;
            padding: 40px;
            box-shadow: var(--shadow);
            border: 1px solid rgba(0, 0, 0, 0.05);
        }
        
        .contact-info-box h3 {
            color: var(--primary);
            margin-bottom: 30px;
            position: relative;
            padding-bottom: 15px;
        }
        
        .contact-info-box h3:after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 3px;
            background: var(--secondary);
        }
        
        .contact-item {
            display: flex;
            margin-bottom: 30px;
            align-items: flex-start;
        }
        
        .contact-icon {
            min-width: 50px;
            height: 50px;
            background: var(--light);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--secondary);
            font-size: 20px;
            margin-right: 20px;
        }
        
        .contact-details h4 {
            font-size: 18px;
            margin-bottom: 8px;
        }
        
        .contact-form {
            background: white;
            border-radius: 15px;
            padding: 40px;
            box-shadow: var(--shadow);
            border: 1px solid rgba(0, 0, 0, 0.05);
        }
        
        .form-group {
            margin-bottom: 25px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 10px;
            font-weight: 500;
            color: var(--dark);
        }
        
        .form-control {
            width: 100%;
            padding: 15px 20px;
            border: 1px solid #e1e5eb;
            border-radius: 8px;
            font-family: 'Roboto', sans-serif;
            font-size: 16px;
            transition: var(--transition);
            background: #f9fbfd;
        }
        
        .form-control:focus {
            border-color: var(--secondary);
            outline: none;
            box-shadow: 0 0 0 3px rgba(255, 107, 0, 0.15);
            background: white;
        }
        
        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }
        
        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 80px 0 30px;
        }
        
        .footer-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 50px;
        }
        
        .footer-col h4 {
            font-size: 20px;
            margin-bottom: 25px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-col h4:after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 40px;
            height: 3px;
            background: var(--secondary);
        }
        
        .footer-col ul {
            list-style: none;
        }
        
        .footer-col ul li {
            margin-bottom: 15px;
        }
        
        .footer-col ul li a {
            color: #bdc3c7;
            text-decoration: none;
            transition: var(--transition);
        }
        
        .footer-col ul li a:hover {
            color: var(--secondary);
            padding-left: 5px;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-links a {
            width: 45px;
            height: 45px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            transition: var(--transition);
            font-size: 18px;
        }
        
        .social-links a:hover {
            background: var(--secondary);
            transform: translateY(-5px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #bdc3c7;
            font-size: 15px;
        }
        
        /* Responsive Styles */
        @media (max-width: 992px) {
            .step {
                flex: 0 0 calc(50% - 30px);
                margin-bottom: 40px;
            }
            
            .step:not(:last-child):after {
                display: none;
            }
        }
        
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 38px;
            }
            
            .hero p {
                font-size: 18px;
            }
            
            nav ul {
                display: none;
            }
            
            .menu-toggle {
                display: block;
            }
            
            .step {
                flex: 0 0 100%;
            }
            
            section {
                padding: 80px 0;
            }
        }
        
        @media (max-width: 576px) {
            section {
                padding: 60px 0;
            }
            
            .section-title {
                margin-bottom: 40px;
            }
            
            .contact-info {
                flex-direction: column;
                align-items: flex-start;
            }
            
            .phone {
                margin-bottom: 10px;
            }
            
            .hero-stats {
                flex-direction: column;
                align-items: center;
            }
            
            .stat-item {
                width: 100%;
                max-width: 300px;
            }
        }
        
        /* Animations */
        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .animate-on-scroll {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s ease, transform 0.6s ease;
        }
        
        .animate-on-scroll.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <div class="logo-text">FF <span class="logo-highlight">Group</span></div>
            </div>
            
            <nav>
                <ul>
                    <li><a href="#home">Главная</a></li>
                    <li><a href="#services">Услуги</a></li>
                    <li><a href="#benefits">Преимущества</a></li>
                    <li><a href="#process">Как это работает</a></li>
                    <li><a href="#contact">Контакты</a></li>
                </ul>
            </nav>
            
            <div class="contact-info">
                <div class="phone">
                    <i class="fas fa-phone-alt"></i>
                    <span>+7 (977) 424-20-78</span>
                </div>
                <a href="#contact" class="btn btn-outline">Заказать звонок</a>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container hero-content">
            <h1>Фулфилмент для продавцов маркетплейсов</h1>
            <p>Полный комплекс услуг по хранению, обработке и доставке товаров для Wildberries, Ozon, Яндекс.Маркет и других площадок. Увеличиваем продажи, снижаем расходы!</p>
            <a href="#contact" class="btn">Начать сотрудничество</a>
            
            <div class="hero-stats">
                <div class="stat-item animate-on-scroll">
                    <div class="stat-number">+47%</div>
                    <div class="stat-text">Рост продаж у клиентов</div>
                </div>
                <div class="stat-item animate-on-scroll">
                    <div class="stat-number">-35%</div>
                    <div class="stat-text">Снижение логистических издержек</div>
                </div>
                <div class="stat-item animate-on-scroll">
                    <div class="stat-number">99%</div>
                    <div class="stat-text">Заказов отправлены вовремя</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Marketplace Section -->
    <section class="marketplace-section">
        <div class="container">
            <h3 class="marketplace-title">Работаем со всеми популярными маркетплейсами</h3>
            <div class="marketplace-logos">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9a/Wildberries_logo.png/320px-Wildberries_logo.png" alt="Wildberries" class="marketplace-logo">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a0/Ozon_Logo_2020.svg/320px-Ozon_Logo_2020.svg.png" alt="Ozon" class="marketplace-logo">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/5d/Yandex_Market_icon.svg/320px-Yandex_Market_icon.svg.png" alt="Яндекс.Маркет" class="marketplace-logo">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/45/SberMarket_Logo.png/320px-SberMarket_Logo.png" alt="SberMarket" class="marketplace-logo">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/0f/Lamoda_logo.png/320px-Lamoda_logo.png" alt="Lamoda" class="marketplace-logo">
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section class="services" id="services">
        <div class="container">
            <h2 class="section-title">Наши услуги для продавцов</h2>
            <div class="services-grid">
                <div class="service-card animate-on-scroll">
                    <div class="service-icon">
                        <i class="fas fa-warehouse"></i>
                    </div>
                    <h3>Хранение товаров</h3>
                    <p>Современные складские помещения с контролем температуры и влажности. Индивидуальные условия для различных категорий товаров.</p>
                    <div class="service-highlight">Под требования маркетплейсов</div>
                </div>
                
                <div class="service-card animate-on-scroll">
                    <div class="service-icon">
                        <i class="fas fa-boxes"></i>
                    </div>
                    <h3>Приём и обработка заказов</h3>
                    <p>Автоматизированная система приёма и обработки заказов 24/7. Интеграция с вашей CRM или маркетплейсом.</p>
                    <div class="service-highlight">Скорость обработки 2-4 часа</div>
                </div>
                
                <div class="service-card animate-on-scroll">
                    <div class="service-icon">
                        <i class="fas fa-box-open"></i>
                    </div>
                    <h3>Упаковка и маркировка</h3>
                    <p>Профессиональная упаковка товаров по стандартам маркетплейсов. Печать этикеток и маркировка FBS/FBY.</p>
                    <div class="service-highlight">Соответствие требованиям WB, Ozon</div>
                </div>
                
                <div class="service-card animate-on-scroll">
                    <div class="service-icon">
                        <i class="fas fa-truck"></i>
                    </div>
                    <h3>Доставка по России и СНГ</h3>
                    <p>Оптимальные логистические решения. Доставка по всей России и странам СНГ с отслеживанием и уведомлениями.</p>
                    <div class="service-highlight">Снижение стоимости доставки до 30%</div>
                </div>
                
                <div class="service-card animate-on-scroll">
                    <div class="service-icon">
                        <i class="fas fa-undo-alt"></i>
                    </div>
                    <h3>Обработка возвратов</h3>
                    <p>Полный цикл работы с возвратами: прием, проверка, восстановление товарного вида, возврат на склад.</p>
                    <div class="service-highlight">Снижение потерь от возвратов</div>
                </div>
                
                <div class="service-card animate-on-scroll">
                    <div class="service-icon">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h3>Аналитика и отчетность</h3>
                    <p>Подробные отчеты по продажам, остаткам и движению товара. Рекомендации по оптимизации ассортимента.</p>
                    <div class="service-highlight">Онлайн-кабинет 24/7</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Benefits Section -->
    <section class="benefits" id="benefits">
        <div class="container">
            <h2 class="section-title">Почему выбирают FF Group</h2>
            <div class="benefits-grid">
                <div class="benefit-card animate-on-scroll">
                    <div class="benefit-icon">
                        <i class="fas fa-lock"></i>
                    </div>
                    <div class="benefit-content">
                        <h3>Безопасность и сохранность</h3>
                        <p>Современные системы безопасности, видеонаблюдение и страхование товаров. Контроль качества на всех этапах.</p>
                    </div>
                </div>
                
                <div class="benefit-card animate-on-scroll">
                    <div class="benefit-icon">
                        <i class="fas fa-bolt"></i>
                    </div>
                    <div class="benefit-content">
                        <h3>Скорость обработки</h3>
                        <p>Отправка заказов в день поступления. Среднее время обработки заказа - 2 часа. Ускоренная доставка до пунктов выдачи.</p>
                    </div>
                </div>
                
                <div class="benefit-card animate-on-scroll">
                    <div class="benefit-icon">
                        <i class="fas fa-ruble-sign"></i>
                    </div>
                    <div class="benefit-content">
                        <h3>Экономия до 40%</h3>
                        <p>Гибкая система тарифов без скрытых платежей. Снижение расходов на логистику, упаковку и хранение.</p>
                    </div>
                </div>
                
                <div class="benefit-card animate-on-scroll">
                    <div class="benefit-icon">
                        <i class="fas fa-headset"></i>
                    </div>
                    <div class="benefit-content">
                        <h3>Персональный менеджер</h3>
                        <p>Эксперт по работе с маркетплейсами, который знает особенности вашего бизнеса и всегда готов помочь.</p>
                    </div>
                </div>
                
                <div class="benefit-card animate-on-scroll">
                    <div class="benefit-icon">
                        <i class="fas fa-sync-alt"></i>
                    </div>
                    <div class="benefit-content">
                        <h3>Автоматизация процессов</h3>
                        <p>Интеграция с вашими каналами продаж. Автоматическое обновление остатков и статусов заказов.</p>
                    </div>
                </div>
                
                <div class="benefit-card animate-on-scroll">
                    <div class="benefit-icon">
                        <i class="fas fa-chart-pie"></i>
                    </div>
                    <div class="benefit-content">
                        <h3>Аналитика и оптимизация</h3>
                        <p>Отчеты по ключевым показателям. Рекомендации по улучшению карточек товаров и увеличению продаж.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Process Section -->
    <section class="process" id="process">
        <div class="container">
            <h2 class="section-title">Как это работает</h2>
            <div class="process-steps">
                <div class="step animate-on-scroll">
                    <div class="step-number">1</div>
                    <h3>Интеграция</h3>
                    <p>Подключаем ваш кабинет продавца к нашей системе</p>
                </div>
                
                <div class="step animate-on-scroll">
                    <div class="step-number">2</div>
                    <h3>Доставка товара</h3>
                    <p>Привозим товар на наш склад или принимаем вашу поставку</p>
                </div>
                
                <div class="step animate-on-scroll">
                    <div class="step-number">3</div>
                    <h3>Обработка заказов</h3>
                    <p>Мы принимаем заказы с маркетплейсов и отправляем их покупателям</p>
                </div>
                
                <div class="step animate-on-scroll">
                    <div class="step-number">4</div>
                    <h3>Вывод денег</h3>
                    <p>Вы получаете деньги от маркетплейса за вычетом нашей комиссии</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials -->
    <section class="testimonials">
        <div class="container">
            <h2 class="section-title">Отзывы наших клиентов</h2>
            <div class="testimonial-grid">
                <div class="testimonial-card animate-on-scroll">
                    <div class="testimonial-content">
                        <p>С FF Group мои продажи на Wildberries выросли на 60% за полгода. Логистика перестала быть головной болью, теперь я могу сосредоточиться на развитии бизнеса.</p>
                    </div>
                    <div class="testimonial-author">
                        <div class="author-avatar">ИП</div>
                        <div class="author-info">
                            <h4>Иван Петров</h4>
                            <div class="author-role">Продавец на WB, Озон</div>
                        </div>
                    </div>
                </div>
                
                <div class="testimonial-card animate-on-scroll">
                    <div class="testimonial-content">
                        <p>Отличный сервис! Особенно ценю скорость обработки заказов и работу с возвратами. Теперь все возвраты обрабатываются в 3 раза быстрее, что положительно сказывается на рейтинге.</p>
                    </div>
                    <div class="testimonial-author">
                        <div class="author-avatar">ОК</div>
                        <div class="author-info">
                            <h4>Ольга Козлова</h4>
                            <div class="author-role">Владелец бренда косметики</div>
                        </div>
                    </div>
                </div>
                
                <div class="testimonial-card animate-on-scroll">
                    <div class="testimonial-content">
                        <p>Работаем с FF Group больше года. За это время снизили расходы на логистику на 35%, а количество вовремя отправленных заказов достигло 99%. Рекомендую!</p>
                    </div>
                    <div class="testimonial-author">
                        <div class="author-avatar">СМ</div>
                        <div class="author-info">
                            <h4>Сергей Морозов</h4>
                            <div class="author-role">Директор интернет-магазина</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <h2 class="section-title">Наши контакты</h2>
            <div class="contact-container">
                <div class="contact-info-box animate-on-scroll">
                    <h3>Контактная информация</h3>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div class="contact-details">
                            <h4>Адрес склада</h4>
                            <p>Деревня Апаринки, дом 4А</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-phone-alt"></i>
                        </div>
                        <div class="contact-details">
                            <h4>Телефон</h4>
                            <p>+7 (977) 424-20-78</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div class="contact-details">
                            <h4>Email</h4>
                            <p>info@ff-group.ru</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-clock"></i>
                        </div>
                        <div class="contact-details">
                            <h4>Режим работы</h4>
                            <p>Пн-Пт: 9:00 - 18:00<br>Сб: 10:00 - 15:00<br>Вс: выходной</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-warehouse"></i>
                        </div>
                        <div class="contact-details">
                            <h4>Площадь склада</h4>
                            <p>5000 м² с возможностью расширения</p>
                        </div>
                    </div>
                </div>
                
                <div class="contact-form animate-on-scroll">
                    <h3>Рассчитайте стоимость услуг</h3>
                    <form id="requestForm">
                        <div class="form-group">
                            <label for="name">Ваше имя</label>
                            <input type="text" id="name" class="form-control" required placeholder="Иванов Иван">
                        </div>
                        
                        <div class="form-group">
                            <label for="phone">Телефон</label>
                            <input type="tel" id="phone" class="form-control" required placeholder="+7 (999) 999-99-99">
                        </div>
                        
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" class="form-control" required placeholder="email@example.com">
                        </div>
                        
                        <div class="form-group">
                            <label for="marketplace">Основной маркетплейс</label>
                            <select id="marketplace" class="form-control">
                                <option value="">Выберите маркетплейс</option>
                                <option value="wb">Wildberries</option>
                                <option value="ozon">Ozon</option>
                                <option value="ym">Яндекс.Маркет</option>
                                <option value="other">Другой</option>
                            </select>
                        </div>
                        
                        <div class="form-group">
                            <label for="message">Опишите ваш товар и объемы</label>
                            <textarea id="message" class="form-control" placeholder="Категория товара, среднее количество заказов в день, особенности хранения и т.д."></textarea>
                        </div>
                        
                        <button type="submit" class="btn">Получить расчет</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-container">
                <div class="footer-col">
                    <div class="logo-text" style="color: white; margin-bottom: 20px;">FF <span class="logo-highlight">Group</span></div>
                    <p>Профессиональные фулфилмент услуги для продавцов маркетплейсов. Мы заботимся о ваших товарах как о своих собственных.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-vk"></i></a>
                        <a href="#"><i class="fab fa-telegram"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
                
                <div class="footer-col">
                    <h4>Услуги</h4>
                    <ul>
                        <li><a href="#">Хранение товаров</a></li>
                        <li><a href="#">Обработка заказов</a></li>
                        <li><a href="#">Упаковка и маркировка</a></li>
                        <li><a href="#">Доставка по РФ и СНГ</a></li>
                        <li><a href="#">Работа с возвратами</a></li>
                    </ul>
                </div>
                
                <div class="footer-col">
                    <h4>Для маркетплейсов</h4>
                    <ul>
                        <li><a href="#">Wildberries</a></li>
                        <li><a href="#">Ozon</a></li>
                        <li><a href="#">Яндекс.Маркет</a></li>
                        <li><a href="#">SberMarket</a></li>
                        <li><a href="#">Lamoda</a></li>
                    </ul>
                </div>
                
                <div class="footer-col">
                    <h4>Контакты</h4>
                    <ul>
                        <li><i class="fas fa-map-marker-alt"></i> Деревня Апаринки, дом 4А</li>
                        <li><i class="fas fa-phone-alt"></i> +7 (977) 424-20-78</li>
                        <li><i class="fas fa-envelope"></i> info@ff-group.ru</li>
                        <li><i class="fas fa-clock"></i> Пн-Пт: 9:00 - 18:00</li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                &copy; 2023 FF Group. Все права защищены. ИНН 1234567890 ОГРН 1234567890123
            </div>
        </div>
    </footer>

    <script>
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
        
        // Form submission
        document.getElementById('requestForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // In a real application, you would send the form data to a server
            // Here we'll just show an alert
            alert('Спасибо за вашу заявку! Наш менеджер свяжется с вами в течение 15 минут для расчета стоимости услуг.');
            this.reset();
        });
        
        // Sticky header
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            header.classList.toggle('sticky', window.scrollY > 0);
        });
        
        // Animation on scroll
        function animateOnScroll() {
            const elements = document.querySelectorAll('.animate-on-scroll');
            
            elements.forEach(element => {
                const elementPosition = element.getBoundingClientRect().top;
                const screenPosition = window.innerHeight / 1.3;
                
                if (elementPosition < screenPosition) {
                    element.classList.add('visible');
                }
            });
        }
        
        window.addEventListener('scroll', animateOnScroll);
        window.addEventListener('load', animateOnScroll);
    </script>
</body>
</html>
