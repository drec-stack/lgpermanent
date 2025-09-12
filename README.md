<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Салон красоты LG Permanent - профессиональные услуги перманентного макияжа, тату, стрижек и депиляции в Высокой Горе">
    <meta name="keywords" content="салон красоты, перманентный макияж, тату, стрижки, депиляция, Высокая Гора">
    <meta name="author" content="LG Permanent">
    <meta property="og:title" content="LG Permanent - Салон красоты">
    <meta property="og:description" content="Профессиональные услуги красоты в Высокой Горе">
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://lgpermanent.ru">
    <title>LG Permanent - Салон красоты</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>💄</text></svg>">
    <script src="https://api-maps.yandex.ru/2.1/?apikey=0b34e566-9e52-458c-a6c5-8d23faf8e164&lang=ru_RU" type="text/javascript"></script>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #fef8fa;
            color: #333;
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Шапка сайта */
        header {
            background: linear-gradient(135deg, #ffcce6 0%, #e6ccff 100%);
            padding: 15px 0;
            box-shadow: 0 2px 15px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
            backdrop-filter: blur(10px);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            text-decoration: none;
            transition: transform 0.3s;
        }
        
        .logo:hover {
            transform: scale(1.05);
        }
        
        .logo-circle {
            width: 55px;
            height: 55px;
            background: linear-gradient(135deg, #d63384 0%, #6f42c1 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            color: white;
            font-weight: bold;
            font-size: 22px;
            box-shadow: 0 4px 12px rgba(214, 51, 132, 0.3);
        }
        
        .logo-text {
            font-size: 26px;
            font-weight: 800;
            color: #d63384;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
        }
        
        .logo-text span {
            color: #6f42c1;
        }
        
        /* Мобильное меню */
        .menu-toggle {
            display: none;
            flex-direction: column;
            justify-content: space-around;
            width: 35px;
            height: 30px;
            background: transparent;
            border: none;
            cursor: pointer;
            padding: 0;
            z-index: 1001;
        }
        
        .menu-toggle span {
            width: 100%;
            height: 3px;
            background: linear-gradient(135deg, #d63384 0%, #6f42c1 100%);
            border-radius: 3px;
            transition: all 0.3s ease;
        }
        
        nav ul {
            display: flex;
            list-style: none;
            gap: 25px;
        }
        
        nav ul li a {
            text-decoration: none;
            color: #495057;
            font-weight: 600;
            font-size: 16px;
            padding: 8px 15px;
            border-radius: 25px;
            transition: all 0.3s ease;
            position: relative;
        }
        
        nav ul li a:hover {
            color: #d63384;
            background: rgba(255, 255, 255, 0.2);
            transform: translateY(-2px);
        }
        
        nav ul li a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            width: 0;
            height: 2px;
            background: linear-gradient(135deg, #d63384 0%, #6f42c1 100%);
            transition: all 0.3s ease;
            transform: translateX(-50%);
        }
        
        nav ul li a:hover::after {
            width: 70%;
        }
        
        /* Герой секция */
        .hero {
            background: linear-gradient(135deg, rgba(255, 204, 230, 0.1) 0%, rgba(230, 204, 255, 0.1) 100%),
                        url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect width="100" height="100" fill="%23f8f9fa"/><path d="M0,0 L100,100" stroke="%23e9ecef" stroke-width="1"/></svg>');
            padding: 100px 0;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 100%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
            animation: float 6s ease-in-out infinite;
        }
        
        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            color: #d63384;
            margin-bottom: 25px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
            font-weight: 800;
            line-height: 1.2;
        }
        
        .hero p {
            font-size: 1.25rem;
            color: #6c757d;
            margin-bottom: 40px;
            line-height: 1.6;
            font-weight: 400;
        }
        
        .hero-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }
        
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            background: linear-gradient(135deg, #d63384 0%, #6f42c1 100%);
            color: white;
            padding: 15px 35px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 16px;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            box-shadow: 0 4px 15px rgba(214, 51, 132, 0.3);
            position: relative;
            overflow: hidden;
        }
        
        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
            transition: left 0.5s ease;
        }
        
        .btn:hover::before {
            left: 100%;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(214, 51, 132, 0.4);
        }
        
        .btn-vk {
            background: linear-gradient(135deg, #4a76a8 0%, #2a4d7a 100%);
            box-shadow: 0 4px 15px rgba(74, 118, 168, 0.3);
        }
        
        .btn-vk:hover {
            box-shadow: 0 8px 25px rgba(74, 118, 168, 0.4);
        }
        
        .btn-location {
            background: linear-gradient(135deg, #6f42c1 0%, #4a2d8a 100%);
            box-shadow: 0 4px 15px rgba(111, 66, 193, 0.3);
        }
        
        .btn-location:hover {
            box-shadow: 0 8px 25px rgba(111, 66, 193, 0.4);
        }
        
        /* Секция услуг */
        .services {
            padding: 100px 0;
            background: white;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 60px;
            color: #6f42c1;
            font-size: 2.5rem;
            font-weight: 700;
            position: relative;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: linear-gradient(135deg, #d63384 0%, #6f42c1 100%);
            border-radius: 2px;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
        }
        
        .service-card {
            background: linear-gradient(135deg, #ffffff 0%, #f8f9fa 100%);
            padding: 35px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.08);
            transition: all 0.3s ease;
            text-align: center;
            border: 1px solid rgba(214, 51, 132, 0.1);
            position: relative;
            overflow: hidden;
        }
        
        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(135deg, #d63384 0%, #6f42c1 100%);
            transform: scaleX(0);
            transition: transform 0.3s ease;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.12);
        }
        
        .service-card:hover::before {
            transform: scaleX(1);
        }
        
        .service-icon {
            font-size: 3rem;
            color: #d63384;
            margin-bottom: 25px;
            height: 80px;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
        }
        
        .service-card:hover .service-icon {
            transform: scale(1.1) rotate(5deg);
        }
        
        .service-card h3 {
            color: 6f42c1;
            margin-bottom: 20px;
            font-size: 1.5rem;
            font-weight: 600;
        }
        
        .service-card p {
            color: #6c757d;
            line-height: 1.6;
            margin-bottom: 20px;
            font-size: 15px;
        }
        
        .price {
            font-weight: 700;
            color: #d63384;
            font-size: 1.25rem;
            margin: 25px 0;
            display: block;
        }
        
        .btn-gallery {
            background: linear-gradient(135deg, #20c997 0%, #199d76 100%);
            padding: 12px 25px;
            font-size: 14px;
            box-shadow: 0 4px 15px rgba(32, 201, 151, 0.3);
            margin-top: 15px;
        }
        
        .btn-gallery:hover {
            box-shadow: 0 8px 25px rgba(32, 201, 151, 0.4);
        }
        
        /* Секция "О нас" */
        .about {
            padding: 100px 0;
            background: linear-gradient(135deg, #f9d5e5 0%, #d6eaf8 100%);
            position: relative;
        }
        
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }
        
        .about-text {
            padding-right: 30px;
        }
        
        .about-text p {
            font-size: 16px;
            line-height: 1.8;
            color: #495057;
            margin-bottom: 25px;
            text-align: justify;
        }
        
        .about-image {
            height: 450px;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
            background: linear-gradient(45deg, #ffcce6, #e6ccff);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: 700;
            font-size: 1.5rem;
            text-align: center;
            padding: 30px;
            position: relative;
        }
        
        .about-image::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(45deg, rgba(255,204,230,0.8), rgba(230,204,255,0.8));
        }
        
        .about-image span {
            position: relative;
            z-index: 2;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }
        
        /* Секция преимуществ */
        .benefits {
            padding: 100px 0;
            background: white;
        }
        
        .benefits-list {
            max-width: 900px;
            margin: 0 auto;
        }
        
        .benefit-item {
            display: grid;
            grid-template-columns: auto 1fr;
            gap: 30px;
            align-items: center;
            margin-bottom: 40px;
            padding: 35px;
            background: linear-gradient(135deg, #ffffff 0%, #f8f9fa 100%);
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.08);
            border: 1px solid rgba(214, 51, 132, 0.1);
            transition: transform 0.3s ease;
        }
        
        .benefit-item:hover {
            transform: translateX(10px);
        }
        
        .benefit-icon {
            width: 70px;
            height: 70px;
            background: linear-gradient(135deg, #d63384 0%, #6f42c1 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            color: white;
            box-shadow: 0 8px 20px rgba(214, 51, 132, 0.3);
        }
        
        .benefit-text h3 {
            color: #6f42c1;
            font-size: 1.5rem;
            margin-bottom: 15px;
            font-weight: 600;
        }
        
        .benefit-text p {
            color: #6c757d;
            line-height: 1.6;
            font-size: 15px;
        }
        
        /* Новые стили для системы отзывов */
        .testimonials-filter {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 15px;
            margin-bottom: 40px;
            padding: 0 20px;
        }
        
        .filter-btn {
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            border: 2px solid #dee2e6;
            color: #6c757d;
            padding: 12px 25px;
            border-radius: 25px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 600;
            font-size: 14px;
        }
        
        .filter-btn:hover {
            background: linear-gradient(135deg, #e9ecef 0%, #dee2e6 100%);
            transform: translateY(-2px);
        }
        
        .filter-btn.active {
            background: linear-gradient(135deg, #d63384 0%, #6f42c1 100%);
            color: white;
            border-color: #d63384;
            box-shadow: 0 4px 15px rgba(214, 51, 132, 0.3);
        }
        
        .testimonial-category {
            display: none;
            animation: fadeIn 0.5s ease;
        }
        
        .testimonial-category.active {
            display: grid;
        }
        
        .testimonial-card {
            background: white;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.08);
            position: relative;
            border-left: 4px solid #d63384;
            transition: all 0.3s ease;
        }
        
        .testimonial-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.15);
        }
        
        .testimonial-service {
            position: absolute;
            top: 15px;
            right: 15px;
            background: linear-gradient(135deg, #6f42c1 0%, #4a2d8a 100%);
            color: white;
            padding: 5px 12px;
            border-radius: 15px;
            font-size: 12px;
            font-weight: 600;
        }
        
        .testimonial-rating {
            color: #ffc107;
            margin-bottom: 15px;
        }
        
        .testimonial-text {
            font-style: italic;
            color: #495057;
            line-height: 1.6;
            margin-bottom: 20px;
            font-size: 15px;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .author-avatar {
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, #ffcce6 0%, #e6ccff 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            color: #6f42c1;
            font-size: 18px;
        }
        
        .author-info {
            flex: 1;
        }
        
        .author-name {
            font-weight: 700;
            color: #6f42c1;
            font-size: 16px;
        }
        
        .author-age {
            color: #6c757d;
            font-size: 14px;
        }
        
        .testimonial-date {
            color: #adb5bd;
            font-size: 12px;
            margin-top: 5px;
        }
        
        .no-reviews {
            text-align: center;
            padding: 60px 20px;
            color: #6c757d;
            font-style: italic;
            grid-column: 1 / -1;
        }
        
        .no-reviews i {
            font-size: 48px;
            color: #dee2e6;
            margin-bottom: 20px;
            display: block;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        /* Секция местоположения */
        .location {
            padding: 100px 0;
            background: white;
        }
        
        .location-content {
            text-align: center;
            max-width: 700px;
            margin: 0 auto 40px;
        }
        
        .location-content p {
            font-size: 16px;
            color: #6c757d;
            margin-bottom: 30px;
            line-height: 1.6;
        }
        
        .map-container {
            height: 450px;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
            border: 1px solid rgba(214, 51, 132, 0.1);
            position: relative;
        }
        
        #main-map {
            width: 100%;
            height: 100%;
        }
        
        .map-loading {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
            background: #f8f9fa;
            color: #6c757d;
            font-style: italic;
        }
        
        /* Футер */
        footer {
            background: linear-gradient(135deg, #2c3034 0%, #1a1d21 100%);
            color: white;
            padding: 70px 0 30px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 40px;
            margin-bottom: 50px;
        }
        
        .footer-section h3 {
            color: #d63384;
            margin-bottom: 25px;
            font-size: 1.5rem;
            font-weight: 600;
        }
        
        .footer-section p {
            margin-bottom: 15px;
            font-size: 15px;
            color: #adb5bd;
            display: flex;
            align-items: center;
            gap: 12px;
        }
        
        .footer-section i {
            color: #d63384;
            width: 20px;
        }
        
        .social-links {
            display: flex;
            gap: 20px;
            margin-top: 25px;
        }
        
        .social-links a {
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, #d63384 0%, #6f42c1 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 20px;
            transition: all 0.3s ease;
            text-decoration: none;
        }
        
        .social-links a:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(214, 51, 132, 0.4);
        }
        
        .footer-bottom {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid #495057;
            color: #adb5bd;
            font-size: 14px;
        }
        
        /* Модальные окна */
        .modal {
            display: none;
            position: fixed;
            z-index: 2000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.95);
            overflow-y: auto;
            backdrop-filter: blur(5px);
        }
        
        .modal-content {
            background: white;
            margin: 40px auto;
            padding: 40px;
            border-radius: 25px;
            width: 90%;
            max-width: 900px;
            position: relative;
            box-shadow: 0 25px 50px rgba(0,0,0,0.3);
            animation: modalSlideIn 0.3s ease;
        }
        
        .close {
            color: #aaa;
            position: absolute;
            top: 20px;
            right: 25px;
            font-size: 2rem;
            font-weight: bold;
            cursor: pointer;
            transition: color 0.3s ease;
            z-index: 2001;
        }
        
        .close:hover {
            color: #d63384;
        }
        
        .modal-map-container {
            height: 400px;
            border-radius: 15px;
            overflow: hidden;
            margin: 25px 0;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            position: relative;
        }
        
        #modal-map {
            width: 100%;
            height: 100%;
        }
        
        .modal-map-loading {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
            background: #f8f9fa;
            color: #6c757d;
            font-style: italic;
        }
        
        /* Галерея работ */
        .gallery-title {
            text-align: center;
            color: #6f42c1;
            margin-bottom: 35px;
            font-size: 2rem;
            font-weight: 600;
        }
        
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }
        
        .gallery-item {
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            height: 200px;
            background: linear-gradient(45deg, #ffcce6, #e6ccff);
            display: flex;
            align-items: center;
            justify-content: center;
            color: #6c757d;
            font-style: italic;
            cursor: pointer;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .gallery-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(45deg, rgba(255,204,230,0.8), rgba(230,204,255,0.8));
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        
        .gallery-item:hover::before {
            opacity: 1;
        }
        
        .gallery-item:hover {
            transform: scale(1.05);
            box-shadow: 0 15px 35px rgba(0,0,0,0.2);
        }
        
        .gallery-item span {
            position: relative;
            z-index: 2;
            text-align: center;
            padding: 20px;
        }
        
        .gallery-description {
            text-align: center;
            color: #6c757d;
            font-style: italic;
            font-size: 16px;
            margin-top: 25px;
        }
        
        /* Анимации */
        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(5deg); }
        }
        
        @keyframes modalSlideIn {
            from { transform: translateY(-50px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
        
        /* Стиль для загрузки */
        .loading {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(255, 255, 255, 0.9);
            z-index: 9999;
            justify-content: center;
            align-items: center;
            flex-direction: column;
        }
        
        .loading-spinner {
            width: 50px;
            height: 50px;
            border: 5px solid #f3f3f3;
            border-top: 5px solid #d63384;
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }
        
        .loading-text {
            margin-top: 20px;
            color: #6f42c1;
            font-size: 18px;
        }
        
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        /* Адаптивность */
        @media (max-width: 1200px) {
            .container {
                padding: 0 30px;
            }
            
            .hero h1 {
                font-size: 3rem;
            }
        }
        
        @media (max-width: 992px) {
            .about-content {
                grid-template-columns: 1fr;
                gap: 40px;
            }
            
            .about-text {
                padding-right: 0;
                order: 2;
            }
            
            .about-image {
                order: 1;
                height: 350px;
            }
            
            .services-grid {
                grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            }
            
            .testimonial-grid {
                grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            }
        }
        
        @media (max-width: 768px) {
            .menu-toggle {
                display: flex;
            }
            
            nav {
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background: linear-gradient(135deg, #ffcce6 0%, #e6ccff 100%);
                box-shadow: 0 5px 15px rgba(0,0,0,0.1);
                max-height: 0;
                overflow: hidden;
                transition: max-height 0.3s ease;
            }
            
            nav.active {
                max-height: 400px;
            }
            
            nav ul {
                flex-direction: column;
                padding: 20px;
                gap: 15px;
            }
            
            nav ul li a {
                display: block;
                text-align: center;
                padding: 15px;
                background: rgba(255, 255, 255, 0.2);
                border-radius: 10px;
            }
            
            .hero {
                padding: 80px 0;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .btn {
                width: 100%;
                max-width: 300px;
            }
            
            .section-title {
                font-size: 2rem;
            }
            
            .services-grid {
                grid-template-columns: 1fr;
            }
            
            .service-card {
                padding: 25px;
            }
            
            .benefit-item {
                grid-template-columns: 1fr;
                text-align: center;
                gap: 20px;
                padding: 25px;
            }
            
            .benefit-icon {
                margin: 0 auto;
            }
            
            .map-container {
                height: 350px;
            }
            
            .footer-content {
                grid-template-columns: 1fr;
                text-align: center;
            }
            
            .social-links {
                justify-content: center;
            }
            
            .modal-content {
                padding: 30px 20px;
                margin: 20px auto;
            }
            
            .modal-map-container {
                height: 300px;
            }
            
            .gallery-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            
            /* Адаптивность для новой системы отзывов */
            .testimonials-filter {
                gap: 10px;
            }
            
            .filter-btn {
                padding: 10px 20px;
                font-size: 13px;
            }
            
            .testimonial-card {
                padding: 20px;
            }
            
            .testimonial-service {
                position: static;
                margin-bottom: 15px;
                display: inline-block;
            }
            
            .testimonial-author {
                flex-direction: column;
                align-items: flex-start;
                gap: 10px;
            }
            
            .author-avatar {
                width: 40px;
                height: 40px;
                font-size: 16px;
            }
            
            /* Специальные стили для мобильных карт */
            .map-container, .modal-map-container {
                -webkit-overflow-scrolling: touch;
            }
            
            #main-map, #modal-map {
                touch-action: manipulation;
            }
        }
        
        @media (max-width: 480px) {
            .container {
                padding: 0 15px;
            }
            
            .logo-circle {
                width: 45px;
                height: 45px;
                font-size: 18px;
            }
            
            .logo-text {
                font-size: 22px;
            }
            
            .hero {
                padding: 60px 0;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .section-title {
                font-size: 1.8rem;
            }
            
            .service-card {
                padding: 20px;
            }
            
            .service-icon {
                font-size: 2.5rem;
                height: 60px;
            }
            
            .about-image {
                height: 250px;
                font-size: 1.2rem;
            }
            
            .testimonial-card {
                padding: 25px;
            }
            
            .map-container {
                height: 300px;
            }
            
            .modal-content {
                width: 95%;
                padding: 25px 15px;
            }
            
            .modal-map-container {
                height: 250px;
            }
            
            .gallery-grid {
                grid-template-columns: 1fr;
            }
            
            .gallery-item {
                height: 180px;
            }
            
            .footer-section h3 {
                font-size: 1.3rem;
            }
            
            /* Адаптивность для системы отзывов */
            .testimonials-filter {
                flex-direction: column;
                align-items: center;
            }
            
            .filter-btn {
                width: 100%;
                max-width: 250px;
                text-align: center;
            }
            
            .testimonial-grid {
                grid-template-columns: 1fr;
            }
        }
        
        /* Специальные стили для мобильных устройств */
        @media (max-width: 768px) and (orientation: landscape) {
            .map-container {
                height: 250px;
            }
            
            .modal-map-container {
                height: 250px;
            }
        }
    </style>
</head>
<body>
    <!-- Индикатор загрузки -->
    <div class="loading" id="loading">
        <div class="loading-spinner"></div>
        <div class="loading-text">Загрузка...</div>
    </div>

    <!-- Шапка сайта -->
    <header>
        <div class="container">
            <div class="header-content">
                <a href="#" class="logo">
                    <div class="logo-circle">LG</div>
                    <div class="logo-text">Permanent<span>Beauty</span></div>
                </a>
                <button class="menu-toggle" id="menuToggle">
                    <span></span>
                    <span></span>
                    <span></span>
                </button>
                <nav id="mainNav">
                    <ul>
                        <li><a href="#services">Услуги</a></li>
                        <li><a href="#about">О нас</a></li>
                        <li><a href="#benefits">Преимущества</a></li>
                        <li><a href="#testimonials">Отзывы</a></li>
                        <li><a href="#location">Местоположение</a></li>
                        <li><a href="#contact">Контакты</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- Герой секция -->
    <section class="hero">
        <div class="container hero-content">
            <h1>Салон красоты LG Permanent</h1>
            <p>Профессиональные услуги красоты для современных людей, ценящих качество и внимание к деталям</p>
            <div class="hero-buttons">
                <a href="https://vk.com/club221779829" class="btn btn-vk" target="_blank" rel="noopener noreferrer">
                    <i class="fab fa-vk"></i> Оставить заявку в ВК
                </a>
                <button class="btn btn-location" onclick="openLocationModal()">
                    <i class="fas fa-map-marker-alt"></i> Посмотреть на карте
                </button>
            </div>
        </div>
    </section>

    <!-- Секция услуг -->
    <section class="services" id="services">
        <div class="container">
            <h2 class="section-title">Наши услуги</h2>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon" onclick="openGallery('brows')">
                        <i class="fas fa-eye"></i>
                    </div>
                    <h3>Перманент бровей</h3>
                    <p>Идеальная форма бровей на 1-2 года. Коррекция и насыщение цветом</p>
                    <span class="price">от 5000 руб.</span>
                    <button class="btn btn-gallery" onclick="openGallery('brows')">
                        <i class="fas fa-images"></i> Примеры работ
                    </button>
                </div>
                
                <div class="service-card">
                    <div class="service-icon" onclick="openGallery('lashes')">
                        <i class="fas fa-eye"></i>
                    </div>
                    <h3>Перманент ресниц</h3>
                    <p>Эффект накрашенных ресниц 24/7. Подчеркивание естественной красоты глаз</p>
                    <span class="price">от 4000 руб.</span>
                    <button class="btn btn-gallery" onclick="openGallery('lashes')">
                        <i class="fas fa-images"></i> Примеры работ
                    </button>
                </div>
                
                <div class="service-card">
                    <div class="service-icon" onclick="openGallery('lips')">
                        <i class="fas fa-kiss-wink-heart"></i>
                    </div>
                    <h3>Перманент губ</h3>
                    <p>Коррекция контура, увеличение объема и равномерное заполнение цветом</p>
                    <span class="price">от 6000 руб.</span>
                    <button class="btn btn-gallery" onclick="openGallery('lips')">
                        <i class="fas fa-images"></i> Примеры работ
                    </button>
                </div>
                
                <div class="service-card">
                    <div class="service-icon" onclick="openGallery('tattoo')">
                        <i class="fas fa-pen-fancy"></i>
                    </div>
                    <h3>Тату</h3>
                    <p>Художественные татуировки любой сложности от профессиональных мастеров</p>
                    <span class="price">от 3000 руб.</span>
                    <button class="btn btn-gallery" onclick="openGallery('tattoo')">
                        <i class="fas fa-images"></i> Примеры работ
                    </button>
                </div>
                
                <div class="service-card">
                    <div class="service-icon" onclick="openGallery('haircut')">
                        <i class="fas fa-scissors"></i>
                    </div>
                    <h3>Стрижка мужская/женская</h3>
                    <p>Профессиональные стрижки с учетом особенностей ваших волос и структуры лица</p>
                    <span class="price">от 1000 руб.</span>
                    <button class="btn btn-gallery" onclick="openGallery('haircut')">
                        <i class="fas fa-images"></i> Примеры работ
                    </button>
                </div>
                
                <div class="service-card">
                    <div class="service-icon" onclick="openGallery('depilation')">
                        <i class="fas fa-fire"></i>
                    </div>
                    <h3>Лазерная депиляция</h3>
                    <p>Современные методы удаления нежелательных волос на всех участках тела</p>
                    <span class="price">от 2000 руб.</span>
                    <button class="btn btn-gallery" onclick="openGallery('depilation')">
                        <i class="fas fa-images"></i> Примеры работ
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Секция "О нас" -->
    <section class="about" id="about">
        <div class="container">
            <h2 class="section-title">О нашем салоне</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>Салон красоты LG Permanent — это место, где работают настоящие профессионалы, влюбленные в свое дело. Мы предлагаем широкий спектр услуг для женщин и мужчин, которые хотят выглядеть безупречно каждый день.</p>
                    <p>Наша команда состоит из сертифицированных мастеров с многолетним опытом работы. Мы регулярно повышаем квалификацию и следим за новейшими тенденциями в индустрии красоты.</p>
                    <p>Мы используем только качественные материалы и современное оборудование, чтобы обеспечить нашим клиентам максимальный комфорт и безопасность во время процедур.</p>
                </div>
                <div class="about-image">
                    <span>Салон красоты премиум-класса</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Секция преимуществ -->
    <section class="benefits" id="benefits">
        <div class="container">
            <h2 class="section-title">Почему выбирают нас</h2>
            <div class="benefits-list">
                <div class="benefit-item">
                    <div class="benefit-icon">
                        <i class="fas fa-award"></i>
                    </div>
                    <div class="benefit-text">
                        <h3>Высокое качество услуг</h3>
                        <p>Мы используем только профессиональные материалы и оборудование премиум-класса</p>
                    </div>
                </div>
                
                <div class="benefit-item">
                    <div class="benefit-icon">
                        <i class="fas fa-user-md"></i>
                    </div>
                    <div class="benefit-text">
                        <h3>Опытные мастера</h3>
                        <p>Наши специалисты имеют многолетний опыт и регулярно проходят обучение</p>
                    </div>
                </div>
                
                <div class="benefit-item">
                    <div class="benefit-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <div class="benefit-text">
                        <h3>Безопасность и стерильность</h3>
                        <p>Строгое соблюдение санитарных норм и использование одноразовых инструментов</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Секция отзывов -->
    <section class="testimonials" id="testimonials">
        <div class="container">
            <h2 class="section-title">Отзывы наших клиентов</h2>
            
            <!-- Фильтр по услугам -->
            <div class="testimonials-filter">
                <button class="filter-btn active" data-category="all">Все отзывы</button>
                <button class="filter-btn" data-category="brows">Брови</button>
                <button class="filter-btn" data-category="lashes">Ресницы</button>
                <button class="filter-btn" data-category="lips">Губы</button>
                <button class="filter-btn" data-category="tattoo">Тату</button>
                <button class="filter-btn" data-category="haircut">Стрижки</button>
                <button class="filter-btn" data-category="depilation">Депиляция</button>
            </div>
            
            <div class="testimonial-category active" id="all-reviews">
                <div class="testimonial-grid">
                    <!-- Отзывы будут подгружаться через JavaScript -->
                </div>
            </div>
            
            <!-- Отдельные категории отзывов -->
            <div class="testimonial-category" id="brows-reviews">
                <div class="testimonial-grid">
                    <!-- Отзывы на брови -->
                </div>
            </div>
            
            <div class="testimonial-category" id="lashes-reviews">
                <div class="testimonial-grid">
                    <!-- Отзывы на ресницы -->
                </div>
            </div>
            
            <div class="testimonial-category" id="lips-reviews">
                <div class="testimonial-grid">
                    <!-- Отзывы на губы -->
                </div>
            </div>
            
            <div class="testimonial-category" id="tattoo-reviews">
                <div class="testimonial-grid">
                    <!-- Отзывы на тату -->
                </div>
            </div>
            
            <div class="testimonial-category" id="haircut-reviews">
                <div class="testimonial-grid">
                    <!-- Отзывы на стрижки -->
                </div>
            </div>
            
            <div class="testimonial-category" id="depilation-reviews">
                <div class="testimonial-grid">
                    <!-- Отзывы на депиляцию -->
                </div>
            </div>
        </div>
    </section>

    <!-- Секция местоположения -->
    <section class="location" id="location">
        <div class="container">
            <h2 class="section-title">Мы находимся</h2>
            <div class="location-content">
                <p>Наш салон расположен в селе Высокая Гора, к нам легко добраться на любом транспорте</p>
                <button class="btn btn-location" onclick="openLocationModal()">
                    <i class="fas fa-map-marker-alt"></i> Посмотреть на карте
                </button>
            </div>
            <div class="map-container">
                <div class="map-loading" id="main-map-loading">Загрузка карты...</div>
                <div id="main-map"></div>
            </div>
        </div>
    </section>

    <!-- Футер -->
    <footer id="contact">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>Контакты</h3>
                    <p><i class="fas fa-phone"></i> +7 927 030-00-92</p>
                    <p><i class="fas fa-envelope"></i> info@lgpermanent.ru</p>
                    <p><i class="fas fa-map-marker-alt"></i> с. Высокая Гора, ул. Большая Красная, 156</p>
                </div>
                
                <div class="footer-section">
                    <h3>Часы работы</h3>
                    <p><i class="fas fa-clock"></i> Пн-Пт: 10:00 - 20:00</p>
                    <p><i class="fas fa-clock"></i> Сб: 11:00 - 18:00</p>
                    <p><i class="fas fa-clock"></i> Вс: выходной</p>
                </div>
                
                <div class="footer-section">
                    <h3>Мы в соцсетях</h3>
                    <p>Подписывайтесь на наши страницы чтобы быть в курсе акций и новостей</p>
                    <div class="social-links">
                        <a href="https://vk.com/club221779829" target="_blank" rel="noopener noreferrer"><i class="fab fa-vk"></i></a>
                        <a href="#" onclick="showComingSoon()"><i class="fab fa-instagram"></i></a>
                        <a href="#" onclick="showComingSoon()"><i class="fab fa-telegram"></i></a>
                        <a href="#" onclick="showComingSoon()"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
            </div>
            
            <div class="footer-bottom">
                <p>&copy; 2023 LG Permanent Beauty. Все права защищены.</p>
            </div>
        </div>
    </footer>

    <!-- Модальное окно с картой -->
    <div id="locationModal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('locationModal')">&times;</span>
            <h2 class="gallery-title">Мы находимся здесь</h2>
            <div class="modal-map-container">
                <div class="modal-map-loading" id="modal-map-loading">Загрузка карты...</div>
                <div id="modal-map"></div>
            </div>
            <p><i class="fas fa-map-marker-alt"></i> с. Высокая Гора, ул. Большая Красная, 156</p>
            <p><i class="fas fa-phone"></i> +7 927 030-00-92</p>
            <p><i class="fas fa-clock"></i> Пн-Пт: 10:00 - 20:00, Сб: 11:00 - 18:00</p>
            <div style="text-align: center; margin-top: 25px;">
                <a href="https://yandex.ru/maps/43/vysochayushchaya-gora/?ll=49.302000%2C55.863000&z=16" class="btn" target="_blank" rel="noopener noreferrer">
                    <i class="fas fa-external-link-alt"></i> Открыть в Яндекс.Картах
                </a>
            </div>
        </div>
    </div>

    <!-- Модальные окна галерей -->
    <div id="galleryModal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('galleryModal')">&times;</span>
            <h2 class="gallery-title" id="galleryTitle">Галерея работ</h2>
            <div class="gallery-grid" id="galleryContent">
                <!-- Контент галереи будет добавляться через JavaScript -->
            </div>
            <p class="gallery-description" id="galleryDescription"></p>
        </div>
    </div>

    <!-- Модальное окно "Скоро" -->
    <div id="comingSoonModal" class="modal">
        <div class="modal-content" style="text-align: center; max-width: 500px;">
            <span class="close" onclick="closeModal('comingSoonModal')">&times;</span>
            <h2 class="gallery-title">Скоро!</h2>
            <div style="font-size: 80px; margin: 30px 0;">🚧</div>
            <p>Данный раздел находится в разработке. Скоро здесь появится новая информация!</p>
            <button class="btn" onclick="closeModal('comingSoonModal')" style="margin-top: 20px;">
                Понятно
            </button>
        </div>
    </div>

    <script>
        // Инициализация карт
        let mainMap, modalMap;
        let isMobile = /Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent);
        
        // Точные координаты для села Высокая Гора, Татарстан
        const salonCoordinates = [55.917673, 49.312312];
        
        // Данные для галерей
        const galleryData = {
            brows: {
                title: "Перманент бровей - Примеры работ",
                description: "Идеальная форма и насыщенный цвет на 1-2 года",
                items: 6
            },
            lashes: {
                title: "Перманент ресниц - Примеры работ", 
                description: "Эффект накрашенных ресниц 24/7",
                items: 5
            },
            lips: {
                title: "Перманент губ - Примеры работ",
                description: "Коррекция контура и равномерное заполнение цветом",
                items: 4
            },
            tattoo: {
                title: "Тату - Примеры работ",
                description: "Художественные татуировки любой сложности",
                items: 6
            },
            haircut: {
                title: "Стрижки - Примеры работ", 
                description: "Профессиональные стрижки для женщин и мужчин",
                items: 5
            },
            depilation: {
                title: "Лазерная депиляция - Результаты",
                description: "Современные методы удаления нежелательных волос",
                items: 4
            }
        };

        // Данные отзывов
        const testimonialsData = {
            all: [
                {
                    id: 1,
                    service: "brows",
                    serviceName: "Перманент бровей",
                    rating: 5,
                    text: "Очень довольна результатом! Бровки выглядят естественно и аккуратно. Мастер учла все пожелания и дала подробные рекомендации по уходу.",
                    author: "Анна",
                    age: 32,
                    date: "15.12.2023",
                    avatar: "А"
                },
                {
                    id: 2,
                    service: "lips",
                    serviceName: "Перманент губ",
                    rating: 5,
                    text: "Делала перманент губ. Результат превзошел все ожидания! Цвет подобрали идеально под мой цветотип. Теперь экономлю кучу времени по утрам.",
                    author: "Мария",
                    age: 28,
                    date: "10.12.2023",
                    avatar: "М"
                },
                {
                    id: 3,
                    service: "haircut",
                    serviceName: "Стрижка",
                    rating: 5,
                    text: "Хожу в этот салон уже несколько лет. Всегда качественный сервис и приятная атмосфера. Особенно рекомендую мастера по стрижкам!",
                    author: "Дмитрий",
                    age: 35,
                    date: "08.12.2023",
                    avatar: "Д"
                },
                {
                    id: 4,
                    service: "depilation",
                    serviceName: "Депиляция",
                    rating: 4,
                    text: "Проходила курс лазерной депиляции. Результатом очень довольна! Безболезненно и эффективно. Специалисты внимательные и профессиональные.",
                    author: "Екатерина",
                    age: 29,
                    date: "05.12.2023",
                    avatar: "Е"
                },
                {
                    id: 5,
                    service: "tattoo",
                    serviceName: "Татуировка",
                    rating: 5,
                    text: "Сделала первую татуичку в этом салоне. Мастер - настоящий художник! Учтены все пожелания, работа выполнена аккуратно и профессионально.",
                    author: "Ольга",
                    age: 26,
                    date: "03.12.2023",
                    avatar: "О"
                },
                {
                    id: 6,
                    service: "lashes",
                    serviceName: "Перманент ресниц",
                    rating: 4,
                    text: "Эффект просто потрясающий! Просыпаюсь с красивыми ресницами, не нужно тратить время на тушь. Очень удобно для повседневной жизни.",
                    author: "Светлана",
                    age: 31,
                    date: "01.12.2023",
                    avatar: "С"
                }
            ],
            brows: [
                {
                    id: 1,
                    service: "brows",
                    serviceName: "Перманент бровей",
                    rating: 5,
                    text: "Очень довольна результатом! Бровки выглядят естественно и аккуратно. Мастер учла все пожелания и дала подробные рекомендации по уходу.",
                    author: "Анна",
                    age: 32,
                    date: "15.12.2023",
                    avatar: "А"
                },
                {
                    id: 7,
                    service: "brows",
                    serviceName: "Перманент бровей",
                    rating: 5,
                    text: "Делала коррекцию бровей. Мастер - волшебница! Подобрала идеальную форму и цвет. Теперь не представляю жизни без перманента.",
                    author: "Ирина",
                    age: 27,
                    date: "28.11.2023",
                    avatar: "И"
                },
                {
                    id: 8,
                    service: "brows",
                    serviceName: "Перманент бровей",
                    rating: 4,
                    text: "Хороший результат, брови смотрятся естественно. Процедура прошла комфортно, мастер все объяснила и показала.",
                    author: "Наталья",
                    age: 34,
                    date: "25.11.2023",
                    avatar: "Н"
                }
            ],
            lashes: [
                {
                    id: 6,
                    service: "lashes",
                    serviceName: "Перманент ресниц",
                    rating: 4,
                    text: "Эффект просто потрясающий! Просыпаюсь с красивыми ресницами, не нужно тратить время на тушь. Очень удобно для повседневной жизни.",
                    author: "Светлана",
                    age: 31,
                    date: "01.12.2023",
                    avatar: "С"
                },
                {
                    id: 9,
                    service: "lashes",
                    serviceName: "Перманент ресниц",
                    rating: 5,
                    text: "Обожаю свой новый взгляд! Ресницы выглядят натурально, но в то же время выразительно. Спасибо мастеру за ювелирную работу!",
                    author: "Виктория",
                    age: 25,
                    date: "20.11.2023",
                    avatar: "В"
                }
            ],
            lips: [
                {
                    id: 2,
                    service: "lips",
                    serviceName: "Перманент губ",
                    rating: 5,
                    text: "Делала перманент губ. Результат превзошел все ожидания! Цвет подобрали идеально под мой цветотип. Теперь экономлю кучу времени по утрам.",
                    author: "Мария",
                    age: 28,
                    date: "10.12.2023",
                    avatar: "М"
                },
                {
                    id: 10,
                    service: "lips",
                    serviceName: "Перманент губ",
                    rating: 5,
                    text: "Контур губ просто идеальный! Цвет насыщенный и естественный. Мастер настоящий профессионал своего дела.",
                    author: "Александра",
                    age: 30,
                    date: "18.11.2023",
                    avatar: "А"
                }
            ],
            tattoo: [
                {
                    id: 5,
                    service: "tattoo",
                    serviceName: "Татуировка",
                    rating: 5,
                    text: "Сделала первую татуировку в этом салоне. Мастер - настоящий художник! Учтены все пожелания, работа выполнена аккуратно и профессионально.",
                    author: "Ольга",
                    age: 26,
                    date: "03.12.2023",
                    avatar: "О"
                },
                {
                    id: 11,
                    service: "tattoo",
                    serviceName: "Татуировка",
                    rating: 5,
                    text: "Делал покрытие старой татуировки. Результат превзошел все ожидания! Качество работы на высшем уровне.",
                    author: "Алексей",
                    age: 33,
                    date: "15.11.2023",
                    avatar: "А"
                }
            ],
            haircut: [
                {
                    id: 3,
                    service: "haircut",
                    serviceName: "Стрижка",
                    rating: 5,
                    text: "Хожу в этот салон уже несколько лет. Всегда качественный сервис и приятная атмосфера. Особенно рекомендую мастера по стрижкам!",
                    author: "Дмитрий",
                    age: 35,
                    date: "08.12.2023",
                    avatar: "Д"
                },
                {
                    id: 12,
                    service: "haircut",
                    serviceName: "Стрижка",
                    rating: 4,
                    text: "Отличная стрижка! Мастер подобрала идеальную форму под тип лица. Волосы лежат прекрасно даже после домашней укладки.",
                    author: "Елена",
                    age: 29,
                    date: "12.11.2023",
                    avatar: "Е"
                }
            ],
            depilation: [
                {
                    id: 4,
                    service: "depilation",
                    serviceName: "Депиляция",
                    rating: 4,
                    text: "Проходила курс лазерной депиляции. Результатом очень довольна! Безболезненно и эффективно. Специалисты внимательные и профессиональные.",
                    author: "Екатерина",
                    age: 29,
                    date: "05.12.2023",
                    avatar: "Е"
                },
                {
                    id: 13,
                    service: "depilation",
                    serviceName: "Депиляция",
                    rating: 5,
                    text: "Лучшая лазерная депиляция в городе! Аппарат современный, процедура комфортная, результат заметен уже после первого сеанса.",
                    author: "Татьяна",
                    age: 31,
                    date: "10.11.2023",
                    avatar: "Т"
                }
            ]
        };

        // Управление мобильным меню
        const menuToggle = document.getElementById('menuToggle');
        const mainNav = document.getElementById('mainNav');
        
        menuToggle.addEventListener('click', function() {
            this.classList.toggle('active');
            mainNav.classList.toggle('active');
            document.body.style.overflow = mainNav.classList.contains('active') ? 'hidden' : '';
        });
        
        // Закрытие меню при клике на ссылку
        document.querySelectorAll('nav a').forEach(link => {
            link.addEventListener('click', function() {
                menuToggle.classList.remove('active');
                mainNav.classList.remove('active');
                document.body.style.overflow = '';
            });
        });

        // Функция для создания звезд рейтинга
        function createRatingStars(rating) {
            let stars = '';
            for (let i = 1; i <= 5; i++) {
                if (i <= rating) {
                    stars += '<i class="fas fa-star"></i>';
                } else {
                    stars += '<i class="far fa-star"></i>';
                }
            }
            return stars;
        }

        // Функция для отображения отзывов
        function renderTestimonials(category) {
            const testimonials = testimonialsData[category];
            const container = document.getElementById(`${category}-reviews`).querySelector('.testimonial-grid');
            
            container.innerHTML = '';
            
            if (testimonials.length === 0) {
                container.innerHTML = `
                    <div class="no-reviews">
                        <i class="fas fa-comment-slash"></i>
                        <p>Пока нет отзывов по этой услуге</p>
                        <p>Будьте первым, кто оставит отзыв!</p>
                    </div>
                `;
                return;
            }
            
            testimonials.forEach(testimonial => {
                const testimonialElement = document.createElement('div');
                testimonialElement.className = 'testimonial-card';
                testimonialElement.innerHTML = `
                    <div class="testimonial-service">${testimonial.serviceName}</div>
                    <div class="testimonial-rating">${createRatingStars(testimonial.rating)}</div>
                    <p class="testimonial-text">${testimonial.text}</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">${testimonial.avatar}</div>
                        <div class="author-info">
                            <div class="author-name">${testimonial.author}, ${testimonial.age} лет</div>
                            <div class="testimonial-date">${testimonial.date}</div>
                        </div>
                    </div>
                `;
                container.appendChild(testimonialElement);
            });
        }

        // Функция для переключения категорий
        function filterTestimonials(category) {
            // Убираем активный класс со всех кнопок
            document.querySelectorAll('.filter-btn').forEach(btn => {
                btn.classList.remove('active');
            });
            
            // Добавляем активный класс на выбранную кнопку
            document.querySelector(`.filter-btn[data-category="${category}"]`).classList.add('active');
            
            // Скрываем все категории
            document.querySelectorAll('.testimonial-category').forEach(cat => {
                cat.classList.remove('active');
            });
            
            // Показываем выбранную категорию
            document.getElementById(`${category}-reviews`).classList.add('active');
            
            // Если это не "все отзывы", рендерим конкретную категорию
            if (category !== 'all') {
                renderTestimonials(category);
            }
        }

        // Инициализация системы отзывов
        function initTestimonials() {
            // Рендерим все отзывы по умолчанию
            renderTestimonials('all');
            
            // Добавляем обработчики для кнопок фильтра
            document.querySelectorAll('.filter-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    const category = this.getAttribute('data-category');
                    filterTestimonials(category);
                });
            });
            
            // Предзагружаем остальные отзывы
            ['brows', 'lashes', 'lips', 'tattoo', 'haircut', 'depilation'].forEach(category => {
                renderTestimonials(category);
            });
        }

        // Функция инициализации основной карты
        function initMainMap() {
            // Показываем индикатор загрузки
            document.getElementById('main-map-loading').style.display = 'flex';
            
            ymaps.ready(function() {
                try {
                    mainMap = new ymaps.Map("main-map", {
                        center: salonCoordinates,
                        zoom: 16,
                        controls: ['zoomControl', 'fullscreenControl']
                    });
                    
                    // Добавляем метку
                    let placemark = new ymaps.Placemark(salonCoordinates, {
                        hintContent: 'LG Permanent Beauty',
                        balloonContent: 'Салон красоты LG Permanent<br>с. Высокая Гора, ул. Большая Красная, 156'
                    }, {
                        iconLayout: 'default#image',
                        iconImageHref: 'https://cdn-icons-png.flaticon.com/512/684/684908.png',
                        iconImageSize: [40, 40],
                        iconImageOffset: [-20, -40]
                    });
                    
                    mainMap.geoObjects.add(placemark);
                    
                    // Скрываем индикатор загрузки
                    document.getElementById('main-map-loading').style.display = 'none';
                    
                    // Для мобильных устройств добавляем специальные настройки
                    if (isMobile) {
                        mainMap.behaviors.disable('scrollZoom');
                        mainMap.behaviors.enable('multiTouch');
                    }
                } catch (error) {
                    console.error('Ошибка инициализации карты:', error);
                    document.getElementById('main-map-loading').textContent = 'Ошибка загрузки карты';
                }
            });
        }
        
        // Функция инициализации карты в модальном окне
        function initModalMap() {
            // Показываем индикатор загрузки
            document.getElementById('modal-map-loading').style.display = 'flex';
            
            ymaps.ready(function() {
                try {
                    modalMap = new ymaps.Map("modal-map", {
                        center: salonCoordinates,
                        zoom: 17,
                        controls: ['zoomControl', 'fullscreenControl']
                    });
                    
                    // Добавляем метку
                    let placemark = new ymaps.Placemark(salonCoordinates, {
                        hintContent: 'LG Permanent Beauty',
                        balloonContent: 'Салон красоты LG Permanent<br>с. Высокая Гора, ул. Большая Красная, 156<br>Телефон: +7 927 030-00-92'
                    }, {
                        iconLayout: 'default#image',
                        iconImageHref: 'https://cdn-icons-png.flaticon.com/512/684/684908.png',
                        iconImageSize: [40, 40],
                        iconImageOffset: [-20, -40]
                    });
                    
                    modalMap.geoObjects.add(placemark);
                    
                    // Скрываем индикатор загрузки
                    document.getElementById('modal-map-loading').style.display = 'none';
                    
                    // Для мобильных устройств добавляем специальные настройки
                    if (isMobile) {
                        modalMap.behaviors.disable('scrollZoom');
                        modalMap.behaviors.enable('multiTouch');
                        
                        // Перерисовываем карту после небольшой задержки
                        setTimeout(() => {
                            if (modalMap) {
                                modalMap.container.fitToViewport();
                            }
                        }, 100);
                    }
                } catch (error) {
                    console.error('Ошибка инициализации модальной карты:', error);
                    document.getElementById('modal-map-loading').textContent = 'Ошибка загрузка карты';
                }
            });
        }
        
        // Функции для открытия модальных окон
        function openLocationModal() {
            document.getElementById('locationModal').style.display = 'block';
            document.body.style.overflow = 'hidden';
            
            // Инициализируем карту только когда модальное окно открыто
            setTimeout(() => {
                if (!modalMap) {
                    initModalMap();
                } else {
                    // Если карта уже создана, перерисовываем ее
                    setTimeout(() => {
                        if (modalMap) {
                            modalMap.container.fitToViewport();
                        }
                    }, 100);
                }
            }, 50);
        }
        
        function openGallery(type) {
            const gallery = galleryData[type];
            if (!gallery) return;
            
            document.getElementById('galleryTitle').textContent = gallery.title;
            document.getElementById('galleryDescription').textContent = gallery.description;
            
            const galleryContent = document.getElementById('galleryContent');
            galleryContent.innerHTML = '';
            
            for (let i = 1; i <= gallery.items; i++) {
                const galleryItem = document.createElement('div');
                galleryItem.className = 'gallery-item';
                galleryItem.innerHTML = `<span>Пример работы ${i}<br><small>Нажмите для просмотра</small></span>`;
                galleryContent.appendChild(galleryItem);
            }
            
            document.getElementById('galleryModal').style.display = 'block';
            document.body.style.overflow = 'hidden';
        }
        
        function showComingSoon() {
            document.getElementById('comingSoonModal').style.display = 'block';
            document.body.style.overflow = 'hidden';
        }
        
        // Функция закрытия модальных окон
        function closeModal(modalId) {
            document.getElementById(modalId).style.display = 'none';
            document.body.style.overflow = '';
        }
        
        // Закрытие модальных окон при клике вне их
        window.onclick = function(event) {
            const modals = document.getElementsByClassName('modal');
            for (let modal of modals) {
                if (event.target == modal) {
                    modal.style.display = 'none';
                    document.body.style.overflow = '';
                }
            }
        }
        
        // Плавная прокрутка для якорных ссылок
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    // Закрываем меню если оно открыто
                    menuToggle.classList.remove('active');
                    mainNav.classList.remove('active');
                    
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Инициализация основной карты при загрузке страницы
        document.addEventListener('DOMContentLoaded', function() {
            // Показываем индикатор загрузки
            document.getElementById('loading').style.display = 'flex';
            
            // Загружаем карту с небольшой задержкой для лучшей производительности
            setTimeout(function() {
                initMainMap();
                // Инициализируем систему отзывов
                initTestimonials();
                // Скрываем индикатор загрузки
                document.getElementById('loading').style.display = 'none';
            }, 1000);
            
            // Закрытие меню при ресайзе (на больших экранах)
            window.addEventListener('resize', function() {
                if (window.innerWidth > 768) {
                    menuToggle.classList.remove('active');
                    mainNav.classList.remove('active');
                    document.body.style.overflow = '';
                }
                
                // Перерисовываем карты при изменении размера
                if (mainMap) {
                    setTimeout(() => {
                        mainMap.container.fitToViewport();
                    }, 100);
                }
                if (modalMap && document.getElementById('locationModal').style.display === 'block') {
                    setTimeout(() => {
                        modalMap.container.fitToViewport();
                    }, 100);
                }
            });
            
            // Добавляем анимации при скролле
            const animateOnScroll = function() {
                const elements = document.querySelectorAll('.service-card, .benefit-item, .testimonial-card');
                
                elements.forEach(element => {
                    const elementTop = element.getBoundingClientRect().top;
                    const elementBottom = element.getBoundingClientRect().bottom;
                    
                    if (elementTop < window.innerHeight - 100 && elementBottom > 0) {
                        element.style.opacity = '1';
                        element.style.transform = 'translateY(0)';
                    }
                });
            };
            
            // Инициализируем анимации
            document.querySelectorAll('.service-card, .benefit-item, .testimonial-card').forEach(element => {
                element.style.opacity = '0';
                element.style.transform = 'translateY(50px)';
                element.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            });
            
            window.addEventListener('scroll', animateOnScroll);
            animateOnScroll(); // Первоначальная проверка
            
            // Обработка касаний для мобильных устройств
            if (isMobile) {
                document.addEventListener('touchstart', function() {}, {passive: true});
            }
            
            // Обработка ошибок
            window.addEventListener('error', function(e) {
                console.error('Ошибка:', e.error);
                document.getElementById('loading').style.display = 'none';
            });
        });
    </script>
</body>
</html>
