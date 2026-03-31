<!DOCTYPE html>
<html lang="zh-HK">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>STEVEN | 天王教育 DSE 理科奪星導師</title>
    <meta name="description" content="STEVEN 沙田石門天王教育，專攻 DSE Chemistry & Biology。CUHK 藥劑系，提供私補式貼心教學及 24 小時問書服務。">
    <style>
        :root {
            --primary: #003366; /* CUHK Blue style */
            --accent: #FFD700; /* Star Gold */
            --text: #333;
            --light-bg: #f8f9fa;
            --white: #ffffff;
            --youtube-red: #FF0000;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; font-family: "Helvetica Neue", Helvetica, Arial, sans-serif; }

        body { line-height: 1.6; color: var(--text); }

        /* Navigation */
        nav { background: var(--white); padding: 0.5rem 5%; display: flex; justify-content: space-between; align-items: center; box-shadow: 0 2px 5px rgba(0,0,0,0.1); position: sticky; top: 0; z-index: 100; height: 80px; }

        /* [UPDATED] Logo Styles */
        .logo-container { display: flex; align-items: center; text-decoration: none; color: inherit; height: 100%; }
        .logo-img { height: 60px; width: auto; margin-right: 15px; } /* Adjustable logo size */
        .logo-text { font-size: 1.5rem; font-weight: bold; color: var(--primary); display: flex; flex-direction: column; line-height: 1.2; }
        .logo-sub { font-size: 0.8rem; color: #666; font-weight: normal; }

        .nav-links a { margin-left: 20px; text-decoration: none; color: var(--text); font-weight: 500; display: inline-block; }
        .cta-btn { background: var(--primary); color: var(--white); padding: 10px 20px; border-radius: 5px; text-decoration: none; font-weight: bold; transition: 0.3s; }
        .cta-btn:hover { background: #002244; }

        /* Hero Section */
        .hero { 
            background: linear-gradient(rgba(0,51,102,0.85), rgba(0,51,102,0.85)), url('https://images.unsplash.com/photo-1532094349884-543bc11b234d?auto=format&fit=crop&w=1920'); 
            background-size: cover; 
            background-position: center; 
            color: var(--white); 
            padding: 100px 5%; 
            text-align: center; 
        }
        .hero h1 { font-size: 3rem; margin-bottom: 1rem; line-height: 1.2; }
        .hero p { font-size: 1.2rem; margin-bottom: 2rem; max-width: 800px; margin-left: auto; margin-right: auto; }
        .hero-tags span { display: inline-block; background: var(--accent); color: var(--primary); padding: 5px 15px; border-radius: 20px; margin: 5px; font-weight: bold; font-size: 0.9rem; }

        /* Stats Section */
        .stats { display: flex; justify-content: space-around; padding: 40px 5%; background: var(--white); text-align: center; flex-wrap: wrap; box-shadow: 0 4px 6px rgba(0,0,0,0.05); position: relative; z-index: 10; margin-top: -30px; border-radius: 10px; max-width: 1000px; margin-left: auto; margin-right: auto; }
        .stat-item { flex: 1; min-width: 150px; margin: 10px; }
        .stat-number { font-size: 2.5rem; font-weight: bold; color: var(--primary); display: block; }

        /* General Section Styles */
        section { padding: 80px 5%; }
        .section-title { font-size: 2rem; color: var(--primary); margin-bottom: 20px; border-left: 5px solid var(--accent); padding-left: 15px; }

        /* About Section */
        .about { background: var(--light-bg); display: flex; flex-wrap: wrap; align-items: center; }
        .about-text { flex: 1; min-width: 300px; padding-right: 40px; }
        .about-img { flex: 1; min-width: 300px; height: 400px; background: #e0e0e0; border-radius: 10px; display: flex; align-items: center; justify-content: center; color: #666; overflow: hidden; }

        /* Schools List Section */
        .schools-section { background: var(--primary); color: white; text-align: center; padding: 60px 5%; }
        .schools-title { color: var(--accent); font-size: 2rem; margin-bottom: 10px; font-weight: bold; }
        .schools-subtitle { color: #ccc; margin-bottom: 40px; font-size: 1.1rem; letter-spacing: 2px; }

        .schools-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 40px; max-width: 1200px; margin: 0 auto; }

        .school-category { text-align: left; background: rgba(255,255,255,0.05); padding: 30px; border-radius: 10px; border: 1px solid rgba(255,255,255,0.1); }
        .school-category h3 { font-size: 1.5rem; margin-bottom: 20px; padding-bottom: 10px; border-bottom: 2px solid; display: inline-block; }

        /* Elite Style */
        .elite-cat h3 { color: #FFD700; border-color: #FFD700; }
        .elite-cat .school-list li:before { content: "👑"; margin-right: 10px; }

        /* Remedial Style */
        .remedial-cat h3 { color: #4FC3F7; border-color: #4FC3F7; }
        .remedial-cat .school-list li:before { content: "📈"; margin-right: 10px; }

        .school-list { list-style: none; columns: 1; }
        .school-list li { margin-bottom: 12px; font-size: 1rem; color: #eee; display: flex; align-items: center; }

        /* Features */
        .feature-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 30px; margin-top: 40px; }
        .feature-card { padding: 30px; border: 1px solid #eee; border-radius: 10px; text-align: center; transition: 0.3s; background: white; }
        .feature-card:hover { transform: translateY(-5px); box-shadow: 0 10px 20px rgba(0,0,0,0.1); border-color: var(--primary); }
        .feature-icon { font-size: 3rem; margin-bottom: 20px; display: block; }

        /* Video Portal Styles */
        .video-section { background: #fff; }
        .video-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px; margin-top: 40px; }
        .video-card { border-radius: 10px; overflow: hidden; box-shadow: 0 4px 10px rgba(0,0,0,0.1); transition: 0.3s; text-decoration: none; color: inherit; display: block; }
        .video-card:hover { transform: translateY(-5px); box-shadow: 0 8px 15px rgba(0,0,0,0.2); }
        .video-thumbnail { width: 100%; height: 200px; background: #000; position: relative; display: flex; align-items: center; justify-content: center; overflow: hidden; }
        .video-thumbnail img { width: 100%; height: 100%; object-fit: cover; opacity: 0.8; }
        .play-icon { font-size: 3rem; color: white; position: absolute; z-index: 2; text-shadow: 0 2px 10px rgba(0,0,0,0.5); }
        .video-info { padding: 20px; }
        .video-info h3 { font-size: 1.1rem; margin-bottom: 10px; color: var(--primary); }
        .youtube-btn { display: inline-block; background: var(--youtube-red); color: white; padding: 10px 25px; border-radius: 50px; text-decoration: none; font-weight: bold; margin-top: 30px; transition: 0.3s; }
        .youtube-btn:hover { background: #cc0000; }

        /* Timetable Styles */
        .timetable-section { background: var(--light-bg); }
        .table-container { overflow-x: auto; /* Allow scrolling on mobile */ background: white; border-radius: 10px; box-shadow: 0 4px 10px rgba(0,0,0,0.05); }
        table { width: 100%; border-collapse: collapse; min-width: 600px; /* Force width for scroll */ }
        th { background: var(--primary); color: white; padding: 15px; text-align: left; }
        td { padding: 15px; border-bottom: 1px solid #eee; color: #555; vertical-align: middle; }
        tr:last-child td { border-bottom: none; }
        tr:hover td { background: #f0f4f8; }
        .subject-tag { display: inline-block; padding: 3px 8px; border-radius: 4px; font-size: 0.8rem; font-weight: bold; margin-right: 5px; }
        .chem { background: #e3f2fd; color: #1976d2; }
        .bio { background: #e8f5e9; color: #388e3c; }
        .video-class { background: #eee; color: #666; }

        /* Testimonials */
        .testimonials { background: var(--white); }
        .testimonial-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px; margin-top: 30px; }
        .testimonial-card { background: #f8f9fa; padding: 30px; border-radius: 10px; font-style: italic; border: 1px solid #eee; }
        .student-name { display: block; margin-top: 20px; font-weight: bold; color: var(--primary); font-style: normal; text-align: right; }

        /* CTA Section */
        .cta-section { text-align: center; background: var(--light-bg); }
        .whatsapp-float { position: fixed; bottom: 30px; right: 30px; background: #25D366; color: white; width: 60px; height: 60px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 30px; box-shadow: 0 4px 10px rgba(0,0,0,0.3); z-index: 1000; text-decoration: none; transition: transform 0.3s; }
        .whatsapp-float:hover { transform: scale(1.1); }

        /* Footer */
        footer { background: #333; color: #aaa; text-align: center; padding: 20px; font-size: 0.9rem; }

        @media (max-width: 768px) {
            .hero h1 { font-size: 2rem; }
            .nav-links { display: none; }
            .about-text { padding-right: 0; margin-bottom: 30px; }
            .stats { margin-top: 0; border-radius: 0; }
            .school-category { text-align: center; }
            .school-list li { justify-content: center; }
            .school-list li:before { display: none; } /* Simplify for mobile */
            .logo-text { display: none; } /* On very small screens, only show logo icon */
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body>

    <nav>
        <a href="#" class="logo-container">
            <img src="https://github.com/chenzhenyang217-netizen/STEVEN.github.io/blob/8740650f8979c82ff8ff0b371a2e8c8b69c83366/JPEG%E5%BD%B1%E5%83%8F-4B86-811F-D8-0.JPEG?raw=true" class="logo-img">
            <div class="logo-text">
                Steven Sir 
                <span class="logo-sub">天王教育 | DSE理科專家</span>
            </div>
        </a>
        <div class="nav-links">
            <a href="#about">導師簡介</a>
            <a href="#schools">最強戰績</a>
            <a href="#timetable">時間表</a>
            <a href="#contact" class="cta-btn">立即報名</a>
        </div>
    </nav>

    <section class="hero">
        <div class="hero-tags">
            <span>🔥 全沙田最有實力</span>
            <span>💊 CUHK 醫學院</span>
            <span>⭐ DSE 奪星專家</span>
        </div>
        <h1>理科想奪星？<br>揀 Steven Sir！</h1>
        <p>專攻 DSE Chemistry & Biology | 私補式貼心教學 | 24小時無限問書<br>最強星級配套，助你輕鬆應付學校考試及 DSE。</p>
        <a href="https://wa.me/85212345678" class="cta-btn" style="padding: 15px 30px; font-size: 1.2rem; display: inline-block; margin-top: 20px;">
            <i class="fab fa-whatsapp"></i> 預約免費試堂
        </a>
    </section>

    <section class="stats">
        <div class="stat-item">
            <span class="stat-number">100%</span>
            <span>用心教學</span>
        </div>
        <div class="stat-item">
            <span class="stat-number">24hr</span>
            <span>WhatsApp 支援</span>
        </div>
        <div class="stat-item">
            <span class="stat-number">10+</span>
            <span>團隊奪星總數</span>
        </div>
    </section>

    <section id="about" class="about">
        <div class="about-text">
            <h2 class="section-title">關於 Steven Sir</h2>
            <p style="margin-bottom: 15px;"><strong>親身於 DSE Chemistry ⚛️ Biology 🧬 奪星</strong></p>
            <ul style="list-style: none; margin-bottom: 20px;">
                <li style="margin-bottom: 8px;">🎓 中大醫學院 • 藥劑學 (Pharmacy, CUHK)</li>
                <li style="margin-bottom: 8px;">🧬 副修生命科學：細胞及分子生物學</li>
                <li style="margin-bottom: 8px;">🏆 天王教育 (Tim Wong Education) 首席導師</li>
            </ul>
            <p>「若果不曾走過，怎會懂？因為我識教，先會有咁多學生！」</p>
            <p>我不僅教你知識，更教你考試的策略。從題目設計到批改，我與團隊都親力親為，因為我們關心每個學生的進度。</p>
        </div>
        <div class="about-img">
            <img src="https://github.com/chenzhenyang217-netizen/STEVEN.github.io/blob/8740650f8979c82ff8ff0b371a2e8c8b69c83366/JPEG%E5%BD%B1%E5%83%8F-4B86-811F-D8-0.JPEG?raw=true" style="width:100%; height:100%; object-fit:cover;">
        </div>
    </section>

    <section id="schools" class="schools-section">
        <div class="schools-title">最強拔尖．最強保底</div>
        <div class="schools-subtitle">無論名校定底子弱，來到 Steven Sir 課堂都能進步！</div>

        <div class="schools-grid">
            <div class="school-category elite-cat">
                <h3>👑 名校之選．頂尖實力</h3>
                <p style="color:#ccc; margin-bottom:15px; font-size:0.9rem;">來自全港 Band 1 名校的尖子首選，目標衝擊 5** / 醫科神科</p>
                <ul class="school-list">
                    <li><strong>拔萃女書院 (DGS)</strong></li>
                    <li><strong>喇沙書院 (La Salle College)</strong></li>
                    <li><strong>聖公會曾肇添中學 (SKHTST)</strong></li>
                    <li><strong>九龍真光中學 </strong></li>
                    <li>浸信會呂明才中學</li>
                    <li>沙田官立中學</li>
                    <li>沙田崇真中學</li>
                    <li>沙田培英中學</li>
                    <li>聖公會林裘謀中學</li>
                    <li>聖羅撒書院</li>
                    <li>五旬節林漢光中學</li>
                    <li>香港浸會大學附屬學校王錦輝中小學</li>
                    <li>培僑書院</li>
                    <li>沙田循道衞理中學</li>
                    <li>沙田蘇浙公學</li>
                    <li>天主教郭得勝中學</li>
                    <li>賽馬會體藝中學</li>
                    <li>國際基督教優質音樂中學暨小學</li>
                    <li>香港神託會培基書院</li>
                </ul>
            </div>

            <div class="school-category remedial-cat">
                <h3>📈 保底之選．絕地翻身</h3>
                <p style="color:#ccc; margin-bottom:15px; font-size:0.9rem;">由 U/2 升上 4/5，專攻合格及升 Grade 策略，重建信心！</p>
                <ul class="school-list">
                    <li>基督書院</li>
                    <li>樂善堂楊葛小琳中學</li>
                    <li>保良局胡忠中學</li>
                    <li>青年會書院</li>
                    <li>沙田蘇浙公學</li>
                    <li>林大輝中學</li>
                    <li>馬鞍山崇真中學</li>
                    <li>宣道會鄭榮之中學</li>
                    <li>聖母無玷聖心書院</li>
                    <li>香港中文大學校友會聯會陳震夏中學</li>
                </ul>
            </div>
        </div>
    </section>

    <section id="features" class="features">
        <h2 class="section-title" style="text-align: center; border: none; margin-bottom: 50px;">為什麼選擇我們？</h2>
        <div class="feature-grid">
            <div class="feature-card">
                <span class="feature-icon">💬</span>
                <h3>24小時無限問書</h3>
                <p>做卷遇到唔識？隨時 WhatsApp 我。我會用最清晰的方式，甚至拍片一步步解釋俾你聽。</p>
            </div>
            <div class="feature-card">
                <span class="feature-icon">📚</span>
                <h3>超強筆記 + 題海戰術</h3>
                <p>獨家編制筆記，涵蓋 DSE 陷阱位。針對 2025/26 出題方向，不做無用功。</p>
            </div>
            <div class="feature-card">
                <span class="feature-icon">🎯</span>
                <h3>私補式貼心教學</h3>
                <p>不同於大型補習社的疏離感，我地關心每一位學生的進度，提供針對性建議。</p>
            </div>
        </div>
    </section>

    <section id="videos" class="video-section">
        <h2 class="section-title" style="text-align: center; border:none;">真材實料．免費試堂影片</h2>
        <p style="text-align: center; color: #666;">不用付費，先看教學風格。清晰概念，一聽即明！</p>

        <div class="video-grid">
            <a href="https://youtu.be/v6YZgokO0Pg" target="_blank" class="video-card">
                <div class="video-thumbnail">
                    <img src="https://github.com/chenzhenyang217-netizen/STEVEN.github.io/blob/c587f1688095cfbd507431e4ef2e6fefc2e4d5ec/%E9%87%8D%E6%BA%AB%20%E5%BF%85%E7%9D%87%E7%B3%BB%E5%88%97.png?raw=true" alt="Chem Video">
                    <i class="fas fa-play-circle play-icon"></i>
                </div>
                <div class="video-info">
                    <h3>🧬 DSE Biology Photosynthesis(1)：Photochemical Reaction</h3>
                    <p>3大搶分字眼｜考評局伏位。</p>
                </div>
            </a>
            <a href="https://youtu.be/4-W6_Zso7Rc?si=ZroiyOqkZ3i2y5bS" class="video-card">
                <div class="video-thumbnail">
                    <img src="https://github.com/chenzhenyang217-netizen/STEVEN.github.io/blob/c587f1688095cfbd507431e4ef2e6fefc2e4d5ec/%E9%87%8D%E6%BA%AB%20%E5%BF%85%E7%9D%87%E7%B3%BB%E5%88%97.png?raw=true" alt="Bio Video">
                    <i class="fas fa-play-circle play-icon"></i>
                </div>
                <div class="video-info">
                    <h3>🧬 DSE Biology Photosynthesis(2):Calvin Cycle</h3>
                    <p>DSE MC最常混淆位｜輕鬆攞分。</p>
                </div>
            </a>
            <a href="https://www.youtube.com/@yourschannel" target="_blank" class="video-card">
                <div class="video-thumbnail">
                    <img src="https://images.unsplash.com/photo-1434030216411-0b793f4b4173?auto=format&fit=crop&w=600" alt="Exam Skills">
                    <i class="fas fa-play-circle play-icon"></i>
                </div>
                <div class="video-info">
                    <h3>🔥 考前 30 日溫習策略</h3>
                    <p>如何編排時間表？最後衝刺的心態調整。</p>
                </div>
            </a>
        </div>
        <div style="text-align: center;">
            <a href="https://www.youtube.com/@STEVEN__DSE-z8h" target="_blank" class="youtube-btn">
                <i class="fab fa-youtube"></i> 訂閱我的 YouTube 頻道
            </a>
        </div>
    </section>

    <section id="timetable" class="timetable-section">
        <h2 class="section-title">2026 常規課程時間表</h2>
        <p style="margin-bottom: 20px;">地點：沙田石門京瑞廣場 (天王教育) | <span style="color:red; font-weight:bold;">Video Class</span> 任何時間段，隨時重溫！</p>

        <div class="table-container">
            <table>
                <thead>
                    <tr>
                        <th width="15%">年級</th>
                        <th width="25%">科目</th>
                        <th width="40%">上課時間</th>
                        <th width="20%">狀態</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td><strong>S.3 (中三)</strong></td>
                        <td><span class="subject-tag chem">CHEM</span> <span class="subject-tag bio">BIO</span> 終極大考衝刺班</td>
                        <td>
                            星期六 6:00-7:30 pm (Chemistry)<br>
                            星期六 8:00-9:30 pm (Biology)<br>
                            星期日 7:00-8:30 pm (實戰操卷班 📝)
                        </td>
                        <td style="color: #e67e22; font-weight: bold;">🔥 即將滿額</td>
                    </tr>
                    <tr>
                        <td><strong>S.6 (中六)</strong></td>
                        <td><span class="subject-tag chem">CHEM</span> 終極衝刺班</td>
                        <td>星期六 7:30 – 9:00 pm</td>
                        <td style="color: #e67e22; font-weight: bold;">🔥 最後召集</td>
                    </tr>
                    <tr>
                        <td><strong>S.5 (中五)</strong></td>
                        <td><span class="subject-tag chem">CHEM</span> 常規拔尖/補底班</td>
                        <td>星期日 7:00 – 8:30 pm</td>
                        <td style="color: green;">招生中</td>
                    </tr>
                    <tr>
                        <td><strong>S.5 (中五)</strong></td>
                        <td><span class="subject-tag bio">BIO</span> 常規拔尖/補底班</td>
                        <td>星期日 5:00 – 6:30 pm</td>
                        <td style="color: green;">招生中</td>
                    </tr>
                    <tr>
                        <td><strong>S.4 (中四)</strong></td>
                        <td><span class="subject-tag bio">BIO</span> 常規拔尖/補底班</td>
                        <td>星期二 7:40 – 9:10 pm</td>
                        <td style="color: green;">招生中</td>
                    </tr>
                    <tr>
                        <td><strong>S.4 (中四)</strong></td>
                        <td><span class="subject-tag chem">CHEM</span> 常規拔尖/補底班</td>
                        <td>星期三 7:40 – 9:10 pm</td>
                        <td style="color: green;">招生中</td>
                    </tr>
                    <tr>
                        <td><strong>全級別</strong></td>
                        <td><span class="subject-tag video-class">VIDEO</span> 自選topic重溫模式</td>
                        <td>任何時間段，隨時重溫！</td>
                        <td style="color: #555;">📼 彈性上課</td>
                    </tr>
                </tbody>
            </table>
        </div>
    </section>

    <section id="testimonials" class="testimonials">
        <h2 class="section-title">學生真實好評</h2>
        <div class="testimonial-grid">
            <div class="testimonial-card">
                <p>"Steven 真係超有心機！💖 最正係佢會特登拍片，一步步解釋俾我聽，令我掌握每個概念！"</p>
                <span class="student-name">- 沙田培英中學 葉同學</span>
            </div>
            <div class="testimonial-card">
                <p>"本身 Chem 成績麻麻，補咗 Steven 之後，今次居然進步到全級第三！配套超實用！"</p>
                <span class="student-name">- 中聖書院 譚同學</span>
            </div>
            <div class="testimonial-card">
                <p>"多謝 Steven 的悉心教導，令我在考試中大幅進步！常規課程超級幫到我！"</p>
                <span class="student-name">- 九龍真光中學 謝同學</span>
            </div>
        </div>
    </section>

    <section id="contact" class="cta-section">
        <h2 class="section-title" style="border:none; margin-bottom: 10px;">加入我們，下一個奪星就是你</h2>
        <p style="margin-bottom: 30px;">地點：沙田石門京瑞廣場 (天王教育)</p>

        <div style="background: #fff3cd; padding: 20px; border-radius: 10px; display: inline-block; margin-bottom: 30px; border: 1px solid #ffeeba;">
            <p style="color: #856404; margin: 0;"><strong>🔥 新生優惠：報讀 Bio/Chem 可享 $200 學費資助！</strong></p>
        </div>
        <br>

        <a href="https://wa.me/85265572013" class="cta-btn" style="padding: 15px 40px; font-size: 1.3rem; display: inline-block;">
            立即 WhatsApp 查詢 / 報名
        </a>
    </section>

    <footer>
        <p>&copy; 2026 STEVEN. All Rights Reserved. | 天王教育 Tim Wong Education</p>
    </footer>

    <a href="https://wa.me/85265572013" class="whatsapp-float" target="_blank">
        <i class="fab fa-whatsapp"></i>
    </a>

</body>
</html>
