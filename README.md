# Currency_conversion
**Aim: Currency Conversion Program in Java**

The aim of this Java program is to create a currency conversion tool that allows users to convert an amount from one currency to another. The program will demonstrate the use of variables, user input, and basic arithmetic operations to perform currency conversion.

**Procedure:**

1. **User Input:** The program prompts the user to enter the following information:
   - Amount to be converted
   - Source currency (e.g., USD, EUR, JPY)
   - Target currency (e.g., USD, EUR, JPY)

2. **Exchange Rates:** The program should have predefined exchange rates for different currency pairs. These rates will be used to perform the currency conversion.

3. **Calculation:** The program calculates the converted amount using the formula:
   ```
   convertedAmount = amountToConvert * exchangeRateSourceToTarget
   ```

4. **Display Result:** The program displays the original amount, the source currency, the converted amount, and the target currency.

**Example Code:**

```java
import java.util.Scanner;

public class CurrencyConverter {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the amount to convert: ");
        double amountToConvert = scanner.nextDouble();

        System.out.print("Enter the source currency (e.g., USD, EUR, JPY): ");
        String sourceCurrency = scanner.next();

        System.out.print("Enter the target currency (e.g., USD, EUR, JPY): ");
        String targetCurrency = scanner.next();

        // Define exchange rates (example rates, replace with actual rates)
        double exchangeRateUSDToEUR = 0.85;
        double exchangeRateUSDtoJPY = 110.0;

        double convertedAmount = 0.0;

        if (sourceCurrency.equalsIgnoreCase("USD") && targetCurrency.equalsIgnoreCase("EUR")) {
            convertedAmount = amountToConvert * exchangeRateUSDToEUR;
        } else if (sourceCurrency.equalsIgnoreCase("USD") && targetCurrency.equalsIgnoreCase("JPY")) {
            convertedAmount = amountToConvert * exchangeRateUSDtoJPY;
        } else {
            System.out.println("Currency pair not supported.");
            System.exit(0);
        }

        System.out.println("Original Amount: " + amountToConvert + " " + sourceCurrency);
        System.out.println("Converted Amount: " + convertedAmount + " " + targetCurrency);

        scanner.close();
    }
}
```

**Result:**

Upon running the program, the user will be able to input the amount, source currency, and target currency. The program will then display the original amount, converted amount, and currencies involved in the conversion. Please note that the example code provided uses simplified exchange rates and should be replaced with actual exchange rates for accurate conversions.
