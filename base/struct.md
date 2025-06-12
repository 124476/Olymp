# Структура

```
#include <algorithm>
#include <iostream>
#include <string>
#include <vector>

using namespace std;

struct MyStruct
{
	int id;
	string name;
	void print() {
		cout << "id: " << id << ", " << "name: " << name << ";" << endl;
	}
};


int main()
{
	cin.tie(0);
	cout.tie(0);
	ios_base::sync_with_stdio(false);

	MyStruct myStruct;

	myStruct.id = 1;
	myStruct.name = "First struct";

	myStruct.print();

	return 0;
};
```