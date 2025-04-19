# Shadow-Art-Calculator

A Python tool that calculates the perfect time of day to create shadow art installations based on sun position, shadow length, and angle.

## Overview

The Shadow Art Calculator is a unique utility that helps artists, photographers, architects, and designers determine exactly when the sun will cast shadows with specific properties at a given location. By eliminating guesswork from shadow planning, this tool enables precise shadow-based installations and photography.

## Problem Addressed

Creating shadow art or planning shadow-dependent designs involves complex astronomical calculations that most artists lack the expertise to perform. This calculator bridges the gap between creative vision and technical precision by:

- Eliminating the need to wait for hours hoping for the right conditions
- Accounting for location-specific sun patterns
- Handling seasonal variations in sun position
- Calculating both shadow length and angle simultaneously
- Providing precise timing for ephemeral shadow effects

## Features

- Calculate shadow properties based on:
  - Geographic location (latitude/longitude)
  - Date
  - Desired shadow length (as a ratio of object height)
  - Desired shadow angle/direction
- Returns a list of times when conditions will match your specifications
- Provides shadow directions in both degrees and cardinal directions
- Includes practical setup tips for shadow installations

## Installation

1. Clone this repository:
   ```
   git clone https://github.com/username/shadow-art-calculator.git
   cd shadow-art-calculator
   ```

2. Install required dependencies:
   ```
   pip install ephem
   ```

## Usage

Run the script and follow the interactive prompts:

```
python shadow_art_calculator.py
```

You'll be asked to enter:
- Your latitude and longitude
- Target date
- Desired shadow length ratio
- Optional: desired shadow angle

The program will then calculate and display times when shadows will match your criteria.

### Example Input:

```
Enter latitude (decimal degrees, positive for North): 40.7128
Enter longitude (decimal degrees, positive for East): -74.0060
Enter date (YYYY-MM-DD) or press Enter for today: 2025-06-21
Enter desired shadow length ratio (e.g., 1.5 for 1.5x object height): 1.0
Enter desired shadow angle in degrees (0-360, 0=North, 90=East, etc.) or press Enter for any angle: 270
```

### Example Output:

```
Optimal times for shadow art installation:
Time: 09:15, Shadow Length: 1.02x object height, Shadow Angle: 272.3° (W)
Time: 09:25, Shadow Length: 0.98x object height, Shadow Angle: 268.7° (W)

Setup Tips:
- For vertical objects, ensure they're perfectly upright.
- Use a compass to orient your shadow receiver in the optimal direction.
- Arrive at least 30 minutes before the calculated time to set up.
- Account for elevation changes and potential obstructions.
```

## Applications

- **Art Installations**: Create precisely timed shadow art
- **Photography**: Plan shots with specific shadow effects
- **Architecture**: Study building shadow patterns
- **Urban Planning**: Design shadow-optimized public spaces
- **Solar Engineering**: Assess shading impacts on solar installations
- **Sundial Design**: Create accurate shadow-based time instruments
- **Archaeological Research**: Study ancient shadow alignments

## How It Works

The calculator uses the `ephem` library to determine sun positions throughout the day. It calculates:

1. Shadow length using trigonometry (shadow length = object height / tan(sun altitude))
2. Shadow angle (opposite of sun's azimuth)
3. Times when these values match specified criteria

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Acknowledgments

- PyEphem library for astronomical calculations
- Shadow artists and photographers who inspired this tool
