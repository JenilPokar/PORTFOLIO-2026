<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jenil Pokar | Portfolio</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600&family=Inter:wght@300;400;500&display=swap" rel="stylesheet">
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://unpkg.com/lucide@latest"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        heading: ['"Space Grotesk"', 'sans-serif'],
                        body: ['"Inter"', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <style>
        @media(pointer:fine){*{cursor:none}}
        @media(pointer:coarse){.cc,.cd{display:none!important}}
        .cc{width:22px;height:22px;border:2px solid #A3E635;border-radius:50%;position:fixed;pointer-events:none;z-index:99999;transition:transform .12s ease,background .12s ease,width .12s ease,height .12s ease;transform:translate(-50%,-50%)}
        .cc.h{width:54px;height:54px;background:rgba(163,230,53,.12)}
        .cd{width:6px;height:6px;background:#A3E635;border-radius:50%;position:fixed;pointer-events:none;z-index:99999;transform:translate(-50%,-50%)}

        .loader{position:fixed;inset:0;background:#000;z-index:100000;display:flex;flex-direction:column;align-items:center;justify-content:center;transition:transform .9s cubic-bezier(.76,0,.24,1)}
        .loader.out{transform:translateY(-100%)}
        .lbar{width:180px;height:2px;background:#262626;margin-top:20px;border-radius:1px;overflow:hidden}
        .lfill{height:100%;background:#A3E635;animation:lf 1.4s ease-in-out forwards}
        @keyframes lf{0%{width:0}100%{width:100%}}

        .sh{position:fixed;pointer-events:none;z-index:0}
        .sh1{width:280px;height:280px;border:2px solid #A3E635;border-radius:50%;top:8%;right:-80px;opacity:.06;animation:f1 22s ease-in-out infinite}
        .sh2{width:180px;height:180px;border:2px solid #A3E635;bottom:15%;left:-40px;opacity:.05;transform:rotate(45deg);animation:f2 26s ease-in-out infinite}
        .sh3{width:0;height:0;border-left:70px solid transparent;border-right:70px solid transparent;border-bottom:120px solid rgba(163,230,53,.05);top:55%;right:8%;opacity:.6;animation:f3 19s ease-in-out infinite}
        .sh4{width:130px;height:130px;background:rgba(163,230,53,.04);border-radius:30% 70% 70% 30%/30% 30% 70% 70%;top:25%;left:12%;animation:mr 16s ease-in-out infinite}
        @keyframes f1{0%,100%{transform:translateY(0) rotate(0)}50%{transform:translateY(-35px) rotate(180deg)}}
        @keyframes f2{0%,100%{transform:translateY(0) rotate(45deg)}50%{transform:translateY(25px) rotate(225deg)}}
        @keyframes f3{0%,100%{transform:translateY(0) translateX(0)}33%{transform:translateY(-25px) translateX(18px)}66%{transform:translateY(18px) translateX(-12px)}}
        @keyframes mr{0%,100%{border-radius:30% 70% 70% 30%/30% 30% 70% 70%}25%{border-radius:58% 42% 75% 25%/76% 46% 54% 24%}50%{border-radius:50% 50% 33% 67%/55% 27% 73% 45%}75%{border-radius:33% 67% 58% 42%/63% 68% 32% 37%}}

        .spot{position:fixed;width:500px;height:500px;background:radial-gradient(circle,rgba(163,230,53,.06) 0%,transparent 70%);transform:translate(-50%,-50%);pointer-events:none;z-index:1}

        .pg{position:absolute;inset:0;opacity:0;transform:translateY(30px);pointer-events:none;transition:opacity .5s ease,transform .5s ease;overflow-y:auto;overflow-x:hidden}
        .pg.on{opacity:1;transform:translateY(0);pointer-events:all}
        .pg::-webkit-scrollbar{width:4px}
        .pg::-webkit-scrollbar-track{background:transparent}
        .pg::-webkit-scrollbar-thumb{background:#A3E635;border-radius:2px}

        .sc{transition:stroke-dashoffset 1.5s cubic-bezier(.4,0,.2,1)}

        .tl-dot{animation:pd 2s ease-in-out infinite}
        @keyframes pd{0%,100%{box-shadow:0 0 0 0 rgba(163,230,53,.4)}50%{box-shadow:0 0 0 14px rgba(163,230,53,0)}}

        .gc{background:rgba(23,23,23,.5);border:1px solid #262626;transition:border-color .3s,box-shadow .3s}
        .gc:hover{border-color:rgba(163,230,53,.3);box-shadow:0 0 40px rgba(163,230,53,.05)}

        .nl{position:relative}
        .nl::after{content:'';position:absolute;bottom:-4px;left:0;width:0;height:2px;background:#A3E635;transition:width .3s ease}
        .nl.on::after{width:100%}

        .mg{transition:transform .18s ease}

        .s1{opacity:0;transform:translateY(28px);transition:all .6s ease .1s}
        .s2{opacity:0;transform:translateY(28px);transition:all .6s ease .2s}
        .s3{opacity:0;transform:translateY(28px);transition:all .6s ease .3s}
        .s4{opacity:0;transform:translateY(28px);transition:all .6s ease .4s}
        .s5{opacity:0;transform:translateY(28px);transition:all .6s ease .5s}
        .s6{opacity:0;transform:translateY(28px);transition:all .6s ease .6s}
        .s7{opacity:0;transform:translateY(28px);transition:all .6s ease .7s}
        .s8{opacity:0;transform:translateY(28px);transition:all .6s ease .8s}
        .pg.on .s1,.pg.on .s2,.pg.on .s3,.pg.on .s4,.pg.on .s5,.pg.on .s6,.pg.on .s7,.pg.on .s8{opacity:1;transform:translateY(0)}

        .grain::after{content:'';position:fixed;inset:0;background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='.03'/%3E%3C/svg%3E");pointer-events:none;z-index:0;opacity:.4}

        @keyframes fadeUp{from{opacity:0;transform:translateY(12px)}to{opacity:1;transform:translateY(0)}}

        .badge-glow{animation:bg 3s ease-in-out infinite}
        @keyframes bg{0%,100%{filter:drop-shadow(0 0 8px rgba(163,230,53,.1))}50%{filter:drop-shadow(0 0 20px rgba(163,230,53,.25))}}

        .soc-icon{width:42px;height:42px;border-radius:50%;border:1px solid #262626;display:flex;align-items:center;justify-content:center;transition:border-color .3s,background .3s,transform .3s}
        .soc-icon:hover{border-color:rgba(163,230,53,.5);background:rgba(163,230,53,.08);transform:translateY(-3px)}
        .soc-icon svg{width:18px;height:18px;stroke:#a3a3a3;fill:none;stroke-width:1.8;transition:stroke .3s}
        .soc-icon:hover svg{stroke:#A3E635}

        @media(max-width:768px){.sh{display:none}.desk-only{display:none!important}}
        @media(min-width:769px){.mob-only{display:none!important}}
    </style>
</head>
<body class="bg-black text-white font-body overflow-hidden grain">

<!-- Loader -->
<div class="loader" id="loader">
    <p class="font-heading text-base tracking-[.35em] text-neutral-500 uppercase">Jenil Pokar</p>
    <div class="lbar"><div class="lfill"></div></div>
</div>

<!-- Cursor -->
<div class="cc" id="cur"></div>
<div class="cd" id="dot"></div>

<!-- Spotlight -->
<div class="spot" id="spot"></div>

<!-- Shapes -->
<div class="sh sh1"></div>
<div class="sh sh2"></div>
<div class="sh sh3"></div>
<div class="sh sh4"></div>

<!-- Navigation -->
<nav class="fixed top-0 left-0 right-0 z-50 px-5 py-4" style="background:rgba(0,0,0,.72);backdrop-filter:blur(14px);-webkit-backdrop-filter:blur(14px)">
    <div class="max-w-6xl mx-auto flex items-center justify-between">
        <button onclick="go('home')" class="font-heading text-lg font-semibold tracking-tight hv">JP<span class="text-lime-400">.</span></button>
        <div class="flex items-center gap-6 md:gap-8">
            <button onclick="go('home')" class="nl on text-sm font-medium tracking-wide text-neutral-300 hover:text-white transition-colors hv" data-p="home">Home</button>
            <button onclick="go('skills')" class="nl text-sm font-medium tracking-wide text-neutral-300 hover:text-white transition-colors hv" data-p="skills">Skills</button>
            <button onclick="go('achievements')" class="nl text-sm font-medium tracking-wide text-neutral-300 hover:text-white transition-colors hv" data-p="achievements">Achievements</button>
            <button onclick="go('education')" class="nl text-sm font-medium tracking-wide text-neutral-300 hover:text-white transition-colors hv" data-p="education">Education</button>
        </div>
    </div>
</nav>

<!-- Pages -->
<div class="relative w-full h-screen" id="wrap">

<!-- ========== HOME ========== -->
<section class="pg on" id="p-home">
<div class="min-h-screen flex items-center justify-center px-5 pt-20 pb-16">
<div class="max-w-6xl mx-auto w-full">
    <div class="grid lg:grid-cols-2 gap-12 lg:gap-16 items-center">
        <!-- Text -->
        <div>
            <div class="s1 inline-flex items-center gap-2 px-3 py-1.5 rounded-full border border-neutral-800 mb-6">
                <span class="w-2 h-2 rounded-full bg-lime-400 animate-pulse"></span>
                <span class="text-[11px] tracking-widest uppercase text-neutral-400">Open to Opportunities</span>
            </div>
            <h1 class="s2 font-heading text-5xl md:text-7xl font-semibold tracking-tight leading-[1.05] mb-6">
                Hi, I'm<br><span class="text-lime-400">Jenil</span> Pokar
            </h1>
            <p class="s3 text-base md:text-lg text-neutral-400 leading-relaxed mb-6 max-w-md">
                B.Tech Artificial Intelligence &amp; Data Science student at Shah &amp; Anchor Kutchhi Engineering College, Mumbai. Building intelligent solutions with curiosity and code.
            </p>

            <!-- Social Links -->
            <div class="s4 flex items-center gap-3 mb-8">
                <a href="https://github.com/JenilPokar" target="_blank" rel="noopener" class="soc-icon hv" aria-label="GitHub">
                    <svg viewBox="0 0 24 24"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/></svg>
                </a>
                <a href="https://www.linkedin.com/in/jenil-pokar-048719387/" target="_blank" rel="noopener" class="soc-icon hv" aria-label="LinkedIn">
                    <svg viewBox="0 0 24 24"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg>
                </a>
                <a href="https://www.instagram.com/jeniill__/" target="_blank" rel="noopener" class="soc-icon hv" aria-label="Instagram">
                    <svg viewBox="0 0 24 24"><rect x="2" y="2" width="20" height="20" rx="5" ry="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/><line x1="17.5" y1="6.5" x2="17.51" y2="6.5"/></svg>
                </a>
                <a href="mailto:jenilpokar8@gmail.com" class="soc-icon hv" aria-label="Email">
                    <svg viewBox="0 0 24 24"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"/></svg>
                </a>
            </div>

            <div class="s5 flex flex-wrap items-center gap-4 mb-10">
                <button onclick="go('skills')" class="mg hv inline-flex items-center gap-2 px-6 py-3 bg-lime-400 text-black font-medium text-sm tracking-wide rounded-full hover:bg-lime-300 transition-colors">
                    Explore My Work <i data-lucide="arrow-right" class="w-4 h-4"></i>
                </button>
                <button onclick="go('education')" class="mg hv inline-flex items-center gap-2 px-6 py-3 border border-neutral-700 text-white font-medium text-sm tracking-wide rounded-full hover:border-neutral-500 transition-colors">
                    Education
                </button>
            </div>
            <div class="s6 flex items-center gap-8">
                <div><div class="text-2xl font-heading font-semibold" id="c-sgpa">0</div><div class="text-[11px] text-neutral-500 tracking-wide mt-1">SGPA Sem 1</div></div>
                <div class="w-px h-10 bg-neutral-800"></div>
                <div><div class="text-2xl font-heading font-semibold" id="c-cet">0</div><div class="text-[11px] text-neutral-500 tracking-wide mt-1">CET Overall %ile</div></div>
                <div class="w-px h-10 bg-neutral-800"></div>
                <div><div class="text-2xl font-heading font-semibold" id="c-certs">0</div><div class="text-[11px] text-neutral-500 tracking-wide mt-1">Certifications</div></div>
            </div>
        </div>
        <!-- Image -->
        <div class="s4 flex justify-center lg:justify-end">
            <div class="relative">
                <div class="absolute -inset-4 border border-lime-400/20 rounded-3xl rotate-3"></div>
                <div class="absolute -inset-4 border border-neutral-800 rounded-3xl -rotate-2"></div>
                <div class="relative w-64 h-80 sm:w-72 sm:h-96 md:w-80 md:h-[420px] rounded-2xl overflow-hidden">
                    <img src="https://z-cdn-media.chatglm.cn/files/7dab264c-d917-4c04-949c-daec3e856699.jpg?auth_key=1878154691-16ed0836aa81498888ac6ab574fc4eca-0-1cd41b5c10d1f5440754e0056e0d4402" alt="Jenil Pokar" class="w-full h-full object-cover" style="object-position:center 15%">
                    <div class="absolute inset-0 bg-gradient-to-t from-black/60 via-transparent to-transparent"></div>
                </div>
                <div class="absolute -bottom-5 -left-5 bg-neutral-900/90 backdrop-blur-sm border border-neutral-800 rounded-xl px-4 py-3" style="animation:fadeUp .6s ease .8s both">
                    <div class="text-[10px] text-neutral-500 uppercase tracking-wider">Location</div>
                    <div class="text-sm font-medium flex items-center gap-1.5"><i data-lucide="map-pin" class="w-3.5 h-3.5 text-lime-400"></i>Mumbai, India</div>
                </div>
                <div class="absolute -top-4 -right-4 bg-neutral-900/90 backdrop-blur-sm border border-neutral-800 rounded-xl px-4 py-3" style="animation:fadeUp .6s ease 1s both">
                    <div class="text-[10px] text-neutral-500 uppercase tracking-wider">Course</div>
                    <div class="text-sm font-medium">AI &amp; Data Science</div>
                </div>
            </div>
        </div>
    </div>

    <!-- Nav Cards -->
    <div class="s7 grid sm:grid-cols-3 gap-5 mt-16 lg:mt-20">
        <button onclick="go('skills')" class="mg hv gc group text-left p-6 rounded-2xl">
            <div class="w-11 h-11 rounded-xl bg-lime-400/10 flex items-center justify-center mb-4 group-hover:scale-110 transition-transform duration-300"><i data-lucide="cpu" class="w-5 h-5 text-lime-400"></i></div>
            <h3 class="font-heading text-lg font-semibold mb-1.5">Skills</h3>
            <p class="text-sm text-neutral-500 leading-relaxed">Technical proficiencies &amp; tools I work with</p>
            <div class="flex items-center gap-1 mt-4 text-lime-400 text-sm font-medium"><span>View</span><i data-lucide="arrow-up-right" class="w-4 h-4 group-hover:translate-x-1 group-hover:-translate-y-1 transition-transform"></i></div>
        </button>
        <button onclick="go('achievements')" class="mg hv gc group text-left p-6 rounded-2xl">
            <div class="w-11 h-11 rounded-xl bg-lime-400/10 flex items-center justify-center mb-4 group-hover:scale-110 transition-transform duration-300"><i data-lucide="trophy" class="w-5 h-5 text-lime-400"></i></div>
            <h3 class="font-heading text-lg font-semibold mb-1.5">Achievements</h3>
            <p class="text-sm text-neutral-500 leading-relaxed">Certifications, badges &amp; competitive exam scores</p>
            <div class="flex items-center gap-1 mt-4 text-lime-400 text-sm font-medium"><span>View</span><i data-lucide="arrow-up-right" class="w-4 h-4 group-hover:translate-x-1 group-hover:-translate-y-1 transition-transform"></i></div>
        </button>
        <button onclick="go('education')" class="mg hv gc group text-left p-6 rounded-2xl">
            <div class="w-11 h-11 rounded-xl bg-lime-400/10 flex items-center justify-center mb-4 group-hover:scale-110 transition-transform duration-300"><i data-lucide="graduation-cap" class="w-5 h-5 text-lime-400"></i></div>
            <h3 class="font-heading text-lg font-semibold mb-1.5">Education</h3>
            <p class="text-sm text-neutral-500 leading-relaxed">Academic journey from school to engineering</p>
            <div class="flex items-center gap-1 mt-4 text-lime-400 text-sm font-medium"><span>View</span><i data-lucide="arrow-up-right" class="w-4 h-4 group-hover:translate-x-1 group-hover:-translate-y-1 transition-transform"></i></div>
        </button>
    </div>
</div>
</div>
</section>

<!-- ========== SKILLS ========== -->
<section class="pg" id="p-skills">
<div class="min-h-screen px-5 pt-28 pb-20">
<div class="max-w-6xl mx-auto">
    <div class="s1 mb-14">
        <div class="text-[11px] tracking-widest uppercase text-lime-400 mb-3">What I Know</div>
        <h2 class="font-heading text-4xl md:text-5xl font-semibold tracking-tight">Skills &amp; Technologies</h2>
        <p class="text-neutral-400 mt-3 max-w-lg">A snapshot of my technical abilities, continuously growing through coursework, certifications, and hands-on projects.</p>
    </div>
    <div class="s2 grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6 md:gap-8 mb-16" id="skillGrid"></div>
    <div class="s3 mb-16">
        <h3 class="font-heading text-xl font-semibold mb-5 flex items-center gap-2"><i data-lucide="wrench" class="w-5 h-5 text-lime-400"></i>Tools &amp; Platforms</h3>
        <div class="flex flex-wrap gap-3" id="toolTags"></div>
    </div>
    <div class="s4 gc rounded-2xl p-6 md:p-8">
        <h3 class="font-heading text-xl font-semibold mb-2 flex items-center gap-2"><i data-lucide="rocket" class="w-5 h-5 text-lime-400"></i>Currently Learning</h3>
        <p class="text-neutral-400 text-sm leading-relaxed mb-5">Expanding my skill set as part of my B.Tech AI &amp; Data Science curriculum and self-driven exploration.</p>
        <div class="grid sm:grid-cols-3 gap-4" id="learningGrid"></div>
    </div>
</div>
</div>
</section>

<!-- ========== ACHIEVEMENTS ========== -->
<section class="pg" id="p-achievements">
<div class="min-h-screen px-5 pt-28 pb-20">
<div class="max-w-6xl mx-auto">
    <div class="s1 mb-14">
        <div class="text-[11px] tracking-widest uppercase text-lime-400 mb-3">Milestones</div>
        <h2 class="font-heading text-4xl md:text-5xl font-semibold tracking-tight">Achievements</h2>
    </div>
    <div class="s2 gc rounded-2xl p-6 md:p-8 mb-6">
        <div class="flex flex-col md:flex-row gap-6 items-start md:items-center">
            <div class="w-full md:w-72 flex-shrink-0">
                <img src="https://z-cdn-media.chatglm.cn/files/060ed9b3-4bcc-46fb-a911-2352746c873f.png?auth_key=1878154691-e21f3b06b0bb4e84ac7b0279fcdc0c77-0-e3b2fe041ec28eb4c35d710fd8f3edab" alt="Google Cloud Skill Badge" class="w-full rounded-xl badge-glow">
            </div>
            <div>
                <div class="flex items-center gap-2 mb-2">
                    <span class="text-[10px] tracking-widest uppercase text-lime-400 bg-lime-400/10 px-2 py-0.5 rounded">Google Cloud</span>
                    <span class="text-[10px] tracking-widest uppercase text-neutral-500 bg-neutral-800 px-2 py-0.5 rounded">Skill Badge</span>
                </div>
                <h3 class="font-heading text-xl md:text-2xl font-semibold mb-2">Prompt Design in Vertex AI</h3>
                <p class="text-sm text-neutral-400 leading-relaxed mb-3">Earned the introductory skill badge in Machine Learning &amp; AI from Google Cloud, demonstrating proficiency in designing effective prompts for Vertex AI models.</p>
                <div class="flex items-center gap-4 text-xs text-neutral-500">
                    <span class="flex items-center gap-1"><i data-lucide="award" class="w-3.5 h-3.5 text-lime-400"></i>Introductory Level</span>
                    <span class="flex items-center gap-1"><i data-lucide="tag" class="w-3.5 h-3.5 text-lime-400"></i>ML &amp; AI</span>
                </div>
            </div>
        </div>
    </div>
    <div class="s3 gc rounded-2xl p-6 md:p-8 mb-6">
        <div class="flex items-start gap-5">
            <div class="w-14 h-14 rounded-2xl bg-lime-400/10 flex items-center justify-center flex-shrink-0">
                <i data-lucide="file-badge" class="w-7 h-7 text-lime-400"></i>
            </div>
            <div class="flex-1">
                <div class="flex flex-wrap items-center gap-2 mb-2">
                    <span class="text-[10px] tracking-widest uppercase text-lime-400 bg-lime-400/10 px-2 py-0.5 rounded">IIT Bombay</span>
                    <span class="text-[10px] tracking-widest uppercase text-neutral-500 bg-neutral-800 px-2 py-0.5 rounded">EduPyramids, SINE</span>
                </div>
                <h3 class="font-heading text-xl font-semibold mb-1">C Programming Certification</h3>
                <p class="text-sm text-neutral-400 leading-relaxed mb-4">Completed C Training with online examination remotely invigilated from IIT Bombay. Course organized at Shah &amp; Anchor Kutchhi Engineering College with material from EduPyramids, SINE, IIT Bombay.</p>
                <div class="flex flex-wrap items-center gap-6 text-sm">
                    <div><span class="text-neutral-500 text-xs block">Score</span><span class="font-heading font-semibold text-lime-400 text-lg">90.00%</span></div>
                    <div class="w-px h-8 bg-neutral-800"></div>
                    <div><span class="text-neutral-500 text-xs block">Credits</span><span class="font-heading font-semibold text-lg">2</span></div>
                    <div class="w-px h-8 bg-neutral-800"></div>
                    <div><span class="text-neutral-500 text-xs block">Date</span><span class="font-heading font-semibold">18 Dec 2025</span></div>
                </div>
            </div>
        </div>
    </div>
    <div class="s4 gc rounded-2xl p-6 md:p-8 mb-6">
        <div class="flex items-center gap-2 mb-2">
            <i data-lucide="bar-chart-3" class="w-5 h-5 text-lime-400"></i>
            <h3 class="font-heading text-xl font-semibold">MHT-CET 2025 Results</h3>
            <span class="text-[10px] tracking-widest uppercase text-neutral-500 bg-neutral-800 px-2 py-0.5 rounded ml-2">PCM Group</span>
        </div>
        <div class="flex items-center gap-2 mb-5">
            <span class="text-sm text-neutral-400">Overall Percentile:</span>
            <span class="font-heading text-2xl font-semibold text-lime-400">83.72</span>
        </div>
        <div class="grid grid-cols-3 gap-4 md:gap-8 mb-6" id="cetGrid"></div>
        <div class="text-xs text-neutral-600 text-center">Percentile scores · Government of Maharashtra · State Common Entrance Test Cell</div>
    </div>
    <div class="s5 gc rounded-2xl p-6 md:p-8">
        <div class="flex items-center gap-2 mb-5">
            <i data-lucide="star" class="w-5 h-5 text-lime-400"></i>
            <h3 class="font-heading text-xl font-semibold">Academic Highlights</h3>
        </div>
        <div class="grid sm:grid-cols-2 gap-4">
            <div class="bg-neutral-900/60 rounded-xl p-5 border border-neutral-800/60">
                <div class="text-[10px] tracking-widest uppercase text-lime-400 mb-2">Semester 1 · B.Tech</div>
                <div class="font-heading text-2xl font-semibold text-lime-400 mb-1">O Grade × 2</div>
                <p class="text-sm text-neutral-400">Engineering Graphics &amp; Exploration Lab — Perfect 10 Grade Points</p>
            </div>
            <div class="bg-neutral-900/60 rounded-xl p-5 border border-neutral-800/60">
                <div class="text-[10px] tracking-widest uppercase text-lime-400 mb-2">HSC 2025</div>
                <div class="font-heading text-2xl font-semibold text-lime-400 mb-1">150 in CS</div>
                <p class="text-sm text-neutral-400">Computer Science — 150/200 in Maharashtra State Board examination</p>
            </div>
            <div class="bg-neutral-900/60 rounded-xl p-5 border border-neutral-800/60">
                <div class="text-[10px] tracking-widest uppercase text-lime-400 mb-2">10th CBSE 2023</div>
                <div class="font-heading text-2xl font-semibold text-lime-400 mb-1">94 in IT</div>
                <p class="text-sm text-neutral-400">Information Technology — A1 Grade, highest among all subjects</p>
            </div>
            <div class="bg-neutral-900/60 rounded-xl p-5 border border-neutral-800/60">
                <div class="text-[10px] tracking-widest uppercase text-lime-400 mb-2">Semester 1 · B.Tech</div>
                <div class="font-heading text-2xl font-semibold text-lime-400 mb-1">SGPA 8.39</div>
                <p class="text-sm text-neutral-400">Strong start to engineering with 193 credit points out of 23 credits</p>
            </div>
        </div>
    </div>
</div>
</div>
</section>

<!-- ========== EDUCATION ========== -->
<section class="pg" id="p-education">
<div class="min-h-screen px-5 pt-28 pb-20">
<div class="max-w-6xl mx-auto">
    <div class="s1 mb-14">
        <div class="text-[11px] tracking-widest uppercase text-lime-400 mb-3">My Journey</div>
        <h2 class="font-heading text-4xl md:text-5xl font-semibold tracking-tight">Education</h2>
    </div>
    <div class="relative">
        <div class="absolute left-5 md:left-7 top-0 bottom-0 w-px bg-gradient-to-b from-lime-400 via-neutral-800 to-neutral-900"></div>
        <div class="s2 relative pl-14 md:pl-20 pb-16">
            <div class="absolute left-3.5 md:left-5.5 top-1 w-4 h-4 rounded-full bg-lime-400 border-4 border-black tl-dot"></div>
            <div class="text-[10px] tracking-widest uppercase text-lime-400 mb-2">2025 — Present · Ongoing</div>
            <h3 class="font-heading text-2xl md:text-3xl font-semibold mb-1">B.Tech in AI &amp; Data Science</h3>
            <p class="text-neutral-400 mb-1">Shah &amp; Anchor Kutchhi Engineering College, Mumbai</p>
            <p class="text-xs text-neutral-600 mb-5">An Autonomous Institute Affiliated to University of Mumbai · PRN: 125BTAI1056</p>
            <div class="gc rounded-2xl p-5 md:p-6">
                <div class="flex items-center justify-between mb-4">
                    <div>
                        <div class="text-[10px] tracking-widest uppercase text-neutral-500 mb-1">Semester 1 · Jan 2026</div>
                        <div class="font-heading text-xl font-semibold">SGPA <span class="text-lime-400">8.39</span></div>
                    </div>
                    <span class="text-xs bg-lime-400/10 text-lime-400 px-3 py-1 rounded-full font-medium">Successful</span>
                </div>
                <div class="overflow-x-auto">
                    <table class="w-full text-sm">
                        <thead><tr class="text-left text-[10px] tracking-widest uppercase text-neutral-500 border-b border-neutral-800">
                            <th class="pb-2 pr-4">Course</th><th class="pb-2 pr-4 w-20">Grade</th><th class="pb-2 pr-4 w-16">GP</th><th class="pb-2 w-16">Credits</th>
                        </tr></thead>
                        <tbody class="text-neutral-300" id="semTable"></tbody>
                    </table>
                </div>
            </div>
        </div>
        <div class="s4 relative pl-14 md:pl-20 pb-16">
            <div class="absolute left-3.5 md:left-5.5 top-1 w-4 h-4 rounded-full bg-neutral-400 border-4 border-black"></div>
            <div class="text-[10px] tracking-widest uppercase text-neutral-500 mb-2">2025 · Completed</div>
            <h3 class="font-heading text-2xl md:text-3xl font-semibold mb-1">HSC (12th Standard)</h3>
            <p class="text-neutral-400 mb-1">Maharashtra State Board of Secondary &amp; Higher Secondary Education, Pune</p>
            <p class="text-xs text-neutral-600 mb-5">Seat No: M026808 · Division: Mumbai</p>
            <div class="gc rounded-2xl p-5 md:p-6">
                <div class="flex items-center justify-between mb-4">
                    <div>
                        <div class="text-[10px] tracking-widest uppercase text-neutral-500 mb-1">Result</div>
                        <div class="font-heading text-xl font-semibold"><span class="text-lime-400">382</span> / 600</div>
                    </div>
                    <div class="text-right">
                        <div class="font-heading text-2xl font-semibold text-lime-400">63.67%</div>
                        <span class="text-xs bg-lime-400/10 text-lime-400 px-3 py-1 rounded-full font-medium">PASS</span>
                    </div>
                </div>
                <div class="space-y-2" id="hscBars"></div>
            </div>
        </div>
        <div class="s6 relative pl-14 md:pl-20">
            <div class="absolute left-3.5 md:left-5.5 top-1 w-4 h-4 rounded-full bg-neutral-600 border-4 border-black"></div>
            <div class="text-[10px] tracking-widest uppercase text-neutral-500 mb-2">2023 · Completed</div>
            <h3 class="font-heading text-2xl md:text-3xl font-semibold mb-1">SSC (10th Standard)</h3>
            <p class="text-neutral-400 mb-1">CBSE · Poddar Brio International School, Badlapur, Thane</p>
            <p class="text-xs text-neutral-600 mb-5">Roll No: 15195645 · DOB: 27 August 2007</p>
            <div class="gc rounded-2xl p-5 md:p-6">
                <div class="flex items-center justify-between mb-4">
                    <div class="text-[10px] tracking-widest uppercase text-neutral-500">Marks Statement Cum Certificate · May 2023</div>
                    <span class="text-xs bg-lime-400/10 text-lime-400 px-3 py-1 rounded-full font-medium">PASS</span>
                </div>
                <div class="grid grid-cols-2 sm:grid-cols-3 gap-3" id="cbseGrid"></div>
            </div>
        </div>
    </div>
</div>
</div>
</section>

</div>

<script>
const skills = [
    { name: 'C Programming', pct: 90, color: '#A3E635' },
    { name: 'Computer Science', pct: 88, color: '#84CC16' },
    { name: 'Eng. Graphics', pct: 95, color: '#A3E635' },
    { name: 'Digital Electronics', pct: 85, color: '#84CC16' },
    { name: 'Google Cloud', pct: 90, color: '#A3E635' },
    { name: 'Prompt Engineering', pct: 78, color: '#84CC16' },
    { name: 'Data Science', pct: 85, color: '#84CC16' }
];
const tools = ['VS Code','Google Cloud Platform','Vertex AI','C','Python Basics','Linux','Git','Engineering Drawing Tools'];
const learning = [
    { icon: 'brain', label: 'Machine Learning', desc: 'Core ML algorithms & concepts' },
    { icon: 'database', label: 'Data Analysis', desc: 'Pandas, NumPy, data wrangling' },
    { icon: 'network', label: 'Deep Learning', desc: 'Neural networks & frameworks' }
];
const semCourses = [
    { name: 'Matrices & Differential Calculus', grade: 'B', gp: 8, cr: 4 },
    { name: 'Applied Physics', grade: 'A', gp: 9, cr: 4 },
    { name: 'Principle of Digital Electronics', grade: 'A', gp: 9, cr: 3 },
    { name: 'Engineering Graphics', grade: 'O', gp: 10, cr: 3 },
    { name: 'Effective & Interactive Communication', grade: 'C', gp: 7, cr: 2 },
    { name: 'Universal Human Values – I', grade: 'A', gp: 9, cr: 2 },
    { name: 'Yoga & Sports', grade: 'D', gp: 6, cr: 2 },
    { name: 'Skill Based Lab – I (C Programming)', grade: 'C', gp: 7, cr: 2 },
    { name: 'Exploration Lab', grade: 'O', gp: 10, cr: 1 }
];
const hscSubjects = [
    { name: 'English', marks: 73, max: 100 },
    { name: 'Mathematics & Statistics', marks: 44, max: 100 },
    { name: 'Physics', marks: 54, max: 100 },
    { name: 'Chemistry', marks: 61, max: 100 },
    { name: 'Computer Science', marks: 150, max: 200 }
];
const cbseSubjects = [
    { name: 'English Lng & Lit.', marks: 77, grade: 'B2' },
    { name: 'Mathematics Standard', marks: 80, grade: 'A2' },
    { name: 'Science', marks: 74, grade: 'B1' },
    { name: 'Social Science', marks: 90, grade: 'A2' },
    { name: 'Hindi', marks: 81, grade: 'A2' },
    { name: 'Information Technology', marks: 94, grade: 'A1' }
];
const cetScores = [
    { name: 'Chemistry', pct: 93.73 },
    { name: 'Physics', pct: 42.77 },
    { name: 'Mathematics', pct: 74.05 }
];

function buildSkills(){
    const g=document.getElementById('skillGrid'),R=45,C=2*Math.PI*R;
    skills.forEach(s=>{
        const off=C*(1-s.pct/100),d=document.createElement('div');
        d.className='flex flex-col items-center';
        d.innerHTML=`<div class="relative w-28 h-28 md:w-32 md:h-32"><svg viewBox="0 0 100 100" class="w-full h-full -rotate-90"><circle cx="50" cy="50" r="${R}" stroke="#262626" stroke-width="7" fill="none"/><circle cx="50" cy="50" r="${R}" stroke="${s.color}" stroke-width="7" fill="none" stroke-dasharray="${C}" stroke-dashoffset="${C}" stroke-linecap="round" class="sc" data-off="${off}"/></svg><div class="absolute inset-0 flex flex-col items-center justify-center"><span class="font-heading text-xl font-semibold">${s.pct}%</span></div></div><span class="text-xs text-neutral-400 mt-3 text-center leading-tight">${s.name}</span>`;
        g.appendChild(d);
    });
}
function buildTools(){
    const g=document.getElementById('toolTags');
    tools.forEach(t=>{const s=document.createElement('span');s.className='px-4 py-2 text-sm border border-neutral-800 rounded-full text-neutral-300 hover:border-lime-400/40 hover:text-lime-400 transition-colors';s.textContent=t;g.appendChild(s);});
}
function buildLearning(){
    const g=document.getElementById('learningGrid');
    learning.forEach(l=>{const d=document.createElement('div');d.className='bg-neutral-900/60 rounded-xl p-4 border border-neutral-800/60';d.innerHTML=`<i data-lucide="${l.icon}" class="w-5 h-5 text-lime-400 mb-2"></i><div class="font-heading font-semibold text-sm mb-0.5">${l.label}</div><div class="text-xs text-neutral-500">${l.desc}</div>`;g.appendChild(d);});
}
function buildCET(){
    const g=document.getElementById('cetGrid'),R=42,C=2*Math.PI*R;
    cetScores.forEach(c=>{
        const off=C*(1-c.pct/100),d=document.createElement('div');
        d.className='flex flex-col items-center';
        d.innerHTML=`<div class="relative w-24 h-24 md:w-28 md:h-28"><svg viewBox="0 0 100 100" class="w-full h-full -rotate-90"><circle cx="50" cy="50" r="${R}" stroke="#262626" stroke-width="6" fill="none"/><circle cx="50" cy="50" r="${R}" stroke="#A3E635" stroke-width="6" fill="none" stroke-dasharray="${C}" stroke-dashoffset="${C}" stroke-linecap="round" class="sc" data-off="${off}"/></svg><div class="absolute inset-0 flex flex-col items-center justify-center"><span class="font-heading text-lg font-semibold">${c.pct}</span><span class="text-[9px] text-neutral-500">%ile</span></div></div><span class="text-xs text-neutral-400 mt-2">${c.name}</span>`;
        g.appendChild(d);
    });
}
function buildSemTable(){
    const t=document.getElementById('semTable');
    semCourses.forEach(c=>{const isO=c.grade==='O',tr=document.createElement('tr');tr.className='border-b border-neutral-800/60';tr.innerHTML=`<td class="py-2.5 pr-4 text-neutral-300">${c.name}</td><td class="py-2.5 pr-4"><span class="font-semibold ${isO?'text-lime-400':''}">${c.grade}</span></td><td class="py-2.5 pr-4 font-heading">${c.gp}</td><td class="py-2.5 text-neutral-500">${c.cr}</td>`;t.appendChild(tr);});
}
function buildHSC(){
    const g=document.getElementById('hscBars');
    hscSubjects.forEach(s=>{
        const pct=(s.marks/s.max)*100,isHL=s.name==='Computer Science',d=document.createElement('div');
        d.innerHTML=`<div class="flex items-center justify-between text-sm mb-1"><span class="text-neutral-300 ${isHL?'text-lime-400 font-semibold':''}">${s.name}</span><span class="font-heading font-semibold ${isHL?'text-lime-400 text-base':''}">${s.marks}<span class="text-neutral-600 text-xs font-normal">/${s.max}</span></span></div><div class="h-1.5 bg-neutral-800 rounded-full overflow-hidden"><div class="h-full rounded-full ${isHL?'bg-lime-400':'bg-neutral-600'} transition-all duration-1000" style="width:0%" data-w="${pct}%"></div></div>`;
        g.appendChild(d);
    });
}
function buildCBSE(){
    const g=document.getElementById('cbseGrid');
    cbseSubjects.forEach(s=>{
        const isHL=s.name==='Information Technology',d=document.createElement('div');
        d.className=`bg-neutral-900/60 rounded-xl p-4 border ${isHL?'border-lime-400/30':'border-neutral-800/60'}`;
        d.innerHTML=`<div class="text-xs text-neutral-500 mb-1 truncate">${s.name}</div><div class="flex items-center gap-2"><span class="font-heading text-xl font-semibold ${isHL?'text-lime-400':''}">${s.marks}</span><span class="text-[10px] tracking-wider ${isHL?'text-lime-400 bg-lime-400/10':'text-neutral-500 bg-neutral-800'} px-2 py-0.5 rounded">${s.grade}</span></div>`;
        g.appendChild(d);
    });
}
buildSkills();buildTools();buildLearning();buildCET();buildSemTable();buildHSC();buildCBSE();

setTimeout(()=>{document.getElementById('loader').classList.add('out');setTimeout(()=>{document.getElementById('loader').style.display='none';animateHome();},900);},1800);

let currentPage='home',skillsAnimated=false,achAnimated=false,eduAnimated=false;
function go(page){
    if(page===currentPage)return;
    document.querySelectorAll('.pg').forEach(p=>p.classList.remove('on'));
    document.querySelectorAll('.nl').forEach(n=>n.classList.toggle('on',n.dataset.p===page));
    currentPage=page;
    const el=document.getElementById('p-'+page);el.scrollTop=0;
    requestAnimationFrame(()=>{el.classList.add('on');lucide.createIcons();
        if(page==='skills'&&!skillsAnimated){setTimeout(animateSkills,400);skillsAnimated=true;}
        if(page==='achievements'&&!achAnimated){setTimeout(animateAch,400);achAnimated=true;}
        if(page==='education'&&!eduAnimated){setTimeout(animateEdu,400);eduAnimated=true;}
    });
}

function animateHome(){countUp('c-sgpa',8.39,1500,2);countUp('c-cet',83.72,1500,2);countUp('c-certs',2,800,0);}
function countUp(id,target,dur,dec){const el=document.getElementById(id),st=performance.now();function step(now){const t=Math.min((now-st)/dur,1),e=1-Math.pow(1-t,3);el.textContent=(target*e).toFixed(dec);if(t<1)requestAnimationFrame(step);else el.textContent=target.toFixed(dec);}requestAnimationFrame(step);}
function animateSkills(){document.querySelectorAll('#skillGrid .sc').forEach(c=>c.style.strokeDashoffset=c.dataset.off);}
function animateAch(){document.querySelectorAll('#cetGrid .sc').forEach(c=>c.style.strokeDashoffset=c.dataset.off);}
function animateEdu(){document.querySelectorAll('#hscBars [data-w]').forEach(b=>setTimeout(()=>b.style.width=b.dataset.w,200));}

const cur=document.getElementById('cur'),dot=document.getElementById('dot'),spot=document.getElementById('spot');
let mx=0,my=0,cx=0,cy=0;
document.addEventListener('mousemove',e=>{mx=e.clientX;my=e.clientY;dot.style.left=mx+'px';dot.style.top=my+'px';spot.style.left=mx+'px';spot.style.top=my+'px';});
function tickCursor(){cx+=(mx-cx)*.15;cy+=(my-cy)*.15;cur.style.left=cx+'px';cur.style.top=cy+'px';requestAnimationFrame(tickCursor);}tickCursor();
document.addEventListener('mouseover',e=>{cur.classList.toggle('h',!!e.target.closest('.hv,button,a'));});
document.querySelectorAll('.mg').forEach(btn=>{btn.addEventListener('mousemove',e=>{const r=btn.getBoundingClientRect();btn.style.transform=`translate(${(e.clientX-r.left-r.width/2)*.25}px,${(e.clientY-r.top-r.height/2)*.25}px)`;});btn.addEventListener('mouseleave',()=>btn.style.transform='translate(0,0)');});
lucide.createIcons();
</script>
</body>
</html>
