{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# SPY500 Job Postings Historical Relationship\n",
    "Varies analysis looking at the relationship between the SPY500 and (JOLTS) Job Openings in the US. \n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Overview:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "The purpopse of the analysis is to investigate the relationship between S&P 500 (SPY) and the U.S. Job openings. The aim is to understand how changes in the labor market correlate with the performance of the SPY Prices. "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Data Source:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "- SPY Data: Historical daily prices of the S&P 500 ETF (SPY) from 2000 to 2024.\n",
    "- JOLTS Data: Monthly data on job openings across various sectors in the U.S. economy, from the U.S. Bureau of Labor Statistics (BLS). "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Analysis Summary:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "#### 1. Data Preprocessing: \n",
    "- Basic Preprocessing was conducted on both datasets to concern matching dates, and formats. \n",
    "- The datasets were merged using the date column. "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "#### 2. Correlation Analysis:\n",
    "**Correlation Hypothesis:** I initially hypothesized that there would be a strong correlation between SPY prices and JOLTS (Job Openings). Generally, strong job opening data reflects a robust economy, as companies expand and create more positions, which in turn should benefit businesses and drive stock prices higher. \n",
    "\n",
    "**Historical Trends:** \n",
    "- Between 2001 and mid-2009, JOLTS consistently trended higher than SPY prices, similar to the periods from 2015-2019 and April 2021 to March 2023. \n",
    "\n",
    "**Recent Divergence:** \n",
    "- From September 2022, an interesting divergence occurs where SPY prices begin to rise while job openings (JOLTS) continue to decline. This suggests that while the labor market appears to be softening, the stock market has started to recover. \n",
    "- What could explain this disconnect? \n",
    "\n",
    "##### **Next Steps/ Future Research:** \n",
    "- I would like to measure for how long on average does JOLTS and SPY Prices start to go down before there is a recession? \n",
    "- What recovers first, JOLTS or SPY?"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "##### SPY 500 VS. JOLTS Totals with Recessions pds. "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Fluctuating Correlation:** \n",
    "- The correlation between SPY and JOLTS is not consistently positive or negative. It swings back and forth, which suggests that the relationship between stock prices and job openings is dynamic. \n",
    "\n",
    "2. **Correlation Around Recessions:** During recessions (shaded areas), the correlation tends to drop or become more volatile. \n",
    "\n",
    "3. **Around 2020, during the COVID-19-induced recession,** there is a significant drop in correlation. The sudden drop could reflect the drastic economic impacts of the pandemic, where the job market and stock prices reacted differently. As I recall, there was a large number of job openings and a lack of talent to fill the roles. "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {
    "vscode": {
     "languageId": "plaintext"
    }
   },
   "source": [
    "#### **3. Moving Average Corelation:**\n",
    "The aim of this analysis was to find the moving average with the strongest positive relationship to SPY Prices. \n",
    "\n",
    "Add Image of Table and Image of chart. "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "#### **4. Predictive Modeling:**\n",
    "\n",
    "- A linear regression model was developed to predict SPY prices using JOLTS data as the independent variable.\n",
    "- The model was trained on historical data up to a certain cutoff date and then used to forecast SPY prices beyond this date. The model focuses on historical data, using SPY and JOLTS data only up to September 30, 2022, for model training. \n",
    "- I select Sept 2022 as the cut off date to train the model because that is when the divergence between JOLTs and SPY Prices start.\n",
    "\n",
    "**Therefore, I wanted to understand what would have been the prices of the SPY 500 if the divergence did not occur.**"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "- When looking at the Percentage difference on July 1, 2024 between Actual SPY Prices (550.81) and the Predicted Price (299.5), there was a 251.3 point difference, or 83.9% difference. \n",
    "- When we compare the July 1, 2024 Predicted Price from the original analysis (above) it was 315.1, for this 2nd analysis it is 299.5, and the actual price was 550.8. "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "#### **5. Conclusion:** "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "- I conducted this analysis to practice my Python skills and explore the relationship between job openings, which typically indicate a strong economy, and the SPY500, a popular ETF tracking the stock market. \n",
    "- I expected that high SPY prices would correlate with strong job openings, and indeed, I found a strong correlation of 0.92. However, I noticed a divergence after October 2022, suggesting a potential shift in economic dynamics. \n",
    "- This could indicate that the market is pricing in future expectations differently than before, perhaps due to changes in monetary policy or other economic factors. For example, investors don't want to miss the strong performance of the SPY 500 and expect monetary policy to help JOLTs in the future. \n",
    "- It’s also possible that businesses are focusing more on innovations such as AI and margins rather than hiring, which could be why job openings have slowed down. "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "#### **Sorry more questions / thought here:**"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**This divergence could suggest several scenarios:**\n",
    "1. Are organizations reducing job openings in anticipation of economic challenges that the stock market has not yet reflected?\n",
    "2. Could the stock market be projecting strong economic growth despite lower JOLTS numbers, especially with unemployment rates at historic lows?\n",
    "3. Do high SPY prices indicate that a strong relationship with JOLTS is no longer necessary? If so, what does this signify about the changing economic landscape? Does the lack of correlation suggest that traditional indicators like JOLTS are becoming less relevant for predicting stock market performance?\n",
    "\n",
    ".............So many questions brewing\n",
    "\n",
    "**What could happen next?**\n",
    "1. I plan to continue to monitor the relationship between JOLTS and SPY as I am interested in seeing what unfolds. \n",
    "2. What could potentially be the next moves?\n",
    "    - **Best Case scenario:** Monetary Policy changes and JOLTs increase as SPY Prices increase as well. If this happens, will JOLTS catch up to SPY to mirror the directional relationship of the past. \n",
    "    - **OK Case Scenario:** Monetary Policy changes and JOLTs increase as SPY Prices trade in a range until JOLT values catch up as a reversion to the mean? Can this be possible? \n",
    "    - **Weird Case Scenario:** JOLT values continue to decrease as SPY Prices continue to increase. \n",
    "    - **Worst case Scenario:** JOLT value stay relatively the same as SPY Prices met it at the predicted values (315 or 299)\n",
    "    - **POOPY DOOPY Case Scenario:** JOLT values continue to decrease low as SPY prices met it to the predicted values (315 or 299). "
   ]
  }
 ],
 "metadata": {
  "language_info": {
   "name": "python"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 2
}
