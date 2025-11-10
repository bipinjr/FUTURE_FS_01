# FUTURE_FS_01 - Personal Professional Portfolio

## Full Stack Web Development Internship - Task 1

### Project Description
A modern, responsive personal portfolio website showcasing skills, projects, and professional information.

### Features
- ✅ Responsive design (mobile-first approach)
- ✅ Smooth scrolling navigation
- ✅ Skills section with progress bars
- ✅ Projects showcase
- ✅ Contact form
- ✅ Professional design with modern UI

### Technologies Used
- HTML5
- CSS3
- JavaScript (Vanilla)
- Font Awesome Icons

### File Structure
```
FUTURE_FS_01/
├── index.html        # Main HTML file
├── styles.css        # CSS styling
├── script.js         # JavaScript functionality
└── README.md         # Project documentation
```

### Installation & Setup
1. Clone this repository
2. Open `index.html` in your web browser
3. Customize the content with your personal information

### Customization Guide
1. **Personal Information**: Edit `index.html` to add your name, email, phone, and location
2. **Skills**: Modify the skills section to match your expertise
3. **Projects**: Update project cards with your actual projects
4. **Styling**: Adjust colors and fonts in `styles.css`

### How to Deploy
You can deploy this portfolio using:
- **GitHub Pages**: Push to GitHub and enable Pages in settings
- **Netlify**: Drag and drop your folder to Netlify
- **Vercel**: Import your repository to Vercel

### Screenshots
_(Add screenshots of your portfolio here)_

### Future Enhancements
- Add blog section
- Integrate backend for contact form
- Add dark mode toggle
- Include testimonials section
- Add animations and transitions

### Author
- GitHub: [bipinjr](https://github.com/bipinjr)
- Future Interns - Full Stack Web Development Internship

### License
This project is open source and available under the MIT License.

---

## Complete Code Files

### styles.css
Create a file named `styles.css` with the following content:

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
    color: #333;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

/* Navbar */
.navbar {
    background: #2c3e50;
    color: white;
    padding: 1rem 0;
    position: sticky;
    top: 0;
    z-index: 100;
}

.navbar .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.nav-brand {
    font-size: 1.5rem;
    font-weight: bold;
}

.nav-menu {
    display: flex;
    list-style: none;
    gap: 2rem;
}

.nav-menu a {
    color: white;
    text-decoration: none;
    transition: color 0.3s;
}

.nav-menu a:hover {
    color: #3498db;
}

/* Hero Section */
.hero {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 100px 0;
    text-align: center;
}

.hero h1 {
    font-size: 3rem;
    margin-bottom: 1rem;
}

.highlight {
    color: #f39c12;
}

.hero h2 {
    font-size: 1.8rem;
    margin-bottom: 1rem;
}

.hero-buttons {
    margin-top: 2rem;
    display: flex;
    gap: 1rem;
    justify-content: center;
}

.btn {
    padding: 12px 30px;
    border-radius: 5px;
    text-decoration: none;
    font-weight: bold;
    transition: all 0.3s;
}

.btn-primary {
    background: #3498db;
    color: white;
}

.btn-primary:hover {
    background: #2980b9;
    transform: translateY(-2px);
}

.btn-secondary {
    background: transparent;
    color: white;
    border: 2px solid white;
}

/* About Section */
.about {
    padding: 80px 0;
    background: #f8f9fa;
}

.section-title {
    text-align: center;
    font-size: 2.5rem;
    margin-bottom: 3rem;
    color: #2c3e50;
}

/* Skills Section */
.skills {
    padding: 80px 0;
}

.skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
}

.skill-card {
    background: white;
    padding: 2rem;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    text-align: center;
    transition: transform 0.3s;
}

.skill-card:hover {
    transform: translateY(-5px);
}

/* Projects Section */
.projects {
    padding: 80px 0;
    background: #f8f9fa;
}

.projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
}

.project-card {
    background: white;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    transition: transform 0.3s;
}

.project-card:hover {
    transform: translateY(-5px);
}

.project-card h3 {
    padding: 1.5rem;
    background: #3498db;
    color: white;
}

.project-card p {
    padding: 1rem 1.5rem;
}

/* Contact Section */
.contact {
    padding: 80px 0;
}

.contact-form {
    max-width: 600px;
    margin: 0 auto;
}

.contact-form input,
.contact-form textarea {
    width: 100%;
    padding: 12px;
    margin-bottom: 1rem;
    border: 1px solid #ddd;
    border-radius: 5px;
}

.contact-form button {
    width: 100%;
    padding: 12px;
    border: none;
    cursor: pointer;
}

/* Footer */
.footer {
    background: #2c3e50;
    color: white;
    text-align: center;
    padding: 2rem 0;
}

@media (max-width: 768px) {
    .hero h1 { font-size: 2rem; }
    .hero h2 { font-size: 1.2rem; }
    .nav-menu { flex-direction: column; gap: 1rem; }
}
```

### script.js
Create a file named `script.js` with the following content:

```javascript
// Smooth scrolling for navigation links
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
            target.scrollIntoView({
                behavior: 'smooth',
                block: 'start'
            });
        }
    });
});

// Contact form handling
const contactForm = document.getElementById('contactForm');
if (contactForm) {
    contactForm.addEventListener('submit', function(e) {
        e.preventDefault();
        
        // Get form values
        const formData = new FormData(this);
        
        // Display success message
        alert('Thank you for your message! I will get back to you soon.');
        
        // Reset form
        this.reset();
    });
}

// Navbar scroll effect
window.addEventListener('scroll', function() {
    const navbar = document.querySelector('.navbar');
    if (window.scrollY > 50) {
        navbar.style.boxShadow = '0 2px 10px rgba(0,0,0,0.1)';
    } else {
        navbar.style.boxShadow = 'none';
    }
});
```

---

### Deployment Instructions

1. **GitHub Pages**:
   - Go to repository Settings
   - Navigate to Pages section
   - Select main branch as source
   - Save and wait for deployment

2. **Netlify**:
   - Sign up on Netlify
   - Drag and drop your project folder
   - Site will be deployed instantly

3. **Vercel**:
   - Import repository to Vercel
   - Configure settings (if needed)
   - Deploy

---

### Task Completion Checklist
- [x] Created repository with naming convention FUTURE_FS_01
- [x] Added index.html with portfolio structure
- [x] Created responsive CSS styling
- [x] Added JavaScript functionality
- [x] Documented project in README
- [ ] Deployed to hosting platform
- [ ] Posted on LinkedIn

### LinkedIn Post Template
```
🚀 Excited to share my first task completion for the Full Stack Web Development Internship at Future Interns!

Task 1: Personal Professional Portfolio Website ✅

✨ Features:
- Responsive design
- Modern UI/UX
- Interactive sections
- Contact form

🔧 Technologies: HTML5, CSS3, JavaScript

🔗 GitHub: [Your Repository Link]
🌐 Live Demo: [Your Deployed Link]

#FutureInterns #WebDevelopment #FullStack #Portfolio #HTML #CSS #JavaScript #InternshipJourney
```

---

**Note**: Remember to customize all content with your personal information before deployment!
