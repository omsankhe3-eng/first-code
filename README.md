
# Personal Expense Tracker

## Overview

A simple command-line based expense tracking application built with Python. This tool helps users manage their personal finances by recording expenses, categorizing them, and generating useful summaries. All data is stored locally in a text file, making it lightweight and easy to use without requiring any database setup.

## Features

The Personal Expense Tracker includes the following capabilities:

1. **Add New Expense** - Record expenses with date, category, amount, and description
2. **View All Expenses** - Display a formatted table of all recorded expenses
3. **Search by Category** - Filter and view expenses from a specific category
4. **Calculate Total Expenses** - Get the sum of all expenses
5. **Category-wise Summary** - View expense breakdown by category with percentages
6. **Delete Last Expense** - Remove the most recently added expense entry

## Technologies/Tools Used

- **Python 3.x** - Core programming language
- **File I/O Operations** - For data persistence using text files
- **Built-in Python Libraries**:
  - `os` - For file system operations

## Steps to Install & Run the Project

### Prerequisites
- Python 3.x installed on your system
- A terminal/command prompt

### Installation Steps

1. **Download the project file**
   ```bash
   # Save the expense_manager.py file to your desired directory
   ```

2. **Navigate to the project directory**
   ```bash
   cd path/to/project/directory
   ```

3. **Run the application**
   ```bash
   python expense_manager.py
   ```

4. **First Run**
   - On first execution, the program will automatically create an `expenses.txt` file to store your data
   - You'll see a welcome message and the main menu

## Instructions for Testing

### Test Case 1: Adding Expenses
1. Run the application
2. Select option `1` (Add Expense)
3. Enter test data:
   - Date: `22-11-2024`
   - Category: `Food`
   - Amount: `500`
   - Description: `Lunch at restaurant`
4. Verify success message appears

### Test Case 2: Viewing All Expenses
1. After adding some expenses, select option `2` (View All Expenses)
2. Verify that all added expenses are displayed in a formatted table
3. Check that date, category, amount, and description are properly aligned

### Test Case 3: Search by Category
1. Add expenses in different categories (Food, Transport, Bills, Shopping, Other)
2. Select option `3` (Search by Category)
3. Enter a category name (e.g., `Food`)
4. Verify only expenses from that category are displayed

### Test Case 4: Calculate Total
1. Add multiple expenses with different amounts
2. Select option `4` (Calculate Total Expenses)
3. Manually verify the total matches the sum of all expenses

### Test Case 5: Category-wise Summary
1. Add expenses across multiple categories
2. Select option `5` (Category-wise Summary)
3. Verify:
   - All categories are listed
   - Amounts are correct
   - Percentages add up to 100%
   - Total matches the overall sum

### Test Case 6: Delete Last Expense
1. Add a few expenses
2. Note the last expense added
3. Select option `6` (Delete Last Expense)
4. Select option `2` to view all expenses
5. Verify the last expense has been removed

### Test Case 7: Empty File Handling
1. Delete the `expenses.txt` file (or start fresh)
2. Try viewing all expenses - should show "No expenses recorded yet!"
3. Try searching by category - should handle gracefully
4. Try calculating total - should show ₹0.00

### Sample Test Data

```
Date: 22-11-2024, Category: Food, Amount: 500, Description: Lunch
Date: 22-11-2024, Category: Transport, Amount: 150, Description: Taxi fare
Date: 23-11-2024, Category: Bills, Amount: 2000, Description: Electricity bill
Date: 23-11-2024, Category: Shopping, Amount: 1500, Description: Groceries
Date: 24-11-2024, Category: Food, Amount: 300, Description: Coffee
```

## File Structure

```
project-directory/
│
├── expense_manager.py    # Main application file
└── expenses.txt          # Auto-generated data file (created on first run)
```

## Notes

- All expense data is stored in `expenses.txt` in the same directory as the script
- The file format is: `date|category|amount|description` (pipe-separated)
- Currency symbol used: ₹ (Indian Rupee)
- Supported categories: Food, Transport, Bills, Shopping, Other (case-insensitive)

## Future Enhancements

Potential improvements for future versions:
- Edit existing expenses
- Delete specific expenses (not just the last one)
- Date range filtering
- Export to CSV/Excel
- Budget setting and alerts
- Monthly/yearly reports
- Data visualization with charts

---

**Happy Expense Tracking!** 💰📊
