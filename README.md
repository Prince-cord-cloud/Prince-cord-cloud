## Hi there 👋

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GitHub Overview - Professional Profile</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #2d333b;
            --secondary-color: #22272e;
            --accent-color: #539bf5;
            --text-color: #cdd9e5;
            --text-secondary: #768390;
            --card-bg: rgba(34, 39, 46, 0.8);
            --border-color: #444c56;
            --success: #57ab5a;
            --warning: #e09b13;
            --danger: #e5534b;
            --gradient: linear-gradient(135deg, #539bf5 0%, #9775fa 100%);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', -apple-system, BlinkMacSystemFont, sans-serif;
        }

        body {
            background-color: var(--primary-color);
            color: var(--text-color);
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }

        .github-overview {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            margin-bottom: 40px;
            padding-bottom: 20px;
            border-bottom: 1px solid var(--border-color);
        }

        .profile-section {
            display: flex;
            align-items: center;
            gap: 20px;
            flex-wrap: wrap;
        }

        .avatar {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid var(--accent-color);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s ease;
        }

        .avatar:hover {
            transform: scale(1.05);
        }

        .profile-info h1 {
            font-size: 2.5rem;
            margin-bottom: 5px;
            background: var(--gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .profile-info p {
            color: var(--text-secondary);
            font-size: 1.2rem;
            margin-bottom: 10px;
        }

        .profile-info .location {
            display: flex;
            align-items: center;
            gap: 8px;
            color: var(--text-secondary);
            margin-top: 5px;
        }

        .stats {
            display: flex;
            gap: 20px;
            margin-top: 15px;
        }

        .stat-item {
            text-align: center;
        }

        .stat-value {
            font-size: 1.8rem;
            font-weight: bold;
            color: var(--accent-color);
        }

        .stat-label {
            font-size: 0.9rem;
            color: var(--text-secondary);
        }

        .theme-toggle {
            background: var(--card-bg);
            border: 1px solid var(--border-color);
            color: var(--text-color);
            padding: 8px 15px;
            border-radius: 6px;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: all 0.3s;
        }

        .theme-toggle:hover {
            background: var(--border-color);
        }

        .main-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin-bottom: 40px;
        }

        .card {
            background: var(--card-bg);
            border-radius: 12px;
            padding: 25px;
            border: 1px solid var(--border-color);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
        }

        .card h2 {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 20px;
            font-size: 1.4rem;
            color: var(--accent-color);
        }

        .card h2 i {
            font-size: 1.2rem;
        }

        .skills-list {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 15px;
        }

        .skill-tag {
            background: rgba(83, 155, 245, 0.1);
            color: var(--accent-color);
            padding: 6px 12px;
            border-radius: 20px;
            font-size: 0.9rem;
            border: 1px solid rgba(83, 155, 245, 0.3);
            transition: all 0.3s;
        }

        .skill-tag:hover {
            background: rgba(83, 155, 245, 0.2);
            transform: scale(1.05);
        }

        .project-item {
            margin-bottom: 15px;
            padding-bottom: 15px;
            border-bottom: 1px solid var(--border-color);
        }

        .project-item:last-child {
            margin-bottom: 0;
            padding-bottom: 0;
            border-bottom: none;
        }

        .project-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 8px;
        }

        .project-title {
            font-weight: 600;
            color: var(--accent-color);
            text-decoration: none;
            font-size: 1.1rem;
        }

        .project-title:hover {
            text-decoration: underline;
        }

        .project-tag {
            background: var(--secondary-color);
            color: var(--text-secondary);
            padding: 3px 8px;
            border-radius: 12px;
            font-size: 0.8rem;
        }

        .project-description {
            color: var(--text-secondary);
            font-size: 0.95rem;
        }

        .project-stats {
            display: flex;
            gap: 15px;
            margin-top: 10px;
            font-size: 0.9rem;
        }

        .project-stat {
            display: flex;
            align-items: center;
            gap: 5px;
            color: var(--text-secondary);
        }

        .contact-links {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .contact-link {
            display: flex;
            align-items: center;
            gap: 12px;
            text-decoration: none;
            color: var(--text-color);
            padding: 12px 15px;
            border-radius: 8px;
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid var(--border-color);
            transition: all 0.3s;
        }

        .contact-link:hover {
            background: rgba(83, 155, 245, 0.1);
            border-color: var(--accent-color);
            transform: translateX(5px);
        }

        .contact-link i {
            font-size: 1.2rem;
            color: var(--accent-color);
            width: 24px;
        }

        .footer {
            text-align: center;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid var(--border-color);
            color: var(--text-secondary);
            font-size: 0.9rem;
        }

        .highlight {
            color: var(--accent-color);
        }

        /* Dark/Light Theme Toggle */
        body.light-theme {
            --primary-color: #f6f8fa;
            --secondary-color: #ffffff;
            --text-color: #24292f;
            --text-secondary: #57606a;
            --card-bg: rgba(255, 255, 255, 0.9);
            --border-color: #d0d7de;
            --gradient: linear-gradient(135deg, #0969da 0%, #8250df 100%);
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .header {
                flex-direction: column;
                align-items: flex-start;
                gap: 20px;
            }

            .profile-info h1 {
                font-size: 2rem;
            }

            .avatar {
                width: 100px;
                height: 100px;
            }

            .main-content {
                grid-template-columns: 1fr;
            }

            .stats {
                justify-content: space-between;
                width: 100%;
            }
        }

        @media (max-width: 480px) {
            .github-overview {
                padding: 10px;
            }

            .profile-section {
                flex-direction: column;
                align-items: flex-start;
            }

            .stats {
                flex-wrap: wrap;
            }

            .card {
                padding: 20px;
            }
        }

        /* Animation for stats */
        @keyframes countUp {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .animated-stat {
            animation: countUp 0.8s ease-out;
        }
    </style>
</head>
<body>
    <div class="github-overview">
        <div class="header">
            <div class="profile-section">
                <img src="https://avatars.githubusercontent.com/u/583231?v=4" alt="Profile Avatar" class="avatar">
                <div class="profile-info">
                    <h1>Alex Johnson</h1>
                    <p>Full Stack Developer & Open Source Contributor</p>
                    <div class="location">
                        <i class="fas fa-map-marker-alt"></i>
                        <span>San Francisco, CA</span>
                    </div>
                    <div class="stats">
                        <div class="stat-item">
                            <div class="stat-value" id="repo-count">24</div>
                            <div class="stat-label">Repositories</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-value" id="follower-count">142</div>
                            <div class="stat-label">Followers</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-value" id="following-count">86</div>
                            <div class="stat-label">Following</div>
                        </div>
                    </div>
                </div>
            </div>
            <button class="theme-toggle" id="themeToggle">
                <i class="fas fa-moon"></i>
                <span>Dark Mode</span>
            </button>
        </div>

        <div class="main-content">
            <div class="card">
                <h2><i class="fas fa-user"></i> About Me</h2>
                <p>I'm a passionate full-stack developer with 5+ years of experience building scalable web applications. I love open-source and contribute regularly to various projects.</p>
                <p>Currently focused on <span class="highlight">React, Node.js, and Cloud Technologies</span>. Always eager to learn new technologies and collaborate on interesting projects.</p>
                
                <h3 style="margin-top: 20px; margin-bottom: 10px; font-size: 1.2rem;">Skills</h3>
                <div class="skills-list">
                    <span class="skill-tag">JavaScript</span>
                    <span class="skill-tag">TypeScript</span>
                    <span class="skill-tag">React</span>
                    <span class="skill-tag">Node.js</span>
                    <span class="skill-tag">Python</span>
                    <span class="skill-tag">AWS</span>
                    <span class="skill-tag">Docker</span>
                    <span class="skill-tag">MongoDB</span>
                    <span class="skill-tag">GraphQL</span>
                    <span class="skill-tag">Kubernetes</span>
                </div>
            </div>

            <div class="card">
                <h2><i class="fas fa-code-branch"></i> Featured Projects</h2>
                
                <div class="project-item">
                    <div class="project-header">
                        <a href="#" class="project-title">React Dashboard Framework</a>
                        <span class="project-tag">TypeScript</span>
                    </div>
                    <p class="project-description">A customizable admin dashboard framework built with React and TypeScript.</p>
                    <div class="project-stats">
                        <div class="project-stat">
                            <i class="fas fa-star"></i>
                            <span>342</span>
                        </div>
                        <div class="project-stat">
                            <i class="fas fa-code-branch"></i>
                            <span>45</span>
                        </div>
                        <div class="project-stat">
                            <i class="fas fa-circle"></i>
                            <span>Updated 2 days ago</span>
                        </div>
                    </div>
                </div>
                
                <div class="project-item">
                    <div class="project-header">
                        <a href="#" class="project-title">E-commerce API</a>
                        <span class="project-tag">Node.js</span>
                    </div>
                    <p class="project-description">A scalable REST API for e-commerce applications with payment integration.</p>
                    <div class="project-stats">
                        <div class="project-stat">
                            <i class="fas fa-star"></i>
                            <span>187</span>
                        </div>
                        <div class="project-stat">
                            <i class="fas fa-code-branch"></i>
                            <span>23</span>
                        </div>
                        <div class="project-stat">
                            <i class="fas fa-circle"></i>
                            <span>Updated 1 week ago</span>
                        </div>
                    </div>
                </div>
                
                <div class="project-item">
                    <div class="project-header">
                        <a href="#" class="project-title">DevOps CLI Tool</a>
                        <span class="project-tag">Python</span>
                    </div>
                    <p class="project-description">Command-line interface for automating deployment workflows across cloud providers.</p>
                    <div class="project-stats">
                        <div class="project-stat">
                            <i class="fas fa-star"></i>
                            <span>89</span>
                        </div>
                        <div class="project-stat">
                            <i class="fas fa-code-branch"></i>
                            <span>12</span>
                        </div>
                        <div class="project-stat">
                            <i class="fas fa-circle"></i>
                            <span>Updated 3 weeks ago</span>
                        </div>
                    </div>
                </div>
            </div>

            <div class="card">
                <h2><i class="fas fa-envelope"></i> Contact & Links</h2>
                <div class="contact-links">
                    <a href="mailto:alex@example.com" class="contact-link">
                        <i class="fas fa-envelope"></i>
                        <div>
                            <div style="font-weight: 600;">Email</div>
                            <div style="font-size: 0.9rem; color: var(--text-secondary);">alex@example.com</div>
                        </div>
                    </a>
                    
                    <a href="https://linkedin.com/in/alexjohnson" target="_blank" class="contact-link">
                        <i class="fab fa-linkedin"></i>
                        <div>
                            <div style="font-weight: 600;">LinkedIn</div>
                            <div style="font-size: 0.9rem; color: var(--text-secondary);">/in/alexjohnson</div>
                        </div>
                    </a>
                    
                    <a href="https://twitter.com/alexdev" target="_blank" class="contact-link">
                        <i class="fab fa-twitter"></i>
                        <div>
                            <div style="font-weight: 600;">Twitter</div>
                            <div style="font-size: 0.9rem; color: var(--text-secondary);">@alexdev</div>
                        </div>
                    </a>
                    
                    <a href="https://alexjohnson.dev" target="_blank" class="contact-link">
                        <i class="fas fa-globe"></i>
                        <div>
                            <div style="font-weight: 600;">Portfolio Website</div>
                            <div style="font-size: 0.9rem; color: var(--text-secondary);">alexjohnson.dev</div>
                        </div>
                    </a>
                </div>
                
                <h3 style="margin-top: 25px; margin-bottom: 10px; font-size: 1.2rem;">Currently Learning</h3>
                <div class="skills-list">
                    <span class="skill-tag">Rust</span>
                    <span class="skill-tag">WebAssembly</span>
                    <span class="skill-tag">Edge Computing</span>
                </div>
            </div>
        </div>

        <div class="footer">
            <p>© <span id="current-year">2023</span> Alex Johnson. All rights reserved.</p>
            <p style="margin-top: 5px;">This profile is updated regularly. Last updated: <span id="current-date">June 2023</span></p>
        </div>
    </div>

    <script>
        // Theme Toggle
        const themeToggle = document.getElementById('themeToggle');
        const themeIcon = themeToggle.querySelector('i');
        const themeText = themeToggle.querySelector('span');
        
        themeToggle.addEventListener('click', () => {
            document.body.classList.toggle('light-theme');
            
            if (document.body.classList.contains('light-theme')) {
                themeIcon.className = 'fas fa-sun';
                themeText.textContent = 'Light Mode';
            } else {
                themeIcon.className = 'fas fa-moon';
                themeText.textContent = 'Dark Mode';
            }
        });

        // Animated Stats Counter
        function animateCounter(element, target) {
            let current = 0;
            const increment = target / 50;
            const timer = setInterval(() => {
                current += increment;
                if (current >= target) {
                    element.textContent = target;
                    element.classList.add('animated-stat');
                    clearInterval(timer);
                } else {
                    element.textContent = Math.floor(current);
                }
            }, 30);
        }

        // Initialize counters when page loads
        document.addEventListener('DOMContentLoaded', () => {
            // Animate stats
            animateCounter(document.getElementById('repo-count'), 24);
            animateCounter(document.getElementById('follower-count'), 142);
            animateCounter(document.getElementById('following-count'), 86);
            
            // Set current year and date
            const currentYear = new Date().getFullYear();
            document.getElementById('current-year').textContent = currentYear;
            
            const options = { year: 'numeric', month: 'long' };
            const currentDate = new Date().toLocaleDateString('en-US', options);
            document.getElementById('current-date').textContent = currentDate;
            
            // Add hover effects to skill tags
            const skillTags = document.querySelectorAll('.skill-tag');
            skillTags.forEach(tag => {
                tag.addEventListener('mouseenter', function() {
                    this.style.transform = 'scale(1.05)';
                });
                
                tag.addEventListener('mouseleave', function() {
                    this.style.transform = 'scale(1)';
                });
            });
            
            // Simulate real-time follower count update (for demo purposes)
            setTimeout(() => {
                const followerElement = document.getElementById('follower-count');
                const newCount = parseInt(followerElement.textContent) + 1;
                followerElement.textContent = newCount;
                followerElement.classList.add('animated-stat');
                
                setTimeout(() => {
                    followerElement.classList.remove('animated-stat');
                }, 1000);
            }, 5000);
        });
    </script>
</body>
</html>
