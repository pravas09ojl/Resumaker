# Resumaker
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modern Resume & Cover Letter Builder</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        /* Global Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f5f7fa;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 20px 0;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 24px;
            font-weight: 700;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 30px;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
        }
        
        .nav-links a:hover {
            opacity: 0.8;
        }
        
        .btn {
            display: inline-block;
            background: white;
            color: #667eea;
            padding: 10px 20px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        /* Hero Section */
        .hero {
            padding: 80px 0;
            text-align: center;
        }
        
        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
            color: #2c3e50;
        }
        
        .hero p {
            font-size: 20px;
            color: #7f8c8d;
            max-width: 700px;
            margin: 0 auto 40px;
        }
        
        /* Builder Sections */
        .builder-section {
            padding: 60px 0;
            background: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            margin-bottom: 40px;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 40px;
            color: #2c3e50;
        }
        
        .section-title h2 {
            font-size: 36px;
            margin-bottom: 15px;
        }
        
        .section-title p {
            color: #7f8c8d;
            max-width: 600px;
            margin: 0 auto;
        }
        
        /* Form Styles */
        .builder-form {
            max-width: 800px;
            margin: 0 auto;
            padding: 30px;
            background: #f9f9f9;
            border-radius: 8px;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
            color: #2c3e50;
        }
        
        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 6px;
            font-family: 'Poppins', sans-serif;
            font-size: 16px;
            transition: all 0.3s ease;
        }
        
        .form-control:focus {
            border-color: #667eea;
            outline: none;
            box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.2);
        }
        
        textarea.form-control {
            min-height: 120px;
            resize: vertical;
        }
        
        .form-row {
            display: flex;
            gap: 20px;
        }
        
        .form-row .form-group {
            flex: 1;
        }
        
        .btn-primary {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border: none;
            padding: 12px 30px;
            border-radius: 30px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            display: inline-block;
            text-align: center;
        }
        
        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        /* Preview Section */
        .preview-section {
            margin-top: 40px;
            padding: 30px;
            background: white;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .preview-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
        }
        
        .preview-actions button {
            margin-left: 10px;
        }
        
        .resume-preview, .letter-preview {
            border: 1px solid #eee;
            padding: 30px;
            min-height: 500px;
            background: white;
        }
        
        /* Blog Section */
        .blog-section {
            padding: 80px 0;
        }
        
        .blog-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }
        
        .blog-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
        }
        
        .blog-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .blog-image {
            height: 200px;
            background: #ddd;
            background-size: cover;
            background-position: center;
        }
        
        .blog-content {
            padding: 20px;
        }
        
        .blog-content h3 {
            margin-bottom: 10px;
            color: #2c3e50;
        }
        
        .blog-content p {
            color: #7f8c8d;
            margin-bottom: 15px;
        }
        
        .read-more {
            color: #667eea;
            text-decoration: none;
            font-weight: 500;
        }
        
        /* Footer */
        footer {
            background: #2c3e50;
            color: white;
            padding: 50px 0 20px;
            text-align: center;
        }
        
        .footer-links {
            display: flex;
            justify-content: center;
            list-style: none;
            margin-bottom: 30px;
        }
        
        .footer-links li {
            margin: 0 15px;
        }
        
        .footer-links a {
            color: white;
            text-decoration: none;
        }
        
        .copyright {
            color: rgba(255, 255, 255, 0.7);
            font-size: 14px;
        }
        
        /* Responsive Styles */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 36px;
            }
            
            .form-row {
                flex-direction: column;
                gap: 0;
            }
            
            .preview-header {
                flex-direction: column;
                align-items: flex-start;
            }
            
            .preview-actions {
                margin-top: 15px;
            }
            
            .preview-actions button {
                margin-left: 0;
                margin-right: 10px;
                margin-bottom: 10px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <div class="logo">ResumePro</div>
                <ul class="nav-links">
                    <li><a href="#resume-builder">Resume Builder</a></li>
                    <li><a href="#cover-letter">Cover Letter</a></li>
                    <li><a href="#blog">Blog</a></li>
                    <li><a href="#contact">Contact</a></li>
                    <li><a href="#" class="btn">Get Started</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h1>Create Professional Resumes & Cover Letters</h1>
            <p>Our free online builder helps you create modern, professional resumes and cover letters that get you hired. No design skills needed.</p>
            <a href="#resume-builder" class="btn-primary">Build Your Resume Now</a>
        </div>
    </section>

    <!-- Resume Builder Section -->
    <section id="resume-builder" class="builder-section">
        <div class="container">
            <div class="section-title">
                <h2>Resume Builder</h2>
                <p>Fill in your details and create a beautiful resume in minutes</p>
            </div>
            
            <div class="builder-form">
                <form id="resumeForm">
                    <div class="form-row">
                        <div class="form-group">
                            <label for="fullName">Full Name</label>
                            <input type="text" id="fullName" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="jobTitle">Professional Title</label>
                            <input type="text" id="jobTitle" class="form-control" required>
                        </div>
                    </div>
                    
                    <div class="form-row">
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="phone">Phone</label>
                            <input type="tel" id="phone" class="form-control" required>
                        </div>
                    </div>
                    
                    <div class="form-group">
                        <label for="address">Address</label>
                        <input type="text" id="address" class="form-control">
                    </div>
                    
                    <div class="form-group">
                        <label for="summary">Professional Summary</label>
                        <textarea id="summary" class="form-control" required></textarea>
                    </div>
                    
                    <div class="form-group">
                        <label>Work Experience</label>
                        <div id="experienceFields">
                            <div class="experience-entry">
                                <div class="form-row">
                                    <div class="form-group">
                                        <input type="text" class="form-control" placeholder="Job Title">
                                    </div>
                                    <div class="form-group">
                                        <input type="text" class="form-control" placeholder="Company">
                                    </div>
                                </div>
                                <div class="form-row">
                                    <div class="form-group">
                                        <input type="text" class="form-control" placeholder="Start Date">
                                    </div>
                                    <div class="form-group">
                                        <input type="text" class="form-control" placeholder="End Date (or Present)">
                                    </div>
                                </div>
                                <div class="form-group">
                                    <textarea class="form-control" placeholder="Job Description"></textarea>
                                </div>
                            </div>
                        </div>
                        <button type="button" class="btn-primary" onclick="addExperienceField()">Add Another Position</button>
                    </div>
                    
                    <div class="form-group">
                        <label>Education</label>
                        <div id="educationFields">
                            <div class="education-entry">
                                <div class="form-row">
                                    <div class="form-group">
                                        <input type="text" class="form-control" placeholder="Degree">
                                    </div>
                                    <div class="form-group">
                                        <input type="text" class="form-control" placeholder="Institution">
                                    </div>
                                </div>
                                <div class="form-row">
                                    <div class="form-group">
                                        <input type="text" class="form-control" placeholder="Year Graduated">
                                    </div>
                                </div>
                            </div>
                        </div>
                        <button type="button" class="btn-primary" onclick="addEducationField()">Add Another Education</button>
                    </div>
                    
                    <div class="form-group">
                        <label>Skills</label>
                        <div id="skillFields">
                            <input type="text" class="form-control" placeholder="Skill (e.g., Project Management)">
                        </div>
                        <button type="button" class="btn-primary" onclick="addSkillField()">Add Another Skill</button>
                    </div>
                    
                    <button type="submit" class="btn-primary">Generate Resume</button>
                </form>
            </div>
            
            <div class="preview-section" id="resumePreviewSection" style="display: none;">
                <div class="preview-header">
                    <h3>Your Resume Preview</h3>
                    <div class="preview-actions">
                        <button class="btn-primary">Download PDF</button>
                        <button class="btn-primary">Print</button>
                    </div>
                </div>
                <div class="resume-preview" id="resumePreview">
                    <!-- Resume preview will be inserted here -->
                </div>
            </div>
        </div>
    </section>

    <!-- Cover Letter Builder Section -->
    <section id="cover-letter" class="builder-section">
        <div class="container">
            <div class="section-title">
                <h2>Cover Letter Builder</h2>
                <p>Create a personalized cover letter that complements your resume</p>
            </div>
            
            <div class="builder-form">
                <form id="coverLetterForm">
                    <div class="form-row">
                        <div class="form-group">
                            <label for="clFullName">Your Name</label>
                            <input type="text" id="clFullName" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="clJobTitle">Job Title You're Applying For</label>
                            <input type="text" id="clJobTitle" class="form-control" required>
                        </div>
                    </div>
                    
                    <div class="form-row">
                        <div class="form-group">
                            <label for="clCompany">Company Name</label>
                            <input type="text" id="clCompany" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="clHiringManager">Hiring Manager's Name (if known)</label>
                            <input type="text" id="clHiringManager" class="form-control">
                        </div>
                    </div>
                    
                    <div class="form-group">
                        <label for="clIntroduction">Introduction Paragraph</label>
                        <textarea id="clIntroduction" class="form-control" required></textarea>
                    </div>
                    
                    <div class="form-group">
                        <label for="clBody">Body Paragraph (Why you're a good fit)</label>
                        <textarea id="clBody" class="form-control" required></textarea>
                    </div>
                    
                    <div class="form-group">
                        <label for="clClosing">Closing Paragraph</label>
                        <textarea id="clClosing" class="form-control" required></textarea>
                    </div>
                    
                    <button type="submit" class="btn-primary">Generate Cover Letter</button>
                </form>
            </div>
            
            <div class="preview-section" id="letterPreviewSection" style="display: none;">
                <div class="preview-header">
                    <h3>Your Cover Letter Preview</h3>
                    <div class="preview-actions">
                        <button class="btn-primary">Download PDF</button>
                        <button class="btn-primary">Print</button>
                    </div>
                </div>
                <div class="letter-preview" id="letterPreview">
                    <!-- Cover letter preview will be inserted here -->
                </div>
            </div>
        </div>
    </section>

    <!-- Blog Section -->
    <section id="blog" class="blog-section">
        <div class="container">
            <div class="section-title">
                <h2>Career Resources & Tips</h2>
                <p>Learn how to create effective resumes and cover letters that get noticed</p>
            </div>
            
            <div class="blog-grid">
                <div class="blog-card">
                    <div class="blog-image" style="background-image: url('https://images.unsplash.com/photo-1450101499163-c8848c66ca85?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60');"></div>
                    <div class="blog-content">
                        <h3>10 Resume Mistakes You Must Avoid</h3>
                        <p>Learn about the most common resume mistakes that can cost you interviews and how to fix them.</p>
                        <a href="#" class="read-more">Read More</a>
                    </div>
                </div>
                
                <div class="blog-card">
                    <div class="blog-image" style="background-image: url('https://images.unsplash.com/photo-1521791136064-7986c2920216?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60');"></div>
                    <div class="blog-content">
                        <h3>How to Write a Cover Letter That Stands Out</h3>
                        <p>Discover the secrets to writing a cover letter that gets hiring managers excited to meet you.</p>
                        <a href="#" class="read-more">Read More</a>
                    </div>
                </div>
                
                <div class="blog-card">
                    <div class="blog-image" style="background-image: url('https://images.unsplash.com/photo-1522202176988-66273c2fd55f?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60');"></div>
                    <div class="blog-content">
                        <h3>Modern Resume Design Trends for 2023</h3>
                        <p>Stay ahead of the competition with these cutting-edge resume design trends that impress recruiters.</p>
                        <a href="#" class="read-more">Read More</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contact">
        <div class="container">
            <div class="logo">ResumePro</div>
            <ul class="footer-links">
                <li><a href="#resume-builder">Resume Builder</a></li>
                <li><a href="#cover-letter">Cover Letter</a></li>
                <li><a href="#blog">Blog</a></li>
                <li><a href="#">Privacy Policy</a></li>
                <li><a href="#">Terms of Service</a></li>
            </ul>
            <p class="copyright">© 2023 ResumePro. All rights reserved.</p>
        </div>
    </footer>

    <script>
        // Resume Form Handling
        document.getElementById('resumeForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Get form values
            const fullName = document.getElementById('fullName').value;
            const jobTitle = document.getElementById('jobTitle').value;
            const email = document.getElementById('email').value;
            const phone = document.getElementById('phone').value;
            const address = document.getElementById('address').value;
            const summary = document.getElementById('summary').value;
            
            // Generate HTML for resume preview
            let resumeHTML = `
                <div style="font-family: Arial, sans-serif; max-width: 800px; margin: 0 auto;">
                    <header style="background: #2c3e50; color: white; padding: 30px; text-align: center;">
                        <h1 style="margin: 0; font-size: 36px;">${fullName}</h1>
                        <p style="margin: 5px 0 0; font-size: 18px;">${jobTitle}</p>
                    </header>
                    
                    <div style="padding: 30px;">
                        <div style="display: flex; justify-content: space-between; margin-bottom: 20px; flex-wrap: wrap;">
                            <div style="margin-right: 20px;">Email: ${email}</div>
                            <div style="margin-right: 20px;">Phone: ${phone}</div>
                            <div>Address: ${address}</div>
                        </div>
                        
                        <section style="margin-bottom: 30px;">
                            <h2 style="border-bottom: 2px solid #2c3e50; padding-bottom: 5px; color: #2c3e50;">PROFESSIONAL SUMMARY</h2>
                            <p>${summary}</p>
                        </section>
                        
                        <section style="margin-bottom: 30px;">
                            <h2 style="border-bottom: 2px solid #2c3e50; padding-bottom: 5px; color: #2c3e50;">WORK EXPERIENCE</h2>
                            ${generateExperienceHTML()}
                        </section>
                        
                        <section style="margin-bottom: 30px;">
                            <h2 style="border-bottom: 2px solid #2c3e50; padding-bottom: 5px; color: #2c3e50;">EDUCATION</h2>
                            ${generateEducationHTML()}
                        </section>
                        
                        <section>
                            <h2 style="border-bottom: 2px solid #2c3e50; padding-bottom: 5px; color: #2c3e50;">SKILLS</h2>
                            ${generateSkillsHTML()}
                        </section>
                    </div>
                </div>
            `;
            
            // Insert into preview section
            document.getElementById('resumePreview').innerHTML = resumeHTML;
            document.getElementById('resumePreviewSection').style.display = 'block';
            
            // Scroll to preview
            document.getElementById('resumePreviewSection').scrollIntoView({ behavior: 'smooth' });
        });
        
        // Cover Letter Form Handling
        document.getElementById('coverLetterForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Get form values
            const fullName = document.getElementById('clFullName').value;
            const jobTitle = document.getElementById('clJobTitle').value;
            const company = document.getElementById('clCompany').value;
            const hiringManager = document.getElementById('clHiringManager').value || 'Hiring Manager';
            const introduction = document.getElementById('clIntroduction').value;
            const body = document.getElementById('clBody').value;
            const closing = document.getElementById('clClosing').value;
            
            // Generate HTML for cover letter preview
            let letterHTML = `
                <div style="font-family: Arial, sans-serif; max-width: 800px; margin: 0 auto; padding: 30px;">
                    <div style="text-align: right; margin-bottom: 30px;">
                        <p>${fullName}</p>
                        <p>${document.getElementById('email').value || 'your@email.com'}</p>
                        <p>${document.getElementById('phone').value || '(123) 456-7890'}</p>
                    </div>
                    
                    <div style="margin-bottom: 20px;">
                        <p>${new Date().toLocaleDateString('en-US', { month: 'long', day: 'numeric', year: 'numeric' })}</p>
                        <p>${hiringManager}</p>
                        <p>${company}</p>
                    </div>
                    
                    <div style="margin-bottom: 20px;">
                        <p>Dear ${hiringManager},</p>
                    </div>
                    
                    <div style="margin-bottom: 20px;">
                        <p>${introduction}</p>
                    </div>
                    
                    <div style="margin-bottom: 20px;">
                        <p>${body}</p>
                    </div>
                    
                    <div style="margin-bottom: 20px;">
                        <p>${closing}</p>
                    </div>
                    
                    <div style="margin-top: 40px;">
                        <p>Sincerely,</p>
                        <p>${fullName}</p>
                    </div>
                </div>
            `;
            
            // Insert into preview section
            document.getElementById('letterPreview').innerHTML = letterHTML;
            document.getElementById('letterPreviewSection').style.display = 'block';
            
            // Scroll to preview
            document.getElementById('letterPreviewSection').scrollIntoView({ behavior: 'smooth' });
        });
        
        // Helper functions for resume sections
        function generateExperienceHTML() {
            const experienceEntries = document.querySelectorAll('.experience-entry');
            let html = '';
            
            experienceEntries.forEach(entry => {
                const jobTitle = entry.querySelector('.form-row:nth-child(1) .form-group:nth-child(1) input').value;
                const company = entry.querySelector('.form-row:nth-child(1) .form-group:nth-child(2) input').value;
                const startDate = entry.querySelector('.form-row:nth-child(2) .form-group:nth-child(1) input').value;
                const endDate = entry.querySelector('.form-row:nth-child(2) .form-group:nth-child(2) input').value;
                const description = entry.querySelector('textarea').value;
                
                if (jobTitle || company) {
                    html += `
                        <div style="margin-bottom: 20px;">
                            <h3 style="margin: 0;">${jobTitle}</h3>
                            <div style="display: flex; justify-content: space-between; margin-bottom: 5px;">
                                <p style="margin: 0; font-weight: bold;">${company}</p>
                                <p style="margin: 0;">${startDate} - ${endDate}</p>
                            </div>
                            <p style="margin: 0;">${description}</p>
                        </div>
                    `;
                }
            });
            
            return html || '<p>No work experience added.</p>';
        }
        
        function generateEducationHTML() {
            const educationEntries = document.querySelectorAll('.education-entry');
            let html = '';
            
            educationEntries.forEach(entry => {
                const degree = entry.querySelector('.form-row:nth-child(1) .form-group:nth-child(1) input').value;
                const institution = entry.querySelector('.form-row:nth-child(1) .form-group:nth-child(2) input').value;
                const year = entry.querySelector('.form-row:nth-child(2) .form-group:nth-child(1) input').value;
                
                if (degree || institution) {
                    html += `
                        <div style="margin-bottom: 15px;">
                            <h3 style="margin: 0;">${degree}</h3>
                            <div style="display: flex; justify-content: space-between; margin-bottom: 5px;">
                                <p style="margin: 0; font-weight: bold;">${institution}</p>
                                <p style="margin: 0;">${year}</p>
                            </div>
                        </div>
                    `;
                }
            });
            
            return html || '<p>No education added.</p>';
        }
        
        function generateSkillsHTML() {
            const skillInputs = document.querySelectorAll('#skillFields input');
            let skills = [];
            
            skillInputs.forEach(input => {
                if (input.value.trim()) {
                    skills.push(input.value.trim());
                }
            });
            
            if (skills.length > 0) {
                return '<ul style="columns: 2; list-style-position: inside;">' + 
                       skills.map(skill => `<li>${skill}</li>`).join('') + 
                       '</ul>';
            }
            
            return '<p>No skills added.</p>';
        }
        
        // Add more fields functions
        function addExperienceField() {
            const experienceFields = document.getElementById('experienceFields');
            const newField = document.createElement('div');
            newField.className = 'experience-entry';
            newField.style.marginTop = '20px';
            newField.style.paddingTop = '20px';
            newField.style.borderTop = '1px dashed #ddd';
            newField.innerHTML = `
                <div class="form-row">
                    <div class="form-group">
                        <input type="text" class="form-control" placeholder="Job Title">
                    </div>
                    <div class="form-group">
                        <input type="text" class="form-control" placeholder="Company">
                    </div>
                </div>
                <div class="form-row">
                    <div class="form-group">
                        <input type="text" class="form-control" placeholder="Start Date">
                    </div>
                    <div class="form-group">
                        <input type="text" class="form-control" placeholder="End Date (or Present)">
                    </div>
                </div>
                <div class="form-group">
                    <textarea class="form-control" placeholder="Job Description"></textarea>
                </div>
                <button type="button" class="btn-primary" onclick="this.parentNode.remove()" style="background: #e74c3c;">Remove This Position</button>
            `;
            experienceFields.appendChild(newField);
        }
        
        function addEducationField() {
            const educationFields = document.getElementById('educationFields');
            const newField = document.createElement('div');
            newField.className = 'education-entry';
            newField.style.marginTop = '20px';
            newField.style.paddingTop = '20px';
            newField.style.borderTop = '1px dashed #ddd';
            newField.innerHTML = `
                <div class="form-row">
                    <div class="form-group">
                        <input type="text" class="form-control" placeholder="Degree">
                    </div>
                    <div class="form-group">
                        <input type="text" class="form-control" placeholder="Institution">
                    </div>
                </div>
                <div class="form-row">
                    <div class="form-group">
                        <input type="text" class="form-control" placeholder="Year Graduated">
                    </div>
                </div>
                <button type="button" class="btn-primary" onclick="this.parentNode.remove()" style="background: #e74c3c;">Remove This Education</button>
            `;
            educationFields.appendChild(newField);
        }
        
        function addSkillField() {
            const skillFields = document.getElementById('skillFields');
            const newField = document.createElement('input');
            newField.type = 'text';
            newField.className = 'form-control';
            newField.style.marginTop = '10px';
            newField.placeholder = 'Skill (e.g., Project Management)';
            skillFields.appendChild(newField);
        }
    </script>
</body>
</html>
