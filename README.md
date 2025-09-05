<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AiStadioHsn | حسن قاسمی</title>
  <style>
    /* تنظیمات کلی */
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }
    
    body {
      font-family: Tahoma, sans-serif;
      margin: 0;
      padding: 0;
      background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
      color: #333;
      text-align: center;
      line-height: 1.6;
    }
    
    /* هدر */
    header {
      background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
      color: white;
      padding: 70px 20px;
      position: relative;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    }
    
    header h1 {
      margin: 0;
      font-size: 2.5rem;
      text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
    }
    
    header p {
      font-size: 1.2rem;
      margin-top: 15px;
      opacity: 0.9;
    }
    
    /* بخش‌ها */
    section {
      padding: 50px 20px;
      max-width: 1200px;
      margin: 0 auto;
    }
    
    h2 {
      margin-bottom: 30px;
      color: #2a5298;
      font-size: 2rem;
      position: relative;
      display: inline-block;
      padding-bottom: 10px;
    }
    
    h2:after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 50%;
      transform: translateX(-50%);
      width: 80px;
      height: 4px;
      background: linear-gradient(90deg, #1e3c72, #2a5298);
      border-radius: 2px;
    }
    
    /* مهارت‌ها */
    .skills {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 25px;
    }
    
    .skill {
      background: white;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.08);
      width: 250px;
      transition: transform 0.3s, box-shadow 0.3s;
    }
    
    .skill:hover {
      transform: translateY(-5px);
      box-shadow: 0 8px 20px rgba(0,0,0,0.12);
    }
    
    /* دکمه‌های نمونه کارها */
    .portfolio-buttons {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 15px;
      margin-bottom: 40px;
    }
    
    .portfolio-buttons button {
      padding: 14px 22px;
      border: none;
      border-radius: 12px;
      font-size: 1rem;
      cursor: pointer;
      font-weight: bold;
      transition: all 0.3s;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      color: white !important;
    }
    
    .portfolio-buttons button:hover, 
    .portfolio-buttons button.active {
      transform: translateY(-3px);
      box-shadow: 0 6px 12px rgba(0,0,0,0.15);
      opacity: 0.95;
    }
    
    /* رنگ‌بندی دکمه‌ها */
    button[onclick*="all"] {
      background: linear-gradient(135deg, #6c5ce7, #a29bfe);
    }
    
    button[onclick*="civil"] {
      background: linear-gradient(135deg, #3498db, #74b9ff);
    }
    
    button[onclick*="environment"] {
      background: linear-gradient(135deg, #2ecc71, #55efc4);
    }
    
    button[onclick*="jewelry"] {
      background: linear-gradient(135deg, #f39c12, #fdcb6e);
    }
    
    button[onclick*="kids"] {
      background: linear-gradient(135deg, #e84393, #fd79a8);
    }
    
    button[onclick*="romantic"] {
      background: linear-gradient(135deg, #e74c3c, #ff7675);
    }
    
    button[onclick*="cafe-restaurant"] {
      background: linear-gradient(135deg, #d35400, #f39c12);
    }
    
    button[onclick*="fashion"] {
      background: linear-gradient(135deg, #9b59b6, #a29bfe);
    }
    
    /* فوتر */
    footer {
      background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
      color: white;
      padding: 40px 20px;
      margin-top: 50px;
    }
    
    .socials {
      margin-top: 25px;
      display: flex;
      justify-content: center;
      gap: 25px;
      flex-wrap: wrap;
    }
    
    .social-item {
      display: flex;
      flex-direction: column;
      align-items: center;
      text-decoration: none;
      color: white;
      transition: transform 0.3s;
      width: 90px;
    }
    
    .social-item:hover {
      transform: translateY(-5px);
    }
    
    .social-icon {
      width: 70px;
      height: 70px;
      border-radius: 18px;
      display: flex;
      align-items: center;
      justify-content: center;
      background: rgba(255, 255, 255, 0.15);
      transition: all 0.3s;
      cursor: pointer;
      box-shadow: 0 6px 15px rgba(0,0,0,0.2);
      position: relative;
      overflow: hidden;
      margin-bottom: 12px;
    }
    
    .social-icon:before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(45deg, transparent, rgba(255,255,255,0.2), transparent);
      transform: translateX(-100%);
      transition: transform 0.6s;
    }
    
    .social-icon:hover:before {
      transform: translateX(100%);
    }
    
    .social-icon:hover {
      background: rgba(255, 255, 255, 0.25);
      box-shadow: 0 10px 20px rgba(0,0,0,0.3);
      transform: scale(1.1);
    }
    
    .social-icon img {
      width: 40px;
      height: 40px;
      object-fit: contain;
    }
    
    .social-name {
      font-size: 1rem;
      font-weight: bold;
      margin-top: 5px;
      text-shadow: 1px 1px 2px rgba(0,0,0,0.3);
    }
    
    /* استایل‌های مودال و گالری */
    .modal {
      display: none;
      position: fixed;
      z-index: 1000;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0,0,0,0.95);
      overflow: auto;
      padding: 20px;
    }
    
    .modal-content {
      margin: auto;
      display: block;
      max-width: 90%;
      max-height: 85%;
      margin-top: 40px;
      border-radius: 8px;
      box-shadow: 0 5px 25px rgba(0,0,0,0.25);
      animation: zoom 0.3s ease;
    }
    
    @keyframes zoom {
      from {transform: scale(0.9); opacity: 0;}
      to {transform: scale(1); opacity: 1;}
    }
    
    .close {
      position: absolute;
      top: 25px;
      right: 35px;
      color: #f1f1f1;
      font-size: 45px;
      font-weight: bold;
      cursor: pointer;
      transition: 0.3s;
      z-index: 1001;
    }
    
    .close:hover {
      color: #ffcc00;
      transform: rotate(90deg);
    }
    
    .gallery {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
      margin-top: 30px;
    }
    
    .gallery-item {
      width: 220px;
      height: 220px;
      object-fit: cover;
      cursor: pointer;
      border-radius: 10px;
      transition: all 0.3s;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    }
    
    .gallery-item:hover {
      transform: scale(1.05) rotate(2deg);
      box-shadow: 0 8px 20px rgba(0,0,0,0.2);
    }
    
    .category-title {
      margin-top: 40px;
      color: #2a5298;
      border-bottom: 3px solid #2a5298;
      padding-bottom: 12px;
      display: inline-block;
      font-size: 1.5rem;
    }
    
    .placeholder {
      color: #777;
      font-style: italic;
      margin: 50px 0;
      font-size: 1.1rem;
    }
    
    /* منوی همبرگری */
    .menu-btn {
      position: fixed;
      top: 25px;
      left: 25px;
      background: rgba(255, 255, 255, 0.2);
      border: none;
      border-radius: 8px;
      width: 50px;
      height: 50px;
      cursor: pointer;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      gap: 5px;
      z-index: 1002;
      transition: 0.3s;
      backdrop-filter: blur(5px);
    }
    
    .menu-btn:hover {
      background: rgba(255, 255, 255, 0.3);
    }
    
    .menu-btn span {
      display: block;
      width: 30px;
      height: 3px;
      background: white;
      border-radius: 2px;
      transition: 0.3s;
    }
    
    .nav-menu {
      position: fixed;
      top: 0;
      left: -300px;
      width: 280px;
      height: 100%;
      background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
      padding: 100px 25px 25px;
      z-index: 1001;
      transition: 0.4s;
      box-shadow: 2px 0 15px rgba(0,0,0,0.2);
    }
    
    .nav-menu.active {
      left: 0;
    }
    
    .nav-menu a {
      display: flex;
      align-items: center;
      color: white;
      text-decoration: none;
      padding: 18px;
      margin: 15px 0;
      border-radius: 8px;
      transition: 0.3s;
      font-size: 1.1rem;
    }
    
    .nav-menu a i {
      margin-left: 12px;
      font-size: 1.2rem;
    }
    
    .nav-menu a:hover {
      background: rgba(255, 255, 255, 0.15);
      transform: translateX(5px);
    }
    
    .overlay {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0,0,0,0.7);
      z-index: 1000;
    }
    
    .overlay.active {
      display: block;
    }
    
    /* ریسپانسیو */
    @media (max-width: 768px) {
      header h1 {
        font-size: 2rem;
      }
      
      header p {
        font-size: 1rem;
      }
      
      .portfolio-buttons {
        gap: 10px;
      }
      
      .portfolio-buttons button {
        padding: 12px 16px;
        font-size: 0.9rem;
      }
      
      .gallery-item {
        width: 150px;
        height: 150px;
      }
      
      .socials {
        gap: 15px;
      }
      
      .social-icon {
        width: 60px;
        height: 60px;
      }
      
      .social-icon img {
        width: 32px;
        height: 32px;
      }
      
      .social-name {
        font-size: 0.9rem;
      }
    }
  </style>
</head>
<body>

  <!-- منوی همبرگری -->
  <button class="menu-btn" onclick="toggleMenu()">
    <span></span>
    <span></span>
    <span></span>
  </button>
  
  <div class="nav-menu" id="navMenu">
    <a href="#about" onclick="toggleMenu()">معرفی من</a>
    <a href="#skills" onclick="toggleMenu()">مهارت‌ها</a>
    <a href="#portfolio" onclick="toggleMenu()">نمونه کارها</a>
    <a href="#contact" onclick="toggleMenu()">تماس با من</a>
  </div>
  
  <div class="overlay" id="overlay" onclick="toggleMenu()"></div>

  <header>
    <h1>حسن قاسمی | AiStadioHsn</h1>
    <p>خالق محتوای | طراحی لوگو | طراحی پوستر | ویدیو کوتاه با هوش مصنوعی</p>
  </header>

  <section id="about">
    <h2>درباره من</h2>
    <p>
      سلام، من حسن هستم! به دنیای خلاقیت و هوش مصنوعی خوش آمدید.  
      من در AiStadioHsn به تولید محتوا با استفاده از آخرین تکنولوژی‌های هوش مصنوعی می‌پردازم.  
      از طراحی پوستر و لوگو گرفته تا ساخت ویدیوهای کوتاه و جذاب، تمام تلاشم این است که ایده‌های شما را به بهترین شکل ممکن زنده کنم. 🌹
    </p>
  </section>

  <section id="skills">
    <h2>مهارت‌ها</h2>
    <div class="skills">
      <div class="skill">🎨 طراحی پوستر</div>
      <div class="skill">🏷️ طراحی لوگو</div>
      <div class="skill">🎬 ویدیو کوتاه AI</div>
      <div class="skill">📢 پوستر کمپین بازاریابی</div>
      <div class="skill">💡 لوگو استارتاپ تکنولوژی</div>
      <div class="skill">📱 ویدیو معرفی محصول</div>
    </div>
  </section>

  <section id="portfolio">
    <h2>نمونه‌کارها</h2>
    <div class="portfolio-buttons">
      <button onclick="showCategory('all')">همه کارها</button>
      <button onclick="showCategory('civil')">مهندسی عمران</button>
      <button onclick="showCategory('environment')">محیط زیست</button>
      <button onclick="showCategory('jewelry')">جواهرات</button>
      <button onclick="showCategory('kids')">کودکانه</button>
      <button onclick="showCategory('romantic')">عاشقانه</button>
      <button onclick="showCategory('cafe-restaurant')">کافه و رستوران</button>
      <button onclick="showCategory('fashion')">مد و فشن</button>
    </div>
    
    <!-- گالری تصاویر -->
    <div id="gallery-container">
      <p class="placeholder">لطفاً یک دسته از بالا انتخاب کنید تا نمونه‌کارهای مربوطه نمایش داده شوند.</p>
    </div>
    
    <!-- مودال برای نمایش تصویر در اندازه بزرگ -->
    <div id="imageModal" class="modal">
      <span class="close" onclick="closeModal()">&times;</span>
      <img class="modal-content" id="modalImage">
    </div>
  </section>

  <footer id="contact">
    <p>ارتباط با من</p>
    <div class="socials">
      <a href="https://t.me/AiStadioHsn" class="social-item" target="_blank" rel="noopener noreferrer">
        <div class="social-icon" style="background: linear-gradient(135deg, #0088cc, #00a8ff);">
          <img src="https://upload.wikimedia.org/wikipedia/commons/8/83/Telegram_2019_Logo.svg" alt="Telegram">
        </div>
        <span class="social-name">تلگرام</span>
      </a>
      <a href="https://instagram.com/AiStadioHsn" class="social-item" target="_blank" rel="noopener noreferrer">
        <div class="social-icon" style="background: linear-gradient(135deg, #e4405f, #fcaf45);">
          <img src="https://upload.wikimedia.org/wikipedia/commons/e/e7/Instagram_logo_2016.svg" alt="Instagram">
        </div>
        <span class="social-name">اینستاگرام</span>
      </a>
      <a href="https://youtube.com/@aistadiohsn?sub_confirmation=1" class="social-item" target="_blank" rel="noopener noreferrer">
        <div class="social-icon" style="background: linear-gradient(135deg, #ff0000, #ff5e5e);">
          <img src="https://upload.wikimedia.org/wikipedia/commons/4/42/YouTube_icon_%282013-2017%29.png" alt="YouTube">
        </div>
        <span class="social-name">یوتیوب</span>
      </a>
      <a href="https://wa.me/989199124951" class="social-item" target="_blank" rel="noopener noreferrer">
        <div class="social-icon" style="background: linear-gradient(135deg, #25d366, #128c7e);">
          <img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/WhatsApp.svg" alt="WhatsApp">
        </div>
        <span class="social-name">واتساپ</span>
      </a>
    </div>
  </footer>

  <script>
    // شیء حاوی تصاویر هر دسته
    const portfolioImages = {
      civil: [
        "https://i.ibb.co/Q7WyJ4vD/IMG-20250902-083237-373.jpg",
        "https://i.ibb.co/pBcvP6mW/IMG-20250902-083237-243.jpg",
        "https://i.ibb.co/Xftw6B0G/IMG-20250902-083237-739.jpg",
        "https://i.ibb.co/0jcjkF44/IMG-20250902-083237-709.jpg"
      ],
      environment: [
        "https://i.ibb.co/0jwsgXgm/Leonardo-Phoenix-10-Ecofriendly-company-logo-featuring-intrica-0.jpg",
        "https://i.ibb.co/0yZStYSb/Leonardo-Phoenix-10-Ecofriendly-company-logo-featuring-intrica-1.jpg",
        "https://i.ibb.co/1Y25rgC4/Leonardo-Phoenix-10-Ecofriendly-company-logo-featuring-intrica-2.jpg",
        "https://i.ibb.co/Rkx77qyw/Leonardo-Phoenix-10-Ecofriendly-company-logo-featuring-intrica-3.jpg"
      ],
      jewelry: [
        "https://i.ibb.co/TDXxBm4V/Leonardo-Phoenix-10-Luxury-jewelry-brand-logo-featuring-a-gold-0.jpg",
        "https://i.ibb.co/9HFLWH3X/Leonardo-Phoenix-10-Luxury-jewelry-brand-logo-featuring-a-gold-2.jpg",
        "https://i.ibb.co/Q7zQBxvp/Leonardo-Phoenix-10-Luxury-jewelry-brand-logo-featuring-a-gold-3.jpg"
      ],
      kids: [
        "https://i.ibb.co/hFrxdQKz/Leonardo-Phoenix-10-Playful-kids-brand-logo-featuring-a-variet-1.jpg",
        "https://i.ibb.co/S4JtJxk3/Leonardo-Phoenix-10-Playful-kids-brand-logo-featuring-a-variet-0.jpg",
        "https://i.ibb.co/3yVsWcct/Leonardo-Phoenix-10-Playful-kids-brand-logo-featuring-a-variet-2.jpg",
        "https://i.ibb.co/M56ZmyQd/Leonardo-Phoenix-10-Playful-kids-brand-logo-featuring-a-variet-3.jpg"
      ],
      romantic: [
        "https://i.ibb.co/9k5B3LS9/Lucid-Origin-A-romantic-cinematic-portrait-of-a-beautiful-Iran-2.jpg",
        "https://i.ibb.co/gZFyJ5bx/Lucid-Origin-A-romantic-cinematic-portrait-of-a-beautiful-Iran-1.jpg",
        "https://i.ibb.co/cXCFDDSZ/Lucid-Origin-A-romantic-cinematic-portrait-of-a-beautiful-Iran-0.jpg",
        "https://i.ibb.co/GvR3jVRF/GPT-Image-1-A-romantic-cinematic-portrait-of-an-Iranian-Muslim-0.png"
      ],
      'cafe-restaurant': [
        "https://i.ibb.co/XrvdQSjd/Lucid-Origin-Elegant-golden-fork-and-knife-intricately-forming-0.jpg",
        "https://i.ibb.co/rfbVnwGr/Lucid-Origin-Elegant-golden-fork-and-knife-intricately-forming-2.jpg",
        "https://i.ibb.co/yBcYG326/Lucid-Origin-Elegant-golden-fork-and-knife-intricately-forming-1.jpg",
        "https://i.ibb.co/m5rkmLM0/Leonardo-Phoenix-10-Artistic-coffee-shop-logo-featuring-a-deli-1.jpg",
        "https://i.ibb.co/1YPgQrcQ/Leonardo-Phoenix-10-Artistic-coffee-shop-logo-featuring-a-deli-0.jpg",
        "https://i.ibb.co/WWBk4M2n/Leonardo-Phoenix-10-Artistic-coffee-shop-logo-featuring-a-deli-2.jpg",
        "https://i.ibb.co/MkxDSL5K/Leonardo-Phoenix-10-Artistic-coffee-shop-logo-featuring-a-deli-3.jpg"
      ],
      fashion: [
        "https://i.ibb.co/ymX9dvfP/GPT-Image-1-A-cinematic-fashion-poster-featuring-a-tall-elegan-0.png",
        "https://i.ibb.co/Rp1vgWcx/GPT-Image-1-A-minimalist-fashion-logo-concept-featuring-a-styl-0.png",
        "https://i.ibb.co/d0kwdxyx/GPT-Image-1-A-highend-fashion-poster-featuring-a-dramatic-silh-0.png",
        "https://i.ibb.co/Lz5Ym4J5/Lucid-Origin-A-glamorous-fashion-editorial-portrait-of-a-stunn-2.jpg",
        "https://i.ibb.co/S7yDPGky/Lucid-Origin-A-glamorous-fashion-editorial-portrait-of-a-stunn-1.jpg",
        "https://i.ibb.co/7N6g5FXk/Lucid-Origin-A-glamorous-fashion-editorial-portrait-of-a-stunn-0.jpg",
        "https://i.ibb.co/xqgKJf20/Lucid-Origin-A-cinematic-fashion-portrait-of-a-Persian-female-2.jpg",
        "https://i.ibb.co/nq7nNQXM/Lucid-Origin-A-cinematic-fashion-portrait-of-a-Persian-female-0.jpg",
        "https://i.ibb.co/YF1m4pqn/Lucid-Origin-A-cinematic-fashion-portrait-of-a-Persian-female-1.jpg",
        "https://i.ibb.co/MD5Rktk6/Lucid-Origin-A-highfashion-editorial-portrait-of-a-confident-f-2.jpg",
        "https://i.ibb.co/LzhkWVVr/Lucid-Origin-A-highfashion-editorial-portrait-of-a-confident-f-0.jpg"
      ]
    };

    // تابع برای نمایش تمام تصاویر
    function showAllWorks() {
      const galleryContainer = document.getElementById('gallery-container');
      galleryContainer.innerHTML = '<h3 class="category-title">همه نمونه کارها</h3>';
      
      const categories = {
        civil: "مهندسی عمران",
        environment: "محیط زیست",
        jewelry: "جواهرات",
        kids: "کودکانه",
        romantic: "عاشقانه",
        'cafe-restaurant': "کافه و رستوران",
        fashion: "مد و فشن"
      };
      
      for (const [category, title] of Object.entries(categories)) {
        const categoryTitle = document.createElement('h4');
        categoryTitle.className = 'category-title';
        categoryTitle.style.marginTop = '40px';
        categoryTitle.textContent = title;
        galleryContainer.appendChild(categoryTitle);
        
        const galleryDiv = document.createElement('div');
        galleryDiv.className = 'gallery';
        
        portfolioImages[category].forEach(imageUrl => {
          const img = document.createElement('img');
          img.src = imageUrl;
          img.alt = title;
          img.className = 'gallery-item';
          img.onclick = function() {
            openModal(imageUrl);
          };
          galleryDiv.appendChild(img);
        });
        
        galleryContainer.appendChild(galleryDiv);
      }
    }

    // تابع برای نمایش تصاویر هر دسته
    function showCategory(category) {
      const buttons = document.querySelectorAll('.portfolio-buttons button');
      buttons.forEach(btn => btn.classList.remove('active'));
      event.target.classList.add('active');
      
      if (category === 'all') {
        showAllWorks();
        return;
      }
      
      const galleryContainer = document.getElementById('gallery-container');
      const categoryTitle = {
        civil: "مهندسی عمران",
        environment: "محیط زیست",
        jewelry: "جواهرات",
        kids: "کودکانه",
        romantic: "عاشقانه",
        'cafe-restaurant': "کافه و رستوران",
        fashion: "مد و فشن"
      };
      
      // ایجاد عنوان دسته
      galleryContainer.innerHTML = `<h3 class="category-title">${categoryTitle[category]}</h3>`;
      
      // ایجاد گالری تصاویر
      const galleryDiv = document.createElement('div');
      galleryDiv.className = 'gallery';
      
      portfolioImages[category].forEach(imageUrl => {
        const img = document.createElement('img');
        img.src = imageUrl;
        img.alt = categoryTitle[category];
        img.className = 'gallery-item';
        img.onclick = function() {
          openModal(imageUrl);
        };
        galleryDiv.appendChild(img);
      });
      
      galleryContainer.appendChild(galleryDiv);
    }

    // توابع مربوط به مودال
    function openModal(imageUrl) {
      const modal = document.getElementById('imageModal');
      const modalImg = document.getElementById('modalImage');
      modal.style.display = 'block';
      modalImg.src = imageUrl;
    }

    function closeModal() {
      document.getElementById('imageModal').style.display = 'none';
    }

    // توابع مربوط به منوی همبرگری
    function toggleMenu() {
      const navMenu = document.getElementById('navMenu');
      const overlay = document.getElementById('overlay');
      navMenu.classList.toggle('active');
      overlay.classList.toggle('active');
    }

    // بستن مودال با کلیک خارج از تصویر
    window.onclick = function(event) {
      const modal = document.getElementById('imageModal');
      if (event.target == modal) {
        closeModal();
      }
    }
  </script>

</body>
</html>
