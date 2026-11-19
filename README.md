function dailyLog232() {
  const hourlyUsage = [12, 15, 18, 10, 22, 25, 19, 14];

  const totalUsage = hourlyUsage.reduce(
    (sum, usage) => sum + usage,
    0
  );

  const averageUsage = totalUsage / hourlyUsage.length;
  const peakUsage = Math.max(...hourlyUsage);
  const peakHour = hourlyUsage.indexOf(peakUsage) + 1;

  console.log("Daily Energy Consumption Report");
  console.log("--------------------------------");
  console.log(`Total Usage: ${totalUsage} kWh`);
  console.log(`Average Usage: ${averageUsage.toFixed(2)} kWh`);
  console.log(`Peak Usage: ${peakUsage} kWh`);
  console.log(`Peak Hour: ${peakHour}`);
}

dailyLog232();
