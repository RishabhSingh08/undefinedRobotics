<script>
  const stats = [
    { value: '$38.5K+', label: 'Value Raised' },
    { value: '4,000+', label: 'Underserved Individuals Reached' },
    { value: '36', label: 'FTC Teams Connected' },
    { value: '12', label: 'Regional/National Awards' },
    { value: '42', label: 'Profesionals Connected' }
  ];
</script>

<div class="grid grid-cols-2 md:grid-cols-5 gap-8">
  {#each stats as stat, index}
    <div class="text-center {index === stats.length - 1 ? 'col-span-2 md:col-span-1' : ''}">
      <div class="text-3xl md:text-4xl font-bold bg-gradient-to-r from-yellow-500 to-yellow-100 bg-clip-text text-transparent mb-2">
        {stat.value}
      </div>
      <div class="text-gray-300">{stat.label}</div>
    </div>
  {/each}
</div>
