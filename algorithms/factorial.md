# Факториал

## Предрассчет

```
#include <iostream>

using namespace std;

long long factorials[] = {
	1, 1, 2, 6, 24, 120, 720, 5040, 40320, 362880, 3628800, 39916800, 479001600,
};

long long fac(int n) {
	if (n < 0) return 1;
	return factorials[n];
}

int main()
{
	cin.tie(0);
	cout.tie(0);
	ios_base::sync_with_stdio(false);

	int n;
	cin >> n;

	cout << fac(n);

	return 0;
};
```

## Циклом

```
#include <iostream>

using namespace std;

int main()
{
	cin.tie(0);
	cout.tie(0);
	ios_base::sync_with_stdio(false);

	int n;
	cin >> n;

	int sm = 1;

	for (int i = 2; i <= n; i++)
		sm *= i;

	cout << sm;

	return 0;
};
```