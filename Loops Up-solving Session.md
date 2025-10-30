## 1st Problem 

```CPP
int n; cin >> n;
for (int number = 1; number <= n; number++) {
	cout << i << endl;
}
```

## 2nd problem 

```CPP
int n; cin >> n;
for (int i = 1; i <= 12; i++) {
	cout << n << " * " << i << " = " << n * i << endl;
}
```

## 3rd Problem

```CPP
int n; cin >> n;
int mx = 0;

for (int i = 0; i < n; i++) {
	int num; cin >> num;
	
	if (num > mx) {
		mx = num;
	} // mx = max(mx, num) .. you need to #include <algorithm>
}

cout << mx << endl;
```


## 4th Problem

```CPP
int n; cin >> n;
int pos = 0, neg = 0, even = 0, odd = 0;

for (int i = 0; i < n; i++) {
	int num; cin >> num;
	
	if (num > 0) pos++;
	else if (num < 0) neg++;

	if (num % 2 == 0) even++;
	else odd++;
}

cout << "Even: " << even << el;
cout << "Odd: " << odd << el;
cout << "Positive: " << pos << el;
cout << "Negative: " << neg << el;
```

## 5th Problem

```CPP
char ch; cin >> ch;
string CF = "codeforces";

for (int i = 0; i < 10; i++) {
	if (ch == CF[i]) {
		cout << "YES" << endl;
		return;
	}
}

cout << "NO" << el;
```

## 6th Problem

```CPP
int n; cin >> n;

for (int i = 0; i < n; i++) {
	cout << "10";
}

cout << "1" << endl;
```

## 7th Problem

```CPP
int T; 
cin >> T;

while (T--) {
	int x; cin >> x;

	if (x > 24) cout << "YES" << endl;
	else cout << "NO" << endl;
}
```

## 8th Problem

```CPP
string num; cin >> num;

int n = num.size();
int endPos = n - 1;

while (num[endPos] == '0') {
	endPos--;
}

string reversed_number = "";
for (int i = endPos; i >= 0; i--) {
	reversed_number += num[i];
}

cout << reversed_number << endl;

if (reversed_number == num) {
	cout << "YES";
}
else cout << "NO";
```

## 9th Problem

```CPP
int n; cin >> n;

for (int number = 2; number <= n; number++) {
	int num_of_divisors = 0;
	for (int i = 1; i <= number; i++) {
		if (number % i == 0) num_of_divisors++;
	}

	if (num_of_divisors == 2) cout << number << ' ';
}
```

## 10th Problem

```CPP
while (true) {
	int n, m; cin >> n >> m;
	if (n <= 0 || m <= 0) break;

	int start, end;

	if (n < m) start = n, end = m;
	else start = m, end = n;

	int sum = 0;
	for (int i = start; i <= end; i++) {
		cout << i << ' ';
		sum += i;
	}

	cout << "sum =" << sum << endl;
}
```

## 11th Problem

```CPP
int n; cin >> n;
for (int i = n; i > 0; i--) {
	for (int j = 0; j < i; j++) {
		cout << '*';
	}
	
	cout << endl;
}
```

## 12th Problem

```CPP
int n; cin >> n;

int numberAtCurrentLevel = 1;
for (int whitespaces = n - 1; whitespaces >= 0; whitespaces--) {
	for (int i = 0; i < whitespaces; i++) cout << ' ';
	for (int i = 0; i < numberAtCurrentLevel; i++) cout << '*';
	cout << endl;

	numberAtCurrentLevel += 2;
}
```

## 13th Problem

```CPP
int n, a, b; cin >> n >> a >> b;

int sum = 0;
for (int number = 1; number <= n; number++) {
	int sum_of_digits = 0;

	int current_number = number;
	while (current_number) {
		sum_of_digits += current_number % 10;
		current_number /= 10;
	}

	if (sum_of_digits >= a && sum_of_digits <= b) sum += number;
}

cout << sum << endl;
```

## 14th Problem

```CPP
int n; cin >> n;
int fir = 0, sec = 1;

if (n == 1) cout << "0" << endl;
else {
	cout << "0 1 ";
	for (int i = 2; i < n; i++) {
		int next = fir + sec;
		cout << next << ' ';

		fir = sec;
		sec = next;
	}
}
```

## 15th Problem

```CPP
int T; 
cin >> T;

while (T--) {
	int h, x, y; cin >> h >> x >> y;

	h -= y;
	int cnt = 1;

	while (h > 0) {
		h -= x;
		cnt++;
	}

	cout << cnt << endl;
}
```
## 16th Problem

```CPP
int n; cin >> n;
int prim = 0, sec = 0;

for (int i = 0; i < n; i++) {
	for (int j = 0; j < n; j++) {
		int num; cin >> num;
		
		if (i == j) prim += num;
		if (i + j == n - 1) sec += num;
	}
}

cout << abs(prim - sec) << endl;
```