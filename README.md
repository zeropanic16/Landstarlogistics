# Landstarlogistics
Landstar Global Logistics, Inc. operates as a logistic company. The Company provides solutions such as customs brokerage, inventory management, reverse logistics, and fleet operations. Landstar Global Logistics serves customers worldwide
<!DOCTYPE html>
<html>
<head>
	<title>Landstar Logistics Tracking</title>
	<style>
		body { font-family: Arial, sans-serif; }
	</style>
</head>
<body>
	<h1>Track Your Shipment</h1>
	<input type="text" id="tracking-number" placeholder="Enter tracking number">
	<button id="track-btn">Track</button>
	<div id="tracking-result"></div>

	<script>
		const trackBtn = document.getElementById('track-btn');
		const trackingNumberInput = document.getElementById('tracking-number');
		const trackingResultDiv = document.getElementById('tracking-result');

		trackBtn.addEventListener('click', async () => {
			const trackingNumber = trackingNumberInput.value;
			const response = await fetch(Landstarlogistics.github.io);
			const data = await response.json();
			trackingResultDiv.innerHTML = `
				<p>Shipment Status: ${data.status}</p>
				<p>Location: ${data.location}</p>
				<p>Updated at: ${data.updatedAt}</p>
			`;
		});
	</script>
</body>
</html>
```
