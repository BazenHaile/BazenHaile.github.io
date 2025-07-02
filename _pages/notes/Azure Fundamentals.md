<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cloud Computing Ecosystem - Interactive Guide</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            color: #333;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
            overflow: hidden;
            min-height: 100vh;
        }
        
        .header {
            background: linear-gradient(45deg, #4285f4, #ea4335, #fbbc05, #34a853);
            color: white;
            padding: 30px;
            text-align: center;
            position: relative;
        }
        
        .header h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }
        
        .page-indicator {
            position: absolute;
            top: 20px;
            right: 20px;
            background: rgba(255,255,255,0.2);
            padding: 10px 20px;
            border-radius: 25px;
            font-weight: bold;
        }
        
        .navigation {
            background: #f8f9fa;
            padding: 20px;
            border-bottom: 3px solid #4285f4;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        .nav-btn {
            background: white;
            border: 2px solid #4285f4;
            color: #4285f4;
            padding: 12px 20px;
            border-radius: 25px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.3s ease;
            margin: 5px;
        }
        
        .nav-btn:hover, .nav-btn.active {
            background: #4285f4;
            color: white;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(66, 133, 244, 0.3);
        }
        
        .page {
            display: none;
            padding: 40px;
            min-height: 600px;
            animation: fadeIn 0.5s ease-in-out;
        }
        
        .page.active {
            display: block;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .page h2 {
            color: #1a73e8;
            font-size: 2.2em;
            margin-bottom: 30px;
            text-align: center;
            border-bottom: 3px solid #4285f4;
            padding-bottom: 15px;
        }
        
        .page h3 {
            color: #333;
            font-size: 1.5em;
            margin: 25px 0 15px 0;
        }
        
        .connection-box {
            background: linear-gradient(135deg, #e3f2fd, #f1f8e9);
            border-left: 5px solid #4caf50;
            padding: 25px;
            margin: 25px 0;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        .connection-box h4 {
            color: #2e7d32;
            margin-bottom: 15px;
            font-size: 1.3em;
        }
        
        .benefits-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
            margin: 30px 0;
        }
        
        .benefit-card {
            background: white;
            padding: 25px;
            border-radius: 15px;
            box-shadow: 0 6px 12px rgba(0,0,0,0.1);
            border-top: 4px solid #34a853;
            transition: transform 0.3s ease;
        }
        
        .benefit-card:hover {
            transform: translateY(-5px);
        }
        
        .benefit-card h4 {
            color: #1a73e8;
            margin-bottom: 15px;
            font-size: 1.3em;
        }
        
        .platform-examples {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-top: 15px;
        }
        
        .platform-tag {
            background: #e8f0fe;
            color: #1a73e8;
            padding: 6px 12px;
            border-radius: 20px;
            font-size: 0.85em;
            font-weight: 500;
        }
        
        .cost-comparison {
            display: grid;
            grid-template-columns: 1fr auto 1fr;
            gap: 30px;
            align-items: center;
            margin: 30px 0;
            background: white;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 6px 12px rgba(0,0,0,0.1);
        }
        
        .cost-model {
            text-align: center;
            padding: 20px;
            background: #f8f9fa;
            border-radius: 15px;
        }
        
        .cost-model h4 {
            color: #1a73e8;
            margin-bottom: 15px;
            font-size: 1.4em;
        }
        
        .cost-bar {
            height: 60px;
            border-radius: 10px;
            margin: 15px 0;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            font-size: 1.1em;
        }
        
        .capex-bar {
            background: linear-gradient(45deg, #ea4335, #d32f2f);
        }
        
        .opex-bar {
            background: linear-gradient(45deg, #34a853, #2e7d32);
        }
        
        .arrow {
            font-size: 2em;
            color: #4285f4;
            font-weight: bold;
        }
        
        .service-pyramid {
            display: flex;
            flex-direction: column;
            align-items: center;
            margin: 30px 0;
            gap: 15px;
        }
        
        .pyramid-level {
            background: linear-gradient(45deg, #4285f4, #34a853);
            color: white;
            padding: 25px;
            border-radius: 15px;
            text-align: center;
            font-weight: bold;
            transition: all 0.3s ease;
            cursor: pointer;
        }
        
        .pyramid-level:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 16px rgba(0,0,0,0.2);
        }
        
        .pyramid-level:nth-child(1) { 
            width: 90%; 
            background: linear-gradient(45deg, #ea4335, #fbbc05); 
        }
        .pyramid-level:nth-child(2) { 
            width: 70%; 
            background: linear-gradient(45deg, #4285f4, #34a853); 
        }
        .pyramid-level:nth-child(3) { 
            width: 50%; 
            background: linear-gradient(45deg, #9c27b0, #673ab7); 
        }
        
        .cloud-types {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin: 30px 0;
        }
        
        .cloud-type {
            background: white;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 6px 12px rgba(0,0,0,0.1);
            text-align: center;
            transition: transform 0.3s ease;
        }
        
        .cloud-type:hover {
            transform: translateY(-8px);
        }
        
        .cloud-type.public { border-top: 5px solid #4285f4; }
        .cloud-type.private { border-top: 5px solid #ea4335; }
        .cloud-type.hybrid { border-top: 5px solid #fbbc05; }
        
        .cloud-icon {
            font-size: 3em;
            margin-bottom: 15px;
        }
        
        .responsibility-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            margin: 30px 0;
        }
        
        .responsibility-side {
            background: white;
            padding: 25px;
            border-radius: 15px;
            box-shadow: 0 6px 12px rgba(0,0,0,0.1);
        }
        
        .responsibility-side.customer {
            border-left: 5px solid #ea4335;
        }
        
        .responsibility-side.provider {
            border-left: 5px solid #34a853;
        }
        
        .responsibility-item {
            background: #f8f9fa;
            padding: 12px;
            margin: 10px 0;
            border-radius: 8px;
            border-left: 3px solid #ddd;
        }
        
        .big-picture-summary {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            padding: 30px;
            border-radius: 20px;
            margin: 30px 0;
            text-align: center;
        }
        
        .big-picture-summary h3 {
            font-size: 1.8em;
            margin-bottom: 20px;
        }
        
        .flow-diagram {
            display: flex;
            align-items: center;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            margin: 30px 0;
        }
        
        .flow-step {
            background: white;
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            text-align: center;
            min-width: 200px;
            border-top: 4px solid #4285f4;
        }
        
        .flow-arrow {
            font-size: 2em;
            color: #4285f4;
        }
        
        .next-prev {
            display: flex;
            justify-content: space-between;
            padding: 20px 40px;
            background: #f8f9fa;
            border-top: 1px solid #e0e0e0;
        }
        
        .next-prev button {
            background: #4285f4;
            color: white;
            border: none;
            padding: 12px 24px;
            border-radius: 25px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.3s ease;
        }
        
        .next-prev button:hover:not(:disabled) {
            background: #1a73e8;
            transform: translateY(-2px);
        }
        
        .next-prev button:disabled {
            background: #ccc;
            cursor: not-allowed;
        }
        
        @media (max-width: 768px) {
            .container {
                margin: 10px;
                border-radius: 15px;
            }
            
            .header h1 {
                font-size: 2em;
            }
            
            .page {
                padding: 20px;
            }
            
            .navigation {
                padding: 15px;
            }
            
            .nav-btn {
                padding: 10px 15px;
                font-size: 0.9em;
            }
            
            .cost-comparison {
                grid-template-columns: 1fr;
                gap: 20px;
            }
            
            .arrow {
                transform: rotate(90deg);
            }
            
            .responsibility-grid {
                grid-template-columns: 1fr;
            }
            
            .flow-diagram {
                flex-direction: column;
            }
            
            .flow-arrow {
                transform: rotate(90deg);
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <div class="page-indicator">
                <span id="current-page">1</span> / <span id="total-pages">6</span>
            </div>
            <h1>🌳 Cloud Computing Ecosystem</h1>
            <p>Interactive Guide: How All the Pieces Connect</p>
        </div>
        
        <div class="navigation">
            <button class="nav-btn active" onclick="showPage(0)">📖 Overview</button>
            <button class="nav-btn" onclick="showPage(1)">🚀 Benefits</button>
            <button class="nav-btn" onclick="showPage(2)">💰 Cost Models</button>
            <button class="nav-btn" onclick="showPage(3)">🏗️ Service Types</button>
            <button class="nav-btn" onclick="showPage(4)">🌐 Deployment</button>
            <button class="nav-btn" onclick="showPage(5)">🤝 Responsibility</button>
            <button class="nav-btn" onclick="showPage(6)">🎯 Big Picture</button>
        </div>
        
        <!-- Page 0: Overview -->
        <div class="page active">
            <h2>📖 The Cloud Computing Tree</h2>
            
            <div class="connection-box">
                <h4>🌳 How This Guide Works</h4>
                <p>Like a tree, cloud computing has interconnected parts that support each other. Each page explores one "branch" of knowledge, and the final page shows how they all connect in your real administrative work.</p>
            </div>
            
            <h3>What You'll Learn:</h3>
            
            <div class="flow-diagram">
                <div class="flow-step">
                    <h4>🚀 Benefits</h4>
                    <p><em>Why</em> move to cloud</p>
                </div>
                <div class="flow-arrow">→</div>
                <div class="flow-step">
                    <h4>💰 Cost Models</h4>
                    <p><em>How</em> you pay</p>
                </div>
                <div class="flow-arrow">→</div>
                <div class="flow-step">
                    <h4>🏗️ Service Types</h4>
                    <p><em>What</em> you get</p>
                </div>
            </div>
            
            <div class="flow-diagram">
                <div class="flow-step">
                    <h4>🌐 Deployment</h4>
                    <p><em>Where</em> it runs</p>
                </div>
                <div class="flow-arrow">→</div>
                <div class="flow-step">
                    <h4>🤝 Responsibility</h4>
                    <p><em>Who</em> does what</p>
                </div>
                <div class="flow-arrow">→</div>
                <div class="flow-step">
                    <h4>🎯 Big Picture</h4>
                    <p><em>How</em> it connects</p>
                </div>
            </div>
            
            <div class="connection-box">
                <h4>🎯 Your Admin Journey</h4>
                <p><strong>From:</strong> Managing Exchange servers, file servers, and GIS hardware</p>
                <p><strong>To:</strong> Orchestrating Gmail, Microsoft 365, and ArcGIS Online services</p>
                <p><strong>Result:</strong> Focus on user enablement instead of infrastructure maintenance</p>
            </div>
        </div>
        
        <!-- Page 1: Benefits -->
        <div class="page">
            <h2>🚀 Cloud Computing Benefits</h2>
            
            <div class="connection-box">
                <h4>🔗 Connection to Your Work</h4>
                <p>These benefits are <em>why</em> your organization moved from on-premises servers to Google Workspace, Microsoft 365, and ArcGIS Online. Each benefit solves a real business problem you've experienced.</p>
            </div>
            
            <div class="benefits-grid">
                <div class="benefit-card">
                    <h4>🔄 High Availability</h4>
                    <p>Services stay running with 99.9%+ uptime, even when things break.</p>
                    <p><strong>Your experience:</strong> Gmail rarely goes down because Google has multiple data centers. If one fails, others take over automatically.</p>
                    <div class="platform-examples">
                        <span class="platform-tag">Gmail SLA</span>
                        <span class="platform-tag">Exchange Online</span>
                        <span class="platform-tag">ArcGIS Online</span>
                    </div>
                </div>
                
                <div class="benefit-card">
                    <h4>📈 Scalability</h4>
                    <p>Manually add or remove resources based on your needs.</p>
                    <p><strong>Your experience:</strong> Adding 50 new Microsoft 365 licenses takes minutes in the admin console, not weeks of server procurement.</p>
                    <div class="platform-examples">
                        <span class="platform-tag">User Licenses</span>
                        <span class="platform-tag">Storage Quotas</span>
                        <span class="platform-tag">Teams Capacity</span>
                    </div>
                </div>
                
                <div class="benefit-card">
                    <h4>⚡ Elasticity</h4>
                    <p>Resources automatically adjust to demand in real-time.</p>
                    <p><strong>Your experience:</strong> ArcGIS Online credits scale automatically when your Story Map goes viral - you use more when needed, less when quiet.</p>
                    <div class="platform-examples">
                        <span class="platform-tag">ArcGIS Credits</span>
                        <span class="platform-tag">SharePoint Storage</span>
                        <span class="platform-tag">Drive Space</span>
                    </div>
                </div>
                
                <div class="benefit-card">
                    <h4>🚀 Agility</h4>
                    <p>Rapidly deploy and test new solutions without infrastructure delays.</p>
                    <p><strong>Your experience:</strong> Testing Power Apps or Google Apps Script takes minutes, not months of server setup and approvals.</p>
                    <div class="platform-examples">
                        <span class="platform-tag">Power Apps</span>
                        <span class="platform-tag">Apps Script</span>
                        <span class="platform-tag">Quick Deployment</span>
                    </div>
                </div>
                
                <div class="benefit-card">
                    <h4>🔒 Disaster Recovery</h4>
                    <p>Automatic backups and geographic redundancy protect your data.</p>
                    <p><strong>Your experience:</strong> When laptops crash, OneDrive and Google Drive files are still safe. No more tape backups or recovery procedures.</p>
                    <div class="platform-examples">
                        <span class="platform-tag">OneDrive Sync</span>
                        <span class="platform-tag">Drive Backup</span>
                        <span class="platform-tag">Email Archive</span>
                    </div>
                </div>
                
                <div class="benefit-card">
                    <h4>🔧 Reduced Management</h4>
                    <p>No more server patching, hardware maintenance, or software updates.</p>
                    <p><strong>Your experience:</strong> Google and Microsoft handle all the backend maintenance. You focus on user support and governance.</p>
                    <div class="platform-examples">
                        <span class="platform-tag">Auto Updates</span>
                        <span class="platform-tag">No Patching</span>
                        <span class="platform-tag">24/7 Monitoring</span>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Page 2: Cost Models -->
        <div class="page">
            <h2>💰 Cost Models: CapEx vs OpEx</h2>
            
            <div class="connection-box">
                <h4>🔗 Connection to Benefits</h4>
                <p>The cloud benefits you just learned about are made possible by shifting from <em>Capital Expenditure</em> (buying) to <em>Operational Expenditure</em> (renting). This change in how you pay enables all those benefits.</p>
            </div>
            
            <div class="cost-comparison">
                <div class="cost-model">
                    <h4>📊 CapEx (Traditional)</h4>
                    <div class="cost-bar capex-bar">$50,000 Upfront</div>
                    <p><strong>What you used to buy:</strong></p>
                    <ul style="text-align: left; margin-top: 15px;">
                        <li>Exchange Server licenses ($5,000+)</li>
                        <li>Windows Server licenses ($1,500+)</li>
                        <li>ArcGIS Server software ($15,000+)</li>
                        <li>Physical hardware ($20,000+)</li>
                        <li>Storage systems ($8,000+)</li>
                    </ul>
                    <p style="margin-top: 15px; color: #ea4335;"><strong>Problems:</strong> Depreciation, obsolescence, maintenance costs</p>
                </div>
                
                <div class="arrow">→</div>
                
                <div class="cost-model">
                    <h4>📅 OpEx (Cloud)</h4>
                    <div class="cost-bar opex-bar">$36/month per user</div>
                    <p><strong>What you now subscribe to:</strong></p>
                    <ul style="text-align: left; margin-top: 15px;">
                        <li>Microsoft 365 E3: $36/user/month</li>
                        <li>Google Workspace: $12-18/user/month</li>
                        <li>ArcGIS Online: Credit-based consumption</li>
                        <li>No hardware costs</li>
                        <li>Included support & updates</li>
                    </ul>
                    <p style="margin-top: 15px; color: #34a853;"><strong>Benefits:</strong> Predictable, scalable, always current</p>
                </div>
            </div>
            
            <h3>💳 Consumption-Based Pricing</h3>
            <div class="benefit-card">
                <h4>ArcGIS Online Credits Example</h4>
                <p>Instead of paying flat fees, you pay for what you actually use:</p>
                <ul style="margin-top: 10px;">
                    <li><strong>Storing maps:</strong> 1.2 credits per 10MB per month</li>
                    <li><strong>Geocoding addresses:</strong> 0.5 credits per 1,000 addresses</li>
                    <li><strong>Routing analysis:</strong> 0.005 credits per route calculated</li>
                    <li><strong>Static maps:</strong> 0 credits (free to view)</li>
                </ul>
                <p style="margin-top: 15px;">This means you only pay when you're actively using advanced features, not for basic map viewing.</p>
            </div>
            
            <div class="connection-box">
                <h4>🎯 Why This Matters for Your Next Decision</h4>
                <p>Understanding OpEx vs CapEx helps you choose the right <em>service type</em> (our next topic). When you think in monthly costs instead of upfront purchases, SaaS solutions like Gmail become more attractive than building your own email server.</p>
            </div>
        </div>
        
        <!-- Page 3: Service Types -->
        <div class="page">
            <h2>🏗️ Cloud Service Types</h2>
            
            <div class="connection-box">
                <h4>🔗 Connection to Cost Models</h4>
                <p>Now that you understand OpEx thinking, you can choose the right service level. The more convenience you want (SaaS), the higher the monthly cost but lower management burden. The more control you need (IaaS), the lower the service cost but higher management responsibility.</p>
            </div>
            
            <div class="service-pyramid">
                <div class="pyramid-level">
                    <h3>📧 SaaS - Software as a Service</h3>
                    <p><strong>Your daily tools:</strong> Gmail, Teams, ArcGIS Online, SharePoint</p>
                    <p><strong>You manage:</strong> User accounts, data, permissions</p>
                    <p><strong>Provider manages:</strong> Everything else</p>
                    <div style="margin-top: 10px; font-size: 0.9em;">
                        <span style="background: rgba(255,255,255,0.2); padding: 5px 10px; border-radius: 15px; margin: 0 5px;">Ready to use</span>
                        <span style="background: rgba(255,255,255,0.2); padding: 5px 10px; border-radius: 15px; margin: 0 5px;">Highest cost</span>
                        <span style="background: rgba(255,255,255,0.2); padding: 5px 10px; border-radius: 15px; margin: 0 5px;">Least control</span>
                    </div>
                </div>
                
                <div class="pyramid-level">
                    <h3>🔧 PaaS - Platform as a Service</h3>
                    <p><strong>Your development tools:</strong> Power Apps, Google Apps Script, Azure Functions</p>
                    <p><strong>You manage:</strong> Application logic, data connections, user access</p>
                    <p><strong>Provider manages:</strong> Runtime, OS, servers, networking</p>
                    <div style="margin-top: 10px; font-size: 0.9em;">
                        <span style="background: rgba(255,255,255,0.2); padding: 5px 10px; border-radius: 15px; margin: 0 5px;">Build apps</span>
                        <span style="background: rgba(255,255,255,0.2); padding: 5px 10px; border-radius: 15px; margin: 0 5px;">Medium cost</span>
                        <span style="background: rgba(255,255,255,0.2); padding: 5px 10px; border-radius: 15px; margin: 0 5px;">Some control</span>
                    </div>
                </div>
                
                <div class="pyramid-level">
                    <h3>🖥️ IaaS - Infrastructure as a Service</h3>
                    <p><strong>When you need custom servers:</strong> Google Cloud VMs for ArcGIS Server</p>
                    <p><strong>You manage:</strong> OS, applications, data, networking, security</p>
                    <p><strong>Provider manages:</strong> Physical hardware, hypervisor, facility</p>
                    <div style="margin-top: 10px; font-size: 0.9em;">
                        <span style="background: rgba(255,255,255,0.2); padding: 5px 10px; border-radius: 15px; margin: 0 5px;">Full control</span>
                        <span style="background: rgba(255,255,255,0.2); padding: 5px 10px; border-radius: 15px; margin: 0 5px;">Lowest cost</span>
                        <span style="background: rgba(255,255,255,0.2); padding: 5px 10px; border-radius: 15px; margin: 0 5px;">Most work</span>
                    </div>
                </div>
            </div>
            
            <h3>🎯 Real Decision Examples from Your Experience</h3>
            
            <div class="benefits-grid">
                <div class="benefit-card">
                    <h4>📧 Need: Email System</h4>
                    <p><strong>Choice:</strong> SaaS (Gmail/Outlook 365)</p>
                    <p><strong>Why:</strong> Email is not your core business. You want it to "just work" without server management.</p>
                    <p><strong>Alternative:</strong> IaaS (Exchange on VMs) = More work, same result</p>
                </div>
                
                <div class="benefit-card">
                    <h4>🗺️ Need: Web Mapping</h4>
                    <p><strong>Choice:</strong> SaaS (ArcGIS Online)</p>
                    <p><strong>Why:</strong> Quick map deployment, automatic scaling, no server maintenance.</p>
                    <p><strong>Alternative:</strong> IaaS (ArcGIS Server) = Only if you need extreme customization</p>
                </div>
                
                <div class="benefit-card">
                    <h4>📱 Need: Custom Business App</h4>
                    <p><strong>Choice:</strong> PaaS (Power Apps)</p>
                    <p><strong>Why:</strong> You focus on business logic, Microsoft handles the platform.</p>
                    <p><strong>Alternative:</strong> IaaS (Custom VMs) = Unnecessary complexity</p>
                </div>
            </div>
            
            <div class="connection-box">
                <h4>🎯 Leading to Deployment Decisions</h4>
                <p>Your service type choice influences <em>where</em> it runs. SaaS typically runs in public cloud, but enterprise needs might require private or hybrid deployment models (our next topic).</p>
            </div>
        </div>
        
        <!-- Page 4: Deployment Models -->
        <div class="page">
            <h2>🌐 Cloud Deployment Models</h2>
            
            <div class="connection-box">
                <h4>🔗 Connection to Service Types</h4>
                <p>You've chosen your service type (SaaS, PaaS, or IaaS). Now you need to decide <em>where</em> it runs. Most of your daily tools (Gmail, Microsoft 365) run in public cloud, but some organizations need private or hybrid approaches for security or compliance reasons.</p>
            </div>
            
            <div class="cloud-types">
                <div class="cloud-type public">
                    <div class="cloud-icon">🌍</div>
                    <h3>Public Cloud</h3>
                    <p><strong>What you use daily:</strong></p>
                    <ul style="text-align: left; margin: 15px 0;">
                        <li>Google Workspace (Gmail, Drive, Meet)</li>
                        <li>Microsoft 365 (Outlook, Teams, SharePoint)</li>
                        <li>ArcGIS Online (Story Maps, web maps)</li>
                    </ul>
                    <p><strong>Characteristics:</strong></p>
                    <ul style="text-align: left; margin: 15px 0;">
                        <li>✅ Shared infrastructure (cost-effective)</li>
                        <li>✅ Always updated with latest features</li>
                        <li>✅ Global availability and redundancy</li>
                        <li>⚠️ Less customization options</li>
                        <li>⚠️ Data location may vary</li>
                    </ul>
                </div>
                
                <div class="cloud-type private">
                    <div class="cloud-icon">🏢</div>
                    <h3>Private Cloud</h3>
                    <p><strong>Less common, but you might see:</strong></p>
                    <ul style="text-align: left; margin: 15px 0;">
                        <li>ArcGIS Enterprise on dedicated servers</li>
                        <li>Private Exchange deployment</li>
                        <li>Custom SharePoint farms</li>
                    </ul>
                    <p><strong>Characteristics:</strong></p>
                    <ul style="text-align: left; margin: 15px 0;">
                        <li>✅ Full control over data and customization</li>
                        <li>✅ Meets strict compliance requirements</li>
                        <li>✅ Predictable performance</li>
                        <li>❌ Higher cost and complexity</li>
                        <li>❌ You manage updates and maintenance</li>
                    </ul>
                </div>
                
                <div class="cloud-type hybrid">
                    <div class="cloud-icon">🔄</div>
                    <h3>Hybrid Cloud</h3>
                    <p><strong>Common enterprise scenarios:</strong></p>
                    <ul style="text-align: left; margin: 15px 0;">
                        <li>Exchange on-premises + Exchange Online</li>
                        <li>Azure AD Connect (on-prem + cloud identity)</li>
                        <li>ArcGIS Enterprise + ArcGIS Online integration</li>
                    </ul>
                    <p><strong>Characteristics:</strong></p>
                    <ul style="text-align: left; margin: 15px 0;">
                        <li>✅ Best of both worlds</li>
                        <li>✅ Gradual migration path</li>
                        <li>✅ Keep sensitive data on-premises</li>
                        <li>⚠️ Complex integration and management</li>
                        <li>⚠️ Requires expertise in both environments</li>
                    </ul>
                </div>
            </div>
            
            <h3>🎯 Real Deployment Decision Examples</h3>
            
            <div class="benefits-grid">
                <div class="benefit-card">
                    <h4>📧 Email Migration Scenario</h4>
                    <p><strong>Starting point:</strong> Exchange Server on-premises</p>
                    <p><strong>Hybrid phase:</strong> Exchange Hybrid (some mailboxes on-prem, some in cloud)</p>
                    <p><strong>End state:</strong> Exchange Online (public cloud)</p>
                    <p><strong>Your role:</strong> Managing coexistence, user migration batches, mail flow rules</p>
                </div>
                
                <div class="benefit-card">
                    <h4>🗺️ GIS Data Sensitivity</h4>
                    <p><strong>Public maps:</strong> ArcGIS Online (public cloud)</p>
                    <p><strong>Sensitive data:</strong> ArcGIS Enterprise on-premises (private)</p>
                    <p><strong>Integration:</strong> Portal-to-portal sharing (hybrid)</p>
                    <p><strong>Your role:</strong> Managing data classification and sharing policies</p>
                </div>
                
                <div class="benefit-card">
                    <h4>👥 Identity Management</h4>
                    <p><strong>User accounts:</strong> Active Directory on-premises</p>
                    <p><strong>Cloud services:</strong> Azure AD (public cloud)</p>
                    <p><strong>Integration:</strong> Azure AD Connect sync (hybrid)</p>
                    <p><strong>Your role:</strong> Single sign-on configuration, password sync</p>
                </div>
            </div>
            
            <div class="connection-box">
                <h4>🎯 This Affects Responsibility</h4>
                <p>Your deployment choice directly impacts <em>who manages what</em>. Public cloud means the provider handles most infrastructure tasks. Private cloud means you handle everything. Hybrid means you manage the integration complexity between both worlds.</p>
            </div>
        </div>
        
        <!-- Page 5: Shared Responsibility -->
        <div class="page">
            <h2>🤝 Shared Responsibility Model</h2>
            
            <div class="connection-box">
                <h4>🔗 Connection to Everything</h4>
                <p>This is where all your previous decisions come together. The <em>benefits</em> you want, the <em>cost model</em> you choose, the <em>service type</em> you pick, and the <em>deployment model</em> you select all determine exactly what you're responsible for vs. what the cloud provider handles.</p>
            </div>
            
            <div class="responsibility-grid">
                <div class="responsibility-side customer">
                    <h3>👤 Your Responsibilities (Always)</h3>
                    <div class="responsibility-item">
                        <strong>User Account Management</strong><br>
                        Creating users, assigning licenses, managing groups in Google Admin or Microsoft 365 Admin Center
                    </div>
                    <div class="responsibility-item">
                        <strong>Data Classification & Permissions</strong><br>
                        Setting up sharing policies, sensitivity labels, who can access what data
                    </div>
                    <div class="responsibility-item">
                        <strong>Content Governance</strong><br>
                        Retention policies, legal holds, content lifecycle management
                    </div>
                    <div class="responsibility-item">
                        <strong>Security Policies</strong><br>
                        Conditional access, multi-factor authentication, mobile device management
                    </div>
                    <div class="responsibility-item">
                        <strong>License Management</strong><br>
                        Right-sizing subscriptions, monitoring usage, cost optimization
                    </div>
                    <div class="responsibility-item">
                        <strong>Integration & Workflows</strong><br>
                        Connecting systems, Power Automate flows, custom applications
                    </div>
                </div>
                
                <div class="responsibility-side provider">
                    <h3>☁️ Provider Responsibilities (Always)</h3>
                    <div class="responsibility-item">
                        <strong>Physical Infrastructure</strong><br>
                        Data centers, power, cooling, physical security, network hardware
                    </div>
                    <div class="responsibility-item">
                        <strong>Platform Maintenance</strong><br>
                        Server patching, OS updates, security fixes, capacity planning
                    </div>
                    <div class="responsibility-item">
                        <strong>Service Availability</strong><br>
                        99.9% uptime guarantees, redundancy, failover, disaster recovery
                    </div>
                    <div class="responsibility-item">
                        <strong>Data Protection</strong><br>
                        Encryption at rest and in transit, backup infrastructure, geo-replication
                    </div>
                    <div class="responsibility-item">
                        <strong>Compliance Certifications</strong><br>
                        SOC 2, GDPR, HIPAA, FedRAMP compliance and auditing
                    </div>
                    <div class="responsibility-item">
                        <strong>Feature Development</strong><br>
                        New capabilities, performance improvements, bug fixes
                    </div>
                </div>
            </div>
            
            <h3>⚖️ How Service Type Changes Your Responsibilities</h3>
            
            <div class="benefits-grid">
                <div class="benefit-card">
                    <h4>📧 SaaS Example: Gmail</h4>
                    <p><strong>You manage:</strong></p>
                    <ul style="text-align: left;">
                        <li>User provisioning and deprovisioning</li>
                        <li>Email retention policies</li>
                        <li>Sharing and DLP settings</li>
                        <li>Mobile device policies</li>
                    </ul>
                    <p><strong>Google manages:</strong> Everything else</p>
                </div>
                
                <div class="benefit-card">
                    <h4>🔧 PaaS Example: Power Apps</h4>
                    <p><strong>You manage:</strong></p>
                    <ul style="text-align: left;">
                        <li>Application logic and design</li>
                        <li>Data connectors and sources</li>
                        <li>User permissions within the app</li>
                        <li>App lifecycle and updates</li>
                    </ul>
                    <p><strong>Microsoft manages:</strong> Platform, runtime, scaling</p>
                </div>
                
                <div class="benefit-card">
                    <h4>🖥️ IaaS Example: Custom GIS Server</h4>
                    <p><strong>You manage:</strong></p>
                    <ul style="text-align: left;">
                        <li>Operating system patching</li>
                        <li>ArcGIS Server installation/updates</li>
                        <li>Security configuration</li>
                        <li>Performance monitoring</li>
                        <li>Backup procedures</li>
                    </ul>
                    <p><strong>Provider manages:</strong> Just the virtual machine hardware</p>
                </div>
            </div>
            
            <div class="connection-box">
                <h4>🎯 Your Role Evolution</h4>
                <p><strong>Before Cloud:</strong> Server administrator, patch manager, backup operator, hardware troubleshooter</p>
                <p><strong>With Cloud:</strong> Service orchestrator, user enabler, security governance, business enablement</p>
                <p>The shared responsibility model lets you focus on what matters to your business instead of keeping servers running.</p>
            </div>
        </div>
        
        <!-- Page 6: Big Picture -->
        <div class="page">
            <h2>🎯 The Big Picture: How Everything Connects</h2>
            
            <div class="big-picture-summary">
                <h3>🌳 The Complete Cloud Ecosystem</h3>
                <p>Like a tree, each part supports the others. Here's how all the concepts work together in your real administrative work:</p>
            </div>
            
            <h3>🔄 The Decision Flow</h3>
            
            <div class="flow-diagram">
                <div class="flow-step">
                    <h4>1. Business Need</h4>
                    <p>"We need better email reliability"</p>
                </div>
                <div class="flow-arrow">→</div>
                <div class="flow-step">
                    <h4>2. Benefit Analysis</h4>
                    <p>High availability + reduced management</p>
                </div>
                <div class="flow-arrow">→</div>
                <div class="flow-step">
                    <h4>3. Cost Model</h4>
                    <p>OpEx vs CapEx evaluation</p>
                </div>
            </div>
            
            <div class="flow-diagram">
                <div class="flow-step">
                    <h4>4. Service Choice</h4>
                    <p>SaaS (Exchange Online) vs IaaS (Exchange on VMs)</p>
                </div>
                <div class="flow-arrow">→</div>
                <div class="flow-step">
                    <h4>5. Deployment Model</h4>
                    <p>Public cloud vs hybrid migration</p>
                </div>
                <div class="flow-arrow">→</div>
                <div class="flow-step">
                    <h4>6. Responsibility Split</h4>
                    <p>What you manage vs what Microsoft manages</p>
                </div>
            </div>
            
            <h3>🎯 Three Real Examples from Your Experience</h3>
            
            <div class="benefits-grid">
                <div class="benefit-card">
                    <h4>📧 Email System Transformation</h4>
                    <p><strong>Need:</strong> Reliable email, reduce downtime</p>
                    <p><strong>Benefits:</strong> High availability, disaster recovery</p>
                    <p><strong>Cost:</strong> $6/user/month vs $50K server</p>
                    <p><strong>Service:</strong> SaaS (Exchange Online)</p>
                    <p><strong>Deployment:</strong> Public cloud (maybe hybrid during migration)</p>
                    <p><strong>Your role:</strong> User management, not server management</p>
                </div>
                
                <div class="benefit-card">
                    <h4>🗺️ Web Mapping Platform</h4>
                    <p><strong>Need:</strong> Quick map deployment for public</p>
                    <p><strong>Benefits:</strong> Agility, scalability, elasticity</p>
                    <p><strong>Cost:</strong> Pay-per-credit consumption</p>
                    <p><strong>Service:</strong> SaaS (ArcGIS Online)</p>
                    <p><strong>Deployment:</strong> Public cloud</p>
                    <p><strong>Your role:</strong> Content governance, not infrastructure</p>
                </div>
                
                <div class="benefit-card">
                    <h4>📱 Custom Business App</h4>
                    <p><strong>Need:</strong> Asset tracking app</p>
                    <p><strong>Benefits:</strong> Rapid development, no server setup</p>
                    <p><strong>Cost:</strong> Included in Microsoft 365 subscription</p>
                    <p><strong>Service:</strong> PaaS (Power Apps)</p>
                    <p><strong>Deployment:</strong> Public cloud</p>
                    <p><strong>Your role:</strong> App logic, not platform management</p>
                </div>
            </div>
            
            <h3>🚀 Your Administrative Journey</h3>
            
            <div class="connection-box">
                <h4>🔄 The Transformation</h4>
                <p><strong>Phase 1 - Traditional IT:</strong> Managing Exchange servers, file servers, backup tapes, patch schedules</p>
                <p><strong>Phase 2 - Hybrid Cloud:</strong> Some services in cloud (Office 365), some on-premises, complex integration</p>
                <p><strong>Phase 3 - Cloud-First:</strong> Most services in cloud, focus on user experience and business enablement</p>
                <p><strong>Phase 4 - Cloud-Native:</strong> New solutions start in cloud, traditional infrastructure is exception</p>
            </div>
            
            <div class="big-picture-summary">
                <h3>💡 Key Insights for Decision Making</h3>
                <p><strong>Start with the business need</strong> → This determines which benefits matter most → Guides your cost model preference → Influences service type choice → Affects deployment model → Defines responsibility boundaries</p>
                <br>
                <p><strong>Remember:</strong> Every cloud decision is really a business decision about <em>where you want to spend your time and expertise</em>. The cloud lets you focus on what makes your organization unique instead of keeping generic infrastructure running.</p>
                <br>
                <p><strong>Your value as an admin</strong> has shifted from <em>"keeping the lights on"</em> to <em>"enabling business innovation"</em> through smart service orchestration.</p>
            </div>
        </div>
        
        <div class="next-prev">
            <button id="prevBtn" onclick="previousPage()" disabled>← Previous</button>
            <button id="nextBtn" onclick="nextPage()">Next →</button>
        </div>
    </div>

    <script>
        let currentPage = 0;
        const totalPages = 7;
        
        function showPage(pageIndex) {
            // Hide all pages
            const pages = document.querySelectorAll('.page');
            pages.forEach(page => page.classList.remove('active'));
            
            // Remove active class from all nav buttons
            const navBtns = document.querySelectorAll('.nav-btn');
            navBtns.forEach(btn => btn.classList.remove('active'));
            
            // Show selected page
            pages[pageIndex].classList.add('active');
            navBtns[pageIndex].classList.add('active');
            
            // Update page indicator
            currentPage = pageIndex;
            document.getElementById('current-page').textContent = pageIndex + 1;
            document.getElementById('total-pages').textContent = totalPages;
            
            // Update navigation buttons
            document.getElementById('prevBtn').disabled = pageIndex === 0;
            document.getElementById('nextBtn').disabled = pageIndex === totalPages - 1;
            
            // Update button text for last page
            if (pageIndex === totalPages - 1) {
                document.getElementById('nextBtn').textContent = 'Complete ✓';
            } else {
                document.getElementById('nextBtn').textContent = 'Next →';
            }
        }
        
        function nextPage() {
            if (currentPage < totalPages - 1) {
                showPage(currentPage + 1);
            }
        }
        
        function previousPage() {
            if (currentPage > 0) {
                showPage(currentPage - 1);
            }
        }
        
        // Keyboard navigation
        document.addEventListener('keydown', function(event) {
            if (event.key === 'ArrowRight' || event.key === ' ') {
                event.preventDefault();
                nextPage();
            } else if (event.key === 'ArrowLeft') {
                event.preventDefault();
                previousPage();
            }
        });
        
        // Add smooth transitions
        document.querySelectorAll('.benefit-card, .cloud-type, .pyramid-level').forEach(card => {
            card.addEventListener('click', function() {
                this.style.transform = 'scale(0.95)';
                setTimeout(() => {
                    this.style.transform = '';
                }, 150);
            });
        });
    </script>
</body>
</html>
