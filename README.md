# Baipang<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <title>林炯诚 · 安全工程+计算机 | 个人主页</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: #f8fafc;
            color: #0f172a;
            line-height: 1.5;
            scroll-behavior: smooth;
        }

        .container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 2rem 1.5rem;
        }

        /* 卡片样式 */
        .card {
            background: white;
            border-radius: 1.5rem;
            box-shadow: 0 8px 20px rgba(0,0,0,0.03), 0 2px 6px rgba(0,0,0,0.05);
            padding: 1.8rem;
            margin-bottom: 2rem;
            transition: all 0.2s ease;
            border: 1px solid #eef2f6;
        }

        .section-title {
            font-size: 1.75rem;
            font-weight: 700;
            letter-spacing: -0.3px;
            border-left: 5px solid #3b82f6;
            padding-left: 1rem;
            margin-bottom: 1.5rem;
            color: #0f172a;
        }

        .badge {
            display: inline-block;
            background: #eef2ff;
            color: #1e40af;
            border-radius: 40px;
            padding: 0.2rem 0.8rem;
            font-size: 0.75rem;
            font-weight: 500;
        }

        /* 头像区 + 个人资料卡 */
        .profile-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            align-items: flex-start;
        }
        .profile-avatar {
            flex: 1;
            min-width: 200px;
            text-align: center;
        }
        .avatar-img {
            width: 180px;
            height: 180px;
            object-fit: cover;
            border-radius: 50%;
            border: 4px solid white;
            box-shadow: 0 12px 24px -8px rgba(0,0,0,0.15);
            background: #d9e2ef;
        }
        .profile-info-card {
            flex: 2;
            background: linear-gradient(135deg, #ffffff 0%, #f9fafb 100%);
            border-radius: 1.5rem;
            padding: 1.5rem;
            box-shadow: 0 6px 14px rgba(0,0,0,0.05);
            border: 1px solid #e2e8f0;
        }
        .info-row {
            display: flex;
            flex-wrap: wrap;
            margin-bottom: 0.75rem;
            align-items: baseline;
        }
        .info-label {
            width: 100px;
            font-weight: 600;
            color: #334155;
        }
        .info-content {
            flex: 1;
            color: #1e293b;
        }
        .tag-group {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-top: 0.5rem;
        }
        .skill-tag {
            background: #eef2ff;
            padding: 0.2rem 0.8rem;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 500;
        }
        .interest-tag {
            background: #f1f5f9;
            padding: 0.3rem 1rem;
            border-radius: 30px;
            font-size: 0.85rem;
        }

        /* 网格布局（奖项/竞赛）*/
        .grid-2col {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            gap: 1rem;
        }
        .list-item {
            display: flex;
            align-items: baseline;
            gap: 0.75rem;
            padding: 0.6rem 0;
            border-bottom: 1px dashed #eef2f6;
        }
        .list-icon {
            color: #3b82f6;
            width: 24px;
            font-size: 1rem;
        }
        .patent-box {
            background: #fefce8;
            border-left: 4px solid #eab308;
            padding: 0.8rem;
            border-radius: 1rem;
            margin-top: 0.5rem;
        }

        /* 照片画廊 */
        .gallery {
            display: flex;
            flex-wrap: wrap;
            gap: 1.2rem;
            justify-content: center;
            margin-top: 1rem;
        }
        .gallery-item {
            flex: 1;
            min-width: 180px;
            border-radius: 1.2rem;
            overflow: hidden;
            background: #f1f5f9;
            box-shadow: 0 6px 12px rgba(0,0,0,0.05);
            transition: transform 0.2s;
        }
        .gallery-item:hover {
            transform: translateY(-4px);
        }
        .gallery-item img {
            width: 100%;
            height: 160px;
            object-fit: cover;
            display: block;
        }
        .gallery-caption {
            padding: 0.6rem;
            font-size: 0.8rem;
            text-align: center;
            font-weight: 500;
            background: white;
        }

        /* 时间线规划 */
        .timeline {
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }
        .timeline-node {
            display: flex;
            gap: 1rem;
            align-items: flex-start;
        }
        .timeline-year {
            min-width: 80px;
            font-weight: 700;
            color: #3b82f6;
            background: #eef2ff;
            padding: 0.2rem 0.8rem;
            border-radius: 30px;
            text-align: center;
            font-size: 0.9rem;
        }
        .timeline-text {
            background: #f8fafc;
            padding: 0.6rem 1rem;
            border-radius: 1rem;
            flex: 1;
        }

        hr {
            margin: 1rem 0;
            border: 0;
            height: 1px;
            background: #e2e8f0;
        }

        footer {
            text-align: center;
            margin-top: 2rem;
            padding: 1.5rem;
            color: #5b6e8c;
            font-size: 0.85rem;
            border-top: 1px solid #e2e8f0;
        }

        @media (max-width: 720px) {
            .container {
                padding: 1rem;
            }
            .profile-grid {
                flex-direction: column;
                align-items: center;
            }
            .info-label {
                width: 100%;
                margin-bottom: 0.2rem;
            }
            .info-row {
                flex-direction: column;
            }
            .timeline-node {
                flex-direction: column;
            }
            .timeline-year {
                align-self: flex-start;
            }
        }
    </style>
</head>
<body>

<div class="container">
    <!-- ********** 个人资料卡 + 头像 (截图核心区域) ********** -->
    <div class="profile-grid" id="personalCard">
        <div class="profile-avatar">
            <img class="avatar-img" src="https://picsum.photos/id/77/200/200" alt="个人照片 - 篮球场剪影">
            <div style="margin-top: 1rem;">
                <i class="fas fa-basketball-ball" style="color:#ef4444;"></i> 篮球 · 
                <i class="fas fa-music" style="color:#8b5cf6;"></i> 音乐 · 
                <i class="fas fa-plane-departure" style="color:#0ea5e9;"></i> 旅行
            </div>
        </div>
        <div class="profile-info-card">
            <h2 style="font-size: 1.9rem; font-weight: 700; margin-bottom: 0.25rem;">陈志远 <span style="font-size: 1rem; font-weight: normal; background:#eef2ff; padding:2px 10px; border-radius:40px;">23安全工程2班 · 辅修计算机</span></h2>
            <p style="color: #475569; margin-bottom: 1rem;"><i class="fas fa-map-marker-alt"></i> 粤港澳大湾区 · 雅思冲刺7.0 | 目标港校硕士</p>
            <div class="info-row">
                <div class="info-label"><i class="fas fa-graduation-cap"></i> 教育背景</div>
                <div class="info-content">安全工程 (主修) + 计算机科学与技术 (辅修) | 2023级，GPA 3.7+/4.0</div>
            </div>
            <div class="info-row">
                <div class="info-label"><i class="fas fa-code"></i> 核心技能</div>
                <div class="info-content">
                    <div class="tag-group">
                        <span class="skill-tag">Fluent (CFD)</span>
                        <span class="skill-tag">SolidWorks</span>
                        <span class="skill-tag">AutoCAD</span>
                        <span class="skill-tag">Python / 数据分析</span>
                        <span class="skill-tag">机器学习基础</span>
                    </div>
                </div>
            </div>
            <div class="info-row">
                <div class="info-label"><i class="fas fa-heart"></i> 兴趣&记忆</div>
                <div class="info-content">
                    热衷篮球对抗赛&组织校园音乐节，独自背包走过川西与云南；最珍贵的记忆是主办社区公益活动被 <strong>茂名日报&南方日报</strong> 报道，以及获得可再生能源国家级奖项。
                </div>
            </div>
            <div class="info-row">
                <div class="info-label"><i class="fas fa-language"></i> 语言目标</div>
                <div class="info-content">IELTS 7.0 (备考中) · 日常英文文献阅读/技术写作</div>
            </div>
            <!-- 截图提示（符合作业要求）-->
            <div style="margin-top: 1rem; font-size: 0.7rem; color: #6c86a3; border-top: 1px solid #eef2f6; padding-top: 0.6rem;">
                <i class="fas fa-camera"></i> 个人资料快照（已涵盖关键信息）— 作业博客截图区域
            </div>
        </div>
    </div>

    <!-- ********** 照片画廊 · 值得展示的记忆瞬间 ********** -->
    <div class="card">
        <div class="section-title"><i class="fas fa-images"></i> 光影·值得纪念的时刻</div>
        <div class="gallery">
            <div class="gallery-item">
                <img src="https://picsum.photos/id/26/400/250" alt="社区公益活动合影（模拟）">
                <div class="gallery-caption"><i class="fas fa-newspaper"></i> 茂名“康乐暖春”公益活动，登上茂名日报</div>
            </div>
            <div class="gallery-item">
                <img src="https://picsum.photos/id/169/400/250" alt="校园十大歌手现场">
                <div class="gallery-caption"><i class="fas fa-microphone-alt"></i> 策划23-24校园十大歌手 & 绿美广东活动</div>
            </div>
            <div class="gallery-item">
                <img src="https://picsum.photos/id/155/400/250" alt="可再生能源竞赛颁奖">
                <div class="gallery-caption"><i class="fas fa-trophy"></i> “中国中车杯”国家级三等奖颁奖现场</div>
            </div>
            <div class="gallery-item">
                <img src="https://picsum.photos/id/20/400/250" alt="安全宣传五进活动">
                <div class="gallery-caption"><i class="fas fa-shield-alt"></i> 2025安全宣传“五进”广州行·荔湾区</div>
            </div>
        </div>
        <p style="margin-top: 0.8rem; font-size: 0.85rem; color:#475569;"><i class="fas fa-camera-retro"></i> 从社区公益到全国竞赛，每一次协作与创新都塑造着更完整的我。</p>
    </div>

    <!-- ********** 科研经历 & 竞赛成果 + 专利 ********** -->
    <div class="card">
        <div class="section-title"><i class="fas fa-flask"></i> 科研经历 · 竞赛荣誉</div>
        <div class="grid-2col">
            <div>
                <h3 style="font-weight: 600; margin-bottom: 0.5rem;"><i class="fas fa-microscope"></i> 竞赛奖项</h3>
                <div class="list-item"><span class="list-icon">🏅</span> 24-25创新创业训练计划（校级立项）</div>
                <div class="list-item"><span class="list-icon">🥈</span> 24-25“挑战杯”校级二等奖</div>
                <div class="list-item"><span class="list-icon">🌱</span> 第四届环境生态公益设计大赛三等奖（校级）</div>
                <div class="list-item"><span class="list-icon">♻️</span> 大学生节能减排大赛三等奖（校级）[两项不同赛事]</div>
                <div class="list-item"><span class="list-icon">🚀</span> 三创赛（省级）</div>
                <div class="list-item"><span class="list-icon">⚙️</span> “中国中车杯”全国大学生可再生能源优秀科技作品竞赛 <strong>国家级三等奖</strong></div>
                <div class="list-item"><span class="list-icon">🌾</span> 2024粤港澳大学生“双百杯”乡村振兴创新创业竞赛 省级优秀奖</div>
                <div class="list-item"><span class="list-icon">🏆</span> 节能减排大赛三等奖（校级）</div>
            </div>
            <div>
                <h3 style="font-weight: 600; margin-bottom: 0.5rem;"><i class="fas fa-gavel"></i> 知识产权 & 荣誉</h3>
                <div class="patent-box">
                    <i class="fas fa-file-alt" style="color:#ca8a04;"></i> <strong>授权专利</strong><br>
                    一种用于高功率激光器的磁控复合相变换热系统及方法 (专利申请授权)
                </div>
                <div style="margin-top: 1rem;">
                    <div class="list-item"><span class="list-icon">⭐</span> 优秀共青团员</div>
                    <div class="list-item"><span class="list-icon">🤝</span> 学生会志愿服务工作先进个人</div>
                </div>
                <div style="margin-top: 1rem; background:#eef2ff; padding:0.8rem; border-radius:1rem;">
                    <i class="fas fa-chalkboard-user"></i> <strong>学术履历亮点</strong><br>
                    将安全工程与热流体仿真结合于激光器散热系统，完成专利撰写；辅修计算机后对智能算法+能源系统优化产生深度兴趣。
                </div>
            </div>
        </div>
    </div>

    <!-- ********** 社会实践 · 活动组织 ********** -->
    <div class="card">
        <div class="section-title"><i class="fas fa-hands-helping"></i> 社会实践 & 组织策划</div>
        <div class="grid-2col">
            <div>
                <h3><i class="fas fa-calendar-check"></i> 公益足迹</h3>
                <div class="list-item"><span class="list-icon">❤️</span> 赵广军生命热线社会活动（志愿服务）</div>
                <div class="list-item"><span class="list-icon">📰</span> <strong>主办</strong> 茂名市茂南区“康乐迎新春”&“康乐暖春”社区公益活动<br> 
                <span style="font-size: 0.8rem; color:#2d6a4f;">✅ 被茂名日报 & 南方日报专题报道</span></div>
                <div class="list-item"><span class="list-icon">🚸</span> 参与组织策划 2025年安全宣传“五进”广州行荔湾区</div>
            </div>
            <div>
                <h3><i class="fas fa-music"></i> 校园文化 & 大型活动</h3>
                <div class="list-item"><span class="list-icon">🎤</span> 组织策划 校内23-24年十大歌手活动、绿美广东，春入校园等大型校园活动</div>
                <div class="list-item"><span class="list-icon">🌳</span> “绿美广东”生态文明系列活动联合发起人之一</div>
                <div class="list-item"><span class="list-icon">📢</span> 多次负责院级文体赛事与志愿者招募，累计服务时长200h+</div>
            </div>
        </div>
    </div>

    <!-- ********** 专业技能 ｜ 自我评估 + 技术兴趣 ********** -->
    <div class="card">
        <div class="section-title"><i class="fas fa-brain"></i> 自我评估 · 技术栈与兴趣方向</div>
        <div style="display: flex; flex-wrap: wrap; gap: 1.5rem;">
            <div style="flex: 1;">
                <h3>📌 已具备的专业能力</h3>
                <ul style="margin-left: 1.2rem; margin-top: 0.5rem; list-style-type: none;">
                    <li style="margin-bottom: 0.5rem;">✓ <strong>工程仿真与设计</strong>：熟练使用Fluent进行热流场分析；SolidWorks / CAD 完成三维建模与工程制图。</li>
                    <li style="margin-bottom: 0.5rem;">✓ <strong>安全工程基础</strong>：火灾爆炸、风险评价、工业通风等核心知识，结合计算机做智能监测初步探索。</li>
                    <li style="margin-bottom: 0.5rem;">✓ <strong>编程与数据处理</strong>：Python (Pandas, Matplotlib)，SQL数据库基础，数据结构与算法 (辅修课程)。</li>
                    <li style="margin-bottom: 0.5rem;">✓ <strong>科研创新素养</strong>：专利撰写经验，竞赛答辩与团队领导力，荣获多项省级/国家级奖项。</li>
                </ul>
            </div>
            <div style="flex: 1;">
                <h3>🚀 兴趣领域 & 深度学习方向</h3>
                <div class="tag-group" style="margin-bottom: 0.8rem;">
                    <span class="interest-tag"><i class="fas fa-robot"></i> AI大数据分析</span>
                    <span class="interest-tag"><i class="fas fa-database"></i> 智慧城市 & 安全应急</span>
                    <span class="interest-tag"><i class="fas fa-chart-line"></i> 机器学习预测</span>
                    <span class="interest-tag"><i class="fas fa-cloud-sun"></i> 能源系统智能优化</span>
                </div>
                <p><strong>🎯 最想学习的知识：</strong> 大规模数据处理 (Spark/Hadoop)、深度学习框架(PyTorch)、AIoT边缘智能；希望将AI技术与安全工程/热管理结合，构建智慧安全预警系统。</p>
                <hr>
                <p><strong>⭐ 自我评价：</strong> 跨学科背景 (安全+计算机) 使我具备系统化工程思维与编程能力，敢于挑战“AI for Science”的新范式。目前在准备雅思同时自学《机器学习实战》及斯坦福CS229课程，强化数据科学项目经历。</p>
            </div>
        </div>
    </div>

    <!-- ********** 未来三年规划 | 香港硕士目标 ********** -->
    <div class="card">
        <div class="section-title"><i class="fas fa-chart-simple"></i> 未来三年发展蓝图 · 逐梦港校</div>
        <div class="timeline">
            <div class="timeline-node">
                <div class="timeline-year">2026.03 - 2026.12</div>
                <div class="timeline-text">
                    <strong>🎯 语言 & 科研冲刺期</strong><br>
                    · 雅思目标7.0 (小分不低于6.0) — 密集备考，6/9月刷分。<br>
                    · 保持高GPA (主修+辅修)，完善可再生能源竞赛成果转化，争取一篇学术论文或专利深化。<br>
                    · 参与计算机视觉/数据分析开源项目，丰富GitHub，夯实AI基础。<br>
                    · 确定港校目标项目: 香港大学/港科大/港中文 智能建筑、数据科学、机械工程交叉方向。
                </div>
            </div>
            <div class="timeline-node">
                <div class="timeline-year">2027.01 - 2027.08</div>
                <div class="timeline-text">
                    <strong>📬 申请 & 毕业设计阶段</strong><br>
                    · 完成文书撰写、联系导师投递申请 (研究型硕士/授课型硕士双线准备)。<br>
                    · 毕业设计结合“AI+相变换热系统预测”或安全智能监测，展示交叉学科能力。<br>
                    · 争取相关实习/助研经历 (能源类企业或大数据岗位)，强化软实力。<br>
                    · 获得港校录取通知书，准备签证及入学事宜。
                </div>
            </div>
            <div class="timeline-node">
                <div class="timeline-year">2027.09 - 2029.06</div>
                <div class="timeline-text">
                    <strong>🎓 香港硕士深造 & 职业起航</strong><br>
                    · 攻读授课型/研究型硕士，专注智慧城市安全、AI驱动的节能系统等前沿课题。<br>
                    · 利用香港国际平台参与学术会议，争取顶会/期刊论文产出，建立行业人脉。<br>
                    · 同步探索留港工作/读博可能，期望成为“AI+安全工程”复合型研发专家，回馈大湾区科技发展。
                </div>
            </div>
        </div>
        <p style="margin-top: 1rem; background:#eef2ff; border-radius: 1rem; padding: 0.8rem;"><i class="fas fa-quote-left"></i> 选择香港硕士的原因：优质教育资源+国际视野+大湾区机遇，辅修计算机背景与安全工程结合能更好适应未来智能技术浪潮。通过研究生阶段系统提升算法能力，致力于可持续能源与公共安全交叉创新。</p>
    </div>
    
    <!-- 个人寄语 + 额外的资料快照备份 (方便截图)-->
    <div class="card" style="background: linear-gradient(110deg, #f0f9ff, #ffffff);">
        <div style="display: flex; justify-content: space-between; flex-wrap: wrap; align-items: center;">
            <div>
                <i class="fas fa-envelope-open-text" style="font-size: 2rem; color:#3b82f6;"></i>
                <h3 style="margin-top: 0.2rem;">保持联系 & 更多资料</h3>
                <p>📧 zhiyuan.chen@example.edu · GitHub: @zhiyuan_safe_ai · 作品集持续更新中</p>
                <p>📸 个人资料截图已包含基本信息、获奖科研规划等，满足作业博客存档需求。</p>
            </div>
            <div>
                <span class="badge"><i class="fas-regular fa-file-lines"></i> 更新于2026.03</span>
            </div>
        </div>
    </div>

    <footer>
        <i class="fas fa-camera"></i> 本页面可截取个人资料卡、成就与实践模块作为作业博客附图 · 陈志远 安全工程+计算机 热爱篮球/音乐/旅行<br>
        梦想成为跨学科技术开拓者 — 香港硕士，即刻启程。
    </footer>
</div>
</body>
</html>
