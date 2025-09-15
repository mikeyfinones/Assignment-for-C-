## Activity A1

#include <iostream>
using namespace std;

int main() {
    int a = 8, b = 3, c = 2;  // hard-coded values

    cout << "a + b * c = " << (a + b * c) << endl;
    cout << "(a + b) * c = " << ((a + b) * c) << endl;
    cout << "a / b * c = " << (a / b * c) << endl;
    cout << "a / (b * c) = " << (a / (b * c)) << endl;

    return 0;
}


## Activity A2
#include <iostream>
#include <iomanip>
using namespace std;

int main() {
    double balance = 100.00;   // starting balance
    int deposits = 4;          // number of deposits
    int withdrawals = 2;       // number of withdrawals

    balance += deposits * 25.50;   // add deposits
    balance -= withdrawals * 12.75; // subtract withdrawals

    cout << fixed << setprecision(2);
    cout << "Final balance = " << balance << endl;

    return 0;
}

## Activity B1

#include <iostream>
using namespace std;

int main() {
    int s1 = 85, s2 = 92, s3 = 77;

    int sum = s1 + s2 + s3;

    cout << "Raw average (implicit): " << (sum / 3) << endl;
    cout << "Correct average (explicit cast): "
         << static cast<double>(sum) / 3 << endl;

    return 0;
}

## Activity B2

#include <iostream>
#include <iomanip>
using namespace std;

int main() {
    int wins, games;
    cin >> wins >> games;

    if (games == 0) {
        cout << "No games played." << endl;
    } else {
        double pct = static_cast<double>(wins) / static_cast<double>(games) * 100.0;
        cout << fixed << setprecision(1);
        cout << "Win% = " << pct << "%" << endl;
    }

    return 0;
}

## Acitivity C

#include <iostream>
#include <iomanip>
using namespace std;

int main() {
    double hours, rate;
    cin >> hours >> rate;

    double regHours = min(hours, 40.0);
    double otHours = max(hours - 40.0, 0.0);

    double gross = regHours * rate + otHours * rate * 1.5;
    double tax = 0.18 * gross;
    double benefits = 35.0;

    cout << fixed << setprecision(2);
    cout << "Regular: " << regHours << ", Overtime: " << otHours << endl;
    cout << "Gross: $" << gross << endl;
    cout << "Tax (18%): $" << tax << endl;
    cout << "Benefits: $" << benefits << endl;
    cout << "Net: $" << net << endl;

    return 0;
}

## Activity D

#include <iostream>
using namespace std;

int main() {
    int items;
    double price;
    cout << "Enter items and price: ";
    cin >> items >> price;

    double total = items * price;

    int discountPercent = 15;
    double discount = total * (static_cast<double>(discountPercent) / 100.0);

    double shipping = 5 + 2 * items;
    double afterDiscount = total - discount;
    if (afterDiscount >= 100.0) shipping = 0;

    cout << fixed << setprecision(2);
    cout << "Total: $" << total << "\n";
    cout << "Discount: $" << discount << "\n";
    cout << "Shipping: $" << shipping << "\n";
    cout << "Grand Total: $" << (afterDiscount + shipping) << "\n";

    return 0;
}
