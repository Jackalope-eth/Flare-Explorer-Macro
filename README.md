# Flare Cleanup Macro for LibreOffice Calc

This macro helps you clean and analyze your **Flare (FLR)** transaction data inside **LibreOffice Calc**. It converts all transaction values from **wei** to **FLR**, calculates a running balance for your wallet, and highlights inbound and outbound transactions for easy tracking.

This macro has been verified to work in LibreOffice V.25.8.2.2

## Where to Get Your Transaction Data

This macro is designed to work with account exports from Flare Explorer (https://flare-explorer.flare.network/).  

**Important:** When exporting, make sure to select your **entire transaction history**. If you export only part of your history, the running balance calculated by the macro will be **incorrect**.

## What the Macro Does

When you run **Flare_Cleanup_Macro**, it will:

1. Ask for your wallet address.
2. Convert the `Value` and `Fee` columns from **wei → FLR**.
3. Add a **Running Balance** column if one doesn’t exist.
4. Calculate your running balance after each transaction.
5. Color-code rows for easy tracking:
   - Green – incoming transactions (account received FLR)  
   - Red – outgoing transactions (account sent FLR)
6. Apply clean borders and formatting for easier reading.

## Installing the Macro

1. Open **LibreOffice Calc**.
2. Press **Alt + F11** (or go to `Tools → Macros → Organize Macros → LibreOffice Basic…`).
3. In the window that appears:
   - Select your document or `My Macros`.
   - Expand **Standard**, or create a new module if needed.
   - Click **New**, and name it something like `FlareTools`.
4. A blank code editor window will open. Delete any existing text and **paste the macro code from the repository**:
5. Click **Save** or go to `File → Save`.
6. Close the editor window.

## Running the Macro

1. Open your transaction export spreadsheet from Flare Explorer in LibreOffice Calc.
2. Go to `Tools → Macros → Run Macro…`.
3. Select the macro:
4. Click **Run**.
5. Enter the wallet address of the exported account (to calculate running balance correctly).

## After Running the Macro

- `Value` and `Fee` amounts are converted from **wei → FLR**.  
- A **Running Balance** column shows your total balance after each transaction.  
- Rows are color-coded for quick reference:
  - Green = incoming FLR  
  - Red = outgoing FLR  
- Headers and borders are formatted neatly for readability.

## Tips & Notes

- Always back up your spreadsheet before running the macro.  
- Ensure your export includes **all transactions** to avoid incorrect running balances.    
- Wallet address matching is case-insensitive.
- This macro only calculates transactions, not token transfers
