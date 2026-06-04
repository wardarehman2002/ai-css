/* =========================
   GENERAL STYLING
========================= */

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    font-family:Arial, sans-serif;
    line-height:1.6;
    background:#fff;
    color:#333;
}

.container{
    width:80%;
    margin:auto;
}

img{
    width:100%;
    display:block;
}

section{
    padding:80px 0;
}

h2{
    text-align:center;
    color:#2f80ed;
    margin-bottom:40px;
    font-size:32px;
}

/* =========================
   HEADER
========================= */

header{
    background:#fff;
    padding:20px 0;
}

.navbar{
    display:flex;
    justify-content:space-between;
    align-items:center;
}

.logo{
    font-size:24px;
    font-weight:bold;
    color:#00a2a2;
}

.nav-links{
    list-style:none;
}

.nav-links li{
    display:inline-block;
    margin-left:20px;
}

.nav-links a{
    text-decoration:none;
    color:#333;
}

.buy-btn{
    background:#2f80ed;
    color:white;
    padding:10px 20px;
    border-radius:20px;
}

/* =========================
   HERO SECTION
========================= */

.hero{
    height:650px;
    background:url("images/hero.jpg");
    background-size:cover;
    background-position:center;
    display:flex;
    align-items:center;
}

.hero-text{
    margin-left:80px;
}

.hero-text h1{
    font-size:55px;
    margin-bottom:15px;
}

.hero-text p{
    color:#2f80ed;
}

/* =========================
   ABOUT US
========================= */

.about-cards{
    display:flex;
    justify-content:space-between;
    gap:25px;
}

.about-card{
    flex:1;
}

.about-card img{
    margin-bottom:15px;
}

.about-card h3{
    color:#2f80ed;
    margin-bottom:10px;
}

/* =========================
   SALE BANNER
========================= */

.sale{
    background:url("images/sale-banner.jpg");
    background-size:cover;
    background-position:center;
    height:500px;

    display:flex;
    justify-content:center;
    align-items:center;
    text-align:center;
}

.sale-content h2{
    font-size:48px;
    color:#2f80ed;
}

.sale-content button{
    margin-top:20px;
    padding:12px 25px;
    border:none;
    background:#2f80ed;
    color:white;
    border-radius:25px;
}

/* =========================
   FEATURES
========================= */

.feature-wrapper{
    display:grid;
    grid-template-columns:repeat(2,1fr);
    gap:40px;
}

.feature-box{
    padding:20px;
}

.feature-box i{
    font-size:30px;
    color:#2f80ed;
    margin-bottom:15px;
}

/* =========================
   PRODUCTS
========================= */

.product-grid{
    display:grid;
    grid-template-columns:repeat(2,1fr);
    gap:30px;
}

.product{
    text-align:center;
}

.product img{
    height:320px;
    object-fit:cover;
}

.product h4{
    margin-top:15px;
}

.price{
    color:#2f80ed;
}

/* =========================
   NEWSLETTER
========================= */

.newsletter{
    background:#f5f5f8;
    text-align:center;
}

.newsletter h2{
    margin-bottom:15px;
}

.newsletter input{
    width:350px;
    padding:12px;
    border:1px solid #ccc;
}

.newsletter button{
    padding:12px 20px;
    border:none;
    background:#2f80ed;
    color:white;
}

/* =========================
   GALLERY
========================= */

.gallery-grid{
    display:grid;
    grid-template-columns:2fr 1fr;
    gap:20px;
}

.gallery-right{
    display:grid;
    gap:20px;
}

/* =========================
   LATEST NEWS
========================= */

.news-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:20px;
}

.news-card{
    background:white;
    box-shadow:0 0 10px rgba(0,0,0,0.1);
}

.news-card img{
    height:200px;
    object-fit:cover;
}

.news-card-content{
    padding:15px;
}

/* =========================
   LAST COLLECTION
========================= */

.collection-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:15px;
}

.collection-grid img{
    height:180px;
    object-fit:cover;
}

/* =========================
   TESTIMONIALS
========================= */

.testimonials{
    background:#f5f5f8;
    text-align:center;
}

.testimonial-img{
    width:80px;
    height:80px;
    border-radius:50%;
    margin:auto;
    margin-bottom:20px;
}

.testimonial-text{
    max-width:700px;
    margin:auto;
}

/* =========================
   LOCATION
========================= */

.location-content{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:20px;
}

.location-content img{
    height:350px;
    object-fit:cover;
}

iframe{
    width:100%;
    height:350px;
    border:none;
}

/* =========================
   FOOTER
========================= */

footer{
    background:#f5f5f8;
    padding:60px 0;
}

.footer-content{
    display:grid;
    grid-template-columns:2fr 1fr 1fr;
    gap:40px;
}

.footer-content h3{
    margin-bottom:15px;
}

.footer-content ul{
    list-style:none;
}

.footer-content ul li{
    margin-bottom:10px;
}

.footer-content a{
    text-decoration:none;
    color:#333;
}

.footer-bottom{
    text-align:center;
    margin-top:30px;
    border-top:1px solid #ddd;
    padding-top:20px;
}

/* =========================
   RESPONSIVE
========================= */

@media(max-width:768px){

    .navbar{
        flex-direction:column;
    }

    .about-cards{
        flex-direction:column;
    }

    .product-grid{
        grid-template-columns:1fr;
    }

    .news-grid{
        grid-template-columns:1fr;
    }

    .collection-grid{
        grid-template-columns:1fr;
    }

    .location-content{
        grid-template-columns:1fr;
    }

    .feature-wrapper{
        grid-template-columns:1fr;
    }

    .gallery-grid{
        grid-template-columns:1fr;
    }

    .footer-content{
        grid-template-columns:1fr;
    }

    .hero-text h1{
        font-size:40px;
    }
}