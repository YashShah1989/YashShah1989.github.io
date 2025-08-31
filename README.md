
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Yash Shah - Content Strategist & Research Analyst</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 50%, #f093fb 70%, #f5576c 100%);
            min-height: 100vh;
            animation: gradientShift 8s ease infinite;
        }

        @keyframes gradientShift {
            0%, 100% { background: linear-gradient(135deg, #667eea 0%, #764ba2 50%, #f093fb 70%, #f5576c 100%); }
            25% { background: linear-gradient(135deg, #4facfe 0%, #00f2fe 30%, #43e97b 60%, #38f9d7 100%); }
            50% { background: linear-gradient(135deg, #fa709a 0%, #fee140 30%, #667eea 60%, #764ba2 100%); }
            75% { background: linear-gradient(135deg, #a8edea 0%, #fed6e3 30%, #667eea 60%, #f093fb 100%); }
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .hero {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(20px);
            border-radius: 30px;
            padding: 60px 40px;
            margin-bottom: 30px;
            text-align: center;
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.15), 
                        0 0 0 1px rgba(255, 255, 255, 0.1),
                        inset 0 1px 0 rgba(255, 255, 255, 0.6);
            animation: fadeInUp 0.8s ease-out;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .profile-img {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            margin: 0 auto 30px;
            border: 6px solid transparent;
            background-clip: padding-box;
            position: relative;
            animation: profileGlow 3s ease-in-out infinite alternate;
            overflow: hidden;
            background: url('https://github.com/YashShah1989/yash-shah-portfolio/blob/main/download.png?raw=true') center/cover;
        }

        .profile-img::before {
            content: '';
            position: absolute;
            top: -6px;
            left: -6px;
            right: -6px;
            bottom: -6px;
            background: linear-gradient(45deg, #667eea, #764ba2, #f093fb, #f5576c, #4facfe, #00f2fe, #43e97b, #38f9d7);
            border-radius: 50%;
            z-index: -1;
            animation: rotate 4s linear infinite;
        }

        @keyframes profileGlow {
            0% { box-shadow: 0 0 20px rgba(102, 126, 234, 0.5); }
            100% { box-shadow: 0 0 40px rgba(245, 87, 108, 0.7), 0 0 60px rgba(67, 233, 123, 0.4); }
        }

        @keyframes rotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .hero h1 {
            font-size: 3.5em;
            margin-bottom: 10px;
            background: linear-gradient(45deg, #667eea, #f093fb, #f5576c, #43e97b);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: textShimmer 3s ease-in-out infinite;
            background-size: 300% 300%;
        }

        @keyframes textShimmer {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }

        .hero h2 {
            font-size: 1.8em;
            color: #666;
            margin-bottom: 20px;
            font-weight: 300;
        }

        .hero-stats {
            display: flex;
            justify-content: center;
            gap: 40px;
            margin-top: 30px;
            flex-wrap: wrap;
        }

        .stat {
            text-align: center;
        }

        .stat-number {
            font-size: 2.5em;
            font-weight: bold;
            color: #667eea;
            display: block;
        }

        .stat-label {
            font-size: 0.9em;
            color: #666;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .section {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(20px);
            border-radius: 25px;
            padding: 40px;
            margin-bottom: 30px;
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.1), 
                        0 0 0 1px rgba(255, 255, 255, 0.1),
                        inset 0 1px 0 rgba(255, 255, 255, 0.6);
            animation: fadeInUp 0.8s ease-out;
            border: 1px solid rgba(255, 255, 255, 0.2);
            position: relative;
            overflow: hidden;
        }

        .section::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 2px;
            background: linear-gradient(90deg, transparent, #667eea, #f093fb, #43e97b, transparent);
            animation: borderFlow 4s linear infinite;
        }

        @keyframes borderFlow {
            0% { left: -100%; }
            100% { left: 100%; }
        }

        .section h3 {
            font-size: 2.2em;
            margin-bottom: 30px;
            color: #333;
            position: relative;
            padding-bottom: 10px;
        }

        .section h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 80px;
            height: 4px;
            background: linear-gradient(45deg, #667eea, #f093fb, #43e97b, #38f9d7);
            border-radius: 2px;
            animation: gradientFlow 2s ease-in-out infinite;
        }

        @keyframes gradientFlow {
            0%, 100% { background: linear-gradient(45deg, #667eea, #f093fb, #43e97b, #38f9d7); }
            50% { background: linear-gradient(45deg, #f5576c, #4facfe, #764ba2, #f093fb); }
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 30px;
        }

        .skill-category {
            background: linear-gradient(135deg, rgba(255, 255, 255, 0.9), rgba(248, 249, 250, 0.8));
            padding: 30px;
            border-radius: 20px;
            border-left: 5px solid transparent;
            background-image: linear-gradient(135deg, rgba(255, 255, 255, 0.9), rgba(248, 249, 250, 0.8)),
                              linear-gradient(45deg, #667eea, #f093fb, #43e97b);
            background-origin: border-box;
            background-clip: padding-box, border-box;
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
        }

        .skill-category::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(102, 126, 234, 0.1), transparent);
            transition: left 0.6s ease;
        }

        .skill-category:hover::before {
            left: 100%;
        }

        .skill-category:hover {
            transform: translateY(-8px) scale(1.02);
            box-shadow: 0 20px 40px rgba(102, 126, 234, 0.2), 
                        0 0 30px rgba(67, 233, 123, 0.1);
        }

        .skill-category h4 {
            font-size: 1.4em;
            margin-bottom: 15px;
            color: #333;
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .skill-tag {
            background: linear-gradient(45deg, #667eea, #f093fb);
            color: white;
            padding: 10px 18px;
            border-radius: 25px;
            font-size: 0.9em;
            font-weight: 500;
            position: relative;
            overflow: hidden;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .skill-tag::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, #43e97b, #38f9d7);
            transition: left 0.3s ease;
            z-index: -1;
        }

        .skill-tag:hover::before {
            left: 0;
        }

        .skill-tag:hover {
            transform: scale(1.05);
            box-shadow: 0 5px 15px rgba(67, 233, 123, 0.4);
        }

        .experience-item {
            background: #f8f9fa;
            padding: 30px;
            border-radius: 15px;
            margin-bottom: 25px;
            border-left: 5px solid #667eea;
            transition: transform 0.3s ease;
        }

        .experience-item:hover {
            transform: translateX(10px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .job-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 15px;
            flex-wrap: wrap;
        }

        .job-title {
            font-size: 1.4em;
            font-weight: bold;
            color: #333;
        }

        .company {
            font-size: 1.2em;
            color: #667eea;
            margin-bottom: 5px;
        }

        .duration {
            background: #667eea;
            color: white;
            padding: 5px 15px;
            border-radius: 15px;
            font-size: 0.9em;
        }

        .achievements {
            margin-top: 15px;
        }

        .achievement {
            background: white;
            padding: 15px;
            margin-bottom: 10px;
            border-radius: 10px;
            border-left: 3px solid #28a745;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
            margin-top: 30px;
        }

        .project-card {
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            padding: 30px;
            border-radius: 15px;
            transition: transform 0.3s ease;
            border: 1px solid #e9ecef;
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        }

        .project-title {
            font-size: 1.3em;
            font-weight: bold;
            margin-bottom: 15px;
            color: #333;
        }

        .project-description {
            color: #666;
            margin-bottom: 20px;
            line-height: 1.6;
        }

        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 20px;
        }

        .project-tag {
            background: #667eea;
            color: white;
            padding: 5px 12px;
            border-radius: 12px;
            font-size: 0.8em;
        }

        .cta-button {
            background: linear-gradient(45deg, #667eea, #f093fb, #43e97b);
            color: white;
            padding: 18px 35px;
            border: none;
            border-radius: 30px;
            font-size: 1.1em;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.4s ease;
            text-decoration: none;
            display: inline-block;
            margin-top: 20px;
            position: relative;
            overflow: hidden;
            background-size: 300% 300%;
            animation: gradientShift 3s ease infinite;
        }

        .cta-button::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.3), transparent);
            transition: left 0.5s ease;
        }

        .cta-button:hover::before {
            left: 100%;
        }

        .cta-button:hover {
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 15px 35px rgba(102, 126, 234, 0.4), 
                        0 5px 15px rgba(67, 233, 123, 0.2);
        }

        .impact-metrics {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .metric-card {
            background: linear-gradient(135deg, #667eea, #f093fb, #43e97b);
            color: white;
            padding: 30px;
            border-radius: 20px;
            text-align: center;
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
            background-size: 300% 300%;
            animation: gradientShift 4s ease infinite;
        }

        .metric-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at center, rgba(255, 255, 255, 0.1) 0%, transparent 70%);
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .metric-card:hover::before {
            opacity: 1;
        }

        .metric-card:hover {
            transform: scale(1.08) translateY(-5px);
            box-shadow: 0 20px 40px rgba(102, 126, 234, 0.3);
        }

        .metric-number {
            font-size: 2.5em;
            font-weight: bold;
            display: block;
            margin-bottom: 10px;
        }

        .certifications {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .cert-item {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            transition: transform 0.3s ease;
        }

        .cert-item:hover {
            transform: scale(1.05);
        }

        .contact-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .contact-item {
            background: #f8f9fa;
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            transition: transform 0.3s ease;
        }

        .contact-item:hover {
            transform: translateY(-5px);
            background: linear-gradient(45deg, #667eea, #764ba2);
            color: white;
        }

        .nav-menu {
            position: fixed;
            top: 20px;
            right: 20px;
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 15px;
            z-index: 1000;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .nav-menu a {
            display: block;
            color: #333;
            text-decoration: none;
            padding: 10px 15px;
            border-radius: 8px;
            transition: all 0.3s ease;
            margin-bottom: 5px;
        }

        .nav-menu a:hover {
            background: #667eea;
            color: white;
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

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }

        @media (max-width: 768px) {
            .hero {
                padding: 40px 20px;
            }
            
            .hero h1 {
                font-size: 2.5em;
            }
            
            .hero-stats {
                gap: 20px;
            }
            
            .job-header {
                flex-direction: column;
                align-items: flex-start;
            }
            
            .nav-menu {
                position: relative;
                top: auto;
                right: auto;
                margin-bottom: 20px;
            }
        }
    </style>
</head>
<body>
    <nav class="nav-menu">
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#experience">Experience</a>
        <a href="#projects">Projects</a>
        <a href="#future">Future</a>
        <a href="#contact">Contact</a>
    </nav>

    <div class="container">
        <!-- Hero Section -->
        <section class="hero" id="about">
            <div class="profile-img"></div>
            <h1>Yash Shah</h1>
            <h2>Content Strategist • Consultant • Research Analyst</h2>
            <p style="font-size: 1.2em; color: #666; max-width: 800px; margin: 0 auto;">
                Results-driven Content Strategist with 14+ years of experience developing data-driven content strategies 
                that drive engagement, enhance SEO performance, and achieve business objectives in the financial services sector.
            </p>
            
            <div class="hero-stats">
                <div class="stat">
                    <span class="stat-number">14+</span>
                    <span class="stat-label">Years Experience</span>
                </div>
                <div class="stat">
                    <span class="stat-number">100+</span>
                    <span class="stat-label">Content Pieces</span>
                </div>
                <div class="stat">
                    <span class="stat-number">20%</span>
                    <span class="stat-label">Traffic Increase</span>
                </div>
            </div>

            <a href="https://bit.ly/YashContentPortfolio" target="_blank" class="cta-button">
                View My Work Portfolio
            </a>
        </section>

        <!-- Impact Metrics -->
        <section class="section">
            <h3>Key Impact Metrics</h3>
            <div class="impact-metrics">
                <div class="metric-card">
                    <span class="metric-number">20%</span>
                    <div>Website Traffic Increase through SEO Optimization</div>
                </div>
                <div class="metric-card">
                    <span class="metric-number">100+</span>
                    <div>Finance Articles Authored</div>
                </div>
                <div class="metric-card">
                    <span class="metric-number">3</span>
                    <div>Major Financial Clients Served</div>
                </div>
                <div class="metric-card">
                    <span class="metric-number">14+</span>
                    <div>Years of Strategic Experience</div>
                </div>
            </div>
        </section>

        <!-- Core Competencies -->
        <section class="section" id="skills">
            <h3>Core Competencies</h3>
            <div class="skills-grid">
                <div class="skill-category">
                    <h4>🎯 Content Strategy & Development</h4>
                    <div class="skill-tags">
                        <span class="skill-tag">Content Strategy</span>
                        <span class="skill-tag">Editorial Planning</span>
                        <span class="skill-tag">Brand Voice Development</span>
                        <span class="skill-tag">Content Audits</span>
                        <span class="skill-tag">Performance Analytics</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h4>🔮 Technology × Creativity</h4>
                    <div class="skill-tags">
                        <span class="skill-tag">AI Content Generation</span>
                        <span class="skill-tag">Data Visualization</span>
                        <span class="skill-tag">Creative Automation</span>
                        <span class="skill-tag">Digital Innovation</span>
                        <span class="skill-tag">Tech Storytelling</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h4>🧘 Mindful Strategy & Analysis</h4>
                    <div class="skill-tags">
                        <span class="skill-tag">Conscious Leadership</span>
                        <span class="skill-tag">Intuitive Insights</span>
                        <span class="skill-tag">Holistic Thinking</span>
                        <span class="skill-tag">Ethical Decision Making</span>
                        <span class="skill-tag">Purpose-Driven Content</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h4>🔍 Research & Analysis</h4>
                    <div class="skill-tags">
                        <span class="skill-tag">Market Research</span>
                        <span class="skill-tag">Data Analysis</span>
                        <span class="skill-tag">Financial Analysis</span>
                        <span class="skill-tag">Competitive Intelligence</span>
                        <span class="skill-tag">Trend Identification</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h4>🚀 Digital Marketing & SEO</h4>
                    <div class="skill-tags">
                        <span class="skill-tag">SEO Optimization</span>
                        <span class="skill-tag">Content Marketing</span>
                        <span class="skill-tag">WordPress CMS</span>
                        <span class="skill-tag">Growth Hacking</span>
                        <span class="skill-tag">Lead Generation</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h4>💼 Financial Expertise</h4>
                    <div class="skill-tags">
                        <span class="skill-tag">Financial Writing</span>
                        <span class="skill-tag">Investment Banking</span>
                        <span class="skill-tag">Mutual Funds</span>
                        <span class="skill-tag">Fintech Content</span>
                        <span class="skill-tag">Regulatory Compliance</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- Professional Experience -->
        <section class="section" id="experience">
            <h3>Professional Experience</h3>
            
            <div class="experience-item">
                <div class="job-header">
                    <div>
                        <div class="job-title">Content Strategy Consultant</div>
                        <div class="company">Eleveight • Financial Services</div>
                    </div>
                    <div class="duration">Jul 2025 - Aug 2025</div>
                </div>
                <p>Delivered expert content strategy services to prominent financial organizations including Waterfield Advisors, DSP Mutual Fund, and Nuvama Mutual Fund.</p>
                <div class="achievements">
                    <div class="achievement">
                        ✅ Created compelling infographics and data visualizations to simplify complex financial concepts
                    </div>
                    <div class="achievement">
                        ✅ Enhanced brand recognition through strategic content alignment with business objectives
                    </div>
                </div>
            </div>

            <div class="experience-item">
                <div class="job-header">
                    <div>
                        <div class="job-title">Business Development Manager</div>
                        <div class="company">Yasman Recycle Pvt Ltd</div>
                    </div>
                    <div class="duration">Oct 2022 - Jun 2025</div>
                </div>
                <p>Led business development initiatives and managed sustainability-focused recycling operations.</p>
                <div class="achievements">
                    <div class="achievement">
                        ✅ Streamlined legal documentation using AI tools, improving efficiency by 40%
                    </div>
                </div>
            </div>

            <div class="experience-item">
                <div class="job-header">
                    <div>
                        <div class="job-title">Content Specialist (Finance)</div>
                        <div class="company">Karza Technologies</div>
                    </div>
                    <div class="duration">Aug 2021 - Sep 2022</div>
                </div>
                <p>Specialized in fintech content creation, brand development, and SEO strategy implementation.</p>
                <div class="achievements">
                    <div class="achievement">
                        ✅ Achieved 20% increase in website traffic through strategic SEO optimization
                    </div>
                </div>
            </div>

            <div class="experience-item">
                <div class="job-header">
                    <div>
                        <div class="job-title">Content Writer</div>
                        <div class="company">Savisha Marketing</div>
                    </div>
                    <div class="duration">Feb 2019 - Jul 2021</div>
                </div>
                <p>Produced high-quality financial content for major corporations.</p>
                <div class="achievements">
                    <div class="achievement">
                        ✅ Authored 100+ finance-related content pieces for Upgrade, Bharti AXA, and HDFC Life
                    </div>
                </div>
            </div>
        </section>

        <!-- Key Projects -->
        <section class="section" id="projects">
            <h3>Featured Projects & Case Studies</h3>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-title">Financial Services Content Strategy</div>
                    <div class="project-description">
                        Developed comprehensive content strategies for Waterfield Advisors and DSP Mutual Fund, 
                        creating engaging infographics and data visualizations.
                    </div>
                    <div class="project-tags">
                        <span class="project-tag">Content Strategy</span>
                        <span class="project-tag">Data Visualization</span>
                        <span class="project-tag">Financial Services</span>
                    </div>
                    <a href="https://bit.ly/YashContentPortfolio" target="_blank" class="cta-button">View Case Study</a>
                </div>

                <div class="project-card">
                    <div class="project-title">SEO-Driven Content Marketing</div>
                    <div class="project-description">
                        Implemented comprehensive SEO strategies resulting in 20% increase in website traffic 
                        and improved organic search rankings.
                    </div>
                    <div class="project-tags">
                        <span class="project-tag">SEO Optimization</span>
                        <span class="project-tag">Content Marketing</span>
                        <span class="project-tag">Analytics</span>
                    </div>
                    <a href="https://bit.ly/YashContentPortfolio" target="_blank" class="cta-button">View Results</a>
                </div>

                <div class="project-card">
                    <div class="project-title">AI-Enhanced Content Creation</div>
                    <div class="project-description">
                        Leveraged AI tools to streamline content creation processes, improving efficiency 
                        and accuracy while maintaining high-quality standards.
                    </div>
                    <div class="project-tags">
                        <span class="project-tag">AI Implementation</span>
                        <span class="project-tag">Process Automation</span>
                        <span class="project-tag">Efficiency Optimization</span>
                    </div>
                    <a href="https://bit.ly/YashContentPortfolio" target="_blank" class="cta-button">Explore Methods</a>
                </div>
            </div>
        </section>

        <!-- Future Endeavours -->
        <section class="section" id="future">
            <h3>🚀 Future Endeavours</h3>
            <div style="background: linear-gradient(135deg, rgba(102, 126, 234, 0.1), rgba(240, 147, 251, 0.1), rgba(67, 233, 123, 0.1)); padding: 40px; border-radius: 20px; text-align: center; position: relative; overflow: hidden;">
                <div style="position: absolute; top: -50%; left: -50%; width: 200%; height: 200%; background: radial-gradient(circle, rgba(102, 126, 234, 0.1) 0%, transparent 70%); animation: float 6s ease-in-out infinite;"></div>
                <div style="font-size: 3em; margin-bottom: 20px; position: relative; z-index: 1;">🤖✨🧘</div>
                <h4 style="font-size: 1.8em; margin-bottom: 20px; color: #333; position: relative; z-index: 1;">Evolving into an AI-Generalist Consultant</h4>
                <p style="font-size: 1.2em; line-height: 1.8; color: #666; max-width: 800px; margin: 0 auto; position: relative; z-index: 1;">
                    My vision is to become a comprehensive AI-Generalist, where <strong>technology meets creativity meets spirituality</strong>. 
                    By integrating my diverse industry background with a passion for problem-solving, I aim to help organizations 
                    unlock profound insights from complex, unstructured data. This unique fusion of artificial intelligence, 
                    creative thinking, and mindful strategy enables me to transform data chaos into compelling narratives 
                    that drive conscious, informed decision-making across industries.
                </p>
                <div style="margin-top: 30px; display: flex; justify-content: center; gap: 15px; flex-wrap: wrap; position: relative; z-index: 1;">
                    <span style="background: linear-gradient(45deg, #667eea, #f093fb); color: white; padding: 12px 24px; border-radius: 25px; font-weight: 500; box-shadow: 0 5px 15px rgba(102, 126, 234, 0.3);">AI Integration</span>
                    <span style="background: linear-gradient(45deg, #43e97b, #38f9d7); color: white; padding: 12px 24px; border-radius: 25px; font-weight: 500; box-shadow: 0 5px 15px rgba(67, 233, 123, 0.3);">Data Storytelling</span>
                    <span style="background: linear-gradient(45deg, #f5576c, #f093fb); color: white; padding: 12px 24px; border-radius: 25px; font-weight: 500; box-shadow: 0 5px 15px rgba(245, 87, 108, 0.3);">Conscious Consulting</span>
                    <span style="background: linear-gradient(45deg, #4facfe, #00f2fe); color: white; padding: 12px 24px; border-radius: 25px; font-weight: 500; box-shadow: 0 5px 15px rgba(79, 172, 254, 0.3);">Cross-Industry Wisdom</span>
                </div>
            </div>
        </section>

        <!-- Passions & Philosophy -->
        <section class="section">
            <h3>💫 Passions & Philosophy</h3>
            <div class="projects-grid">
                <div class="project-card" style="background: linear-gradient(135deg, rgba(102, 126, 234, 0.1), rgba(255, 255, 255, 0.9)); border: 2px solid transparent; background-clip: padding-box; position: relative;">
                    <div style="position: absolute; inset: 0; padding: 2px; background: linear-gradient(45deg, #667eea, #f093fb, #43e97b); border-radius: 15px; z-index: -1;"></div>
                    <div class="project-title">📚 Intellectual Exploration</div>
                    <div class="project-description">
                        My passion for books and movies fuels creative thinking and provides diverse perspectives that 
                        enrich my content strategy approach. Literature and cinema offer endless inspiration 
                        for storytelling, human psychology, and audience engagement techniques.
                    </div>
                    <div style="margin-top: 20px; display: flex; gap: 10px; flex-wrap: wrap;">
                        <span style="background: linear-gradient(45deg, #f5576c, #f093fb); color: white; padding: 10px 18px; border-radius: 20px; font-size: 0.9em; font-weight: 500;">Books</span>
                        <span style="background: linear-gradient(45deg, #4facfe, #00f2fe); color: white; padding: 10px 18px; border-radius: 20px; font-size: 0.9em; font-weight: 500;">Movies</span>
                        <span style="background: linear-gradient(45deg, #43e97b, #38f9d7); color: white; padding: 10px 18px; border-radius: 20px; font-size: 0.9em; font-weight: 500;">Storytelling</span>
                    </div>
                </div>

                <div class="project-card" style="background: linear-gradient(135deg, rgba(67, 233, 123, 0.1), rgba(255, 255, 255, 0.9)); border: 2px solid transparent; background-clip: padding-box; position: relative;">
                    <div style="position: absolute; inset: 0; padding: 2px; background: linear-gradient(45deg, #43e97b, #38f9d7, #667eea); border-radius: 15px; z-index: -1;"></div>
                    <div class="project-title">🧘 Mindful Innovation</div>
                    <div class="project-description">
                        As a certified Iyengar Yoga teacher, I bring mindfulness and spiritual awareness to my professional practice. 
                        This holistic approach enhances problem-solving abilities, maintains clarity in complex decisions, 
                        and creates authentic connections between technology and human consciousness.
                    </div>
                    <div style="margin-top: 20px; display: flex; gap: 10px; flex-wrap: wrap;">
                        <span style="background: linear-gradient(45deg, #667eea, #764ba2); color: white; padding: 10px 18px; border-radius: 20px; font-size: 0.9em; font-weight: 500;">Yoga</span>
                        <span style="background: linear-gradient(45deg, #43e97b, #38f9d7); color: white; padding: 10px 18px; border-radius: 20px; font-size: 0.9em; font-weight: 500;">Meditation</span>
                        <span style="background: linear-gradient(45deg, #f093fb, #f5576c); color: white; padding: 10px 18px; border-radius: 20px; font-size: 0.9em; font-weight: 500;">Conscious Business</span>
                    </div>
                </div>
            </div>

            <!-- Guiding Principles -->
            <div style="margin-top: 40px;">
                <h4 style="text-align: center; font-size: 1.8em; margin-bottom: 30px; color: #333; background: linear-gradient(45deg, #667eea, #f093fb, #43e97b); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;">✨ Guiding Principles ✨</h4>
                <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(400px, 1fr)); gap: 30px;">
                    <div style="background: linear-gradient(135deg, rgba(102, 126, 234, 0.1), rgba(255, 255, 255, 0.9)); padding: 35px; border-radius: 20px; border-left: 5px solid #667eea; font-style: italic; position: relative; overflow: hidden; box-shadow: 0 10px 30px rgba(102, 126, 234, 0.1);">
                        <div style="position: absolute; top: -10px; left: 20px; font-size: 4em; color: rgba(102, 126, 234, 0.3); z-index: 0;">"</div>
                        <div style="position: relative; z-index: 1;">
                            The one thing that doesn't abide by the majority rule is a person's conscience.
                            <br><br>
                            <strong style="background: linear-gradient(45deg, #667eea, #f093fb); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;">— Atticus Finch, To Kill A Mockingbird</strong>
                        </div>
                    </div>
                    <div style="background: linear-gradient(135deg, rgba(240, 147, 251, 0.1), rgba(255, 255, 255, 0.9)); padding: 35px; border-radius: 20px; border-left: 5px solid #f093fb; font-style: italic; position: relative; overflow: hidden; box-shadow: 0 10px 30px rgba(240, 147, 251, 0.1);">
                        <div style="position: absolute; top: -10px; left: 20px; font-size: 4em; color: rgba(240, 147, 251, 0.3); z-index: 0;">"</div>
                        <div style="position: relative; z-index: 1;">
                            To be principled and ethical in a cynical world is the greatest act of rebellion.
                            <br><br>
                            <strong style="background: linear-gradient(45deg, #f093fb, #43e97b); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;">— Yash Shah</strong>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Certifications & Education -->
        <section class="section">
            <h3>Certifications & Education</h3>
            <div class="certifications">
                <div class="cert-item">
                    <h4>PG Program in Investment Banking & Financial Modeling</h4>
                    <p>Datatrained Learning • 2024</p>
                </div>
                <div class="cert-item">
                    <h4>Certified Financial Analyst</h4>
                    <p>Fastlane Careers Pvt Ltd • 2023</p>
                </div>
                <div class="cert-item">
                    <h4>Investment Banking Operations Professional</h4>
                    <p>Imarticus Pvt Ltd • 2017</p>
                </div>
                <div class="cert-item">
                    <h4>Certified Iyengar Yoga Teacher</h4>
                    <p>Om Yoga, Rishikesh</p>
                </div>
                <div class="cert-item">
                    <h4>Bachelor in Management Studies</h4>
                    <p>SIES College, Mumbai • 2007-2010</p>
                </div>
            </div>
        </section>

        <!-- Contact Information -->
        <section class="section" id="contact">
            <h3>Let's Connect</h3>
            <p style="text-align: center; font-size: 1.2em; margin-bottom: 30px; color: #666;">
                Ready to discuss your content strategy needs? Let's create something impactful together.
            </p>
            
            <div class="contact-info">
                <div class="contact-item">
                    <h4>📧 Email</h4>
                    <p>yash.shah@hotmail.com</p>
                </div>
                <div class="contact-item">
                    <h4>📱 Phone</h4>
                    <p>+91-9920662970</p>
                </div>
                <div class="contact-item">
                    <h4>📍 Location</h4>
                    <p>Mumbai, India</p>
                </div>
                <div class="contact-item">
                    <h4>💼 LinkedIn</h4>
                    <p>linkedin.com/in/yash-shah-content-strategist-consultant</p>
                </div>
            </div>

            <div style="text-align: center; margin-top: 40px;">
                <a href="https://bit.ly/YashContentPortfolio" target="_blank" class="cta-button">
                    Explore Full Portfolio
                </a>
                <a href="mailto:yash.shah@hotmail.com" class="cta-button" style="margin-left: 20px;">
                    Get In Touch
                </a>
            </div>
        </section>

        <!-- Footer -->
        <footer style="text-align: center; padding: 40px 20px; color: white;">
            <div style="background: rgba(255, 255, 255, 0.1); backdrop-filter: blur(10px); border-radius: 15px; padding: 30px;">
                <h3 style="margin-bottom: 20px;">Ready to Elevate Your Content Strategy?</h3>
                <p style="font-size: 1.1em; margin-bottom: 25px;">
                    Let's discuss how my expertise in content strategy, financial writing, and research analysis 
                    can drive your business forward.
                </p>
                <a href="mailto:yash.shah@hotmail.com" class="cta-button" style="margin-right: 15px;">
                    Start a Conversation
                </a>
                <a href="https://bit.ly/YashContentPortfolio" target="_blank" class="cta-button">
                    View Portfolio
                </a>
            </div>
        </footer>
    </div>

    <script>
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

        // Add scroll animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.animation = 'fadeInUp 0.8s ease-out';
                }
            });
        }, observerOptions);

        document.querySelectorAll('.section, .experience-item, .project-card').forEach(el => {
            observer.observe(el);
        });

        // Add hover effects for interactive elements
        document.querySelectorAll('.project-card, .experience-item, .skill-category').forEach(card => {
            card.addEventListener('mouseenter', function() {
                this.style.transition = 'all 0.3s ease';
            });
        });
    </script>
</body>

</html>
