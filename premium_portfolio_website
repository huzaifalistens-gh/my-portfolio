import React, { useState, useEffect } from 'react';
import { 
  ArrowUpRight, 
  Mail, 
  Linkedin, 
  ArrowRight, 
  X, 
  FileText, 
  Check, 
  Sparkles, 
  Cpu, 
  Smartphone, 
  Layout, 
  Database, 
  ChevronRight, 
  Layers, 
  Search, 
  MessageSquare,
  MapPin,
  Briefcase,
  Phone
} from 'lucide-react';

const CASE_STUDIES = [
  {
    id: 'fairdrive',
    title: 'FairDrive',
    tagline: 'End-to-End Mobility Ecosystem (Bangladesh Market)',
    category: 'Mobility & Ride-Hailing Suite',
    role: 'Founding Designer (Sep 2024 - Dec 2025)',
    summary: 'A complete multi-sided mobility platform comprising a Customer App, Driver App, and Admin Panel, built to streamline ride booking, driver operations, and complex business workflows.',
    problem: 'Ride-sharing workflows in emerging markets suffered from operational disconnects, high-density dropouts, and complicated navigation layouts across separate user portals.',
    process: 'Designed end-to-end UX flows, created highly scalable UI systems, mapped localized customer-to-driver logic paths, and integrated responsive admin dashboard components.',
    outcome: 'Created a unified ecosystem that significantly simplified complex transit booking workflows, improved multi-point usability, and delivered high-performance user touchpoints.',
    metrics: [
      { label: 'Platform Scope', value: '3-Sided Suite' },
      { label: 'Ecosystem Phase', value: 'Founding UX' },
      { label: 'Target Market', value: 'Bangladesh' }
    ],
    alternatingViews: [
      {
        title: "The Mobility Problem Space",
        desc: "Drivers and riders needed friction-free synchronization. Complexity in map tracking and dispatch requests caused critical journey abandonments.",
        visualType: "flow"
      },
      {
        title: "Adaptive Interface Design",
        desc: "Designed specialized dynamic layouts for driver-specific dashboards and customer-facing responsive booking interfaces.",
        visualType: "wireframe"
      },
      {
        title: "Operational Outcome",
        desc: "Delivered a production-ready design library establishing streamlined dispatch networks, visual path mapping, and clear admin controls.",
        visualType: "ui"
      }
    ]
  },
  {
    id: 'filesure',
    title: 'FileSure',
    tagline: 'Corporate Compliance & Company Intelligence Platform',
    category: 'B2B SaaS / Enterprise Web',
    role: 'UX Designer (Sep 2024 - Dec 2025)',
    summary: 'A sophisticated B2B SaaS platform aggregating Ministry of Corporate Affairs (MCA), Registrar of Companies (ROC), GST, director intelligence, and complex financials into a unified compliance grid.',
    problem: 'Enterprise teams faced severe friction sorting through disparate regulatory pipelines, financial sheets, and scattered identity databases.',
    process: 'Formulated cohesive brand guidelines, designed high-density informational tables, built responsive dashboard widgets, and established the platform\'s unified tone of voice.',
    outcome: 'Successfully shaped a trustworthy, enterprise-grade B2B platform with cohesive visual guidelines that streamline compliance intelligence.',
    metrics: [
      { label: 'Integrations', value: 'MCA / ROC / GST' },
      { label: 'Product Focus', value: 'B2B Compliance' },
      { label: 'Design System', value: 'Token-Driven' }
    ],
    alternatingViews: [
      {
        title: "Aggregation Complexity",
        desc: "Handling highly sensitive legal data required high-trust visualization schemas and minimal visual stress.",
        visualType: "flow"
      },
      {
        title: "Consolidated Grid Interface",
        desc: "Architected clear-cut layout panels focusing on automated alert flags and hierarchical risk parameters.",
        visualType: "wireframe"
      },
      {
        title: "Trustworthy B2B Delivery",
        desc: "Created solid, production-ready guidelines that ensure visual consistency across all data-dense audit modules.",
        visualType: "ui"
      }
    ]
  },
  {
    id: 'lyftindia',
    title: 'Lyft India',
    tagline: 'India-First Regional Ride-Hailing Platform',
    category: 'Kolkata Mobility Portal',
    role: 'UI Designer (Mar 2023 - Aug 2023)',
    summary: 'A Kolkata-based ride-hailing platform offering cab and bike taxi services, centered on building an India-first commuting experience rooted in local urban mobility dynamics.',
    problem: 'Generic ride layouts failed to address regional transport habits, local landmark navigation behaviors, and high-glare outdoor mobile contexts.',
    process: 'Redesigned the core mobile application interfaces, optimized real-time booking flows, and curated regional marketing vectors & Play Store graphics.',
    outcome: 'Significantly enhanced booking flow consistency, visual layout clarity, and digital brand presence across regional marketing assets.',
    metrics: [
      { label: 'Ecosystem', value: 'Cab & Bike Taxi' },
      { label: 'Regional Focus', value: 'India-First' },
      { label: 'Asset Scope', value: 'App & Marketing' }
    ],
    alternatingViews: [
      {
        title: "Urban Mobility Friction",
        desc: "In-trip stress and visual clutter made quick-booking workflows difficult under intense regional commuting conditions.",
        visualType: "flow"
      },
      {
        title: "Booking Consistency Redesign",
        desc: "Created robust and simplified booking paths with prominent, accessible touch-points optimized for bike-taxi bookings.",
        visualType: "wireframe"
      },
      {
        title: "App Store Optimization",
        desc: "Crafted high-fidelity screenshots, promotional banners, and social creatives reinforcing regional appeal.",
        visualType: "ui"
      }
    ]
  }
];

const WORK_EXPERIENCE = [
  {
    role: "UI/UX Designer",
    company: "Filesure India Pvt. Ltd.",
    period: "Sep 2024 - Dec 2025",
    location: "Mumbai, IN (Remote)",
    desc: "Spearheaded design assets for the unified B2B compliance portal. Established scalable design tokens, multi-state risk tracking interfaces, and robust brand blueprints."
  },
  {
    role: "Graphic & UI UX Designer",
    company: "Hittok Pvt. Ltd.",
    period: "Sep 2023 - Aug 2024",
    location: "Kolkata, IN (On-site)",
    desc: "Worked cross-functionally to deliver highly optimized web portals and graphical assets, aligning user experiences with strategic company initiatives."
  },
  {
    role: "Graphic & UI Designer",
    company: "Lyft India Online Cab & Bike Services",
    period: "Mar 2023 - Aug 2023",
    location: "Kolkata, IN (On-site)",
    desc: "Redesigned mobile touchpoints to optimize bike taxi booking metrics. Crafted Play Store layouts and digital campaign systems increasing brand acquisition."
  }
];

export default function App() {
  const [selectedCaseStudy, setSelectedCaseStudy] = useState(null);
  const [activeCaseStudyId, setActiveCaseStudyId] = useState('fairdrive');
  const [aiWorkflowStep, setAiWorkflowStep] = useState(0);
  const [copied, setCopied] = useState(false);

  const scrollToSection = (id) => {
    const el = document.getElementById(id);
    if (el) {
      el.scrollIntoView({ behavior: 'smooth' });
    }
  };

  const copyEmail = () => {
    try {
      const el = document.createElement('textarea');
      el.value = 'huzaifalistens@gmail.com';
      el.setAttribute('readonly', '');
      el.style.position = 'absolute';
      el.style.left = '-9999px';
      document.body.appendChild(el);
      el.select();
      document.execCommand('copy');
      document.body.removeChild(el);
      setCopied(true);
      setTimeout(() => setCopied(false), 2000);
    } catch (err) {
      console.warn('Fallback copy routine initialized: ', err);
    }
  };

  const aiWorkflowData = [
    {
      title: "Research Synthesis",
      action: "Structuring raw qualitative data",
      desc: "Distilling user interviews, domain briefs, and compliance standards into clear behavioral matrices using tailored AI contexts.",
      promptExample: "Analyze raw interview transcripts of regional cab drivers to extract friction patterns around direct sunlight glare and booking interface density.",
      outputMock: "Synthesized 3 core design priorities: 1. Target tap size increase of 24%. 2. High contrast fallback color-mapping. 3. Immediate single-tap audio status feedback."
    },
    {
      title: "User Flow Generation",
      action: "Mapping logical paths",
      desc: "Drafting user specifications and checking for critical edge cases before high-fidelity visual production begins.",
      promptExample: "Generate state-machine rules for a B2B platform when a user has partial document validation and sudden offline network sync dropouts.",
      outputMock: "Defined system states: 1. Render draft flag on localized file buffer. 2. Display persistent recovery banner with clear actions. 3. Auto-queue background checks upon reconnect."
    },
    {
      title: "Wireframe Ideation",
      action: "Rapid structural variations",
      desc: "Generating dynamic interface layout options, structural grids, and functional wireframe elements for complex dash panel suites.",
      promptExample: "Propose structured components for managing multi-source ROC compliance timelines across multi-entity management grids.",
      outputMock: "Proposed Layouts: 1. Segmented timeline navigation tree. 2. Expandable multi-entity grid drawer. 3. Priority card grouping system for critical alert states."
    },
    {
      title: "UX Writing",
      action: "Contextual microcopy draft",
      desc: "Balancing authoritative clarity and professional messaging for error messages, empty-states, and high-frequency UI alerts.",
      promptExample: "Draft precise microcopy warning B2B users of a missing company director identifier without sounding punitive.",
      outputMock: "'Compliance update required. To secure your ROC documentation grid, please verify the 8-digit Director Identification Number (DIN).'"
    },
    {
      title: "Rapid Iteration",
      action: "Optimizing viewport structures",
      desc: "Testing different layout scales, navigational hierarchies, and column metrics to maximize readability on both mobile and desktop views.",
      promptExample: "Review design patterns for standard dashboard viewports to maximize data layout density.",
      outputMock: "Recommended optimization: Swap secondary menu parameters to an interactive vertical collapsible dock, liberating 15% workspace width."
    }
  ];

  const activeProjectData = CASE_STUDIES.find(cs => cs.id === activeCaseStudyId);

  return (
    <div className="min-h-screen bg-[#0F1115] text-white font-sans selection:bg-[#4F8CFF] selection:text-white overflow-x-hidden antialiased">
      
      {/* Navigation */}
      <nav className="sticky top-0 z-40 bg-[#0F1115]/85 backdrop-blur-md border-b border-[#161A22] transition-colors duration-300">
        <div className="max-w-[1200px] mx-auto px-6 h-16 flex items-center justify-between">
          <div className="flex items-center gap-3">
            <span className="w-8 h-8 rounded-lg bg-gradient-to-br from-[#4F8CFF] to-[#8B5CF6] flex items-center justify-center font-bold text-white shadow-lg shadow-[#4F8CFF]/15 text-xs">
              HS
            </span>
            <div>
              <span className="font-semibold block text-sm tracking-tight text-white leading-none">Huzaifa Salim</span>
              <span className="text-[10px] text-[#B3B8C5] mt-1 block">UI/UX &amp; Product Designer</span>
            </div>
          </div>
          
          <div className="hidden md:flex items-center gap-8 text-sm font-medium text-[#B3B8C5]">
            <button onClick={() => scrollToSection('about')} className="hover:text-white transition-colors relative py-2 group">
              About &amp; Journey
              <span className="absolute bottom-0 left-0 w-full h-[1px] bg-[#4F8CFF] scale-x-0 group-hover:scale-x-100 transition-transform origin-left duration-200" />
            </button>
            <button onClick={() => scrollToSection('work')} className="hover:text-white transition-colors relative py-2 group">
              Featured Work
              <span className="absolute bottom-0 left-0 w-full h-[1px] bg-[#4F8CFF] scale-x-0 group-hover:scale-x-100 transition-transform origin-left duration-200" />
            </button>
            <button onClick={() => scrollToSection('experience')} className="hover:text-white transition-colors relative py-2 group">
              Experience
              <span className="absolute bottom-0 left-0 w-full h-[1px] bg-[#4F8CFF] scale-x-0 group-hover:scale-x-100 transition-transform origin-left duration-200" />
            </button>
            <button onClick={() => scrollToSection('ai-workflow')} className="hover:text-white transition-colors relative py-2 group">
              AI Workflow
              <span className="absolute bottom-0 left-0 w-full h-[1px] bg-[#4F8CFF] scale-x-0 group-hover:scale-x-100 transition-transform origin-left duration-200" />
            </button>
            <button onClick={() => scrollToSection('skills')} className="hover:text-white transition-colors relative py-2 group">
              Skills
              <span className="absolute bottom-0 left-0 w-full h-[1px] bg-[#4F8CFF] scale-x-0 group-hover:scale-x-100 transition-transform origin-left duration-200" />
            </button>
          </div>

          <div>
            <button 
              onClick={() => scrollToSection('contact')}
              className="px-4 py-2 text-xs font-semibold bg-[#161A22] border border-[#161A22] hover:border-[#4F8CFF]/50 rounded-lg text-white transition-all shadow-sm"
            >
              Let's Talk
            </button>
          </div>
        </div>
      </nav>

      {/* Hero Section */}
      <section className="relative min-h-[calc(100vh-64px)] flex items-center max-w-[1200px] mx-auto px-6 py-12 z-10">
        <div className="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center w-full">
          
          <div className="lg:col-span-7 space-y-8">
            <div className="inline-flex items-center gap-2 px-3 py-1.5 rounded-full bg-[#161A22] border border-[#161A22] text-[11px] text-[#B3B8C5] tracking-wide font-medium">
              <span className="w-1.5 h-1.5 rounded-full bg-[#4F8CFF] animate-pulse"></span>
              Open to Remote Roles &amp; High-Impact Product Contracts
            </div>

            <div className="space-y-4">
              <h1 className="text-4xl sm:text-7xl font-bold tracking-tight text-white leading-none font-display">
                Huzaifa Salim
              </h1>
              <h2 className="text-xl sm:text-2xl font-semibold text-[#4F8CFF]">
                UI/UX Designer | Product Thinker | AI-Native Designer
              </h2>
            </div>

            <p className="text-lg sm:text-xl text-[#B3B8C5] leading-relaxed max-w-xl font-normal">
              Designing end-to-end digital products—from apps and websites to dashboards, admin panels, and scalable design systems.
            </p>

            <div className="flex flex-wrap items-center gap-4 pt-4">
              <button 
                onClick={() => scrollToSection('work')}
                className="px-6 py-3.5 bg-[#4F8CFF] hover:bg-[#4F8CFF]/90 text-white rounded-lg text-sm font-semibold transition-all inline-flex items-center gap-2 group shadow-lg shadow-[#4F8CFF]/20"
              >
                View Work
                <ArrowRight className="w-4 h-4 group-hover:translate-x-1 transition-transform" />
              </button>
              <button 
                onClick={copyEmail}
                className="px-6 py-3.5 bg-[#161A22] hover:bg-[#161A22]/80 border border-[#161A22] text-white rounded-lg text-sm font-semibold transition-all inline-flex items-center gap-2 shadow-sm"
              >
                <FileText className="w-4 h-4 text-[#4F8CFF]" />
                {copied ? 'Email Copied' : 'Download Resume'}
              </button>
              <button 
                onClick={() => scrollToSection('contact')}
                className="px-6 py-3.5 text-sm font-semibold text-white border-b border-transparent hover:border-white transition-all"
              >
                Let’s Talk
              </button>
            </div>
          </div>

          {/* Core framework system visual blueprint representation */}
          <div className="lg:col-span-5 relative hidden lg:block">
            <div className="absolute inset-0 bg-gradient-to-tr from-[#4F8CFF]/5 to-[#8B5CF6]/5 rounded-2xl filter blur-3xl pointer-events-none" />
            <div className="relative bg-[#161A22] border border-[#161A22] rounded-2xl overflow-hidden shadow-2xl p-6 aspect-[4/5] flex flex-col justify-between">
              <div className="flex justify-between items-center text-[10px] text-[#B3B8C5] font-mono tracking-widest uppercase">
                <span>SYSTEM FRAMEWORK ACTIVE</span>
                <span>FIGMA // FRONTEND</span>
              </div>
              
              <div className="flex-1 flex items-center justify-center relative">
                <svg className="w-full h-full max-h-64 opacity-85" viewBox="0 0 200 200" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M10 10H190V190H10V10Z" stroke="#252B37" strokeWidth="1" strokeDasharray="3 3"/>
                  <line x1="100" y1="10" x2="100" y2="190" stroke="#252B37" strokeWidth="1" strokeDasharray="5 5"/>
                  <line x1="10" y1="100" x2="190" y2="100" stroke="#252B37" strokeWidth="1" strokeDasharray="5 5"/>
                  
                  {/* Styled design interface skeleton */}
                  <rect x="30" y="30" width="140" height="140" rx="8" stroke="#252B37" strokeWidth="1.5" />
                  
                  {/* Grid system visualization components */}
                  <rect x="42" y="45" width="52" height="65" rx="4" fill="#0F1115" stroke="#4F8CFF" strokeWidth="1" />
                  <rect x="106" y="45" width="52" height="65" rx="4" fill="#0F1115" stroke="#252B37" strokeWidth="1" />
                  
                  <line x1="42" y1="125" x2="158" y2="125" stroke="#4F8CFF" strokeWidth="1.5" />
                  <line x1="42" y1="135" x2="110" y2="135" stroke="#252B37" strokeWidth="1.5" />
                  <line x1="42" y1="145" x2="135" y2="145" stroke="#252B37" strokeWidth="13" strokeDasharray="2 2" />
                  
                  <circle cx="150" cy="125" r="3" fill="#8B5CF6"/>
                  <circle cx="106" cy="77" r="3" fill="#4F8CFF"/>
                </svg>
              </div>

              <div className="space-y-1.5 border-t border-[#252B37] pt-4 text-center">
                <p className="text-xs font-semibold text-white">WORKSPACE PREVIEW // 2026</p>
                <p className="text-[10px] text-[#B3B8C5] font-mono leading-none">Designed with mathematical balance, high contrast &amp; scalability</p>
              </div>
            </div>
          </div>

        </div>
      </section>

      {/* About & Narrative Section */}
      <section id="about" className="py-[120px] max-w-[1200px] mx-auto px-6 border-t border-[#161A22] z-10">
        <div className="grid grid-cols-1 lg:grid-cols-12 gap-8 items-start">
          <div className="lg:col-span-4">
            <h3 className="text-sm font-semibold tracking-widest text-[#4F8CFF] uppercase">The Profile</h3>
          </div>
          <div className="lg:col-span-8 space-y-6">
            <p className="text-2xl sm:text-3xl font-medium text-white leading-normal tracking-tight">
              Experienced UI/UX Designer with around three years of hands-on work creating user-friendly digital interfaces. Skilled in designing web and mobile products with a user-first approach, from startups to large-scale solutions.
            </p>
            <p className="text-md text-[#B3B8C5] leading-relaxed max-w-2xl font-light">
              Transitioned with an analytical mindset to solve complex product problems. Uses AI-assisted workflows for rapid research synthesis and spec drafting, while building lightweight prototypes to speed up iteration and stay close to implementation.
            </p>
            
            <div className="grid grid-cols-2 sm:grid-cols-4 gap-6 pt-8 border-t border-[#161A22]">
              <div>
                <span className="block text-3xl font-bold text-white tracking-tight">3+ Years</span>
                <span className="text-xs text-[#B3B8C5] uppercase tracking-wider block mt-1">Design Track Record</span>
              </div>
              <div>
                <span className="block text-3xl font-bold text-white tracking-tight">IIT Guwahati</span>
                <span className="text-xs text-[#B3B8C5] uppercase tracking-wider block mt-1">UX Design Strategy</span>
              </div>
              <div>
                <span className="block text-3xl font-bold text-white tracking-tight">Kolkata</span>
                <span className="text-xs text-[#B3B8C5] uppercase tracking-wider block mt-1">Based in India</span>
              </div>
              <div>
                <span className="block text-3xl font-bold text-white tracking-tight">English / Native</span>
                <span className="text-xs text-[#B3B8C5] uppercase tracking-wider block mt-1">Languages Verified</span>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* Featured Work Grid Section */}
      <section id="work" className="py-[120px] max-w-[1200px] mx-auto px-6 border-t border-[#161A22] z-10">
        <div className="flex flex-col md:flex-row md:items-end justify-between mb-16 gap-4">
          <div className="space-y-4">
            <h3 className="text-sm font-semibold tracking-widest text-[#4F8CFF] uppercase">Selected Products</h3>
            <h2 className="text-3xl sm:text-5xl font-bold text-white tracking-tight">
              End-to-End Workflows
            </h2>
          </div>
          <div className="text-[#B3B8C5] text-sm max-w-xs md:text-right font-medium">
            Select an active project below to populate the interactive Case Study Spotlight view.
          </div>
        </div>

        <div className="grid grid-cols-1 lg:grid-cols-3 gap-8">
          {CASE_STUDIES.map((project) => (
            <div 
              key={project.id}
              onClick={() => {
                setActiveCaseStudyId(project.id);
                scrollToSection('case-study-spotlight');
              }}
              className={`group cursor-pointer rounded-xl bg-[#161A22] border transition-all duration-300 overflow-hidden flex flex-col justify-between h-full hover:-translate-y-1 ${activeCaseStudyId === project.id ? 'border-[#4F8CFF] shadow-lg shadow-[#4F8CFF]/5' : 'border-[#161A22] hover:border-[#252B37]'}`}
            >
              <div className="p-6 space-y-4">
                <div className="flex items-center justify-between">
                  <span className="text-[10px] uppercase tracking-wider text-[#4F8CFF] font-semibold">{project.category}</span>
                  <span className="text-[10px] font-mono text-[#B3B8C5]">{project.id === 'lyftindia' ? 'Kolkata, IN' : 'Remote'}</span>
                </div>
                <h4 className="text-xl font-bold text-white group-hover:text-[#4F8CFF] transition-colors flex items-center justify-between">
                  {project.title}
                  <ArrowUpRight className="w-4 h-4 opacity-0 group-hover:opacity-100 transition-opacity" />
                </h4>
                <p className="text-sm text-[#B3B8C5] leading-relaxed line-clamp-3">
                  {project.summary}
                </p>
              </div>

              {/* Graphical wireframe/preview layout block */}
              <div className="h-44 bg-[#0F1115] border-t border-[#252B37] relative overflow-hidden p-4 flex items-end justify-center">
                {project.id === 'fairdrive' ? (
                  <div className="w-full h-full flex flex-col justify-between text-[10px] font-mono text-[#B3B8C5]">
                    <div className="flex justify-between items-center border-b border-[#161A22] pb-1">
                      <span>CUSTOMER_DRIVER_FLOW</span>
                      <span className="text-emerald-500 flex items-center gap-1">
                        <span className="w-1.5 h-1.5 bg-emerald-500 rounded-full animate-pulse" /> LIVE_DISPATCH
                      </span>
                    </div>
                    <div className="flex-1 flex items-center justify-center relative">
                      <svg className="w-full h-24 opacity-65" viewBox="0 0 200 80" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M15 65 Q 100 15, 185 65" stroke="#4F8CFF" strokeWidth="1.5" strokeDasharray="3 3" />
                        <rect x="8" y="58" width="14" height="14" rx="2" fill="#161A22" stroke="#4F8CFF" />
                        <rect x="178" y="58" width="14" height="14" rx="2" fill="#161A22" stroke="#4F8CFF" />
                        <circle cx="100" cy="40" r="4" fill="#8B5CF6" />
                        <text x="82" y="25" fill="#FFFFFF" fontSize="5">MOBILE_API_SYNC</text>
                      </svg>
                    </div>
                  </div>
                ) : project.id === 'filesure' ? (
                  <div className="w-full h-full flex flex-col justify-between text-[10px] font-mono text-[#B3B8C5]">
                    <div className="flex justify-between items-center border-b border-[#161A22] pb-1">
                      <span>COMPLIANCE_ROUTER</span>
                      <span>SECURE_DATA</span>
                    </div>
                    <div className="flex-1 flex items-center gap-2 px-2 pt-2">
                      <div className="flex-1 bg-[#161A22] border border-[#252B37] rounded p-2 h-16 flex flex-col justify-between">
                        <span className="text-[8px] text-[#B3B8C5]">MCA_SYNC</span>
                        <span className="text-xs font-bold text-[#4F8CFF]">COMPLIANT</span>
                      </div>
                      <div className="flex-1 bg-[#161A22] border border-[#252B37] rounded p-2 h-16 flex flex-col justify-between">
                        <span className="text-[8px] text-[#B3B8C5]">ROC_AUDIT</span>
                        <span className="text-xs font-bold text-[#8B5CF6]">99.8% VERIFIED</span>
                      </div>
                    </div>
                  </div>
                ) : (
                  <div className="w-full h-full flex flex-col justify-between text-[10px] font-mono text-[#B3B8C5]">
                    <div className="flex justify-between items-center border-b border-[#161A22] pb-1">
                      <span>LYFT_INDIA_PORTAL</span>
                      <span>BIKE_TAXES</span>
                    </div>
                    <div className="flex-1 flex items-center justify-center gap-4">
                      <div className="p-2 border border-[#4F8CFF] bg-[#4F8CFF]/10 text-white rounded text-[8px]">
                        RIDE_BOOKING_FLOW
                      </div>
                      <div className="p-2 border border-[#252B37] rounded text-[8px]">
                        PLAY_STORE_ASSET
                      </div>
                    </div>
                  </div>
                )}
              </div>

              <div className="p-6 border-t border-[#161A22] flex justify-between items-center text-xs font-mono text-[#B3B8C5]">
                <span className="truncate max-w-[200px]">Role: {project.role.split(' ')[0]} {project.role.split(' ')[1]}</span>
                <span className="text-[#4F8CFF] group-hover:underline flex items-center gap-1 shrink-0">
                  Select <ChevronRight className="w-3.5 h-3.5" />
                </span>
              </div>
            </div>
          ))}
        </div>
      </section>

      {/* Case Study spotlight walkthrough section */}
      <section id="case-study-spotlight" className="py-[120px] max-w-[1200px] mx-auto px-6 border-t border-[#161A22] z-10 scroll-mt-16">
        <div className="mb-12 space-y-4">
          <h3 className="text-sm font-semibold tracking-widest text-[#4F8CFF] uppercase">Active Case Study Spotlight</h3>
          <h2 className="text-3xl sm:text-4xl font-bold text-white tracking-tight">
            {activeProjectData.title} Workflow &amp; Outcomes
          </h2>
          <p className="text-lg text-[#B3B8C5] max-w-2xl">
            {activeProjectData.tagline} — Rooted in analytical thinking &amp; scalable B2B principles.
          </p>
        </div>

        <div className="grid grid-cols-1 lg:grid-cols-12 gap-12 items-stretch mt-12">
          
          {/* Detailed timeline and workflow insights */}
          <div className="lg:col-span-5 space-y-12 flex flex-col justify-between">
            <div className="space-y-8">
              
              <div className="relative pl-8 border-l border-[#252B37] space-y-2">
                <div className="absolute top-1 left-0 -translate-x-1/2 w-2 h-2 rounded-full bg-[#4F8CFF]" />
                <span className="text-xs uppercase font-mono tracking-widest text-[#4F8CFF]">01 / Context &amp; Problem</span>
                <h4 className="text-lg font-bold text-white">The Structural Challenge</h4>
                <p className="text-[#B3B8C5] text-sm leading-relaxed">{activeProjectData.problem}</p>
              </div>

              <div className="relative pl-8 border-l border-[#252B37] space-y-2">
                <div className="absolute top-1 left-0 -translate-x-1/2 w-2 h-2 rounded-full bg-[#8B5CF6]" />
                <span className="text-xs uppercase font-mono tracking-widest text-[#8B5CF6]">02 / Design Strategy</span>
                <h4 className="text-lg font-bold text-white">Execution Process</h4>
                <p className="text-[#B3B8C5] text-sm leading-relaxed">{activeProjectData.process}</p>
              </div>

              <div className="relative pl-8 border-l border-[#252B37] space-y-2">
                <div className="absolute top-1 left-0 -translate-x-1/2 w-2 h-2 rounded-full bg-emerald-500" />
                <span className="text-xs uppercase font-mono tracking-widest text-emerald-500">03 / Platform Outcomes</span>
                <h4 className="text-lg font-bold text-white">Impact &amp; Results</h4>
                <p className="text-[#B3B8C5] text-sm leading-relaxed">{activeProjectData.outcome}</p>
              </div>

            </div>

            <button
              onClick={() => setSelectedCaseStudy(activeProjectData)}
              className="w-full py-4 bg-[#161A22] hover:bg-[#161A22]/80 border border-[#252B37] hover:border-[#4F8CFF] text-white rounded-lg text-sm font-semibold transition-all inline-flex items-center justify-center gap-2"
            >
              Open Detailed Structural Flow Sheet
              <ArrowUpRight className="w-4 h-4" />
            </button>
          </div>

          {/* Interactive display render of mockup stages */}
          <div className="lg:col-span-7 bg-[#161A22] border border-[#161A22] rounded-xl p-6 flex flex-col justify-between">
            <div className="flex justify-between items-center text-xs font-mono text-[#B3B8C5] border-b border-[#252B37] pb-4 mb-6">
              <span>DESIGN_LOGIC: {activeProjectData.id.toUpperCase()}</span>
              <span>VERIFIED METRICS</span>
            </div>

            <div className="space-y-6 flex-1 flex flex-col justify-center">
              {activeProjectData.alternatingViews.map((view, index) => (
                <div key={index} className="grid grid-cols-1 md:grid-cols-12 gap-6 items-center p-4 rounded-lg bg-[#0F1115] border border-[#161A22]">
                  <div className="md:col-span-5 space-y-1">
                    <span className="text-[10px] font-mono text-[#4F8CFF] uppercase font-bold tracking-widest">Phase 0{index+1}</span>
                    <h5 className="text-sm font-bold text-white">{view.title}</h5>
                    <p className="text-xs text-[#B3B8C5] leading-relaxed">{view.desc}</p>
                  </div>
                  
                  <div className="md:col-span-7 h-24 bg-[#161A22] border border-[#252B37] rounded-lg p-3 flex items-center justify-center overflow-hidden">
                    {view.visualType === "flow" ? (
                      <div className="w-full flex items-center justify-around text-[9px] font-mono text-[#B3B8C5]">
                        <div className="p-1.5 border border-[#4F8CFF] rounded text-white bg-[#0F1115]">USER_INIT</div>
                        <ChevronRight className="w-4 h-4 text-[#B3B8C5]" />
                        <div className="p-1.5 border border-[#8B5CF6] rounded text-white bg-[#0F1115]">DATA_ROUTE</div>
                        <ChevronRight className="w-4 h-4 text-[#B3B8C5]" />
                        <div className="p-1.5 border border-[#252B37] rounded">RESOLVED_VIEW</div>
                      </div>
                    ) : view.visualType === "wireframe" ? (
                      <div className="w-full h-full border border-dashed border-[#252B37] rounded p-2 flex flex-col justify-between">
                        <div className="h-1.5 bg-[#252B37] rounded w-1/3" />
                        <div className="grid grid-cols-3 gap-2">
                          <div className="h-5 border border-[#252B37] bg-[#0F1115] rounded flex items-center justify-center text-[7px] text-[#B3B8C5]">GRID_1</div>
                          <div className="h-5 border border-[#252B37] bg-[#0F1115] rounded flex items-center justify-center text-[7px] text-[#B3B8C5]">GRID_2</div>
                          <div className="h-5 border border-[#4F8CFF] bg-[#4F8CFF]/5 rounded flex items-center justify-center text-[7px] text-[#4F8CFF]">CTA_PROMPT</div>
                        </div>
                      </div>
                    ) : (
                      <div className="w-full h-full flex flex-col justify-between text-[9px] font-mono">
                        <div className="flex justify-between text-white border-b border-[#252B37] pb-1">
                          <span>SYSTEM_KPI</span>
                          <span className="text-[#4F8CFF]">ACTIVE RUNTIME</span>
                        </div>
                        <div className="flex gap-2 items-center flex-1 pt-1.5">
                          <div className="w-2.5 h-2.5 rounded-full bg-[#4F8CFF]" />
                          <div className="flex-1 h-1 bg-[#161A22] rounded overflow-hidden">
                            <div className="w-[85%] h-full bg-[#4F8CFF]" />
                          </div>
                          <span className="text-[#B3B8C5]">99.8% Reliability</span>
                        </div>
                      </div>
                    )}
                  </div>
                </div>
              ))}
            </div>

            <div className="grid grid-cols-3 gap-4 border-t border-[#252B37] pt-4 mt-6">
              {activeProjectData.metrics.map((metric, index) => (
                <div key={index} className="text-center p-2 rounded bg-[#0F1115] border border-[#161A22]">
                  <span className="block text-md sm:text-lg font-bold text-[#4F8CFF] font-mono">{metric.value}</span>
                  <span className="text-[9px] text-[#B3B8C5] uppercase tracking-wider block mt-0.5">{metric.label}</span>
                </div>
              ))}
            </div>
          </div>

        </div>
      </section>

      {/* Recruiter-Friendly Career Timeline Section */}
      <section id="experience" className="py-[120px] max-w-[1200px] mx-auto px-6 border-t border-[#161A22] z-10">
        <div className="grid grid-cols-1 lg:grid-cols-12 gap-12">
          
          <div className="lg:col-span-4 space-y-4">
            <h3 className="text-sm font-semibold tracking-widest text-[#4F8CFF] uppercase">The Trajectory</h3>
            <h2 className="text-3xl sm:text-4xl font-bold text-white tracking-tight">Work History</h2>
            <p className="text-sm text-[#B3B8C5] leading-relaxed">
              Three years of cross-functional experience across remote B2B spaces and on-site regional tech hubs.
            </p>
          </div>

          <div className="lg:col-span-8 space-y-6">
            {WORK_EXPERIENCE.map((job, idx) => (
              <div key={idx} className="bg-[#161A22] border border-[#161A22] hover:border-[#252B37] transition-all p-6 rounded-xl flex flex-col md:flex-row justify-between gap-4">
                <div className="space-y-2">
                  <span className="text-xs uppercase font-mono text-[#4F8CFF] font-semibold tracking-wider block">{job.period}</span>
                  <h4 className="text-lg font-bold text-white">{job.role}</h4>
                  <p className="text-sm text-[#B3B8C5]">{job.desc}</p>
                </div>
                <div className="md:text-right flex flex-col justify-start md:items-end gap-1 shrink-0">
                  <span className="text-sm font-semibold text-white flex items-center gap-1.5">
                    <Briefcase className="w-3.5 h-3.5 text-[#B3B8C5]" />
                    {job.company}
                  </span>
                  <span className="text-xs text-[#B3B8C5] flex items-center gap-1.5">
                    <MapPin className="w-3.5 h-3.5 text-[#B3B8C5]" />
                    {job.location}
                  </span>
                </div>
              </div>
            ))}
          </div>

        </div>
      </section>

      {/* How I use AI in Design Section */}
      <section id="ai-workflow" className="py-[120px] max-w-[1200px] mx-auto px-6 border-t border-[#161A22] z-10">
        <div className="text-center max-w-2xl mx-auto space-y-4 mb-16">
          <h3 className="text-sm font-semibold tracking-widest text-[#4F8CFF] uppercase">Operational Efficiency</h3>
          <h2 className="text-3xl sm:text-5xl font-bold text-white tracking-tight">AI-Assisted Workflows</h2>
          <p className="text-lg text-[#B3B8C5] leading-relaxed">
            Leveraging AI prompts to dramatically optimize qualitative processing, logical flows, microcopy curation, and edge case coverage.
          </p>
        </div>

        {/* Prompt workflow simulator layout */}
        <div className="grid grid-cols-1 lg:grid-cols-12 gap-8 items-stretch">
          
          <div className="lg:col-span-4 flex flex-row lg:flex-col overflow-x-auto lg:overflow-visible gap-2 pb-4 lg:pb-0 scrollbar-hide">
            {aiWorkflowData.map((step, idx) => (
              <button
                key={idx}
                onClick={() => setAiWorkflowStep(idx)}
                className={`w-full text-left p-4 rounded-lg border transition-all flex flex-col gap-1 min-w-[200px] lg:min-w-0 ${aiWorkflowStep === idx ? 'bg-[#161A22] border-[#4F8CFF] text-white shadow-md' : 'bg-[#161A22]/40 border-[#161A22] hover:border-[#252B37] text-[#B3B8C5]'}`}
              >
                <div className="flex items-center justify-between">
                  <span className="text-[10px] font-mono uppercase tracking-wider text-[#B3B8C5]">Phase 0{idx+1}</span>
                  {aiWorkflowStep === idx && <Sparkles className="w-3.5 h-3.5 text-[#4F8CFF] animate-pulse" />}
                </div>
                <span className="text-sm font-bold block text-white">{step.title}</span>
                <span className="text-[11px] opacity-80 line-clamp-1">{step.action}</span>
              </button>
            ))}
          </div>

          <div className="lg:col-span-8 bg-[#161A22] border border-[#161A22] rounded-xl overflow-hidden flex flex-col justify-between shadow-xl min-h-[360px]">
            <div className="px-5 py-3.5 bg-[#0F1115] border-b border-[#252B37] flex items-center justify-between">
              <div className="flex items-center gap-2">
                <Cpu className="w-4 h-4 text-[#4F8CFF]" />
                <span className="text-xs font-mono text-[#B3B8C5]">huzaifa_workflow_agent.sh</span>
              </div>
              <span className="text-[10px] bg-[#161A22] border border-[#252B37] px-2.5 py-0.5 rounded-full text-[#4F8CFF] font-mono">WORKSPACE_ACTIVE</span>
            </div>

            <div className="p-6 space-y-6 flex-1 text-xs sm:text-sm font-mono text-[#B3B8C5]">
              <div className="space-y-1">
                <p className="text-[#B3B8C5] uppercase text-[10px] font-bold tracking-widest flex items-center gap-1.5">
                  <span>$</span> AI Prompt System Input
                </p>
                <div className="bg-[#0F1115] border border-[#252B37] p-3 rounded-md text-white">
                  "{aiWorkflowData[aiWorkflowStep].promptExample}"
                </div>
              </div>

              <div className="space-y-1">
                <p className="text-[#4F8CFF] uppercase text-[10px] font-bold tracking-widest flex items-center gap-1.5">
                  <Check className="w-3.5 h-3.5" /> Generated Spec Output
                </p>
                <div className="bg-[#0F1115] border border-[#252B37] p-4 rounded-md text-[#B3B8C5] leading-relaxed">
                  {aiWorkflowData[aiWorkflowStep].outputMock}
                </div>
              </div>
            </div>

            <div className="p-4 bg-[#0F1115] border-t border-[#252B37] text-xs font-mono text-center text-[#B3B8C5]">
              "{aiWorkflowData[aiWorkflowStep].desc}"
            </div>
          </div>

        </div>

        <div className="mt-16 text-center border-t border-[#161A22] pt-12">
          <p className="text-xl sm:text-2xl font-medium text-white italic max-w-2xl mx-auto">
            “AI amplifies my speed and creativity—not my thinking.”
          </p>
        </div>
      </section>

      {/* Software & Tool stack section */}
      <section className="py-[120px] max-w-[1200px] mx-auto px-6 border-t border-[#161A22] z-10">
        <div className="space-y-8 text-center max-w-xl mx-auto">
          <h3 className="text-sm font-semibold tracking-widest text-[#4F8CFF] uppercase">The Toolkit</h3>
          <h2 className="text-3xl font-bold text-white tracking-tight">Software &amp; Frameworks</h2>
          <p className="text-sm text-[#B3B8C5]">
            Bridging the gap between conceptual high-fidelity design layouts and scalable codebase handoffs.
          </p>
        </div>

        <div className="flex flex-wrap justify-center items-center gap-4 mt-12 max-w-3xl mx-auto">
          {['Figma', 'Miro', 'AI', 'VS Code', 'Framer', 'Illustrator', 'Photoshop', 'After Effects'].map((tool, idx) => (
            <div 
              key={idx}
              className="px-6 py-3 bg-[#161A22] border border-[#161A22] hover:border-[#4F8CFF]/40 text-white rounded-full text-sm font-semibold transition-all duration-300 shadow-sm"
            >
              {tool}
            </div>
          ))}
        </div>
      </section>

      {/* Skills & Expertise Section */}
      <section id="skills" className="py-[120px] max-w-[1200px] mx-auto px-6 border-t border-[#161A22] z-10">
        <div className="grid grid-cols-1 lg:grid-cols-12 gap-12">
          
          <div className="lg:col-span-4 space-y-4">
            <h3 className="text-sm font-semibold tracking-widest text-[#4F8CFF] uppercase">Skillset Matrix</h3>
            <h2 className="text-3xl font-bold text-white tracking-tight">Core Competencies</h2>
            <p className="text-sm text-[#B3B8C5] leading-relaxed">
              Robust capabilities spanning high-fidelity interface systems, operational logic paths, and digital brand development.
            </p>
          </div>

          <div className="lg:col-span-8 grid grid-cols-1 sm:grid-cols-2 gap-8">
            
            {/* Core Skills block */}
            <div className="bg-[#161A22] border border-[#161A22] rounded-xl p-6 space-y-4">
              <h4 className="text-md font-bold text-white border-b border-[#252B37] pb-3 uppercase tracking-wider text-xs">Core Skills</h4>
              <div className="flex flex-wrap gap-2">
                {[
                  'User Experience Design', 'User Interface Design', 'Interaction Design', 
                  'Product Design', 'Web Design', 'Mobile App Design', 'HTML', 'CSS'
                ].map((skill, sIdx) => (
                  <span key={sIdx} className="px-3 py-1.5 bg-[#0F1115] border border-[#252B37] rounded-md text-xs text-[#B3B8C5]">
                    {skill}
                  </span>
                ))}
              </div>
            </div>

            {/* Soft Skills block */}
            <div className="bg-[#161A22] border border-[#161A22] rounded-xl p-6 space-y-4">
              <h4 className="text-md font-bold text-white border-b border-[#252B37] pb-3 uppercase tracking-wider text-xs">Soft Skills</h4>
              <div className="flex flex-wrap gap-2">
                {[
                  'Team Management', 'Attention to Detail', 'Collaboration', 
                  'Time Management', 'Communication', 'Problem-Solving', 'Adaptability'
                ].map((skill, sIdx) => (
                  <span key={sIdx} className="px-3 py-1.5 bg-[#0F1115] border border-[#252B37] rounded-md text-xs text-[#B3B8C5]">
                    {skill}
                  </span>
                ))}
              </div>
            </div>

          </div>

        </div>
      </section>

      {/* Contact Section */}
      <section id="contact" className="py-[120px] max-w-[1200px] mx-auto px-6 border-t border-[#161A22] text-center z-10">
        <div className="max-w-2xl mx-auto space-y-8">
          <h3 className="text-sm font-semibold tracking-widest text-[#4F8CFF] uppercase">Get In Touch</h3>
          <h2 className="text-4xl sm:text-6xl font-bold text-white tracking-tight">Let’s build something impactful.</h2>
          <p className="text-lg text-[#B3B8C5]">
            I am currently looking for remote roles or contract consulting. Feel free to reach out via email or LinkedIn.
          </p>

          <div className="flex flex-wrap items-center justify-center gap-4 pt-4">
            <button 
              onClick={copyEmail}
              className="px-6 py-3.5 bg-[#4F8CFF] hover:bg-[#4F8CFF]/90 text-white rounded-lg text-sm font-semibold transition-all inline-flex items-center gap-2 shadow-lg shadow-[#4F8CFF]/20"
            >
              <Mail className="w-4 h-4" />
              {copied ? 'Email Copied' : 'Email (huzaifalistens@gmail.com)'}
            </button>
            <a 
              href="https://www.linkedin.com/in/huzaifasalim7/" 
              target="_blank" 
              rel="noopener noreferrer"
              className="px-6 py-3.5 bg-[#161A22] hover:bg-[#161A22]/80 border border-[#161A22] text-white rounded-lg text-sm font-semibold transition-all inline-flex items-center gap-2 shadow-sm"
            >
              <Linkedin className="w-4 h-4 text-[#4F8CFF]" />
              Connect on LinkedIn
            </a>
            <a 
              href="https://wa.me/919748154954" 
              target="_blank" 
              rel="noopener noreferrer"
              className="px-6 py-3.5 bg-[#161A22]/60 hover:bg-[#161A22]/80 border border-[#252B37] text-white rounded-lg text-sm font-semibold transition-all inline-flex items-center gap-2 shadow-sm"
            >
              <Phone className="w-4 h-4 text-[#8B5CF6]" />
              WhatsApp Reach Out
            </a>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="border-t border-[#161A22] py-8 bg-[#0F1115]">
        <div className="max-w-[1200px] mx-auto px-6 flex flex-col sm:flex-row items-center justify-between gap-4 text-xs text-[#B3B8C5]">
          <div className="flex items-center gap-2">
            <span className="w-6 h-6 rounded bg-[#161A22] flex items-center justify-center font-bold text-[#4F8CFF] text-[10px]">HS</span>
            <span>&copy; {new Date().getFullYear()} Huzaifa Salim. Portfolio sync from resume standard.</span>
          </div>
          <div className="flex gap-6">
            <button onClick={() => scrollToSection('about')} className="hover:text-white transition-colors">About</button>
            <button onClick={() => scrollToSection('work')} className="hover:text-white transition-colors">Work</button>
            <button onClick={() => scrollToSection('experience')} className="hover:text-white transition-colors">Experience</button>
            <button onClick={() => scrollToSection('ai-workflow')} className="hover:text-white transition-colors">AI Workflow</button>
            <button onClick={copyEmail} className="hover:text-white transition-colors">Copy Contact</button>
          </div>
        </div>
      </footer>

      {/* Detailed Slide-out Drawer Overlay */}
      {selectedCaseStudy && (
        <div className="fixed inset-0 bg-[#0F1115]/90 z-50 flex justify-end backdrop-blur-sm transition-all duration-300">
          <div className="w-full max-w-4xl bg-[#161A22] border-l border-[#252B37] h-full overflow-y-auto flex flex-col justify-between shadow-2xl">
            
            <div className="sticky top-0 bg-[#161A22]/95 border-b border-[#252B37] p-6 flex items-center justify-between z-20 backdrop-blur-md">
              <div>
                <span className="text-xs uppercase tracking-widest text-[#4F8CFF] font-bold">{selectedCaseStudy.category}</span>
                <h3 className="text-2xl font-bold text-white mt-1">{selectedCaseStudy.title} Project Flow Sheet</h3>
              </div>
              <button 
                onClick={() => setSelectedCaseStudy(null)}
                className="p-2.5 bg-[#0F1115] border border-[#252B37] text-[#B3B8C5] hover:text-white rounded-xl transition-all"
              >
                <X className="w-5 h-5" />
              </button>
            </div>

            <div className="p-8 max-w-3xl mx-auto space-y-12 flex-1 pb-24">
              
              <div className="p-6 rounded-xl bg-[#0F1115] border border-[#252B37] space-y-4">
                <span className="text-[10px] uppercase text-[#4F8CFF] font-mono font-bold tracking-widest block">Executive Summary</span>
                <p className="text-sm text-white leading-relaxed">{selectedCaseStudy.summary}</p>
                <div className="grid grid-cols-2 gap-4 pt-4 border-t border-[#252B37]">
                  <div>
                    <span className="text-[9px] uppercase text-[#B3B8C5] font-mono">My Design Role</span>
                    <span className="text-xs font-semibold block text-white mt-1">{selectedCaseStudy.role}</span>
                  </div>
                  <div>
                    <span className="text-[9px] uppercase text-[#B3B8C5] font-mono">Platform Ecosystem</span>
                    <span className="text-xs font-semibold block text-white mt-1">{selectedCaseStudy.category}</span>
                  </div>
                </div>
              </div>

              {/* Problem Space */}
              <div className="space-y-4">
                <h4 className="text-lg font-bold text-white flex items-center gap-2">
                  <span className="w-1.5 h-6 bg-[#4F8CFF] rounded-full block" />
                  01. Context &amp; Core Friction Points
                </h4>
                <p className="text-sm text-[#B3B8C5] leading-relaxed pl-3.5">
                  {selectedCaseStudy.problem}
                </p>
              </div>

              {/* Strategy & Processing */}
              <div className="space-y-4">
                <h4 className="text-lg font-bold text-white flex items-center gap-2">
                  <span className="w-1.5 h-6 bg-[#8B5CF6] rounded-full block" />
                  02. Iteration Strategy &amp; Architecture
                </h4>
                <p className="text-sm text-[#B3B8C5] leading-relaxed pl-3.5">
                  {selectedCaseStudy.process}
                </p>
              </div>

              {/* Wireframe blueprints mock */}
              <div className="space-y-4">
                <h4 className="text-lg font-bold text-white flex items-center gap-2">
                  <span className="w-1.5 h-6 bg-[#252B37] rounded-full block" />
                  03. Grid Schematic Analysis
                </h4>
                
                <div className="border border-[#252B37] bg-[#0F1115] rounded-xl p-6 space-y-4">
                  <div className="flex justify-between items-center text-[10px] font-mono text-[#B3B8C5]">
                    <span>WIREFRAME_VIEWPORT_ENGINE</span>
                    <span>12_COLUMN_ALIGNMENT</span>
                  </div>
                  <div className="h-40 border border-dashed border-[#252B37] rounded-lg p-4 flex flex-col justify-between relative overflow-hidden">
                    <div className="absolute inset-0 bg-[radial-gradient(#1e293b_1px,transparent_1px)] bg-[size:16px_16px] opacity-45" />
                    <div className="z-10 w-full max-w-md space-y-2.5">
                      <div className="h-2 bg-[#252B37] rounded w-1/3" />
                      <div className="h-2 bg-[#252B37] rounded w-2/3" />
                      <div className="grid grid-cols-2 gap-4 pt-2">
                        <div className="h-10 border border-[#252B37] bg-[#161A22] rounded flex items-center justify-center text-[10px] text-[#B3B8C5] font-mono">PRIMARY_PANEL</div>
                        <div className="h-10 border border-[#252B37] bg-[#161A22] rounded flex items-center justify-center text-[10px] text-[#B3B8C5] font-mono">ACTION_BUTTON</div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>

              {/* Outcomes */}
              <div className="space-y-4">
                <h4 className="text-lg font-bold text-white flex items-center gap-2">
                  <span className="w-1.5 h-6 bg-emerald-500 rounded-full block" />
                  04. Measurable System Outcomes
                </h4>
                <p className="text-sm text-[#B3B8C5] leading-relaxed pl-3.5">
                  {selectedCaseStudy.outcome}
                </p>

                <div className="grid grid-cols-3 gap-4 pt-4 pl-3.5">
                  {selectedCaseStudy.metrics.map((met, mIdx) => (
                    <div key={mIdx} className="bg-[#0F1115] border border-[#252B37] p-4 rounded-xl">
                      <span className="block text-2xl font-bold text-[#4F8CFF] font-mono">{met.value}</span>
                      <span className="text-xs text-[#B3B8C5] block mt-1">{met.label}</span>
                    </div>
                  ))}
                </div>
              </div>

            </div>

            <div className="sticky bottom-0 bg-[#161A22]/95 border-t border-[#252B37] p-6 flex justify-between items-center">
              <span className="text-xs text-[#B3B8C5]">Reviewing: {selectedCaseStudy.title}</span>
              <button
                onClick={() => setSelectedCaseStudy(null)}
                className="px-6 py-2.5 bg-[#0F1115] hover:bg-[#0F1115]/80 border border-[#252B37] text-white rounded-lg text-xs font-semibold transition-all"
              >
                Close Viewport
              </button>
            </div>

          </div>
        </div>
      )}

    </div>
  );
}
