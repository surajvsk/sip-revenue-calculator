# SIP Revenue Calculator

This project provides a simple and interactive web-based SIP (Systematic Investment Plan) Revenue Calculator. It allows users to input various parameters like investment amount, duration, number of SIPs, assumed annual returns, and trail income percentage to calculate and visualize the monthly SIP revenue breakup and total projected income. The results are displayed in a paginated table and can be exported to an Excel (CSV) file.

## Features

  * **Interactive Input Sliders:** Easily adjust investment parameters using intuitive range sliders.
  * **Real-time Input Sync:** Slider values are synchronized with numerical input fields for precise control.
  * **Monthly SIP Breakup Table:** View a detailed month-by-month breakdown of inflow, Asset Under Management (AUM), and income/trail.
  * **Dynamic Pagination:** Navigate through large datasets with customizable rows per page and clear pagination controls.
  * **Total Income/Trail Display:** See the cumulative projected income at a glance.
  * **Reset Functionality:** Quickly reset all inputs to their default values.
  * **Export to Excel (CSV):** Download the calculated SIP breakup data as a CSV file for further analysis.
  * **Responsive Design:** Built with Tailwind CSS, ensuring a clean and responsive layout across different screen sizes.

## How to Use

1.  **Open `index.html`:** Simply open the `index.html` file in your web browser.
2.  **Adjust Parameters:**
      * **Select Amount:** Set the monthly investment amount per SIP.
      * **Select Duration:** Define the investment duration in years.
      * **No. of SIP Registered:** Specify the total number of SIPs.
      * **Annualized Assumed Returns:** Enter the expected annual return percentage.
      * **Trail Income:** Input the trail income percentage you expect to earn on the AUM.
3.  **Calculate:** Click the **"CALCULATE"** button to generate the SIP revenue breakup.
4.  **View Results:** The "SIP Revenue Breakup" section will populate with the calculated data.
      * **Total Income/Trail:** Displays the sum of all monthly trail incomes.
      * **Table:** Shows monthly details for Inflow, AUM, and Income/Trail.
5.  **Navigate Table:** Use the pagination controls (`<`, `>`) and the "No. of rows per page" dropdown to browse through the results.
6.  **Reset:** Click the **"RESET"** button to clear all inputs and the calculated data.
7.  **Export Data:** Click the **"Export Excel"** button to download the entire SIP breakup data as a CSV file.

## Technical Details

The calculator is built using:

  * **HTML5:** For the basic structure of the web page.
  * **Tailwind CSS:** A utility-first CSS framework for rapid UI development and responsive design.
  * **JavaScript:** Powers all the interactive elements, calculations, and dynamic table rendering.
  * **Font Awesome:** Used for the "Add to Favourites" icon.

### Calculation Logic

The SIP revenue calculation works as follows:

  * **Monthly Investment:** `monthlyInvestmentPerSip * totalSipCount`
  * **Monthly Return Factor:** `1 + (annualReturnRate / 12)`
  * **Monthly Trail Rate:** `trailIncomeRate / 12`
  * **AUM Calculation (monthly):** `(Previous AUM * Monthly Return Factor) + Monthly Inflow`
  * **Monthly Trail Income:** `Current AUM * Monthly Trail Rate`
  * **Total Income/Trail:** Sum of all `monthlyTrailIncome` over the entire duration.

## Setup

This project is a standalone HTML file and does not require any complex setup.

1.  **Clone the repository (Optional, if you have the file already):**
    ```bash
    git clone [<repository-url>](https://github.com/surajvsk/sip-revenue-calculator.git)
    cd sip-revenue-calculator
    ```
2.  **Open `index.html`:** Directly open the `index.html` file in your preferred web browser.

## Contributing

## Feel free to fork the repository and contribute.
