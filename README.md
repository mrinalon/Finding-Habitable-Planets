# Finding-Habitable-Planets

This Node.js project searches for potentially habitable planets using data from the Kepler Space Telescope. The project reads Kepler data from a CSV file, filters for habitable planets based on certain criteria, and outputs the names of these planets.

## Features

- Reads Kepler data from a CSV file.
- Filters planets based on criteria for habitability.
- Outputs the names of habitable planets.
- Displays the total count of habitable planets found.

## Installation

### Prerequisites

- Node.js (version 12 or higher)
- npm (Node package manager)

### Setup

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/habitable-planets-search.git
    cd habitable-planets-search
    ```

2. Install the required dependencies using npm:

```bash
npm install csv-parse
```

## Usage

1. **Prepare the Kepler Data CSV File**

   Ensure you have a CSV file named `kepler_data.csv` in the project directory. This file should contain the Kepler data with appropriate columns.

2. **Run the Script**

   Execute the script using Node.js:

   ```bash
   node index.js
   ```

   This will read the data from `kepler_data.csv`, filter for habitable planets, and output the names and count of habitable planets found.

## Explanation

- **Dependencies**: The script uses the `csv-parse` library to parse CSV data and the `fs` module to handle file operations.
- **Habitability Criteria**: The `isHabitablePlanet` function checks if a planet meets the following conditions:
  - `koi_disposition` is `CONFIRMED`.
  - `koi_insol` (stellar flux) is between 0.36 and 1.11 times that of Earth.
  - `koi_prad` (planetary radius) is less than 1.6 times that of Earth.
- **Data Processing**: The script reads `kepler_data.csv`, parses each row, and checks if the planet is habitable. If it is, the planet is added to the `habitablePlanets` array.
- **Output**: After processing all data, the script logs the names of habitable planets and the total count found.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributions

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/mrinalon/Finding-Habitable-Planets/issues) if you want to contribute.

---
