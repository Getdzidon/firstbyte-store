# FirstByte Marketplace

> ⚠️ **This is a test website built for demonstration purposes only.**

A fully featured e-commerce storefront demo built with HTML, CSS, and vanilla JavaScript. Deployed on AWS EC2 with a custom domain via Route 53 and SSL via AWS Certificate Manager.

---

## 🌐 Live Demo

Hosted on AWS EC2 behind an Application Load Balancer with HTTPS enabled.

---

## 📁 Project Structure

```
firstbyte-website/
├── index.html          # Main storefront page
├── faq.html            # Frequently Asked Questions
├── shipping.html       # Shipping information
├── returns.html        # Returns & refunds policy
├── privacy.html        # Privacy policy
├── terms.html          # Terms of service
├── 404.html            # Custom 404 error page
├── css/
│   ├── styles.css      # Main stylesheet (variables, layout, components)
│   └── pages.css       # Inner page styles (FAQ, prose, info cards, 404)
├── images/
│   ├── FirstByte Logo1.png
│   ├── Favicon.png
│   ├── hero-banner.jpg
│   └── [product images]
└── .github/
    └── workflows/
        └── ec2.yml     # GitHub Actions CI/CD deploy workflow
```

---

## ✨ Features

### Storefront
- Responsive product grid with category filter (All, Audio, Wearable, Gaming, Mobile, Accessories, Laptop)
- Product cards with image zoom on hover, star ratings, and Hot/New/Sale badges
- Discounted products show crossed-out original price alongside sale price
- Quick View modal for product details without leaving the page
- Add to Cart with live cart sidebar, item quantities, remove items, and running total

### UI & Experience
- Dark / Light mode toggle (persists across scroll)
- Sticky header with frosted glass effect on scroll
- Smooth scroll navigation
- Animated hero section
- Scroll-to-top button
- Toast notifications for cart actions and form submissions
- Animated stats counter in the About section

### Pages
- **FAQ** — accordion-style expandable questions and answers
- **Shipping Info** — delivery tiers, tracking, and international shipping details
- **Returns** — step-by-step return process and refund timeline
- **Privacy Policy** — data collection, usage, and user rights
- **Terms of Service** — usage terms, liability, and intellectual property
- **404** — custom not-found page with navigation back to the store

### Customer Reviews
- Review cards with star ratings, quotes, and verified buyer avatars

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML5, CSS3, Vanilla JavaScript |
| Fonts | Google Fonts — Inter |
| Hosting | AWS EC2 (Amazon Linux) |
| Load Balancer | AWS Application Load Balancer |
| DNS | AWS Route 53 |
| SSL | AWS Certificate Manager (ACM) |
| CI/CD | GitHub Actions |

---

## 🚀 Deployment

Deployments are automated via GitHub Actions. On every push to `main`, the workflow SSHs into the EC2 instance and syncs the latest files.

### Infrastructure Overview
```
User → Route 53 (DNS) → ALB (HTTPS:443) → EC2 Instance (HTTP:80)
                          ↑
                    ACM Certificate
```

- HTTP traffic on port 80 is automatically redirected to HTTPS by the ALB listener rule
- The ACM certificate is attached to the ALB HTTPS listener
- EC2 security group only allows inbound traffic from the ALB security group

---

## 📦 Products

| Product | Category | Price |
|---|---|---|
| Wireless Headphone | Audio | $49.99 ~~$69.99~~ |
| Smartwatch | Wearable | $89.99 |
| Gaming Mouse | Gaming | $29.99 |
| Earbuds Pro | Audio | $34.99 ~~$54.99~~ |
| Phone Stand | Mobile | $14.99 |
| USB-C Hub | Accessories | $39.99 |
| Laptop Sleeve | Laptop | $19.99 |
| Gaming Keyboard | Gaming | $59.99 ~~$79.99~~ |
| Fitness Tracker | Wearable | $44.99 |

---

## 📄 License

This project is for demonstration purposes only and is not intended for commercial use.
