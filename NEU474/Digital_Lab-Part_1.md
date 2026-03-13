# Digital Lab Part 1: The Pit Viper Umwelt Test
**Author:** [YOUR NAME HERE]  
**Date:** [DATE]  

## The Scenario: You are the P.I.

You are investigating the thermoreceptive striking behavior of the Western Diamondback Rattlesnake (*Crotalus atrox*). Using robotic prey, you recorded the `Strike_Latency_sec` (how fast the snake strikes) across three different target temperatures: **25°C (Ambient), 37°C (Mouse Temp), and 40°C (Bird Temp)**.

**Your Tech:** Your "AI Grad Student" (Copilot/Gemini via Positron/Antigravity).

**The Challenge:** You must direct your AI to analyze this data. But remember: your AI does not know what a pit viper is. It has not read Chapter 5 of *An Immense World*. If you do not provide biological guardrails, the AI will make "human-centric" assumptions and ruin the analysis.

---

## Step 1: Load the Data

As the Principal Investigator, you must direct your AI to pull the data directly from our repository. In the Positron Assistant chat, instruct the AI to write the R code to load the PitViper_Thermal_Strikes.csv dataset and display the first few rows.

Give the AI this exact URL to read from:
https://raw.githubusercontent.com/djtobiansky/StatsLab/refs/heads/main/NEU474/PitViper_Thermal_Strikes.csv

Once the AI generates the correct script, paste that code into the R chunk below and run it in your console to verify the data loaded correctly. Ensure the AI annotates each line of code so you can follow along. 

```R
# Paste AI code here to load the CSV and show the head of the dataframe.


```

---

## Step 2: The Naive Analysis (The Trap)

First, let's see what happens when we let the AI run wild without biological context. Instruct your AI to run a One-Way ANOVA comparing `Strike_Latency_sec` across the three `Target_Temp` groups using the *entire* dataset. Ask it to generate a boxplot of these results using `ggplot2`.

Paste the code below, run it, and save the resulting messy graph. Ensure the AI annotates each line of code so you can follow along. 

```R
# Paste AI code here to run a One-Way ANOVA on the whole dataset and plot it.


```

### P.I. Reflection: Why is this wrong?

*Based on Chapter 5 of Ed Yong's text, explain why the graph above looks like a messy, non-significant blob. What variable did the AI ignore, and how does that violate the pit viper's Umwelt?*

**[Type your answer here. Focus on the concept of "thermal contrast."]**

---

## Step 3: The "Umwelt-Corrected" Analysis

Now, act as the Principal Investigator. You must correct your AI Grad Student.

**Your Prompt Log:**
*What exact prompt did you use in the AI chat to tell it to filter the data based on the background environment before re-running the stats?*

**[Type your prompt here. E.g., "Wait, pit vipers rely on thermal..."]**

Have your AI write the code to filter the dataset to only include trials on `20C_Cool_Soil`. Then, run the One-Way ANOVA again, apply a Tukey HSD correction, and plot the clean, corrected data. Ensure the AI annotates each line of code so you can follow along. 

```R
# Paste AI code here to filter the data, run the corrected ANOVA & Tukey HSD, and generate the final boxplot.


```

---

## Step 4: Final Statistical Conclusion

*Look at the output of your corrected Tukey HSD. As the P.I., summarize the findings in one or two sentences (your own words; not the AI's). Is there a statistically significant difference in strike latency between a 37°C target and a 40°C target? What about effect size?*

**[Type your statistical conclusion here.]**

---

**Submission Instructions:**
To submit this lab:

1. Open the Markdown Preview in Positron (usually `Ctrl+Shift+V` or `Cmd+Shift+V`).
2. Right-click the preview and select "Print" or "Export" to save it as a PDF.
3. Upload the PDF and your final corrected boxplot image to Canvas.
