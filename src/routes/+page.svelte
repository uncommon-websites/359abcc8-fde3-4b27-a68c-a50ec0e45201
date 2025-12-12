<script>
    import Navbar from '$lib/components/Navbar.svelte';
    import Footer from '$lib/components/Footer.svelte';
    import FeatureRow from '$lib/components/FeatureRow.svelte';
</script>

<div class="bg-[var(--color-smartplan-dark)] min-h-screen flex flex-col">
    <Navbar />

    <main class="flex-grow">
        <!-- Hero Section -->
        <section class="relative pt-32 pb-20 overflow-hidden">
            <div class="container mx-auto px-6 relative z-10">
                <div class="max-w-4xl mx-auto text-center">
                    <!-- Search/Notification Pill -->
                    <div class="inline-flex items-center gap-2 bg-white/10 backdrop-blur-sm border border-white/10 rounded-full px-4 py-1.5 mb-8">
                        <span class="w-2 h-2 rounded-full bg-[var(--color-smartplan-primary)]"></span>
                        <span class="text-white text-sm font-medium">170K+ users</span>
                        <span class="text-gray-400 text-sm">trust Smartplan</span>
                        <svg class="w-4 h-4 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path></svg>
                    </div>

                    <h1 class="text-5xl md:text-7xl font-bold text-white tracking-tight mb-6 text-balance">
                        Transform shift chaos into automated workforce magic.
                    </h1>
                    
                    <p class="text-lg md:text-xl text-gray-400 mb-10 max-w-2xl mx-auto leading-relaxed text-balance">
                        Stop wasting hours on Excel spreadsheets. Smartplan's intelligent algorithms handle shift scheduling, time tracking, and workforce management—so you can focus on running your business.
                    </p>
                    
                    <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
                        <button class="bg-white hover:bg-gray-100 text-black px-6 py-3 rounded-full font-medium transition-colors flex items-center gap-2">
                            Start Free Trial
                            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                                <path d="M5 12h14M12 5l7 7-7 7"/>
                            </svg>
                        </button>
                        <button class="bg-transparent border border-white/20 hover:bg-white/10 text-white px-6 py-3 rounded-full font-medium transition-colors flex items-center gap-2">
                            Watch Demo
                            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                                <path d="M5 12h14M12 5l7 7-7 7"/>
                            </svg>
                        </button>
                    </div>
                </div>
            </div>

            <!-- Hero Images/Cards -->
            <div class="mt-20 relative">
                <div class="flex justify-center gap-6 overflow-hidden px-6">
                    <!-- Card 1 - Schedule View -->
                    <div class="w-[350px] md:w-[450px] flex-shrink-0 rounded-xl overflow-hidden shadow-2xl border border-white/10 transform -rotate-2 mt-8">
                        <div class="bg-white p-4">
                            <div class="flex items-center justify-between mb-4">
                                <div class="text-xs font-bold text-gray-900">Week 47</div>
                                <div class="h-8 w-24 bg-teal-100 rounded text-teal-700 text-xs flex items-center justify-center font-bold">15 shifts</div>
                            </div>
                            <div class="space-y-2">
                                <div class="grid grid-cols-7 gap-1 text-[10px] text-gray-400 font-medium">
                                    <div>Mon</div><div>Tue</div><div>Wed</div><div>Thu</div><div>Fri</div><div>Sat</div><div>Sun</div>
                                </div>
                                <div class="grid grid-cols-7 gap-1">
                                    <div class="h-16 bg-blue-100 rounded border border-blue-200"></div>
                                    <div class="h-16 bg-green-100 rounded border border-green-200"></div>
                                    <div class="h-16 bg-gray-50 rounded border border-gray-100"></div>
                                    <div class="h-16 bg-purple-100 rounded border border-purple-200"></div>
                                    <div class="h-16 bg-blue-100 rounded border border-blue-200"></div>
                                    <div class="h-16 bg-orange-100 rounded border border-orange-200"></div>
                                    <div class="h-16 bg-gray-50 rounded border border-gray-100"></div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Card 2 (Center) - Employee Card -->
                    <div class="w-[350px] md:w-[450px] flex-shrink-0 rounded-xl overflow-hidden shadow-2xl border border-white/10 z-10">
                        <div class="bg-white h-full flex flex-col">
                            <div class="bg-gradient-to-br from-teal-500 to-cyan-600 p-6">
                                <div class="flex justify-between items-center">
                                    <div class="text-white font-bold">Sarah Jensen</div>
                                    <div class="h-10 w-10 bg-white/20 rounded-full flex items-center justify-center text-white font-bold text-lg">SJ</div>
                                </div>
                                <div class="text-white/80 text-sm mt-1">Barista</div>
                            </div>
                            <div class="p-6 flex-grow space-y-4">
                                <div class="flex justify-between items-center pb-3 border-b border-gray-100">
                                    <span class="text-sm text-gray-500">This week</span>
                                    <span class="text-lg font-bold text-gray-900">32.5 hrs</span>
                                </div>
                                <div class="space-y-2">
                                    <div class="flex items-center gap-2 text-sm">
                                        <div class="w-2 h-2 rounded-full bg-green-500"></div>
                                        <span class="text-gray-600">Mon 09:00 - 17:00</span>
                                    </div>
                                    <div class="flex items-center gap-2 text-sm">
                                        <div class="w-2 h-2 rounded-full bg-green-500"></div>
                                        <span class="text-gray-600">Wed 09:00 - 17:00</span>
                                    </div>
                                    <div class="flex items-center gap-2 text-sm">
                                        <div class="w-2 h-2 rounded-full bg-blue-500"></div>
                                        <span class="text-gray-600">Fri 14:00 - 22:00</span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Card 3 - Time Tracking -->
                    <div class="w-[350px] md:w-[450px] flex-shrink-0 rounded-xl overflow-hidden shadow-2xl border border-white/10 transform rotate-2 mt-8">
                        <div class="bg-white p-4">
                            <div class="flex items-center justify-between mb-4">
                                <div class="text-xs font-bold text-gray-900">Today</div>
                                <div class="h-8 w-24 bg-green-100 rounded text-green-700 text-xs flex items-center justify-center font-bold">5 active</div>
                            </div>
                            <div class="space-y-2">
                                {#each [{name: 'Emma', time: '3h 24m', color: 'green'}, {name: 'Lucas', time: '2h 15m', color: 'blue'}, {name: 'Sofia', time: '4h 02m', color: 'purple'}] as employee}
                                <div class="flex items-center justify-between p-2 bg-gray-50 rounded">
                                    <div class="flex items-center gap-2">
                                        <div class="w-8 h-8 bg-{employee.color}-200 rounded-full"></div>
                                        <span class="text-sm font-medium text-gray-900">{employee.name}</span>
                                    </div>
                                    <span class="text-sm text-gray-600">{employee.time}</span>
                                </div>
                                {/each}
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Logos Section -->
        <section class="py-12 border-y border-white/5 bg-black/20">
            <div class="container mx-auto px-6">
                <p class="text-center text-gray-400 text-sm mb-8">Trusted by retail and hospitality businesses across the Nordics</p>
                <div class="flex flex-wrap justify-center items-center gap-12 md:gap-20 opacity-50 grayscale">
                    <!-- Cafe Brand -->
                    <svg class="h-6 md:h-8 w-auto text-white" viewBox="0 0 100 30" fill="currentColor">
                        <circle cx="15" cy="15" r="8" />
                        <path d="M30,8 L50,8 L50,22 L30,22 Z M35,12 L45,12 L45,18 L35,18 Z" />
                    </svg>
                    <!-- Restaurant -->
                    <svg class="h-6 md:h-8 w-auto text-white" viewBox="0 0 100 30" fill="currentColor">
                        <path d="M15,5 L15,25 M10,5 L10,15 M20,5 L20,15 M40,5 L40,25 M35,5 L45,15 M45,5 L35,15" />
                    </svg>
                    <!-- Retail Store -->
                    <svg class="h-6 md:h-8 w-auto text-white" viewBox="0 0 100 30" fill="currentColor">
                        <rect x="10" y="10" width="30" height="15" />
                        <path d="M10,10 L25,5 L40,10" />
                    </svg>
                    <!-- Hotel -->
                    <svg class="h-6 md:h-8 w-auto text-white" viewBox="0 0 100 30" fill="currentColor">
                        <rect x="10" y="8" width="25" height="17" />
                        <rect x="15" y="12" width="4" height="4" />
                        <rect x="22" y="12" width="4" height="4" />
                        <rect x="15" y="18" width="4" height="4" />
                        <rect x="22" y="18" width="4" height="4" />
                    </svg>
                    <!-- Bar/Pub -->
                    <svg class="h-6 md:h-8 w-auto text-white" viewBox="0 0 100 30" fill="currentColor">
                        <path d="M15,8 L15,25 M12,8 L18,8 M10,12 L20,12 M12,16 L18,16" />
                        <circle cx="15" cy="20" r="3" />
                    </svg>
                </div>
            </div>
        </section>

        <!-- Smartplan Core Section -->
        <section class="py-32 relative overflow-hidden">
            <div class="container mx-auto px-6 relative z-10">
                <div class="text-center mb-24">
                    <h2 class="text-[var(--color-smartplan-primary)] font-mono text-xs tracking-[0.2em] uppercase mb-6">Smartplan Platform</h2>
                    <h3 class="text-4xl md:text-6xl font-bold text-white mb-2 tracking-tight">Intelligent workforce management.</h3>
                    <h3 class="text-4xl md:text-6xl font-bold text-gray-600 tracking-tight">Effortlessly automated.</h3>
                </div>

                <div class="grid md:grid-cols-2 gap-16 items-center max-w-6xl mx-auto">
                    <!-- Teal Card -->
                    <div class="bg-gradient-to-br from-teal-600 to-cyan-700 rounded-3xl p-12 aspect-[4/3] relative overflow-hidden flex items-center justify-center shadow-2xl">
                        <!-- Abstract UI Elements -->
                        <div class="relative z-10 w-full max-w-[320px]">
                            <!-- Schedule Card -->
                            <div class="bg-white/10 backdrop-blur-xl border border-white/20 rounded-2xl p-6 mb-8 shadow-xl relative overflow-hidden group hover:scale-105 transition-transform duration-500">
                                <div class="text-white/80 text-xs uppercase tracking-wider font-medium mb-4">Weekly Schedule</div>
                                <div class="grid grid-cols-7 gap-1 mb-4">
                                    {#each ['M', 'T', 'W', 'T', 'F', 'S', 'S'] as day}
                                    <div class="text-white/60 text-[10px] text-center font-medium">{day}</div>
                                    {/each}
                                </div>
                                <div class="grid grid-cols-7 gap-1">
                                    {#each [1,2,3,4,5,6,7] as i}
                                    <div class="h-8 bg-white/20 rounded"></div>
                                    {/each}
                                </div>
                                <div class="mt-4 flex items-center justify-between">
                                    <span class="text-white/60 text-xs">Total Hours</span>
                                    <span class="text-white font-bold text-lg">156.5</span>
                                </div>
                            </div>
                            
                            <!-- Floating Pills -->
                            <div class="relative">
                                <div class="absolute -left-4 top-0 bg-white text-black px-5 py-2.5 rounded-full text-sm font-semibold shadow-lg flex items-center gap-2 transform -rotate-2">
                                    <div class="w-5 h-5 rounded-full bg-teal-100 flex items-center justify-center text-teal-600">
                                        <svg class="w-3 h-3" fill="currentColor" viewBox="0 0 20 20"><path d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z"/></svg>
                                    </div>
                                    Auto-scheduling
                                </div>
                                <div class="absolute -right-4 top-12 bg-white/10 backdrop-blur-md text-white px-5 py-2.5 rounded-full text-sm font-semibold border border-white/20 flex items-center gap-2 transform rotate-2">
                                    <div class="w-5 h-5 rounded-full bg-cyan-500/30 flex items-center justify-center text-cyan-200">
                                        <svg class="w-3 h-3" fill="currentColor" viewBox="0 0 20 20"><path d="M9 6a3 3 0 11-6 0 3 3 0 016 0zM17 6a3 3 0 11-6 0 3 3 0 016 0zM12.93 17c.046-.327.07-.66.07-1a6.97 6.97 0 00-1.5-4.33A5 5 0 0119 16v1h-6.07zM6 11a5 5 0 015 5v1H1v-1a5 5 0 015-5z"/></svg>
                                    </div>
                                    Time tracking
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Text Content -->
                    <div class="space-y-8">
                        <h3 class="text-4xl md:text-5xl font-bold text-white tracking-tight">From chaos to clarity in minutes.</h3>
                        <p class="text-gray-400 text-lg leading-relaxed max-w-lg">
                            Stop juggling spreadsheets and manual processes. Smartplan's intelligent algorithms automatically optimize schedules based on availability, skills, and business needs—saving you hours every week.
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <!-- White Section -->
        <div class="bg-[#F9FAFB] text-black rounded-t-[4rem] relative z-20 mt-[-2rem] pt-32 pb-32">
            <div class="container mx-auto px-6">
                <!-- Header -->
                <div class="max-w-4xl mb-24">
                    <div class="flex items-center gap-4 mb-6">
                        <div class="h-px w-12 bg-gray-300"></div>
                        <span class="text-gray-500 font-mono text-xs tracking-[0.2em] uppercase">Complete Platform</span>
                    </div>
                    <h2 class="text-4xl md:text-6xl font-bold text-gray-900 mb-2 tracking-tight">Everything you need to manage your workforce.</h2>
                    <h2 class="text-4xl md:text-6xl font-bold text-gray-400 tracking-tight mb-8">All in one place.</h2>
                    
                    <a href="#" class="inline-flex items-center gap-2 text-sm font-semibold border-b border-black pb-0.5 hover:text-gray-600 transition-colors">
                        Explore all features
                        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                            <path d="M5 12h14M12 5l7 7-7 7"/>
                        </svg>
                    </a>
                </div>

                <!-- Features Grid -->
                <div class="flex flex-col lg:flex-row gap-12">
                    <!-- Sidebar Navigation (Sticky) -->
                    <div class="hidden lg:block w-64 flex-shrink-0">
                        <div class="sticky top-32 space-y-4">
                            <div class="flex items-center gap-2 text-sm font-semibold text-black border-l-2 border-black pl-4 py-1">
                                <span class="w-1.5 h-1.5 rounded-full bg-[var(--color-smartplan-primary)]"></span>
                                Smart Scheduling
                            </div>
                            <a href="#" class="block text-sm text-gray-500 pl-4 py-1 hover:text-black border-l-2 border-transparent hover:border-gray-200 transition-colors">Time Tracking</a>
                            <a href="#" class="block text-sm text-gray-500 pl-4 py-1 hover:text-black border-l-2 border-transparent hover:border-gray-200 transition-colors">Team Communication</a>
                            <a href="#" class="block text-sm text-gray-500 pl-4 py-1 hover:text-black border-l-2 border-transparent hover:border-gray-200 transition-colors">Analytics & Reports</a>
                            <a href="#" class="block text-sm text-gray-500 pl-4 py-1 hover:text-black border-l-2 border-transparent hover:border-gray-200 transition-colors">Mobile App</a>
                            <a href="#" class="block text-sm text-gray-500 pl-4 py-1 hover:text-black border-l-2 border-transparent hover:border-gray-200 transition-colors">Payroll Integration</a>
                        </div>
                    </div>

                    <!-- Feature Cards -->
                    <div class="flex-grow space-y-8">
                        <FeatureRow 
                            title="Smart Scheduling" 
                            description="Create perfect schedules in seconds. Our intelligent algorithms consider employee availability, skills, labor costs, and business needs to generate optimal shift plans automatically."
                            icon="schedule"
                            image="schedule"
                        />
                         <FeatureRow 
                            title="Time Tracking" 
                            description="Accurate time tracking made simple. Employees clock in/out from their phones, and all hours are automatically synced with schedules for seamless payroll processing."
                            icon="clock"
                            image="clock"
                        />
                         <FeatureRow 
                            title="Team Communication" 
                            description="Keep everyone in sync. Send shift updates, announcements, and messages directly through the app. No more group texts or missed communications."
                            icon="chat"
                            image="chat"
                        />
                         <FeatureRow 
                            title="Analytics & Reports" 
                            description="Make data-driven decisions. Track labor costs, overtime, attendance patterns, and productivity metrics with real-time dashboards and automated reports."
                            icon="chart"
                            image="chart"
                        />
                         <FeatureRow 
                            title="Mobile App" 
                            description="Manage your team on the go. Both managers and employees get full-featured mobile apps for iOS and Android, making workforce management truly mobile."
                            icon="mobile"
                            image="mobile"
                        />
                         <FeatureRow 
                            title="Payroll Integration" 
                            description="Seamless payroll processing. Export timesheets directly to your payroll system or use our integrations with popular Nordic payroll providers."
                            icon="payroll"
                            image="payroll"
                        />
                    </div>
                </div>

                <!-- Industry Focus Section -->
                <div class="mt-32 text-center max-w-4xl mx-auto mb-24">
                    <div class="w-24 h-24 mx-auto bg-gradient-to-br from-teal-100 to-cyan-100 rounded-full flex items-center justify-center mb-8 relative">
                        <div class="absolute inset-0 bg-white/50 blur-xl rounded-full"></div>
                        <svg class="w-10 h-10 text-teal-600 relative z-10" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4"></path></svg>
                    </div>
                    <h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8 leading-tight">
                        Built for retail and hospitality businesses across the Nordics.
                    </h2>
                    <button class="bg-white border border-gray-200 hover:border-gray-400 text-black px-6 py-3 rounded-full font-medium transition-colors flex items-center gap-2 mx-auto">
                        See customer stories
                        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                            <path d="M5 12h14M12 5l7 7-7 7"/>
                        </svg>
                    </button>
                </div>

                <!-- Trusted By Section -->
                <div class="mb-32">
                    <p class="text-xl text-gray-500 mb-12">Trusted by retail and hospitality businesses. See how they save time with Smartplan.</p>
                    
                    <div class="grid md:grid-cols-3 gap-6">
                        <!-- Main Customer Card -->
                        <div class="md:col-span-2 bg-[#0A0A0A] rounded-3xl p-10 relative overflow-hidden group min-h-[400px] flex flex-col justify-end">
                            <div class="absolute inset-0 bg-gradient-to-t from-black via-black/50 to-transparent"></div>
                            
                            <div class="relative z-10">
                                <div class="flex items-center gap-4 mb-6">
                                    <div class="text-white font-bold text-2xl tracking-tight">Café Nordic</div>
                                    <div class="w-8 h-8 rounded-full bg-[var(--color-smartplan-primary)] flex items-center justify-center text-black font-bold">+</div>
                                    <div class="flex items-center gap-2 text-white font-semibold text-xl tracking-tight">
                                        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                            <rect x="3" y="3" width="7" height="7" rx="1" stroke="white" stroke-width="2"/>
                                            <rect x="14" y="3" width="7" height="7" rx="1" stroke="white" stroke-width="2"/>
                                            <rect x="3" y="14" width="7" height="7" rx="1" stroke="white" stroke-width="2"/>
                                            <rect x="14" y="14" width="7" height="7" rx="1" stroke="white" stroke-width="2"/>
                                        </svg>
                                        Smartplan
                                    </div>
                                </div>
                                <h3 class="text-3xl font-bold text-white mb-4 max-w-md">
                                    How Café Nordic cut scheduling time from 5 hours to 15 minutes per week
                                </h3>
                                <div class="w-10 h-10 rounded-full bg-white/10 backdrop-blur-md border border-white/20 flex items-center justify-center text-white group-hover:bg-white group-hover:text-black transition-colors">
                                    <svg class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="7" y1="17" x2="17" y2="7"></line><polyline points="7 7 17 7 17 17"></polyline></svg>
                                </div>
                            </div>
                        </div>

                        <!-- Smaller Cards -->
                        <div class="space-y-6">
                            <!-- Card 2 -->
                            <div class="bg-[#0A0A0A] rounded-3xl p-8 relative overflow-hidden group h-[240px] flex flex-col justify-between">
                                <div class="absolute inset-0 bg-gradient-to-br from-teal-900/40 to-black"></div>
                                <div class="relative z-10">
                                    <div class="text-white font-bold text-lg mb-2">Retail Chain</div>
                                    <p class="text-gray-400 text-sm">15 stores, 200+ employees</p>
                                </div>
                                <div class="relative z-10 flex justify-end">
                                    <div class="w-12 h-12 rounded-full bg-teal-400/20 blur-xl absolute -left-2 -bottom-2"></div>
                                    <div class="w-10 h-10 rounded-full bg-white/10 backdrop-blur-md border border-white/20 flex items-center justify-center text-white group-hover:bg-white group-hover:text-black transition-colors">
                                        <svg class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="7" y1="17" x2="17" y2="7"></line><polyline points="7 7 17 7 17 17"></polyline></svg>
                                    </div>
                                </div>
                            </div>
                            <!-- Card 3 -->
                            <div class="bg-[#0A0A0A] rounded-3xl p-8 relative overflow-hidden group h-[240px] flex flex-col justify-between">
                                <div class="absolute inset-0 bg-gradient-to-br from-cyan-900/40 to-black"></div>
                                <div class="relative z-10">
                                    <div class="text-white font-bold text-lg mb-2">Hotel Group</div>
                                    <p class="text-gray-400 text-sm">3 locations, 80+ staff</p>
                                </div>
                                <div class="relative z-10 flex justify-end">
                                    <div class="w-12 h-12 rounded-full bg-cyan-400/20 blur-xl absolute -left-2 -bottom-2"></div>
                                    <div class="w-10 h-10 rounded-full bg-white/10 backdrop-blur-md border border-white/20 flex items-center justify-center text-white group-hover:bg-white group-hover:text-black transition-colors">
                                        <svg class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="7" y1="17" x2="17" y2="7"></line><polyline points="7 7 17 7 17 17"></polyline></svg>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Banner -->
                <div class="bg-[#0A0A0A] rounded-3xl p-12 md:p-20 relative overflow-hidden mb-32 text-center">
                    <div class="absolute inset-0 bg-[url('/grid-pattern.svg')] opacity-10"></div>
                    <div class="absolute left-0 top-0 w-64 h-64 bg-yellow-500/10 blur-[100px] rounded-full"></div>
                    <div class="absolute right-0 bottom-0 w-64 h-64 bg-blue-500/10 blur-[100px] rounded-full"></div>
                    
                    <div class="relative z-10 max-w-3xl mx-auto">
                        <h2 class="text-4xl md:text-6xl font-bold text-white mb-6 tracking-tight">
                            Create flexible lending products. <span class="text-[var(--color-canopy-lime)]">With less work.</span>
                        </h2>
                        <p class="text-gray-400 mb-10">
                            Purpose built for developers, our modern, low-code API lets you launch fast and scale with ease.
                        </p>
                        <div class="inline-flex items-center gap-2 bg-white/10 backdrop-blur-md border border-white/10 rounded-full px-4 py-2 text-white text-sm hover:bg-white/20 transition-colors cursor-pointer">
                            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"></path></svg>
                            Canopy Docs
                            <kbd class="bg-black/30 px-1.5 py-0.5 rounded text-xs text-gray-400 font-mono">K</kbd>
                        </div>
                    </div>
                </div>

                <!-- Integrations -->
                <div class="text-center mb-32">
                    <h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4">
                        Card issuers. Payments processors.<br>
                        Credit reporting. <span class="text-gray-400">Whoever you're<br>partnered with, Canopy connects.</span>
                    </h2>
                    <button class="bg-gray-100 hover:bg-gray-200 text-black px-6 py-2 rounded-full text-sm font-medium transition-colors flex items-center gap-2 mx-auto mb-16 mt-8">
                        Explore all integrations
                        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                            <path d="M5 12h14M12 5l7 7-7 7"/>
                        </svg>
                    </button>

                    <div class="grid grid-cols-2 md:grid-cols-4 gap-px bg-gray-200 border border-gray-200 rounded-2xl overflow-hidden">
                        {#each ['checkout.com', 'dwolla', 'modern treasury', 'stripe', 'galileo', 'intercom', 'square', 'tableau'] as logo}
                        <div class="bg-[#F9FAFB] p-12 flex items-center justify-center grayscale opacity-60 hover:grayscale-0 hover:opacity-100 transition-all duration-300">
                            <span class="font-bold text-xl uppercase tracking-wider">{logo}</span>
                        </div>
                        {/each}
                    </div>
                </div>

                <!-- Blog Section -->
                <div class="mb-12">
                    <h2 class="text-4xl font-bold text-gray-900 mb-12">Learn more about next-gen lending.</h2>
                    <div class="grid md:grid-cols-2 gap-8">
                        <!-- Post 1 -->
                        <div class="group cursor-pointer">
                            <div class="bg-gradient-to-br from-gray-200 to-gray-300 rounded-3xl aspect-[16/9] mb-6 relative overflow-hidden">
                                <div class="absolute inset-0 flex items-center justify-center">
                                    <div class="grid grid-cols-6 gap-4 opacity-50">
                                        {#each Array(24) as _}
                                            <svg class="w-6 h-6 text-blue-600 transform -rotate-45" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 10l7-7m0 0l7 7m-7-7v18"></path></svg>
                                        {/each}
                                    </div>
                                </div>
                            </div>
                            <div class="text-xs font-bold text-gray-500 uppercase tracking-wider mb-2">Industry Insights</div>
                            <h3 class="text-2xl font-bold text-gray-900 group-hover:text-blue-600 transition-colors">Middle-market lending is a windfall for non-bank lenders</h3>
                        </div>
                        <!-- Post 2 -->
                        <div class="group cursor-pointer">
                            <div class="bg-gray-100 rounded-3xl aspect-[16/9] mb-6 relative overflow-hidden flex items-center justify-center">
                                <div class="flex gap-4">
                                    <div class="w-16 h-16 rounded-full bg-green-400 blur-xl opacity-80"></div>
                                    <div class="w-20 h-20 rounded-full bg-blue-400 blur-xl opacity-80"></div>
                                    <div class="w-12 h-12 rounded-full bg-purple-400 blur-xl opacity-80"></div>
                                </div>
                            </div>
                            <div class="text-xs font-bold text-gray-500 uppercase tracking-wider mb-2">Industry Insights</div>
                            <h3 class="text-2xl font-bold text-gray-900 group-hover:text-blue-600 transition-colors">The loan lifecycle: From origination to payoff</h3>
                        </div>
                    </div>
                </div>


    </main>

    <Footer />
</div>

