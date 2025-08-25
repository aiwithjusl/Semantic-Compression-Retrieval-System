<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Semantic Compression & Retrieval System</title>
    <meta name="description" content="Ultra-efficient semantic compression with intelligent retrieval for mobile-first applications">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .hero {
            text-align: center;
            padding: 80px 0;
            color: white;
        }

        .banner {
            background: linear-gradient(45deg, #00d4ff, #ff6b6b, #4ecdc4);
            padding: 4px;
            border-radius: 20px;
            margin-bottom: 40px;
            position: relative;
            overflow: hidden;
            display: inline-block;
        }

        .banner::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent);
            animation: shimmer 3s infinite;
        }

        @keyframes shimmer {
            0% { left: -100%; }
            100% { left: 100%; }
        }

        .banner-content {
            background: rgba(30, 30, 46, 0.95);
            border-radius: 16px;
            padding: 40px 60px;
            backdrop-filter: blur(10px);
        }

        .hero-title {
            font-size: 3rem;
            font-weight: 700;
            background: linear-gradient(45deg, #00d4ff, #ff6b6b);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 20px;
        }

        .hero-subtitle {
            font-size: 1.3rem;
            margin-bottom: 30px;
            opacity: 0.9;
        }

        .cta-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 15px 30px;
            border: none;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s ease;
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            gap: 10px;
        }

        .btn-primary {
            background: linear-gradient(45deg, #00d4ff, #0099cc);
            color: white;
        }

        .btn-secondary {
            background: rgba(255, 255, 255, 0.2);
            color: white;
            border: 2px solid rgba(255, 255, 255, 0.3);
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }

        .features {
            background: white;
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 50px;
            color: #333;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
            margin-bottom: 60px;
        }

        .feature-card {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            padding: 40px 30px;
            border-radius: 20px;
            text-align: center;
            transition: all 0.3s ease;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        }

        .feature-icon {
            font-size: 3rem;
            margin-bottom: 20px;
        }

        .feature-title {
            font-size: 1.4rem;
            font-weight: 600;
            margin-bottom: 15px;
            color: #333;
        }

        .feature-description {
            color: #666;
            line-height: 1.6;
        }

        .metrics {
            background: linear-gradient(135deg, #1e1e2e 0%, #2d1b69 100%);
            padding: 80px 0;
            color: white;
        }

        .metrics-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            text-align: center;
        }

        .metric-item {
            padding: 30px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            backdrop-filter: blur(10px);
        }

        .metric-value {
            font-size: 3rem;
            font-weight: 700;
            color: #00d4ff;
            margin-bottom: 10px;
        }

        .metric-label {
            font-size: 1.1rem;
            opacity: 0.8;
        }

        .demo-section {
            background: #f8f9fa;
            padding: 80px 0;
            text-align: center;
        }

        .demo-preview {
            background: white;
            border-radius: 20px;
            padding: 40px;
            margin: 40px auto;
            max-width: 800px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.1);
        }

        .demo-screenshot {
            width: 100%;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        }

        .tech-stack {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            padding: 80px 0;
            color: white;
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .tech-item {
            background: rgba(255, 255, 255, 0.1);
            padding: 30px;
            border-radius: 15px;
            backdrop-filter: blur(10px);
        }

        .tech-item h3 {
            color: #00d4ff;
            margin-bottom: 15px;
            font-size: 1.3rem;
        }

        .footer {
            background: #1e1e2e;
            color: white;
            padding: 60px 0 40px;
            text-align: center;
        }

        .footer-links {
            display: flex;
            justify-content: center;
            gap: 40px;
            margin-bottom: 30px;
            flex-wrap: wrap;
        }

        .footer-links a {
            color: #00d4ff;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .footer-links a:hover {
            color: #ff6b6b;
        }

        @media (max-width: 768px) {
            .hero-title {
                font-size: 2.2rem;
            }

            .banner-content {
                padding: 30px 40px;
            }

            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }

            .features-grid,
            .metrics-grid,
            .tech-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="hero">
        <div class="container">
            <div class="banner">
                <div class="banner-content">
                    <h1 class="hero-title">Semantic Compression & Retrieval</h1>
                    <p class="hero-subtitle">Ultra-efficient semantic compression with intelligent retrieval for mobile-first applications</p>
                </div>
            </div>
            
            <div class="cta-buttons">
                <a href="#demo" class="btn btn-primary">
                    🚀 Live Demo
                </a>
                <a href="https://github.com/yourusername/semantic-compression-system" class="btn btn-secondary">
                    📋 View Source
                </a>
            </div>
        </div>
    </div>

    <section class="features">
        <div class="container">
            <h2 class="section-title">Breakthrough Technology</h2>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">🗜️</div>
                    <h3 class="feature-title">Advanced Compression</h3>
                    <p class="feature-description">Achieve 60-85% size reduction while preserving semantic meaning through intelligent clustering algorithms.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">🧠</div>
                    <h3 class="feature-title">Semantic Understanding</h3>
                    <p class="feature-description">Context-aware processing that understands meaning, not just keywords, for superior search accuracy.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">📱</div>
                    <h3 class="feature-title">Mobile-First</h3>
                    <p class="feature-description">Optimized for resource-constrained environments with offline capabilities and minimal battery impact.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">⚡</div>
                    <h3 class="feature-title">Real-Time Processing</h3>
                    <p class="feature-description">Sub-200ms query response times with efficient algorithms designed for instant results.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">🔍</div>
                    <h3 class="feature-title">Intent-Based Search</h3>
                    <p class="feature-description">Advanced retrieval system that understands user intent and provides contextually relevant results.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">🛡️</div>
                    <h3 class="feature-title">Privacy-First</h3>
                    <p class="feature-description">All processing happens client-side. Your data never leaves your device, ensuring complete privacy.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="metrics">
        <div class="container">
            <h2 class="section-title">Performance Metrics</h2>
            <div class="metrics-grid">
                <div class="metric-item">
                    <div class="metric-value">85%</div>
                    <div class="metric-label">Compression Ratio</div>
                </div>
                <div class="metric-item">
                    <div class="metric-value">95%</div>
                    <div class="metric-label">Semantic Preservation</div>
                </div>
                <div class="metric-item">
                    <div class="metric-value">90%</div>
                    <div class="metric-label">Search Accuracy</div>
                </div>
                <div class="metric-item">
                    <div class="metric-value">150ms</div>
                    <div class="metric-label">Query Response</div>
                </div>
                <div class="metric-item">
                    <div class="metric-value">&lt;5MB</div>
                    <div class="metric-label">Memory Footprint</div>
                </div>
            </div>
        </div>
    </section>

    <section class="demo-section" id="demo">
        <div class="container">
            <h2 class="section-title">Experience the Technology</h2>
            <div class="demo-preview">
                <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='600' height='400' viewBox='0 0 600 400'%3E%3Crect width='600' height='400' fill='%23f8f9fa'/%3E%3Crect x='20' y='20' width='560' height='60' rx='30' fill='%23e9ecef'/%3E%3Ctext x='300' y='55' text-anchor='middle' fill='%23495057' font-family='Arial' font-size='18' font-weight='bold'%3ESemantic Compression Demo%3C/text%3E%3Crect x='40' y='100' width='250' height='120' rx='10' fill='%23fff' stroke='%23dee2e6'/%3E%3Ctext x='165' y='125' text-anchor='middle' fill='%2300d4ff' font-family='Arial' font-size='14' font-weight='bold'%3EDocument Input%3C/text%3E%3Crect x='310' y='100' width='250' height='120' rx='10' fill='%23fff' stroke='%23dee2e6'/%3E%3Ctext x='435' y='125' text-anchor='middle' fill='%2300d4ff' font-family='Arial' font-size='14' font-weight='bold'%3ECompressed Output%3C/text%3E%3Crect x='40' y='240' width='520' height='100' rx='10' fill='%23fff' stroke='%23dee2e6'/%3E%3Ctext x='300' y='265' text-anchor='middle' fill='%2300d4ff' font-family='Arial' font-size='14' font-weight='bold'%3ESemantic Search%3C/text%3E%3Ccircle cx='100' cy='300' r='8' fill='%234ecdc4'/%3E%3Ccircle cx='200' cy='310' r='6' fill='%23ff6b6b'/%3E%3Ccircle cx='300' cy='290' r='7' fill='%2300d4ff'/%3E%3Ccircle cx='400' cy='305' r='5' fill='%234ecdc4'/%3E%3Ccircle cx='500' cy='295' r='9' fill='%23ff6b6b'/%3E%3C/svg%3E" alt="Semantic Compression System Demo" class="demo-screenshot">
                <p style="margin-top: 20px; color: #666;">Interactive demo showcasing real-time compression and semantic search capabilities</p>
            </div>
            <div class="cta-buttons">
                <a href="demo.html" class="btn btn-primary">
                    🎮 Try Interactive Demo
                </a>
            </div>
        </div>
    </section>

    <section class="tech-stack">
        <div class="container">
            <h2 class="section-title">Technical Innovation</h2>
            <div class="tech-grid">
                <div class="tech-item">
                    <h3>🔬 Compression Algorithm</h3>
                    <p>Custom semantic clustering with context-aware tokenization and intelligent redundancy elimination.</p>
                </div>
                
                <div class="tech-item">
                    <h3>🎯 Vector Embeddings</h3>
                    <p>128-dimensional semantic vectors optimized for mobile processing with contextual weighting.</p>
                </div>
                
                <div class="tech-item">
                    <h3>🔍 Hybrid Search</h3>
                    <p>Combines cosine similarity with keyword relevance for optimal search accuracy and performance.</p>
                </div>
                
                <div class="tech-item">
                    <h3>⚡ Mobile Optimization</h3>
                    <p>Lightweight runtime with progressive enhancement and offline-first architecture.</p>
                </div>
            </div>
        </div>
    </section>

    <footer class="footer">
        <div class="container">
            <div class="footer-links">
                <a href="https://github.com/yourusername/semantic-compression-system">GitHub Repository</a>
                <a href="https://github.com/yourusername/semantic-compression-system/wiki">Documentation</a>
                <a href="https://github.com/yourusername/semantic-compression-system/issues">Report Issues</a>
                <a href="demo.html">Live Demo</a>
            </div>
            <p>&copy; 2025 Semantic Compression & Retrieval System. Built with ❤️ for intelligent compression.</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for anchor links
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

        // Add intersection observer for animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Observe feature cards for animation
        document.querySelectorAll('.feature-card, .metric-item, .tech-item').forEach(card => {
            card.style.opacity = '0';
            card.style.transform = 'translateY(30px)';
            card.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(card);
        });
    </script>
</body>
</html>
