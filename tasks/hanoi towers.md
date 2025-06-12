# Головоломка Ханойские башни

Головоломка <Ханойские башни> состоит из трёх стержней, пронумеруем их слева направо: 1, 2 и 3. Также в головоломке используется стопка дисков с отверстием посередине. Радиус дисков уменьшается снизу вверх. Изначально диски расположены на левом стержне (стержень 1), самый большой диск находится внизу. Диски в игре перемещаются по одному со стержня на стержень. Диск можно надеть на стержень, только если он пустой или верхний диск на нём большего размера, чем перемещаемый. Цель головоломки — перенести все диски со стержня 1 на стержень 3.

Требуется найти последовательность ходов, которая решает головоломку <Ханойские башни>.

## Ханойские башни

```
#include <algorithm>
#include <iostream>
#include <string>
#include <vector>

using namespace std;

void f(int n, int a, int b) {
	if (n == 1) {
		cout << a << " " << b << endl;
		return;
	}

	int m = 6 - a - b;

	f(n - 1, a, m);
	cout << a << " " << b << endl;
	f(n - 1, m, b);
}

int main()
{
	cin.tie(0);
	cout.tie(0);
	ios_base::sync_with_stdio(false);

	int n;
	cin >> n;

	int sm = 1;

	for (int i = 0; i < n; i++)
		sm *= 2;

	cout << sm - 1 << endl;

	f(n, 1, 3);

	return 0;
};
```

## Ханойских башнях с четырьмя стержнями

```
#include <algorithm>
#include <iostream>
#include <string>
#include <vector>
#include <map>

using namespace std;

map<int, int> d;

int f(int n) {
    if (n == 1) return 1;
    if (n == 2) return 3;
    if (d.find(n) != d.end())
        return d[n];
    
    int mn = 10000000;
    for (int k = 1; k < n; ++k) {
        int p = 2 * f(k) + (1 << (n - k)) - 1;  // 2^(n-k) - 1
        if (p < mn)
            mn = p;
    }
    d[n] = mn;
    return mn;
}

int main()
{
	cin.tie(0);
	cout.tie(0);
	ios_base::sync_with_stdio(false);

	int n;
	cin >> n;

	cout << f(n);

	return 0;
};
```