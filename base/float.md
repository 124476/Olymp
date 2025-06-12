# Вещественные числа

```
#include <iostream>
#include <iomanip>

using namespace std;

int main() {
    float f = 1.123456789;  // Число с типом float
    double d = 1.123456789;  // Число с типом double

    cout << fixed << setprecision(10); // Хочу 10 знаков после точки, и ни пикселем меньше!
    cout << "Float:  " << f << endl;
    cout << "Double: " << d << endl;

    return 0;
}
```

```
#include <iostream>
#include <iomanip>

using namespace std;

int main() {
    int number = 0b00101010; // Вот такие мы олды, что думаем в двоичном стиле
    cout << hex << number << endl; // А говорим в шестнадцатеричном, как веб-дизайнеры
    cout << dec << setw(4) << setfill('_') << number << "\n" << number * 12 << endl;
    return 0;
}
```

```
#include <iostream>
#include <iomanip>

using namespace std;

int main() {
    int a = 5, c = 0;
    float a_f = (float)a + 2.5f, c_f = 0;  // Я сказал, считай a как float!

    cout << fixed << setprecision(2) << a << endl;
    cout << fixed << setprecision(2) << a_f << endl;

    c = a + (int)a_f; // Отрежь дробную часть, как ниточку на одежде
    c_f = (float)a + a_f;

    cout << fixed << setprecision(2) << c << endl;
    cout << fixed << setprecision(2) << c_f << endl;

    return 0;
}
```

