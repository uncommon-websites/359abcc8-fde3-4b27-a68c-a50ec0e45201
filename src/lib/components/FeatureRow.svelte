<script lang="ts">
    export let title: string;
    export let description: string;
    export let image: string;
    export let icon: string;

    // Extract the bold part of the description (first sentence)
    $: splitDesc = description.split('. ');
    $: boldDesc = splitDesc[0] + '.';
    $: restDesc = splitDesc.slice(1).join('. ');
</script>

<div class="bg-[#F3F4F6] rounded-3xl p-8 md:p-12 transition-all hover:bg-gray-200 group">
    <!-- Header -->
    <div class="flex items-center gap-3 mb-8">
        <div class="text-teal-600">
            {#if icon === 'schedule'}
                <svg class="w-6 h-6" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="4" width="18" height="18" rx="2" ry="2"></rect><line x1="16" y1="2" x2="16" y2="6"></line><line x1="8" y1="2" x2="8" y2="6"></line><line x1="3" y1="10" x2="21" y2="10"></line></svg>
            {:else if icon === 'clock'}
                <svg class="w-6 h-6" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"></circle><polyline points="12 6 12 12 16 14"></polyline></svg>
            {:else if icon === 'chat'}
                <svg class="w-6 h-6" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"></path></svg>
            {:else if icon === 'chart'}
                <svg class="w-6 h-6" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="18" y1="20" x2="18" y2="10"></line><line x1="12" y1="20" x2="12" y2="4"></line><line x1="6" y1="20" x2="6" y2="14"></line></svg>
            {:else if icon === 'mobile'}
                <svg class="w-6 h-6" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="5" y="2" width="14" height="20" rx="2" ry="2"></rect><line x1="12" y1="18" x2="12.01" y2="18"></line></svg>
            {:else if icon === 'payroll'}
                <svg class="w-6 h-6" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="12" y1="1" x2="12" y2="23"></line><path d="M17 5H9.5a3.5 3.5 0 0 0 0 7h5a3.5 3.5 0 0 1 0 7H6"></path></svg>
            {/if}
        </div>
        <h3 class="text-xl font-semibold text-gray-900">{title}</h3>
    </div>

    <!-- Image Placeholder / Abstract UI -->
    <div class="bg-white rounded-xl shadow-sm border border-gray-200 overflow-hidden mb-8 aspect-[16/9] relative group-hover:shadow-md transition-shadow">
        {#if image === 'schedule'}
            <!-- Schedule UI -->
            <div class="p-6 h-full flex flex-col">
                <div class="flex justify-between items-center mb-4 border-b border-gray-100 pb-4">
                    <div class="font-bold text-gray-800">Week 47 • November</div>
                    <div class="px-3 py-1 bg-teal-100 text-teal-700 text-xs font-medium rounded">Optimized</div>
                </div>
                <div class="space-y-2">
                    <div class="grid grid-cols-8 gap-1 text-[10px] text-gray-400 uppercase tracking-wider mb-2">
                        <span>Name</span>
                        <span>M</span>
                        <span>T</span>
                        <span>W</span>
                        <span>T</span>
                        <span>F</span>
                        <span>S</span>
                        <span>S</span>
                    </div>
                    {#each [{name: 'Emma', shifts: [1,0,1,1,0,1,0]}, {name: 'Lucas', shifts: [0,1,0,1,1,0,1]}, {name: 'Sofia', shifts: [1,1,0,0,1,1,0]}] as employee}
                    <div class="grid grid-cols-8 gap-1 items-center">
                        <div class="text-xs font-medium text-gray-900">{employee.name}</div>
                        {#each employee.shifts as shift}
                        <div class="h-6 {shift ? 'bg-teal-100 border-teal-200' : 'bg-gray-50 border-gray-100'} rounded border"></div>
                        {/each}
                    </div>
                    {/each}
                </div>
            </div>
        {:else if image === 'clock'}
            <!-- Time Tracking UI -->
            <div class="p-6 h-full flex flex-col">
                <div class="font-bold text-gray-800 mb-4 border-b border-gray-100 pb-4">Today's Activity</div>
                <div class="space-y-3">
                    {#each [{name: 'Emma Nielsen', time: '09:00 - 17:00', hours: '8h', status: 'active'}, {name: 'Lucas Hansen', time: '14:00 - 22:00', hours: '8h', status: 'active'}, {name: 'Sofia Berg', time: '09:00 - 13:30', hours: '4.5h', status: 'completed'}] as entry}
                    <div class="flex items-center justify-between p-3 bg-gray-50 rounded-lg">
                        <div class="flex items-center gap-3">
                            <div class="w-10 h-10 bg-teal-200 rounded-full flex items-center justify-center text-teal-700 font-bold text-sm">
                                {entry.name.split(' ').map(n => n[0]).join('')}
                            </div>
                            <div>
                                <div class="text-sm font-medium text-gray-900">{entry.name}</div>
                                <div class="text-xs text-gray-500">{entry.time}</div>
                            </div>
                        </div>
                        <div class="text-right">
                            <div class="text-sm font-bold text-gray-900">{entry.hours}</div>
                            <div class="text-xs {entry.status === 'active' ? 'text-green-600' : 'text-gray-500'}">{entry.status}</div>
                        </div>
                    </div>
                    {/each}
                </div>
            </div>
        {:else if image === 'chat'}
            <!-- Communication UI -->
            <div class="p-6 h-full flex flex-col bg-gray-50">
                <div class="font-bold text-gray-800 mb-4">Team Messages</div>
                <div class="space-y-3 flex-grow">
                    <div class="bg-white p-3 rounded-lg shadow-sm">
                        <div class="flex items-center gap-2 mb-2">
                            <div class="w-6 h-6 bg-teal-200 rounded-full"></div>
                            <span class="text-xs font-medium text-gray-900">Manager</span>
                            <span class="text-xs text-gray-400">10:23</span>
                        </div>
                        <p class="text-sm text-gray-700">Schedule for next week is ready! 📅</p>
                    </div>
                    <div class="bg-white p-3 rounded-lg shadow-sm">
                        <div class="flex items-center gap-2 mb-2">
                            <div class="w-6 h-6 bg-blue-200 rounded-full"></div>
                            <span class="text-xs font-medium text-gray-900">Emma</span>
                            <span class="text-xs text-gray-400">10:25</span>
                        </div>
                        <p class="text-sm text-gray-700">Thanks! Looks good 👍</p>
                    </div>
                </div>
                <div class="mt-4 flex gap-2">
                    <div class="flex-grow h-10 bg-white rounded-lg border border-gray-200"></div>
                    <div class="w-10 h-10 bg-teal-600 rounded-lg"></div>
                </div>
            </div>
        {:else if image === 'chart'}
            <!-- Analytics UI -->
            <div class="p-6 h-full bg-white">
                <div class="font-bold text-gray-800 mb-4">Labor Cost Overview</div>
                <div class="flex gap-4 mb-6">
                    <div class="flex-1 p-3 bg-gray-50 rounded-lg">
                        <div class="text-xs text-gray-400 mb-1">This Week</div>
                        <div class="text-2xl font-bold text-gray-900">$4,280</div>
                        <div class="text-xs text-green-600 mt-1">↓ 8% vs last week</div>
                    </div>
                    <div class="flex-1 p-3 bg-gray-50 rounded-lg">
                        <div class="text-xs text-gray-400 mb-1">Total Hours</div>
                        <div class="text-2xl font-bold text-gray-900">156.5</div>
                        <div class="text-xs text-gray-500 mt-1">Across 12 employees</div>
                    </div>
                </div>
                <div class="h-20 flex items-end gap-1">
                    {#each [60, 75, 55, 80, 70, 65, 85] as h}
                        <div class="flex-1 bg-teal-200 rounded-t" style="height: {h}%"></div>
                    {/each}
                </div>
                <div class="flex justify-between mt-2 text-xs text-gray-400">
                    <span>Mon</span><span>Tue</span><span>Wed</span><span>Thu</span><span>Fri</span><span>Sat</span><span>Sun</span>
                </div>
            </div>
        {:else if image === 'mobile'}
            <!-- Mobile App UI -->
            <div class="p-6 h-full flex items-center justify-center bg-gradient-to-br from-gray-50 to-gray-100">
                <div class="w-40 h-full max-h-64 bg-white rounded-3xl shadow-xl border-4 border-gray-800 overflow-hidden flex flex-col">
                    <div class="bg-teal-600 p-3 text-white">
                        <div class="text-xs font-bold">My Schedule</div>
                        <div class="text-[10px] text-teal-100">Week 47</div>
                    </div>
                    <div class="flex-grow p-3 space-y-2">
                        {#each [{day: 'Mon', time: '09-17'}, {day: 'Wed', time: '09-17'}, {day: 'Fri', time: '14-22'}] as shift}
                        <div class="bg-teal-50 rounded p-2 border border-teal-200">
                            <div class="text-xs font-medium text-gray-900">{shift.day}</div>
                            <div class="text-[10px] text-gray-600">{shift.time}</div>
                        </div>
                        {/each}
                    </div>
                    <div class="p-3 border-t border-gray-100 flex gap-2">
                        <div class="flex-1 h-8 bg-gray-100 rounded"></div>
                        <div class="flex-1 h-8 bg-teal-600 rounded"></div>
                    </div>
                </div>
            </div>
        {:else if image === 'payroll'}
            <!-- Payroll Integration UI -->
            <div class="p-6 h-full flex flex-col">
                <div class="font-bold text-gray-800 mb-4 border-b border-gray-100 pb-4">Payroll Export</div>
                <div class="space-y-3 flex-grow">
                    <div class="flex items-center justify-between p-3 bg-gray-50 rounded-lg">
                        <div>
                            <div class="text-sm font-medium text-gray-900">Emma Nielsen</div>
                            <div class="text-xs text-gray-500">40.0 hours • $20/hr</div>
                        </div>
                        <div class="text-sm font-bold text-gray-900">$800.00</div>
                    </div>
                    <div class="flex items-center justify-between p-3 bg-gray-50 rounded-lg">
                        <div>
                            <div class="text-sm font-medium text-gray-900">Lucas Hansen</div>
                            <div class="text-xs text-gray-500">38.5 hours • $22/hr</div>
                        </div>
                        <div class="text-sm font-bold text-gray-900">$847.00</div>
                    </div>
                    <div class="flex items-center justify-between p-3 bg-gray-50 rounded-lg">
                        <div>
                            <div class="text-sm font-medium text-gray-900">Sofia Berg</div>
                            <div class="text-xs text-gray-500">35.0 hours • $21/hr</div>
                        </div>
                        <div class="text-sm font-bold text-gray-900">$735.00</div>
                    </div>
                </div>
                <div class="mt-4 pt-4 border-t border-gray-200 flex justify-between items-center">
                    <span class="text-sm font-medium text-gray-600">Total</span>
                    <span class="text-lg font-bold text-gray-900">$2,382.00</span>
                </div>
            </div>
        {/if}
    </div>

    <!-- Footer -->
    <div class="flex items-end justify-between gap-4">
        <div class="max-w-xl">
            <p class="text-gray-900 text-lg leading-relaxed">
                <span class="font-bold">{boldDesc}</span> <span class="text-gray-600">{restDesc}</span>
            </p>
        </div>
        <button class="w-10 h-10 rounded-full border border-gray-300 flex items-center justify-center text-gray-600 hover:bg-black hover:text-white hover:border-black transition-colors flex-shrink-0">
            <svg class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <line x1="7" y1="17" x2="17" y2="7"></line>
                <polyline points="7 7 17 7 17 17"></polyline>
            </svg>
        </button>
    </div>
</div>
