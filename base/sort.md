# Сортировка

```
sort(d.begin(), d.end(),
	[](pair<int, int> a, pair<int, int> b)
	{
		return a.second < b.second;
	}
);
```