<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bishnupriya PDF World | Complete PDF Solution</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">
    
    <!-- PDF.js for client-side PDF processing -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/2.12.313/pdf.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/pdf-lib/1.17.1/pdf-lib.min.js"></script>
    
    <style>
        :root {
            /* Color Palette - Enhanced */
            --convert: #6366f1;
            --edit: #10b981;
            --security: #f59e0b;
            --organize: #8b5cf6;
            --image: #ec4899;
            --special: #14b8a6;
            --dark: #1e293b;
            --light: #f8fafc;
            --gray: #94a3b8;
            
            /* New Gradient Variables */
            --convert-gradient: linear-gradient(135deg, #6366f1, #818cf8);
            --edit-gradient: linear-gradient(135deg, #10b981, #34d399);
            --security-gradient: linear-gradient(135deg, #f59e0b, #fbbf24);
            --organize-gradient: linear-gradient(135deg, #8b5cf6, #a78bfa);
            --image-gradient: linear-gradient(135deg, #ec4899, #f472b6);
            --special-gradient: linear-gradient(135deg, #14b8a6, #2dd4bf);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
        }

        /* Animated Background */
        .bg-pattern {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 20% 30%, rgba(99, 102, 241, 0.1) 0%, transparent 30%),
                radial-gradient(circle at 80% 70%, rgba(16, 185, 129, 0.1) 0%, transparent 30%);
            z-index: -1;
            animation: float 15s ease-in-out infinite alternate;
        }

        @keyframes float {
            0% { transform: translate(0, 0); }
            50% { transform: translate(-20px, 20px); }
            100% { transform: translate(20px, -20px); }
        }

        /* Header with Glassmorphism */
        header {
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(10px);
            -webkit-backdrop-filter: blur(10px);
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.05);
            border-bottom: 1px solid rgba(255, 255, 255, 0.2);
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1400px;
            margin: 0 auto;
            padding: 1rem 2rem;
        }

        .logo {
            display: flex;
            align-items: center;
            font-size: 1.8rem;
            font-weight: 700;
            background: linear-gradient(90deg, #4f46e5, #7c3aed);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-family: 'Playfair Display', serif;
            position: relative;
        }

        .logo-icon {
            margin-right: 10px;
            font-size: 2rem;
            color: #4f46e5;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }

        /* Hero Section */
        .hero {
            text-align: center;
            padding: 8rem 2rem 6rem;
            position: relative;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1.5rem;
            font-weight: 700;
            background: linear-gradient(90deg, #4f46e5, #7c3aed);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-family: 'Playfair Display', serif;
            line-height: 1.2;
        }

        .hero p {
            font-size: 1.3rem;
            color: var(--dark);
            max-width: 700px;
            margin: 0 auto 3rem;
            opacity: 0.9;
        }

        /* Tools Section */
        .tools-section {
            max-width: 1400px;
            margin: 0 auto;
            padding: 4rem 2rem;
        }

        .section-header {
            text-align: center;
            margin-bottom: 4rem;
        }

        .section-title {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--dark);
            margin-bottom: 1rem;
            font-family: 'Playfair Display', serif;
        }

        .section-subtitle {
            font-size: 1.2rem;
            color: var(--gray);
            max-width: 700px;
            margin: 0 auto;
        }

        /* Tool Categories */
        .tool-category {
            margin-bottom: 4rem;
        }

        .category-header {
            display: flex;
            align-items: center;
            margin-bottom: 2rem;
            padding-bottom: 1rem;
            border-bottom: 2px solid rgba(0, 0, 0, 0.05);
        }

        .category-icon {
            width: 50px;
            height: 50px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 1.5rem;
            color: white;
            font-size: 1.5rem;
        }

        .category-title {
            font-size: 1.8rem;
            font-weight: 600;
            color: var(--dark);
        }

        /* Tools Grid */
        .tools-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
        }

        /* Tool Cards */
        .tool-card {
            background: white;
            border-radius: 16px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.1);
            position: relative;
            z-index: 1;
            border: 1px solid rgba(255, 255, 255, 0.3);
        }

        .tool-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.1);
        }

        .tool-header {
            padding: 1.5rem;
            display: flex;
            align-items: center;
            position: relative;
        }

        .tool-icon {
            width: 50px;
            height: 50px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 1rem;
            color: white;
            font-size: 1.5rem;
        }

        .tool-title {
            font-size: 1.3rem;
            font-weight: 600;
            color: var(--dark);
        }

        .tool-body {
            padding: 0 1.5rem 1.5rem;
        }

        .tool-description {
            color: var(--gray);
            margin-bottom: 1.5rem;
            font-size: 0.95rem;
        }

        .tool-badge {
            display: inline-block;
            padding: 0.3rem 0.8rem;
            border-radius: 50px;
            font-size: 0.75rem;
            font-weight: 600;
            margin-right: 0.5rem;
            margin-bottom: 0.5rem;
        }

        .ai-badge {
            background: rgba(239, 68, 68, 0.1);
            color: #ef4444;
        }

        .new-badge {
            background: rgba(16, 185, 129, 0.1);
            color: #10b981;
        }

        .pro-badge {
            background: rgba(139, 92, 246, 0.1);
            color: #8b5cf6;
        }

        .tool-btn {
            display: inline-flex;
            align-items: center;
            padding: 0.6rem 1.2rem;
            border-radius: 8px;
            text-decoration: none;
            font-weight: 500;
            font-size: 0.9rem;
            transition: all 0.3s ease;
            cursor: pointer;
            border: none;
        }

        .tool-btn i {
            margin-left: 5px;
            font-size: 0.8rem;
            transition: transform 0.3s ease;
        }

        .tool-btn:hover i {
            transform: translateX(3px);
        }

        /* Color Categories */
        .convert-bg {
            background: var(--convert-gradient);
        }

        .edit-bg {
            background: var(--edit-gradient);
        }

        .security-bg {
            background: var(--security-gradient);
        }

        .organize-bg {
            background: var(--organize-gradient);
        }

        .image-bg {
            background: var(--image-gradient);
        }

        .special-bg {
            background: var(--special-gradient);
        }

        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 4rem 2rem 2rem;
        }

        .footer-content {
            max-width: 1400px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 3rem;
        }

        .footer-logo {
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 1rem;
            font-family: 'Playfair Display', serif;
            background: linear-gradient(90deg, #a5b4fc, #c7d2fe);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            display: flex;
            align-items: center;
        }

        .footer-logo i {
            margin-right: 10px;
            font-size: 2rem;
            color: #a5b4fc;
        }

        .copyright {
            text-align: center;
            padding-top: 3rem;
            margin-top: 3rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: var(--gray);
            font-size: 0.9rem;
        }

        /* Modal Styles */
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.5);
        }

        .modal-content {
            background-color: white;
            margin: 10% auto;
            padding: 2rem;
            border-radius: 12px;
            max-width: 500px;
            box-shadow: 0 5px 30px rgba(0,0,0,0.3);
            position: relative;
        }

        .close {
            position: absolute;
            right: 1rem;
            top: 1rem;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Progress Bar */
        progress {
            width: 100%;
            height: 10px;
            border-radius: 5px;
        }

        /* Responsive Design */
        @media (max-width: 1024px) {
            .hero h1 {
                font-size: 3rem;
            }
        }

        @media (max-width: 768px) {
            .tools-grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }

        @media (max-width: 480px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
            
            .tools-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Ad container styles */
        .ad-container {
            background: #f3f4f6;
            border-radius: 8px;
            padding: 1rem;
            margin: 2rem auto;
            text-align: center;
            max-width: 728px;
            border: 1px solid #e5e7eb;
        }

        .ad-label {
            font-size: 0.75rem;
            color: #6b7280;
            text-transform: uppercase;
            margin-bottom: 0.5rem;
        }

        /* Tool result container */
        .result-container {
            display: none;
            margin-top: 1rem;
            padding: 1rem;
            border: 1px dashed #ccc;
            border-radius: 8px;
        }

        .download-btn {
            background: var(--convert);
            color: white;
            padding: 0.5rem 1rem;
            border-radius: 4px;
            text-decoration: none;
            display: inline-block;
            margin-top: 1rem;
        }
    </style>
</head>
<body>
    <!-- Animated Background -->
    <div class="bg-pattern"></div>

    <!-- Header -->
    <header>
        <nav class="navbar">
            <div class="logo">
                <i class="fas fa-file-pdf logo-icon"></i>
                <span>Bishnupriya PDF World</span>
            </div>
            <div class="nav-links">
                <a href="#" id="homeLink">Home</a>
                <a href="#" id="toolsLink">Tools</a>
                <a href="#" id="loginLink">Login</a>
            </div>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <h1>Every Professional PDF Tool You Need</h1>
        <p>47 powerful tools to convert, edit, compress, and manage PDF files with 100% accuracy</p>
        <button id="tryNowBtn" class="tool-btn convert-bg" style="color: white;">Try Now for Free</button>
        
        <!-- Ad Space -->
        <div class="ad-container">
            <div class="ad-label">Advertisement</div>
            <div id="hero-ad">
                <!-- Ad content will be loaded here -->
                <p>Premium PDF Tools - Try Pro Version Today!</p>
                <a href="#" class="download-btn">Upgrade Now</a>
            </div>
        </div>
    </section>

    <!-- Tools Section -->
    <section class="tools-section" id="toolsSection">
        <div class="section-header">
            <h2 class="section-title">Complete PDF Toolkit</h2>
            <p class="section-subtitle">All 47 professional tools organized by category</p>
        </div>

        <!-- Convert Tools -->
        <div class="tool-category">
            <div class="category-header">
                <div class="category-icon convert-bg">
                    <i class="fas fa-exchange-alt"></i>
                </div>
                <h3 class="category-title">Convert</h3>
            </div>
            <div class="tools-grid">
                <!-- PDF to Word -->
                <div class="tool-card">
                    <div class="tool-header">
                        <div class="tool-icon convert-bg">
                            <i class="fas fa-file-word"></i>
                        </div>
                        <h4 class="tool-title">PDF to Word</h4>
                    </div>
                    <div class="tool-body">
                        <p class="tool-description">Convert PDF to editable Word documents with 99% accuracy</p>
                        <span class="tool-badge ai-badge">AI-Powered</span>
                        <button class="tool-btn convert-bg" style="color: white;" onclick="handleToolClick('pdfToWord')">Use Tool <i class="fas fa-arrow-right"></i></button>
                    </div>
                </div>
                
                <!-- PDF to Excel -->
                <div class="tool-card">
                    <div class="tool-header">
                        <div class="tool-icon convert-bg">
                            <i class="fas fa-file-excel"></i>
                        </div>
                        <h4 class="tool-title">PDF to Excel</h4>
                    </div>
                    <div class="tool-body">
                        <p class="tool-description">Extract tables from PDF to Excel with perfect formatting</p>
                        <span class="tool-badge ai-badge">AI-Powered</span>
                        <button class="tool-btn convert-bg" style="color: white;" onclick="handleToolClick('pdfToExcel')">Use Tool <i class="fas fa-arrow-right"></i></button>
                    </div>
                </div>
                
                <!-- PDF to PowerPoint -->
                <div class="tool-card">
                    <div class="tool-header">
                        <div class="tool-icon convert-bg">
                            <i class="fas fa-file-powerpoint"></i>
                        </div>
                        <h4 class="tool-title">PDF to PowerPoint</h4>
                    </div>
                    <div class="tool-body">
                        <p class="tool-description">Convert PDF to editable PowerPoint presentations</p>
                        <span class="tool-badge ai-badge">AI-Powered</span>
                        <button class="tool-btn convert-bg" style="color: white;" onclick="handleToolClick('pdfToPowerPoint')">Use Tool <i class="fas fa-arrow-right"></i></button>
                    </div>
                </div>
                
                <!-- Word to PDF -->
                <div class="tool-card">
                    <div class="tool-header">
                        <div class="tool-icon convert-bg">
                            <i class="fas fa-file-pdf"></i>
                        </div>
                        <h4 class="tool-title">Word to PDF</h4>
                    </div>
                    <div class="tool-body">
                        <p class="tool-description">Convert Word documents to high-quality PDFs</p>
                        <button class="tool-btn convert-bg" style="color: white;" onclick="handleToolClick('wordToPdf')">Use Tool <i class="fas fa-arrow-right"></i></button>
                    </div>
                </div>
                
                <!-- Excel to PDF -->
                <div class="tool-card">
                    <div class="tool-header">
                        <div class="tool-icon convert-bg">
                            <i class="fas fa-file-pdf"></i>
                        </div>
                        <h4 class="tool-title">Excel to PDF</h4>
                    </div>
                    <div class="tool-body">
                        <p class="tool-description">Convert Excel spreadsheets to PDF with proper formatting</p>
                        <button class="tool-btn convert-bg" style="color: white;" onclick="handleToolClick('excelToPdf')">Use Tool <i class="fas fa-arrow-right"></i></button>
                    </div>
                </div>
                
                <!-- PowerPoint to PDF -->
                <div class="tool-card">
                    <div class="tool-header">
                        <div class="tool-icon convert-bg">
                            <i class="fas fa-file-pdf"></i>
                        </div>
                        <h4 class="tool-title">PowerPoint to PDF</h4>
                    </div>
                    <div class="tool-body">
                        <p class="tool-description">Convert presentations to PDF while preserving animations</p>
                        <button class="tool-btn convert-bg" style="color: white;" onclick="handleToolClick('powerPointToPdf')">Use Tool <i class="fas fa-arrow-right"></i></button>
                    </div>
                </div>
                
                <!-- HTML to PDF -->
                <div class="tool-card">
                    <div class="tool-header">
                        <div class="tool-icon convert-bg">
                            <i class="fas fa-file-alt"></i>
                        </div>
                        <h4 class="tool-title">HTML to PDF</h4>
              
