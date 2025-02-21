# Tailwind CSS Classes Not Applying

This repository demonstrates a common issue where Tailwind CSS classes fail to apply as expected.  The problem often stems from incorrect configuration, conflicting styles, or improper usage of directives like `@apply`.  The solution involves checking for common pitfalls and ensuring correct integration with your project.

## Bug

The provided code shows a simple div element with Tailwind classes for background color (`bg-red-500`) and hover effect (`hover:bg-blue-700`).  However, these classes might not be rendered correctly in the browser, leading to unexpected visual results.  This can happen for several reasons:

* **Incorrect Tailwind Configuration:**  The Tailwind CSS build process might not be set up correctly, preventing the classes from being included in the output CSS.
* **Conflicting Styles:** Other CSS rules or styles within your project may override Tailwind's classes.
* **Missing or Incorrect Purge Configuration (if using PurgeCSS):**  If PurgeCSS is used to optimize your Tailwind build, the classes might be removed if not used correctly.
* **Typographical Errors:** Simple typos in class names can prevent their application.
* **Missing or Incorrect Imports:** In JavaScript-based projects, make sure you are properly importing the necessary Tailwind styles.

## Solution

The solution involves a systematic approach to pinpoint the cause:

1. **Verify Tailwind Installation and Configuration:**  Check the Tailwind configuration file (`tailwind.config.js` or similar) to ensure it's correctly pointing to your CSS files and includes any necessary plugins.
2. **Inspect Browser Developer Tools:** Open the browser's developer tools (usually F12) to examine the rendered CSS.  Look for conflicting styles or check if the Tailwind classes are even present in the generated CSS.
3. **Check for Conflicting Styles:** Carefully examine any other CSS rules in your project that might be overriding Tailwind's classes. Use the specificity property to solve the problem.
4. **Ensure Proper Class Usage:** Double-check for any typos in your Tailwind class names. Make sure they are correctly applied to the HTML element.
5. **Review PurgeCSS Configuration (if applicable):** If you use PurgeCSS, check its configuration to ensure that it's not accidentally removing the necessary Tailwind classes.
6. **Proper Importing:** If using JavaScript, ensure you have correctly imported the Tailwind directives and configured your project to incorporate them correctly.

By addressing these points, the issue should be resolved and the Tailwind classes should correctly apply.