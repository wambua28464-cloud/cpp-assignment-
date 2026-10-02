# cpp-assignment-
C++ Programming Assignment

## Question 1: Quickmart Discount Program
```cpp
#include <iostream>
using namespace std;

// Function prototype
float calculateDiscount(int purchase_amnt);

int main() {
    int amount;
    float result, final_pay;
    
    cout << "Enter amount purchases: " << endl;
    cin >> amount;
    
    // Function call
    result = calculateDiscount(amount);
    final_pay = amount - result;
    
    cout << "\n";
    cout << "QUICKMART DISCOUNT PROGRAM " << endl;
    cout << "=============================" << endl;
    cout << "Initial Amount: = Ksh " << amount << endl;
    cout << "Discount = Ksh. " << result << endl;
    cout << "Final amount payable = Ksh. " << final_pay << endl;
    cout << "=============================" << endl;
    
    return 0;
}

// Function definition
float calculateDiscount(int purchase_amnt) {
    float discount;
    if (purchase_amnt < 5000) {
        discount = 0.05 * purchase_amnt;
    }
    else if (purchase_amnt >= 5000 && purchase_amnt <= 9999) {
        discount = 0.1 * purchase_amnt;
    }
    else {
        discount = 0.15 * purchase_amnt;
    }
    return discount;
}
```

---

## Question 2: Electricity Bill Calculator
```cpp
#include <iostream>
using namespace std;

// Function prototype
float calculateBill(int units);

int main() {
    int units;
    float total_bill;
    
    cout << "Enter the number of units consumed: ";
    cin >> units;
    
    // Function call
    total_bill = calculateBill(units);
    
    cout << "\n==========================" << endl;
    cout << "ELECTRICITY BILL REPORT" << endl;
    cout << "==========================" << endl;
    cout << "Units Consumed: " << units << " units" << endl;
    cout << "Total Electricity Bill: Ksh. " << total_bill << endl;
    cout << "==========================" << endl;
    
    return 0;
}

// Function definition
float calculateBill(int units) {
    float bill = 0;
    if (units <= 100) {
        bill = units * 10;
    }
    else if (units <= 200) {
        bill = (100 * 10) + ((units - 100) * 15);
    }
    else {
        bill = (100 * 10) + (100 * 15) + ((units - 200) * 20);
    }
    return bill;
}
```

---

## Question 3: Employee Salary Calculator
```cpp
#include <iostream>
using namespace std;

// Function prototype
float calculateTax(float gross_salary);

int main() {
    float gross_salary, tax_amount, net_salary;
    
    cout << "Enter the employee's gross salary (Ksh): ";
    cin >> gross_salary;
    
    // Function call
    tax_amount = calculateTax(gross_salary);
    
    // Calculate net salary
    net_salary = gross_salary - tax_amount;
    
    cout << "\n==========================" << endl;
    cout << "EMPLOYEE SALARY BREAKDOWN" << endl;
    cout << "==========================" << endl;
    cout << "Gross Salary: Ksh. " << gross_salary << endl;
    cout << "Tax Deducted: Ksh. " << tax_amount << endl;
    cout << "Net Salary Payable: Ksh. " << net_salary << endl;
    cout << "==========================" << endl;
    
    return 0;
}

// Function definition
float calculateTax(float gross_salary) {
    float tax;
    if (gross_salary < 30000) {
        tax = 0.05 * gross_salary;
    }
    else if (gross_salary >= 30000 && gross_salary <= 59999) {
        tax = 0.10 * gross_salary;
    }
    else {
        tax = 0.15 * gross_salary;
    }
    return tax;
}
```