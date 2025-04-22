# [![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1000&color=7B3DB8&width=435&lines=CPF+Validator+in+PHP)](https://git.io/typing-svg)

This PHP script validates CPF numbers by checking if they follow the correct structure and if the check digits are valid. The CPF can be entered with or without formatting (dots and dashes).

The script performs the following steps to validate the CPF:

- **CPF Cleanup**: Removes all non-numeric characters, such as dots and dashes.
- **Structure Validation**: Verifies if the CPF has exactly 11 numeric digits, checks if it is not in a "blacklist" of known invalid CPFs, and ensures it is not a repetitive sequence (e.g., "111.111.111-11").
- **Check Digits Calculation**:
    * **First digit**: Calculated from the first 9 digits of the CPF. The calculation formula takes into account the multiplication of the digits by a decreasing factor from 10 to 2, and the resulting sum is divided by 11 to determine the first check digit.
    * **Second digit**: Similar to the first one, but considers the first 10 digits and calculates the second check digit.

If any of the calculated digits do not match the digits provided in the CPF, the script returns "CPF inválido."

## How to Use:
  * Open the terminal and navigate to the directory where the PHP file is located.
  * Execute the PHP script with the following command:
      - php validator.php
  The script will prompt you to enter the CPF to be validated. Enter the CPF with or without formatting (e.g., 123.456.789-10 or 12345678910).
