# Morgage calculator with real-time interest rates

This repository demonstrates how to integrate the ActiveCalculator Embed SDK into a simple HTML page, showcasing dynamic interest rate updates based on loan terms.

## Quick Start

1. Clone this repository.
2. Open `index.html` in your browser.

## Key Features

- Embeds an ActiveCalculator instance
- Uses Embed SDK to interact with the calculator
- Dynamically updates interest rates when loan term changes

## Customization

### Calculator ID and Element References

Replace these with your specific ActiveCalculator details:

- Calculator ID: `"cm01ccea50001mg0chpyziyke"`
- Loan Term Element: `"UZ-fD48tjm8OzZNONtkdM"`
- Interest Rate Element: `"lT1VZA1-nCUCnlynX6ids"`

### Interest Rates

Update the `window.interestRateMap` object with your desired rates:

```javascript
window.interestRateMap = {
  10: 3.5,
  15: 3.75,
  20: 4,
  30: 4.25
}
```

### Real-time Rates (Server-side)

For WordPress or other server-side environments, you can inject real-time rates directly into the `window` object:

```php
<script>
window.interestRateMap = <?php echo json_encode(get_real_time_rates()); ?>;
</script>
```

Replace `get_real_time_rates()` with your actual function to fetch current rates.

## Requirements

- ActiveCalculator paid plan
- JS API enabled in calculator settings

For more details on the ActiveCalculator Embed SDK, visit the [official documentation](https://docs.activecalculator.com).
