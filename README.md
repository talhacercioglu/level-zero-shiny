# Currency Converter Shiny App

This Shiny app converts the Turkish Lira value entered by the user into US Dollars, Euros, and British Pounds using predefined exchange rates. Users can input the amount in Turkish Lira through the user interface and then click the "Convert" button to see the results.

## Usage

1. **Turkish Lira Amount Input:**
   - Enter the Turkish Lira amount in the input box titled "Turkish Lira:". The minimum value is 0.

2. **Convert Button:**
   - After entering the Turkish Lira amount, click the "Convert" button to initiate the conversion process.

3. **Results:**
   - Once the conversion is complete, you can see the converted values in US Dollars, Euros, and British Pounds.

## Exchange Rates (Sample Values)

- 1 Turkish Lira = 0.033 US Dollars
- 1 Turkish Lira = 0.026 Euros
- 1 Turkish Lira = 0.030 British Pounds

## Installation and Execution

1. Install R and RStudio.
2. In the RStudio console, run the following command to install the required packages:

   ```R
   install.packages(c("shiny", "shinythemes"))

## To run the Shiny app, execute the following command in the RStudio console:
- shiny::runGitHub("USERNAME/REPO")
--(Note: Replace USERNAME and REPO with the GitHub username and repository of this app.)
