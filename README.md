<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Debaprasad Haldar | Business Analyst Portfolio</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.0.0/css/all.min.css">
    <style>
        :root {
            --primary: #1e3a76;
            --secondary: #3f5c92;
            --accent: #7ab4d1;
            --light-accent: #a8d6e6;
            --background: #f5f8fa;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            color: #333;
            background-color: var(--background);
            overflow-x: hidden;
        }
        .bg-primary { background-color: var(--primary); }
        .bg-secondary { background-color: var(--secondary); }
        .bg-accent { background-color: var(--accent); }
        .bg-light-accent { background-color: var(--light-accent); }
        .text-primary { color: var(--primary); }
        .text-secondary { color: var(--secondary); }
        .text-accent { color: var(--accent); }
        .border-primary { border-color: var(--primary); }
        .border-accent { border-color: var(--accent); }
        .btn-primary {
            background-color: var(--primary);
            color: white;
            transition: all 0.3s ease;
        }
        .btn-primary:hover {
            background-color: var(--secondary);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        .btn-secondary {
            background-color: var(--accent);
            color: var(--primary);
            transition: all 0.3s ease;
        }
        .btn-secondary:hover {
            background-color: var(--light-accent);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        .navbar {
            transition: all 0.3s ease;
        }
        .nav-link {
            position: relative;
        }
        .nav-link::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: 0;
            left: 0;
            background-color: var(--accent);
            transition: width 0.3s ease;
        }
        .nav-link:hover::after {
            width: 100%;
        }
        .project-card {
            transition: all 0.3s ease;
            border: 1px solid rgba(0,0,0,0.1);
        }
        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
        }
        .expertise-item {
            transition: all 0.3s ease;
        }
        .expertise-item:hover {
            transform: translateY(-5px);
        }
        .progress-container {
            height: 8px;
            width: 100%;
            background-color: #e0e0e0;
            border-radius: 4px;
            margin: 10px 0;
        }
        .progress-bar {
            height: 100%;
            border-radius: 4px;
            background-color: var(--accent);
            transition: width 1.5s ease-in-out;
        }
        .timeline-item {
            position: relative;
            padding-left: 30px;
            margin-bottom: 30px;
        }
        .timeline-item::before {
            content: '';
            position: absolute;
            left: 0;
            top: 5px;
            width: 14px;
            height: 14px;
            border-radius: 50%;
            background-color: var(--primary);
        }
        .timeline-item::after {
            content: '';
            position: absolute;
            left: 7px;
            top: 25px;
            width: 2px;
            height: calc(100% + 10px);
            background-color: #e0e0e0;
        }
        .timeline-item:last-child::after {
            display: none;
        }
        .project-image {
            height: 200px;
            object-fit: cover;
            object-position: center;
            width: 100%;
        }
        .social-icon {
            transition: all 0.3s ease;
        }
        .social-icon:hover {
            transform: translateY(-5px);
            color: var(--accent);
        }
        @media (max-width: 768px) {
            .project-card {
                margin-bottom: 20px;
            }
        }
    </style>
</head>
<body>
    <!-- Header/Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="navbar container mx-auto px-6 py-3 flex justify-between items-center">
            <a href="#" class="text-2xl font-bold text-primary">Deb<span class="text-accent">Haldar</span></a>
            
            <div class="hidden md:flex space-x-8">
                <a href="#about" class="nav-link text-gray-700 hover:text-primary">About</a>
                <a href="#projects" class="nav-link text-gray-700 hover:text-primary">Projects</a>
                <a href="#expertise" class="nav-link text-gray-700 hover:text-primary">Expertise</a>
                <a href="#kpis" class="nav-link text-gray-700 hover:text-primary">KPIs</a>
                <a href="#experience" class="nav-link text-gray-700 hover:text-primary">Experience</a>
            </div>
            
            <div class="flex items-center space-x-4">
                <a href="https://www.linkedin.com/in/debaprasad-haldar-837717261/" target="_blank" class="social-icon text-secondary">
                    <i class="fab fa-linkedin text-lg"></i>
                </a>
                <a href="https://wa.me/918116694828" target="_blank" class="social-icon text-secondary">
                    <i class="fab fa-whatsapp text-lg"></i>
                </a>
                <a href="#" class="btn-primary px-4 py-2 rounded-lg text-sm font-medium shadow-sm" id="downloadResume">Download Resume</a>
            </div>
            
            <div class="md:hidden cursor-pointer" id="menuButton">
                <i class="fas fa-bars text-primary text-2xl"></i>
            </div>
        </nav>
        
        <!-- Mobile Menu -->
        <div class="md:hidden bg-white w-full absolute left-0 shadow-md hidden" id="mobileMenu">
            <div class="container mx-auto px-6 py-3 flex flex-col space-y-4">
                <a href="#about" class="text-gray-700 hover:text-primary">About</a>
                <a href="#projects" class="text-gray-700 hover:text-primary">Projects</a>
                <a href="#expertise" class="text-gray-700 hover:text-primary">Expertise</a>
                <a href="#kpis" class="text-gray-700 hover:text-primary">KPIs</a>
                <a href="#experience" class="text-gray-700 hover:text-primary">Experience</a>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="py-12 md:py-20 bg-gradient-to-r from-primary to-secondary">
        <div class="container mx-auto px-6 flex flex-col-reverse md:flex-row items-center">
            <div class="md:w-1/2 text-center md:text-left text-white">
                <h1 class="text-3xl md:text-5xl font-bold mb-4">Debaprasad Haldar</h1>
                <h2 class="text-xl md:text-2xl font-semibold mb-6 text-light-accent">Business Analyst | Data-Driven Solutions</h2>
                <p class="text-lg mb-8 max-w-lg">Driving Digital Efficiency Through Insightful Analysis & Agile Execution</p>
                <a href="https://wa.me/918116694828" class="btn-secondary px-6 py-3 rounded-lg text-base md:text-lg font-medium shadow-md inline-block">
                    <i class="fab fa-whatsapp mr-2"></i> Let's Connect
                </a>
            </div>
            <div class="md:w-1/2 mb-10 md:mb-0 flex justify-center md:justify-end">
                <div class="w-60 h-60 md:w-72 md:h-72 rounded-full overflow-hidden border-4 border-light-accent shadow-2xl">
                    <img src="https://page.genspark.site/v1/base64_upload/ebfe5a777d8ead281cb604463dc57366" alt="Debaprasad Haldar" class="w-full h-full object-cover">
                </div>
            </div>
        </div>
    </section>

    <!-- About/Value Proposition -->
    <section id="about" class="py-16 bg-white">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl font-bold text-center mb-12 text-primary">Why Work With Me?</h2>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                <div class="bg-background rounded-lg p-6 shadow-md hover:shadow-xl transition-all duration-300">
                    <div class="text-4xl text-accent mb-4">
                        <i class="fas fa-lightbulb"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-primary">Business-Driven Mindset</h3>
                    <p class="text-gray-600">I approach analysis from a business perspective, ensuring solutions align with strategic objectives and deliver real value.</p>
                </div>
                
                <div class="bg-background rounded-lg p-6 shadow-md hover:shadow-xl transition-all duration-300">
                    <div class="text-4xl text-accent mb-4">
                        <i class="fas fa-comments"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-primary">Strong Communication</h3>
                    <p class="text-gray-600">I excel at translating complex requirements between technical teams and business stakeholders to ensure alignment.</p>
                </div>
                
                <div class="bg-background rounded-lg p-6 shadow-md hover:shadow-xl transition-all duration-300">
                    <div class="text-4xl text-accent mb-4">
                        <i class="fas fa-tasks"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-primary">Agile Delivery Experience</h3>
                    <p class="text-gray-600">My proven experience with Agile methodologies helps teams deliver high-quality solutions incrementally and efficiently.</p>
                </div>
                
                <div class="bg-background rounded-lg p-6 shadow-md hover:shadow-xl transition-all duration-300">
                    <div class="text-4xl text-accent mb-4">
                        <i class="fas fa-user-check"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-primary">User-Centric Thinking</h3>
                    <p class="text-gray-600">I prioritize user needs and data accuracy, creating solutions that are both intuitive and reliable.</p>
                </div>
            </div>
            
            <div class="mt-16 bg-background rounded-lg p-8 shadow-md">
                <h3 class="text-2xl font-semibold mb-4 text-primary">About Me</h3>
                <p class="text-gray-700 mb-6">I am a detail-oriented Business Analyst with a strong foundation in project management and business planning. My analytical skills enable me to identify process inefficiencies and develop data-driven solutions. I excel in Agile methodologies and strive to foster effective communication among stakeholders. My passion lies in leveraging AI technologies to drive operational excellence.</p>
                <p class="text-gray-700">With experience at Webskitters Technology Solutions and Fusion BPO, I've developed expertise in requirement gathering, process optimization, and cross-functional collaboration. My technical background in Mechanical Engineering complements my business acumen, allowing me to bridge the gap between technical capabilities and business needs.</p>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="py-16 bg-background">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl font-bold text-center mb-4 text-primary">Featured Projects</h2>
            <p class="text-center text-gray-600 mb-12 max-w-3xl mx-auto">Showcasing high-impact web and mobile projects that demonstrate my expertise in business analysis, requirement gathering, and solution design.</p>
            
            <h3 class="text-2xl font-semibold mb-6 text-secondary">Web Projects</h3>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 mb-12">
                <!-- Project 1 -->
                <div class="project-card bg-white rounded-lg overflow-hidden">
                    <img src="https://www.customsoftwarelab.com/wp-content/uploads/2023/01/taxterminal-dash.png" alt="Client Tax Portal" class="project-image">
                    <div class="p-6">
                        <h4 class="text-xl font-semibold mb-2 text-primary">Client Tax Portal Modernization</h4>
                        <p class="text-gray-600 mb-4">Enhanced user experience and streamlined backend workflows for over 1,000 annual returns.</p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-light-accent text-primary text-xs font-medium px-2.5 py-0.5 rounded-full">#WebApp</span>
                            <span class="bg-light-accent text-primary text-xs font-medium px-2.5 py-0.5 rounded-full">#UX</span>
                            <span class="bg-light-accent text-primary text-xs font-medium px-2.5 py-0.5 rounded-full">#ProcessFlow</span>
                        </div>
                    </div>
                </div>
                
                <!-- Project 2 -->
                <div class="project-card bg-white rounded-lg overflow-hidden">
                    <img src="https://marketdojo.com/wp-content/uploads/2021/04/Dashboard.png" alt="Vendor Management Interface" class="project-image">
                    <div class="p-6">
                        <h4 class="text-xl font-semibold mb-2 text-primary">Vendor Event Service Management</h4>
                        <p class="text-gray-600 mb-4">Defined end-to-end service catalog requirements, validations, and user stories to support seamless vendor onboarding and management.</p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-light-accent text-primary text-xs font-medium px-2.5 py-0.5 rounded-full">#Integration</span>
                            <span class="bg-light-accent text-primary text-xs font-medium px-2.5 py-0.5 rounded-full">#WorkflowDesign</span>
                            <span class="bg-light-accent text-primary text-xs font-medium px-2.5 py-0.5 rounded-full">#UserStories</span>
                        </div>
                    </div>
                </div>
                
                <!-- Project 3 -->
                <div class="project-card bg-white rounded-lg overflow-hidden">
                    <img src="https://images.ctfassets.net/kepwgvmwgwnt/473U4m2r5a0uXf1SFIeudC/b3542faf35c05442665f2e9967f0a0d0/loan-approval-dash.png" alt="Loan Status Dashboard" class="project-image">
                    <div class="p-6">
                        <h4 class="text-xl font-semibold mb-2 text-primary">Loan Status Transparency Dashboard</h4>
                        <p class="text-gray-600 mb-4">Delivered an intuitive front-end application with real-time status updates for tax advance loans, ensuring full visibility for clients.</p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-light-accent text-primary text-xs font-medium px-2.5 py-0.5 rounded-full">#Dashboard</span>
                            <span class="bg-light-accent text-primary text-xs font-medium px-2.5 py-0.5 rounded-full">#RealTime</span>
                            <span class="bg-light-accent text-primary text-xs font-medium px-2.5 py-0.5 rounded-full">#ClientVisibility</span>
                        </div>
                    </div>
                </div>
            </div>
            
            <h3 class="text-2xl font-semibold mb-6 text-secondary">Mobile App Proposals & Scopes</h3>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Mobile Project 1 -->
                <div class="project-card bg-white rounded-lg overflow-hidden">
                    <img src="https://www.lightico.com/wp-content/uploads/2021/08/digital-completion-journey-banking-How-Banks-Complete-Self-Service-Workflows-with-Digital-Completion-1.jpg" alt="Self-Service Client Mobile App" class="project-image">
                    <div class="p-6">
                        <h4 class="text-xl font-semibold mb-2 text-primary">Self-Service Client Mobile App</h4>
                        <p class="text-gray-600 mb-4">Proposed a secure mobile solution allowing clients to upload documents, track tax return progress, and receive real-time notifications.</p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-light-accent text-primary text-xs font-medium px-2.5 py-0.5 rounded-full">#MobileScope</span>
                            <span class="bg-light-accent text-primary text-xs font-medium px-2.5 py-0.5 rounded-full">#SecureAuth</span>
                            <span class="bg-light-accent text-primary text-xs font-medium px-2.5 py-0.5 rounded-full">#PushNotifications</span>
                        </div>
                    </div>
                </div>
                
                <!-- Mobile Project 2 -->
                <div class="project-card bg-white rounded-lg overflow-hidden">
                    <img src="https://www.cflowapps.com/wp-content/uploads/2023/11/mobile-app-workflow-list-1.png" alt="Staff Workflow Companion App" class="project-image">
                    <div class="p-6">
                        <h4 class="text-xl font-semibold mb-2 text-primary">Staff Workflow Companion App</h4>
                        <p class="text-gray-600 mb-4">Designed the concept and data flow for an internal mobile app supporting remote staff with role-based task management.</p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-light-accent text-primary text-xs font-medium px-2.5 py-0.5 rounded-full">#InternalApp</span>
                            <span class="bg-light-accent text-primary text-xs font-medium px-2.5 py-0.5 rounded-full">#RoleBasedAccess</span>
                            <span class="bg-light-accent text-primary text-xs font-medium px-2.5 py-0.5 rounded-full">#TaskManagement</span>
                        </div>
                    </div>
                </div>
                
                <!-- Mobile Project 3 -->
                <div class="project-card bg-white rounded-lg overflow-hidden">
                    <img src="https://www.loansystems.com/images/static-pages-img/loan-tracker-img.jpg" alt="Client Loan Status Tracker" class="project-image">
                    <div class="p-6">
                        <h4 class="text-xl font-semibold mb-2 text-primary">Client Loan Status Tracker</h4>
                        <p class="text-gray-600 mb-4">Developed a feature set and user flow for a lightweight mobile tool enabling clients to view current loan status and submit additional documentation.</p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-light-accent text-primary text-xs font-medium px-2.5 py-0.5 rounded-full">#MobileTracking</span>
                            <span class="bg-light-accent text-primary text-xs font-medium px-2.5 py-0.5 rounded-full">#StatusUpdates</span>
                            <span class="bg-light-accent text-primary text-xs font-medium px-2.5 py-0.5 rounded-full">#DocumentUpload</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- BA Role & Expertise -->
    <section id="expertise" class="py-16 bg-white">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl font-bold text-center mb-4 text-primary">My Role & Expertise</h2>
            <p class="text-center text-gray-600 mb-12 max-w-3xl mx-auto">As a Business Analyst, I bridge the gap between business needs and technical solutions, ensuring alignment and successful project outcomes.</p>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mb-12">
                <div class="expertise-item p-5 bg-background rounded-lg shadow-md">
                    <div class="text-3xl text-accent mb-3">
                        <i class="fas fa-comments-dollar"></i>
                    </div>
                    <h3 class="text-lg font-semibold mb-2 text-primary">Requirements Elicitation</h3>
                    <p class="text-gray-600">Conduct stakeholder interviews and workshops to gather, analyze, and document business requirements.</p>
                </div>
                
                <div class="expertise-item p-5 bg-background rounded-lg shadow-md">
                    <div class="text-3xl text-accent mb-3">
                        <i class="fas fa-route"></i>
                    </div>
                    <h3 class="text-lg font-semibold mb-2 text-primary">Journey Mapping</h3>
                    <p class="text-gray-600">Create detailed client and staff journey maps to identify pain points and opportunities for improvement.</p>
                </div>
                
                <div class="expertise-item p-5 bg-background rounded-lg shadow-md">
                    <div class="text-3xl text-accent mb-3">
                        <i class="fas fa-file-alt"></i>
                    </div>
                    <h3 class="text-lg font-semibold mb-2 text-primary">Functional Specifications</h3>
                    <p class="text-gray-600">Develop comprehensive functional and non-functional specifications that guide development teams.</p>
                </div>
                
                <div class="expertise-item p-5 bg-background rounded-lg shadow-md">
                    <div class="text-3xl text-accent mb-3">
                        <i class="fas fa-database"></i>
                    </div>
                    <h3 class="text-lg font-semibold mb-2 text-primary">Data Modeling</h3>
                    <p class="text-gray-600">Create data models and validation rules to ensure data integrity and system reliability.</p>
                </div>
                
                <div class="expertise-item p-5 bg-background rounded-lg shadow-md">
                    <div class="text-3xl text-accent mb-3">
                        <i class="fas fa-tasks"></i>
                    </div>
                    <h3 class="text-lg font-semibold mb-2 text-primary">Agile Backlog Management</h3>
                    <p class="text-gray-600">Manage product backlogs, write user stories with clear acceptance criteria, and facilitate sprint planning.</p>
                </div>
                
                <div class="expertise-item p-5 bg-background rounded-lg shadow-md">
                    <div class="text-3xl text-accent mb-3">
                        <i class="fas fa-check-double"></i>
                    </div>
                    <h3 class="text-lg font-semibold mb-2 text-primary">UAT Coordination</h3>
                    <p class="text-gray-600">Plan and coordinate user acceptance testing, ensuring all requirements are verified before deployment.</p>
                </div>
                
                <div class="expertise-item p-5 bg-background rounded-lg shadow-md">
                    <div class="text-3xl text-accent mb-3">
                        <i class="fas fa-users-cog"></i>
                    </div>
                    <h3 class="text-lg font-semibold mb-2 text-primary">Cross-functional Collaboration</h3>
                    <p class="text-gray-600">Work seamlessly with design, development, and QA teams to deliver integrated solutions.</p>
                </div>
                
                <div class="expertise-item p-5 bg-background rounded-lg shadow-md">
                    <div class="text-3xl text-accent mb-3">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h3 class="text-lg font-semibold mb-2 text-primary">Business Intelligence</h3>
                    <p class="text-gray-600">Analyze business data to identify trends and provide insights for strategic decision-making.</p>
                </div>
                
                <div class="expertise-item p-5 bg-background rounded-lg shadow-md">
                    <div class="text-3xl text-accent mb-3">
                        <i class="fas fa-project-diagram"></i>
                    </div>
                    <h3 class="text-lg font-semibold mb-2 text-primary">Process Optimization</h3>
                    <p class="text-gray-600">Identify inefficiencies in business processes and recommend improvements for enhanced productivity.</p>
                </div>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <div class="bg-background p-6 rounded-lg shadow-md">
                    <h3 class="text-xl font-semibold mb-4 text-primary">Tools & Technologies</h3>
                    <div class="grid grid-cols-2 gap-4">
                        <div class="flex items-center space-x-2">
                            <i class="fas fa-check-circle text-accent"></i>
                            <span>JIRA & Confluence</span>
                        </div>
                        <div class="flex items-center space-x-2">
                            <i class="fas fa-check-circle text-accent"></i>
                            <span>Microsoft Excel</span>
                        </div>
                        <div class="flex items-center space-x-2">
                            <i class="fas fa-check-circle text-accent"></i>
                            <span>SQL & Data Analysis</span>
                        </div>
                        <div class="flex items-center space-x-2">
                            <i class="fas fa-check-circle text-accent"></i>
                            <span>Power BI</span>
                        </div>
                        <div class="flex items-center space-x-2">
                            <i class="fas fa-check-circle text-accent"></i>
                            <span>Visio & Process Mapping</span>
                        </div>
                        <div class="flex items-center space-x-2">
                            <i class="fas fa-check-circle text-accent"></i>
                            <span>Agile & Scrum</span>
                        </div>
                        <div class="flex items-center space-x-2">
                            <i class="fas fa-check-circle text-accent"></i>
                            <span>Microsoft Office Suite</span>
                        </div>
                        <div class="flex items-center space-x-2">
                            <i class="fas fa-check-circle text-accent"></i>
                            <span>CRM Systems</span>
                        </div>
                    </div>
                </div>
                
                <div class="bg-background p-6 rounded-lg shadow-md">
                    <h3 class="text-xl font-semibold mb-4 text-primary">Methodologies</h3>
                    <div class="grid grid-cols-2 gap-4">
                        <div class="flex items-center space-x-2">
                            <i class="fas fa-check-circle text-accent"></i>
                            <span>Agile/Scrum</span>
                        </div>
                        <div class="flex items-center space-x-2">
                            <i class="fas fa-check-circle text-accent"></i>
                            <span>Waterfall</span>
                        </div>
                        <div class="flex items-center space-x-2">
                            <i class="fas fa-check-circle text-accent"></i>
                            <span>BPMN</span>
                        </div>
                        <div class="flex items-center space-x-2">
                            <i class="fas fa-check-circle text-accent"></i>
                            <span>Lean Six Sigma</span>
                        </div>
                        <div class="flex items-center space-x-2">
                            <i class="fas fa-check-circle text-accent"></i>
                            <span>User Story Mapping</span>
                        </div>
                        <div class="flex items-center space-x-2">
                            <i class="fas fa-check-circle text-accent"></i>
                            <span>JAD Sessions</span>
                        </div>
                        <div class="flex items-center space-x-2">
                            <i class="fas fa-check-circle text-accent"></i>
                            <span>Gap Analysis</span>
                        </div>
                        <div class="flex items-center space-x-2">
                            <i class="fas fa-check-circle text-accent"></i>
                            <span>Root Cause Analysis</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- KPIs -->
    <section id="kpis" class="py-16 bg-background">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl font-bold text-center mb-4 text-primary">Impact by the Numbers</h2>
            <p class="text-center text-gray-600 mb-12 max-w-3xl mx-auto">Quantifiable results that demonstrate the value I bring to projects and organizations.</p>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <div class="bg-white p-6 rounded-lg shadow-md">
                    <div class="flex items-center mb-4">
                        <div class="text-3xl text-accent mr-4">
                            <i class="fas fa-chart-line"></i>
                        </div>
                        <h3 class="text-xl font-semibold text-primary">30% Reduction in Client Support</h3>
                    </div>
                    <p class="text-gray-600 mb-4">Decreased client support inquiries post-launch of self-service features.</p>
                    <div class="progress-container">
                        <div class="progress-bar" style="width: 30%"></div>
                    </div>
                </div>
                
                <div class="bg-white p-6 rounded-lg shadow-md">
                    <div class="flex items-center mb-4">
                        <div class="text-3xl text-accent mr-4">
                            <i class="fas fa-clock"></i>
                        </div>
                        <h3 class="text-xl font-semibold text-primary">25% Faster Document Processing</h3>
                    </div>
                    <p class="text-gray-600 mb-4">Decreased document processing time through streamlined workflows and intuitive upload flows.</p>
                    <div class="progress-container">
                        <div class="progress-bar" style="width: 25%"></div>
                    </div>
                </div>
                
                <div class="bg-white p-6 rounded-lg shadow-md">
                    <div class="flex items-center mb-4">
                        <div class="text-3xl text-accent mr-4">
                            <i class="fas fa-link"></i>
                        </div>
                        <h3 class="text-xl font-semibold text-primary">100% Traceability</h3>
                    </div>
                    <p class="text-gray-600 mb-4">Complete traceability from user stories to test cases, ensuring quality and compliance.</p>
                    <div class="progress-container">
                        <div class="progress-bar" style="width: 100%"></div>
                    </div>
                </div>
                
                <div class="bg-white p-6 rounded-lg shadow-md">
                    <div class="flex items-center mb-4">
                        <div class="text-3xl text-accent mr-4">
                            <i class="fas fa-tachometer-alt"></i>
                        </div>
                        <h3 class="text-xl font-semibold text-primary">40% Faster Delivery Time</h3>
                    </div>
                    <p class="text-gray-600 mb-4">Reduced average feature delivery time in agile sprints.</p>
                    <div class="progress-container">
                        <div class="progress-bar" style="width: 40%"></div>
                    </div>
                </div>
                
                <div class="bg-white p-6 rounded-lg shadow-md">
                    <div class="flex items-center mb-4">
                        <div class="text-3xl text-accent mr-4">
                            <i class="fas fa-mobile-alt"></i>
                        </div>
                        <h3 class="text-xl font-semibold text-primary">70% Mobile Engagement</h3>
                    </div>
                    <p class="text-gray-600 mb-4">Projected client touchpoints covered by proposed mobile app concepts.</p>
                    <div class="progress-container">
                        <div class="progress-bar" style="width: 70%"></div>
                    </div>
                </div>
                
                <div class="bg-white p-6 rounded-lg shadow-md">
                    <div class="flex items-center mb-4">
                        <div class="text-3xl text-accent mr-4">
                            <i class="fas fa-dollar-sign"></i>
                        </div>
                        <h3 class="text-xl font-semibold text-primary">25% Revenue Increase</h3>
                    </div>
                    <p class="text-gray-600 mb-4">Increased sales revenue through data-driven decision making.</p>
                    <div class="progress-container">
                        <div class="progress-bar" style="width: 25%"></div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Timeline -->
    <section id="experience" class="py-16 bg-white">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl font-bold text-center mb-12 text-primary">Professional Experience</h2>
            
            <div class="max-w-3xl mx-auto">
                <div class="timeline-item">
                    <div class="flex flex-col md:flex-row md:items-center justify-between mb-3">
                        <h3 class="text-xl font-semibold text-primary">Business Analyst</h3>
                        <span class="text-accent font-medium">Dec 2022 - Present</span>
                    </div>
                    <h4 class="text-lg font-medium text-secondary mb-3">Webskitters Technology Solutions Private Limited, Durgapur</h4>
                    <p class="text-gray-600 mb-4">Webskitters Technology Solutions is a technology services company.</p>
                    <ul class="list-disc pl-5 text-gray-600 space-y-2">
                        <li>Conduct business intelligence analysis to drive strategic decision-making.</li>
                        <li>Identify process gaps and recommend improvement initiatives.</li>
                        <li>Develop KPI-driven reports for senior management.</li>
                        <li>Collaborate with cross-functional teams to optimize business processes.</li>
                        <li>Prepare comprehensive documentation to support training and process enhancements.</li>
                        <li>Assist sales teams with data-driven proposals to maximize revenue.</li>
                        <li>Responsible for gathering requirements and handling client calls.</li>
                        <li>Communicate client's business requirements by constructing easy-to-understand data and process models.</li>
                        <li>Analyze and document business processes to facilitate system enhancements.</li>
                        <li>Work closely with developers and testers to ensure business needs are met effectively.</li>
                        <li>Assist in the development of user acceptance testing (UAT) plans and participate in testing efforts.</li>
                    </ul>
                </div>
                
                <div class="timeline-item">
                    <div class="flex flex-col md:flex-row md:items-center justify-between mb-3">
                        <h3 class="text-xl font-semibold text-primary">Customer Support Specialist</h3>
                        <span class="text-accent font-medium">Jun 2022 - Dec 2022</span>
                    </div>
                    <h4 class="text-lg font-medium text-secondary mb-3">Fusion BPO, Remote</h4>
                    <p class="text-gray-600 mb-4">Fusion BPO is a customer support service provider.</p>
                    <ul class="list-disc pl-5 text-gray-600 space-y-2">
                        <li>Managed high volumes of customer inquiries, ensuring excellent customer satisfaction.</li>
                        <li>Provided accurate information regarding products, services, and company policies.</li>
                        <li>Processed service orders and maintained accurate customer records.</li>
                        <li>Utilized CRM systems to track interactions and resolve customer issues efficiently.</li>
                        <li>Implemented proactive strategies to enhance customer retention.</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-primary text-white py-10">
        <div class="container mx-auto px-6">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="mb-6 md:mb-0">
                    <h2 class="text-2xl font-bold mb-2">Debaprasad Haldar</h2>
                    <p class="text-light-accent">Business Analyst | Data-Driven Solutions</p>
                </div>
                
                <div class="flex flex-col items-center md:items-end">
                    <div class="flex space-x-4 mb-4">
                        <a href="https://www.linkedin.com/in/debaprasad-haldar-837717261/" target="_blank" class="social-icon text-white hover:text-accent">
                            <i class="fab fa-linkedin text-2xl"></i>
                        </a>
                        <a href="https://wa.me/918116694828" target="_blank" class="social-icon text-white hover:text-accent">
                            <i class="fab fa-whatsapp text-2xl"></i>
                        </a>
                        <a href="mailto:Debaprasad28.dh@gmail.com" class="social-icon text-white hover:text-accent">
                            <i class="fas fa-envelope text-2xl"></i>
                        </a>
                    </div>
                    <p>Debaprasad28.dh@gmail.com | +91 8116694828</p>
                    <p class="mt-2">&copy; 2024 Debaprasad Haldar. All rights reserved.</p>
                </div>
            </div>
        </div>
    </footer>

    <!-- Script for mobile menu toggle and resume download -->
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Mobile menu toggle
            const menuButton = document.getElementById('menuButton');
            const mobileMenu = document.getElementById('mobileMenu');
            
            menuButton.addEventListener('click', function() {
                mobileMenu.classList.toggle('hidden');
            });
            
            // Close mobile menu when clicking a link
            const mobileLinks = mobileMenu.querySelectorAll('a');
            mobileLinks.forEach(link => {
                link.addEventListener('click', function() {
                    mobileMenu.classList.add('hidden');
                });
            });
            
            // Resume download functionality
            document.getElementById('downloadResume').addEventListener('click', function(e) {
                e.preventDefault();
                
                // Create a simple resume content (you would replace this with actual resume content)
                const resumeContent = `
                    DEBAPRASAD HALDAR
                    Business Analyst | Data-Driven Solutions | Agile Methodologies | Continuous Improvement
                    
                    Contact: +91 8116694828 | Debaprasad28.dh@gmail.com | LinkedIn: https://www.linkedin.com/in/debaprasad-haldar-837717261/
                    Location: India
                    
                    SUMMARY
                    I am a detail-oriented Business Analyst with a strong foundation in project management and business planning. My analytical skills enable me to identify process inefficiencies and develop data-driven solutions. I excel in Agile methodologies and strive to foster effective communication among stakeholders. My passion lies in leveraging AI technologies to drive operational excellence.
                    
                    KEY ACHIEVEMENTS
                    • Sales Revenue Boost: Increased sales revenue by 25% through data-driven decision making.
                    • Process Improvement: Reduced process inefficiencies by 30% using agile methodologies.
                    • Customer Satisfaction: Improved customer satisfaction scores by 15% with effective support.
                    • KPI Report Development: Developed 20+ KPI reports for decision making.
                    
                    EXPERIENCE
                    Business Analyst
                    Webskitters Technology Solutions Private Limited, Durgapur
                    Dec 2022 - Present
                    
                    • Conduct business intelligence analysis to drive strategic decision-making.
                    • Identify process gaps and recommend improvement initiatives.
                    • Develop KPI-driven reports for senior management.
                    • Collaborate with cross-functional teams to optimize business processes.
                    • Prepare comprehensive documentation to support training and process enhancements.
                    • Assist sales teams with data-driven proposals to maximize revenue.
                    • Responsible for gathering requirements and handling client calls.
                    • Communicate client's business requirements by constructing easy-to-understand data and process models.
                    • Analyze and document business processes to facilitate system enhancements.
                    • Work closely with developers and testers to ensure business needs are met effectively.
                    • Assist in the development of user acceptance testing (UAT) plans and participate in testing efforts.
                    
                    Customer Support Specialist
                    Fusion BPO, Remote
                    Jun 2022 - Dec 2022
                    
                    • Managed high volumes of customer inquiries, ensuring excellent customer satisfaction.
                    • Provided accurate information regarding products, services, and company policies.
                    • Processed service orders and maintained accurate customer records.
                    • Utilized CRM systems to track interactions and resolve customer issues efficiently.
                    • Implemented proactive strategies to enhance customer retention.
                    
                    EDUCATION
                    B.Tech in Mechanical Engineering
                    Camellia Institute of Engineering & Technology, Budbud (Durgapur)
                    Aug 2016 - Jun 2020
                    
                    Diploma in Mechanical Engineering
                    Camellia Institute of Polytechnic, Budbud (Durgapur)
                    Aug 2014 - Jun 2016
                    
                    SKILLS
                    • Business Analysis & Planning
                    • Team Collaboration
                    • Continuous Improvement
                    • Process Optimization
                    • Requirements Gathering
                    • Documentation & Reporting
                    • Stakeholder Management
                    • Agile Methodologies
                    • Data Analysis
                    
                    LANGUAGES
                    • English (Native)
                    • Bengali (Native)
                `;
                
                // Create a Blob from the resume content
                const blob = new Blob([resumeContent], { type: 'text/plain' });
                
                // Create a download link
                const downloadLink = document.createElement('a');
                downloadLink.download = 'Debaprasad_Haldar_Resume.txt';
                downloadLink.href = window.URL.createObjectURL(blob);
                
                // Append the link to the body, click it, and remove it
                document.body.appendChild(downloadLink);
                downloadLink.click();
                document.body.removeChild(downloadLink);
            });
            
            // Progress bar animation on scroll
            const progressBars = document.querySelectorAll('.progress-bar');
            
            function animateProgressBars() {
                progressBars.forEach(bar => {
                    const rect = bar.getBoundingClientRect();
                    // If the element is in the viewport
                    if (rect.top < window.innerHeight && rect.bottom >= 0) {
                        // Get width from inline style
                        const width = bar.style.width;
                        // Reset width
                        bar.style.width = 0;
                        // Trigger reflow
                        void bar.offsetWidth;
                        // Animate to intended width
                        bar.style.width = width;
                    }
                });
            }
            
            // Initial animation
            setTimeout(animateProgressBars, 500);
            
            // Re-trigger animation on scroll
            let isScrolling = false;
            window.addEventListener('scroll', function() {
                if (!isScrolling) {
                    isScrolling = true;
                    setTimeout(function() {
                        animateProgressBars();
                        isScrolling = false;
                    }, 100);
                }
            });
            
            // Smooth scrolling for navigation links
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    
                    const targetId = this.getAttribute('href');
                    if (targetId === '#') return;
                    
                    const targetElement = document.querySelector(targetId);
                    if (targetElement) {
                        window.scrollTo({
                            top: targetElement.offsetTop - 80,
                            behavior: 'smooth'
                        });
                    }
                });
            });
        });
    </script>
</body>
</html>
