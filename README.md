<link rel="stylesheet" href="clothing-store.css">
/* ============================================
   CLOTHING STORE —  CSS
   ============================================ */

/* ── VARIABLES ── */
:root {
  --black: #0a0a0a;
  --white: #fafaf8;
  --accent: #2196f3;
  --accent-dark: #0d7ecf;
  --gray-light: #f4f4f1;
  --gray-mid: #c8c8c0;
  --gray-dark: #6a6a62;
  --overlay: rgba(10, 10, 10, 0.45);
  --section-pad: 80px;
  --font-display: 'Cormorant Garamond', serif;
  --font-body: 'Jost', sans-serif;
}

/* ── RESET ── */
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-body);
  background-color: var(--white);
  color: var(--black);
  font-size: 15px;
  line-height: 1.6;
}

img {
  display: block;
  width: 100%;
  object-fit: cover;
}

a {
  text-decoration: none;
  color: inherit;
}

ul {
  list-style: none;
}

/* ============================================
   NAVIGATION
   ============================================ */

nav {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 100;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 48px;
  height: 64px;
  background-color: var(--white);
  border-bottom: 1px solid rgba(0, 0, 0, 0.07);
}

.nav-logo {
  font-family: var(--font-display);
  font-size: 22px;
  font-weight: 600;
  letter-spacing: 0.04em;
  color: var(--accent);
}

.nav-links {
  display: flex;
  gap: 36px;
}

.nav-links a {
  font-size: 12px;
  font-weight: 500;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--black);
  transition: color 0.2s ease;
}

.nav-links a:hover {
  color: var(--accent);
}

.nav-actions {
  display: flex;
  align-items: center;
  gap: 20px;
}

.nav-phone {
  font-size: 12px;
  color: var(--gray-dark);
  letter-spacing: 0.05em;
}

/* ============================================
   BUTTONS
   ============================================ */

.btn {
  display: inline-block;
  padding: 10px 28px;
  font-size: 12px;
  font-weight: 600;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  border-radius: 2px;
  transition: all 0.25s ease;
  cursor: pointer;
  border: none;
}

.btn-primary {
  background-color: var(--accent);
  color: #fff;
}

.btn-primary:hover {
  background-color: var(--accent-dark);
  transform: translateY(-1px);
  box-shadow: 0 6px 20px rgba(33, 150, 243, 0.35);
}

.btn-outline {
  background-color: transparent;
  color: #fff;
  border: 1.5px solid #fff;
}

.btn-outline:hover {
  background-color: #fff;
  color: var(--black);
}

/* ============================================
   HERO
   ============================================ */

.hero {
  margin-top: 64px;
  position: relative;
  height: 88vh;
  min-height: 560px;
  overflow: hidden;
}

.hero-bg {
  position: absolute;
  inset: 0;
  background: linear-gradient(135deg, #1a1a2e 0%, #2c2c3e 50%, #3a2a2a 100%);
}

.hero-bg::after {
  content: '';
  position: absolute;
  inset: 0;
  background: url('https://images.unsplash.com/photo-1483985988355-763728e1935b?w=1600&q=80') center / cover no-repeat;
  opacity: 0.55;
}

.hero-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(to right, rgba(0, 0, 0, 0.65) 35%, transparent 70%);
}

.hero-content {
  position: relative;
  z-index: 2;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 0 80px;
}

.hero-tag {
  font-size: 11px;
  font-weight: 500;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--accent);
  margin-bottom: 16px;
  animation: fadeUp 0.6s 0.2s both;
}

.hero-title {
  font-family: var(--font-display);
  font-size: clamp(52px, 7vw, 96px);
  font-weight: 300;
  color: #fff;
  line-height: 1.05;
  letter-spacing: -0.01em;
  animation: fadeUp 0.7s 0.35s both;
}

.hero-title em {
  font-style: italic;
  color: var(--gray-mid);
}

.hero-sub {
  margin-top: 20px;
  font-size: 14px;
  color: rgba(255, 255, 255, 0.65);
  max-width: 340px;
  line-height: 1.7;
  animation: fadeUp 0.6s 0.5s both;
}

.hero-ctas {
  display: flex;
  gap: 16px;
  margin-top: 36px;
  animation: fadeUp 0.6s 0.65s both;
}

/* ============================================
   SECTION UTILITIES
   ============================================ */

.section-label {
  display: block;
  font-size: 10px;
  font-weight: 500;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--gray-dark);
  text-align: center;
  margin-bottom: 10px;
}

.section-title {
  font-family: var(--font-display);
  font-size: 40px;
  font-weight: 400;
  color: var(--accent);
  letter-spacing: 0.01em;
  text-align: center;
  margin-bottom: 48px;
}

/* ============================================
   ABOUT
   ============================================ */

.about {
  padding: var(--section-pad) 80px;
}

.about-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 32px;
}

.about-card {
  display: flex;
  flex-direction: column;
  gap: 14px;
}

.about-card-img {
  height: 200px;
  overflow: hidden;
  border-radius: 2px;
}

.about-card-img img {
  height: 100%;
  transition: transform 0.5s ease;
}

.about-card:hover .about-card-img img {
  transform: scale(1.04);
}

.about-card-tag {
  font-size: 10px;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  color: var(--accent);
  font-weight: 500;
}

.about-card h3 {
  font-family: var(--font-display);
  font-size: 20px;
  font-weight: 600;
  color: var(--black);
}

.about-card p {
  font-size: 13px;
  color: var(--gray-dark);
  line-height: 1.7;
}

.about-card a {
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--accent);
  display: inline-flex;
  align-items: center;
  gap: 6px;
}

.about-card a::after {
  content: '→';
  transition: transform 0.2s ease;
}

.about-card a:hover::after {
  transform: translateX(4px);
}

/* ============================================
   SALE BANNER
   ============================================ */

.sale-banner {
  position: relative;
  height: 400px;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
}

.sale-banner-bg {
  position: absolute;
  inset: 0;
  background: url('https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=1600&q=80') center / cover no-repeat;
  filter: brightness(0.5);
}

.sale-banner-content {
  position: relative;
  z-index: 2;
  text-align: center;
}

.sale-banner-tag {
  font-size: 11px;
  letter-spacing: 0.25em;
  text-transform: uppercase;
  color: rgba(255, 255, 255, 0.6);
  margin-bottom: 16px;
}

.sale-banner h2 {
  font-family: var(--font-display);
  font-size: clamp(36px, 5vw, 64px);
  font-weight: 300;
  color: #fff;
  letter-spacing: 0.02em;
  margin-bottom: 8px;
}

.sale-banner h2 span {
  color: var(--accent);
  font-style: italic;
}

.sale-banner p {
  font-size: 13px;
  color: rgba(255, 255, 255, 0.65);
  margin-bottom: 28px;
  letter-spacing: 0.05em;
  text-transform: uppercase;
}

/* ============================================
   FEATURES
   ============================================ */

.features {
  padding: var(--section-pad) 80px;
  background-color: var(--gray-light);
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: 64px;
  align-items: center;
}

.features-heading {
  font-family: var(--font-display);
  font-size: 36px;
  font-weight: 400;
  line-height: 1.2;
  color: var(--black);
}

.features-heading span {
  display: block;
  font-family: var(--font-body);
  font-size: 11px;
  font-weight: 500;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--gray-dark);
  margin-bottom: 12px;
}

.features-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 40px;
}

.feature-item {
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.feature-icon {
  width: 44px;
  height: 44px;
  border-radius: 50%;
  background-color: var(--white);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 20px;
  box-shadow: 0 2px 12px rgba(0, 0, 0, 0.08);
}

.feature-item h4 {
  font-size: 14px;
  font-weight: 600;
  color: var(--black);
  letter-spacing: 0.02em;
}

.feature-item p {
  font-size: 12px;
  color: var(--gray-dark);
  line-height: 1.65;
}

/* ============================================
   PRODUCTS
   ============================================ */

.products {
  padding: var(--section-pad) 80px;
}

.products-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 24px;
}

.product-card {
  position: relative;
  overflow: hidden;
  border-radius: 2px;
  cursor: pointer;
}

.product-card-img {
  height: 340px;
  overflow: hidden;
}

.product-card-img img {
  height: 100%;
  transition: transform 0.6s ease;
}

.product-card:hover .product-card-img img {
  transform: scale(1.06);
}

.product-card-info {
  padding: 16px 0 8px;
}

.product-card-info h4 {
  font-size: 13px;
  font-weight: 500;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  color: var(--gray-dark);
}

.product-card-info .price {
  font-family: var(--font-display);
  font-size: 22px;
  font-weight: 600;
  color: var(--black);
  margin-top: 4px;
}

/* ============================================
   SUBSCRIBE
   ============================================ */

.subscribe {
  padding: 72px 80px;
  background-color: var(--gray-light);
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 40px;
}

.subscribe-text h2 {
  font-family: var(--font-display);
  font-size: 32px;
  font-weight: 400;
  color: var(--black);
}

.subscribe-text p {
  font-size: 13px;
  color: var(--gray-dark);
  margin-top: 6px;
}

.subscribe-form {
  display: flex;
  flex: 0 0 420px;
  border: 1.5px solid var(--gray-mid);
  border-radius: 2px;
  overflow: hidden;
  background-color: #fff;
}

.subscribe-form input {
  flex: 1;
  border: none;
  outline: none;
  padding: 14px 20px;
  font-family: var(--font-body);
  font-size: 13px;
  color: var(--black);
  background-color: transparent;
}

.subscribe-form input::placeholder {
  color: var(--gray-mid);
}

.subscribe-form button {
  background-color: var(--accent);
  color: #fff;
  border: none;
  padding: 14px 28px;
  font-family: var(--font-body);
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  cursor: pointer;
  transition: background-color 0.2s ease;
}

.subscribe-form button:hover {
  background-color: var(--accent-dark);
}

/* ============================================
   GALLERY
   ============================================ */

.gallery {
  display: grid;
  grid-template-columns: 1fr 1fr;
}

.gallery-left {
  height: 480px;
  position: relative;
  overflow: hidden;
}

.gallery-right {
  display: grid;
  grid-template-rows: 1fr 1fr;
}

.gallery-right > div {
  height: 240px;
  position: relative;
  overflow: hidden;
}

.gallery-left img,
.gallery-right > div img {
  height: 100%;
  transition: transform 0.6s ease;
}

.gallery-left:hover img,
.gallery-right > div:hover img {
  transform: scale(1.05);
}

.gallery-label {
  position: absolute;
  bottom: 20px;
  left: 20px;
  z-index: 2;
  background-color: var(--black);
  color: #fff;
  font-size: 10px;
  font-weight: 600;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  padding: 6px 14px;
}

.gallery-label.accent {
  background-color: var(--accent);
}

/* ============================================
   NEWS
   ============================================ */

.news {
  padding: var(--section-pad) 80px;
  background-color: var(--gray-light);
}

.news-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 28px;
}

.news-card {
  background-color: var(--white);
  border-radius: 2px;
  overflow: hidden;
  transition: box-shadow 0.3s ease;
}

.news-card:hover {
  box-shadow: 0 12px 40px rgba(0, 0, 0, 0.1);
}

.news-card-img {
  height: 200px;
  overflow: hidden;
}

.news-card-img img {
  height: 100%;
  transition: transform 0.5s ease;
}

.news-card:hover .news-card-img img {
  transform: scale(1.05);
}

.news-card-body {
  padding: 20px;
}

.news-card-body h4 {
  font-family: var(--font-display);
  font-size: 20px;
  font-weight: 600;
  margin-bottom: 8px;
  color: var(--black);
}

.news-card-body p {
  font-size: 12px;
  color: var(--gray-dark);
  line-height: 1.65;
}

.news-card-body a {
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--accent);
  display: inline-flex;
  align-items: center;
  gap: 6px;
  margin-top: 12px;
  transition: gap 0.2s ease;
}

.news-card-body a:hover {
  gap: 10px;
}

/* ============================================
   COLLECTION
   ============================================ */

.collection {
  padding: var(--section-pad) 80px;
}

.collection-header {
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
  margin-bottom: 40px;
}

.collection-header .collection-sub {
  font-size: 10px;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--gray-dark);
  font-weight: 500;
  display: block;
  margin-bottom: 6px;
}

.collection-header h2 {
  font-family: var(--font-display);
  font-size: 40px;
  font-weight: 400;
  color: var(--black);
  letter-spacing: 0.05em;
  text-transform: uppercase;
}

.collection-header a {
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  color: var(--accent);
  transition: color 0.2s ease;
}

.collection-header a:hover {
  color: var(--accent-dark);
}

.collection-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(2, 240px);
  gap: 12px;
}

.collection-item {
  overflow: hidden;
  border-radius: 2px;
  position: relative;
}

.collection-item img {
  height: 100%;
  transition: transform 0.55s ease;
}

.collection-item:hover img {
  transform: scale(1.07);
}

/* ============================================
   TESTIMONIALS
   ============================================ */

.testimonials {
  padding: var(--section-pad) 80px;
  background-color: var(--gray-light);
  text-align: center;
}

.testimonial-card {
  max-width: 640px;
  margin: 0 auto;
  padding: 48px;
  background-color: var(--white);
  border-radius: 4px;
  box-shadow: 0 4px 32px rgba(0, 0, 0, 0.07);
}

.testimonial-avatar {
  width: 72px;
  height: 72px;
  border-radius: 50%;
  overflow: hidden;
  margin: 0 auto 20px;
  border: 3px solid var(--accent);
}

.testimonial-avatar img {
  height: 100%;
}

.stars {
  color: #f4c542;
  font-size: 16px;
  margin-bottom: 16px;
  letter-spacing: 2px;
}

.testimonial-text {
  font-family: var(--font-display);
  font-size: 19px;
  font-style: italic;
  color: var(--black);
  line-height: 1.65;
  margin-bottom: 20px;
}

.testimonial-name {
  font-size: 12px;
  font-weight: 600;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--accent);
}

/* ============================================
   LOCATION
   ============================================ */

.location {
  padding: var(--section-pad) 80px;
}

.location-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 48px;
  align-items: start;
}

.location-imgs {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 12px;
  margin-top: 24px;
}

.location-imgs div {
  height: 200px;
  overflow: hidden;
  border-radius: 2px;
}

.location-imgs div img {
  height: 100%;
  transition: transform 0.5s ease;
}

.location-imgs div:hover img {
  transform: scale(1.05);
}

.location-map {
  height: 280px;
  border-radius: 2px;
  overflow: hidden;
  background-color: #e0e0d8;
  border: 1px solid var(--gray-mid);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 13px;
  color: var(--gray-dark);
}

.location-detail {
  display: flex;
  gap: 12px;
  margin-bottom: 16px;
  align-items: flex-start;
  margin-top: 24px;
}

.location-detail-icon {
  font-size: 18px;
  margin-top: 2px;
  flex-shrink: 0;
}

.location-detail p {
  font-size: 13px;
  color: var(--gray-dark);
  line-height: 1.6;
}

.location-detail strong {
  color: var(--black);
  display: block;
  margin-bottom: 4px;
}

/* ============================================
   FOOTER
   ============================================ */

footer {
  background-color: var(--black);
  color: rgba(255, 255, 255, 0.65);
  padding: 64px 80px 40px;
}

.footer-grid {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr;
  gap: 64px;
  margin-bottom: 48px;
}

.footer-brand p {
  font-size: 13px;
  line-height: 1.7;
  max-width: 280px;
  margin-top: 16px;
}

.footer-col h4 {
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  color: #fff;
  margin-bottom: 20px;
}

.footer-col ul {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.footer-col ul a {
  font-size: 13px;
  color: rgba(255, 255, 255, 0.55);
  transition: color 0.2s ease;
}

.footer-col ul a:hover {
  color: var(--accent);
}

.footer-bottom {
  border-top: 1px solid rgba(255, 255, 255, 0.1);
  padding-top: 28px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.footer-bottom p {
  font-size: 12px;
  color: rgba(255, 255, 255, 0.3);
}

.footer-dots {
  display: flex;
  gap: 8px;
}

.footer-dot {
  width: 8px;
  height: 8px;
  border-radius: 50%;
  background-color: rgba(255, 255, 255, 0.2);
}

.footer-dot.active {
  background-color: var(--accent);
}

/* ============================================
   ANIMATIONS
   ============================================ */

@keyframes fadeUp {
  from {
    opacity: 0;
    transform: translateY(28px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ============================================
   RESPONSIVE — TABLET (max 1024px)
   ============================================ */

@media (max-width: 1024px) {
  nav {
    padding: 0 28px;
  }

  .hero-content,
  .about,
  .features,
  .products,
  .subscribe,
  .news,
  .collection,
  .testimonials,
  .location,
  footer {
    padding-left: 40px;
    padding-right: 40px;
  }

  .features {
    grid-template-columns: 1fr;
    gap: 40px;
  }

  .features-grid {
    grid-template-columns: repeat(3, 1fr);
  }

  .collection-grid {
    grid-template-rows: repeat(2, 200px);
  }
}

/* ============================================
   RESPONSIVE — MOBILE (max 768px)
   ============================================ */

@media (max-width: 768px) {
  nav {
    padding: 0 20px;
  }

  .nav-links,
  .nav-phone {
    display: none;
  }

  .hero-content {
    padding: 0 24px;
  }

  .about,
  .features,
  .products,
  .news,
  .collection,
  .testimonials,
  .location,
  footer {
    padding-left: 20px;
    padding-right: 20px;
  }

  .about-grid {
    grid-template-columns: 1fr;
  }

  .features {
    grid-template-columns: 1fr;
  }

  .features-grid {
    grid-template-columns: 1fr;
    gap: 24px;
  }

  .products-grid {
    grid-template-columns: 1fr;
  }

  .subscribe {
    flex-direction: column;
    align-items: flex-start;
    padding: 48px 20px;
  }

  .subscribe-form {
    flex: 1;
    width: 100%;
  }

  .gallery {
    grid-template-columns: 1fr;
  }

  .gallery-right {
    grid-template-rows: auto;
    grid-template-columns: 1fr 1fr;
  }

  .gallery-right > div {
    height: 200px;
  }

  .news-grid {
    grid-template-columns: 1fr;
  }

  .collection-header {
    flex-direction: column;
    align-items: flex-start;
    gap: 12px;
  }

  .collection-grid {
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(3, 180px);
  }

  .location-grid {
    grid-template-columns: 1fr;
  }

  .footer-grid {
    grid-template-columns: 1fr;
    gap: 32px;
  }
}


https://youtu.be/AeEOQdVEKT0 
