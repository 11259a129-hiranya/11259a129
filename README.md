
1. basic data types
#include &lt;stdio.h&gt;
int main() {
int a = 10; float b = 5.5; char c = &#39;A&#39;; double d = 123.456789;
printf(&quot;Integer: %d\n&quot;, a);
printf(&quot;Float: %.2f\n&quot;, b);
printf(&quot;Character: %c\n&quot;, c);
printf(&quot;Double: %.3lf\n&quot;, d);
return 0;
}
output
Integer: 10
Float: 5.50
Character: A
Double: 123.457
2. Evaluate Expressions using Library Functions
#include &lt;stdio.h&gt;
#include &lt;math.h&gt;
int main() {
float r=3.0, A=2.0, B=4.0, C=6.0, S=5.0, x=2.0, y=3.0, z=4.0;
printf(&quot;πr² = %.2f\n&quot;, M_PI*r*r);
printf(&quot;(A+B+(2C/3A)+A²+2B) = %.2f\n&quot;, A+B+(2*C/(3*A))+pow(A,2)+2*B);
printf(&quot;√S(S-A)(S-B)(S-C) = %.2f\n&quot;, sqrt(S*(S-A)*(S-B)*(S-C)));
printf(&quot;log(x³+y³+z³) = %.2f\n&quot;, log(pow(x,3)+pow(y,3)+pow(z,3)));
return 0;
}
output
πr² = 28.27
(A+B+(2C/3A)+A²+2B) = 20.00
√S(S-A)(S-B)(S-C) = nan
log(x³+y³+z³) = 4.60

3. Problems in Decision Making Statements
(i) Find the Biggest Among 3 Numbers
#include &lt;stdio.h&gt;
int main() {
int a, b, c;
printf(&quot;Enter three numbers: &quot;);
scanf(&quot;%d %d %d&quot;, &amp;a, &amp;b, &amp;c);
if(a &gt;= b &amp;&amp; a &gt;= c)
printf(&quot;%d is the largest\n&quot;, a);
else if(b &gt;= a &amp;&amp; b &gt;= c)
printf(&quot;%d is the largest\n&quot;, b);
else
printf(&quot;%d is the largest\n&quot;, c);
returon 0;
}
outputEnter three numbers: 5 9 2
9 is the largest

(ii) Find Even or Odd
#include &lt;stdio.h&gt;
int main() {
int num;
printf(&quot;Enter a number: &quot;);
scanf(&quot;%d&quot;, &amp;num);
if(num % 2 == 0)
printf(&quot;%d is Even\n&quot;, num);
else
printf(&quot;%d is Odd\n&quot;, num);
return 0;
}
output
Enter a number: 8
8 is Even

(iii) Arithmetic Operations using Switch Case
#include &lt;stdio.h&gt;
int main() {
int a, b, choice;
printf(&quot;Enter two numbers: &quot;);
scanf(&quot;%d %d&quot;, &amp;a, &amp;b);
printf(&quot;1.Addition\n2.Subtraction\n3.Multiplication\n4.Division\n&quot;);
printf(&quot;Enter your choice: &quot;);
scanf(&quot;%d&quot;, &amp;choice);
switch(choice) {
case 1: printf(&quot;Sum = %d\n&quot;, a + b); break;
case 2: printf(&quot;Difference = %d\n&quot;, a - b); break;
case 3: printf(&quot;Product = %d\n&quot;, a * b); break;
case 4: printf(&quot;Quotient = %.2f\n&quot;, (float)a / b); break;
default: printf(&quot;Invalid choice\n&quot;);
}
return 0;
}
output
Enter two numbers: 10 5
1.Addition
2.Subtraction
3.Multiplication
4.Division
Enter your choice: 1
Sum = 15

4. Problems in Looping Statements
(i) Sum of Series using For Loop
#include &lt;stdio.h&gt;
int main() {
int n, sum = 0;
printf(&quot;Enter n: &quot;);
scanf(&quot;%d&quot;, &amp;n);
for(int i = 1; i &lt;= n; i++)
sum += i;
printf(&quot;Sum of series = %d\n&quot;, sum);
return 0;
}
output
Enter n: 5
Sum of series = 15
1

(ii) Sum of Series using While Loop
#include &lt;stdio.h&gt;
int main() {
int n, i = 1, sum = 0;
printf(&quot;Enter n: &quot;);
scanf(&quot;%d&quot;, &amp;n);
while(i &lt;= n) {
sum += i;
i++;
}
printf(&quot;Sum of series = %d\n&quot;, sum);
return 0;
}
output
Enter n: 5
1 + 2 + 3 + 4 + 5 = 15
Sum of series = 15

(iii) Fibonacci Series
#include &lt;stdio.h&gt;
int main() {
int n, a = 0, b = 1, next;
printf(&quot;Enter number of terms: &quot;);
scanf(&quot;%d&quot;, &amp;n);
printf(&quot;Fibonacci Series: &quot;);
for(int i = 1; i &lt;= n; i++) {
printf(&quot;%d &quot;, a);
next = a + b;
a = b;
b = next;
}
return 0;
}
output
Enter number of terms: 7
Fibonacci Series: 0 1 1 2 3
(iv) Check Prime Number
#include &lt;stdio.h&gt;
int main() {
int n, flag = 0;
printf(&quot;Enter a number: &quot;);
scanf(&quot;%d&quot;, &amp;n);

for(int i = 2; i &lt;= n/2; i++) {
if(n % i == 0) {
flag = 1;
break;
}
}
if(flag == 0)
printf(&quot;%d is a Prime number\n&quot;, n);
else
printf(&quot;%d is not a Prime number\n&quot;, n);
return 0;
}
output
Enter a number: 7
7 is a Prime number

5. Linear Search
#include &lt;stdio.h&gt;
int main() {
int n, key, i, found = 0;
printf(&quot;Enter number of elements: &quot;);
scanf(&quot;%d&quot;, &amp;n);
int arr[n];
printf(&quot;Enter elements: &quot;);
for(i = 0; i &lt; n; i++)
scanf(&quot;%d&quot;, &amp;arr[i]);
printf(&quot;Enter element to search: &quot;);
scanf(&quot;%d&quot;, &amp;key);
for(i = 0; i &lt; n; i++) {
if(arr[i] == key) {
printf(&quot;Element found at position %d\n&quot;, i + 1);
found = 1;
break;
}
}
if(!found)
printf(&quot;Element not found.\n&quot;);
return 0;
}
output
Enter number of elements: 5
Enter elements: 10 20 30 40 50
Enter element to search: 30
Element found at position 3

6. Bubble Sort and Insertion Sort
(a) Bubble Sort
#include &lt;stdio.h&gt;
int main() {
int n, i, j, temp;
printf(&quot;Enter number of elements: &quot;);
scanf(&quot;%d&quot;, &amp;n);

int a[n];
printf(&quot;Enter elements: &quot;);
for(i = 0; i &lt; n; i++)
scanf(&quot;%d&quot;, &amp;a[i]);
for(i = 0; i &lt; n-1; i++)
for(j = 0; j &lt; n-i-1; j++)
if(a[j] &gt; a[j+1]) {
temp = a[j];
a[j] = a[j+1];
a[j+1] = temp;
}
printf(&quot;Sorted array: &quot;);
for(i = 0; i &lt; n; i++)
printf(&quot;%d &quot;, a[i]);
return 0;
}
output
Enter number of elements: 5
Enter elements: 5 2 8 1 3
Sorted array: 1 2 3 5 8

(b) Insertion Sort
#include &lt;stdio.h&gt;
int main() {
int n, i, j, key;
printf(&quot;Enter number of elements: &quot;);
scanf(&quot;%d&quot;, &amp;n);
int a[n];
printf(&quot;Enter elements: &quot;);
for(i = 0; i &lt; n; i++)
scanf(&quot;%d&quot;, &amp;a[i]);
for(i = 1; i &lt; n; i++) {
key = a[i];
j = i - 1;
while(j &gt;= 0 &amp;&amp; a[j] &gt; key) {
a[j + 1] = a[j];
j--;
}
a[j + 1] = key;
}
printf(&quot;Sorted array: &quot;);
for(i = 0; i &lt; n; i++)
printf(&quot;%d &quot;, a[i]);
return 0;
}
output
Enter number of elements: 5
Enter elements: 5 2 8 1 3
Sorted array: 1 2 3 5 8

7. Matrix Manipulation (Addition, Subtraction &amp; Multiplication)
#include &lt;stdio.h&gt;
int main() {
int a[10][10], b[10][10], c[10][10], i, j, k, n;
printf(&quot;Enter size of square matrix: &quot;);
scanf(&quot;%d&quot;, &amp;n);

printf(&quot;Enter elements of Matrix A:\n&quot;);
for(i = 0; i &lt; n; i++)
for(j = 0; j &lt; n; j++)
scanf(&quot;%d&quot;, &amp;a[i][j]);
printf(&quot;Enter elements of Matrix B:\n&quot;);
for(i = 0; i &lt; n; i++)
for(j = 0; j &lt; n; j++)
scanf(&quot;%d&quot;, &amp;b[i][j]);
// Addition
printf(&quot;\nAddition of Matrices:\n&quot;);
for(i = 0; i &lt; n; i++) {
for(j = 0; j &lt; n; j++) {
c[i][j] = a[i][j] + b[i][j];
printf(&quot;%d &quot;, c[i][j]);
}
printf(&quot;\n&quot;);
}
// Subtraction
printf(&quot;\nSubtraction of Matrices:\n&quot;);
for(i = 0; i &lt; n; i++) {
for(j = 0; j &lt; n; j++) {
c[i][j] = a[i][j] - b[i][j];
printf(&quot;%d &quot;, c[i][j]);
}
printf(&quot;\n&quot;);
}
// Multiplication
printf(&quot;\nMultiplication of Matrices:\n&quot;);
for(i = 0; i &lt; n; i++) {
for(j = 0; j &lt; n; j++) {
c[i][j] = 0;
for(k = 0; k &lt; n; k++)
c[i][j] += a[i][k] * b[k][j];
printf(&quot;%d &quot;, c[i][j]);
}
printf(&quot;\n&quot;);
}
return 0;
}
output
Enter size of square matrix: 2
Enter elements of Matrix A:
1 2
3 4
Enter elements of Matrix B:
5 6
7 8
Addition of Matrices:

A + B =

6 8
10 12
Subtraction of Matrices:

A − B =

-4 -4
-4 -4
Multiplication of Matrices:

A × B =

19 22
43 50
8.String Operations
#include &lt;stdio.h&gt;
#include &lt;string.h&gt;
int main() {
char s1[100], s2[100], s3[100];
printf(&quot;Enter a string: &quot;);
gets(s1);
strcpy(s2, s1);
printf(&quot;Copied String: %s\n&quot;, s2);
strcpy(s3, s1);
strrev(s3);
printf(&quot;Reversed String: %s\n&quot;, s3);
strcat(s1, s2);
printf(&quot;Concatenated String: %s\n&quot;, s1);
return 0;
}
output
Enter a string: Hello
Copied String: Hello
Reversed String: olleH
Concatenated String: HelloHello

9.Swapping Numbers (Call by Value)
#include &lt;stdio.h&gt;
void swap(int a, int b) {
int temp = a;
a = b;
b = temp;
printf(&quot;Inside function (Call by Value): a=%d b=%d\n&quot;, a, b);
}
int main() {
int x = 10, y = 20;

swap(x, y);
printf(&quot;Outside function: x=%d y=%d\n&quot;, x, y);
return 0;
}
output
Inside function (Call by Value): a=20 b=10
Outside function: x=10 y=20

10.Swapping Numbers (Call by Reference)
#include &lt;stdio.h&gt;
void swap(int *a, int *b) {
int temp = *a;
*a = *b;
*b = temp;
}
int main() {
int x = 10, y = 20;
0012,1002
swap(&amp;x, &amp;y);
printf(&quot;After swap: x=%d y=%d\n&quot;, x, y);
return 0;
}
output
After swap: x=20 y=10

11.Factorial Using Recursion
#include &lt;stdio.h&gt;
int fact(int n) {
if (n == 0)
return 1;
return n * fact(n - 1);
}
int main() {
int n;
printf(&quot;Enter a number: &quot;);
scanf(&quot;%d&quot;, &amp;n);
printf(&quot;Factorial = %d\n&quot;, fact(n));
return 0;
}
ouput
Enter a number: 5
Factorial = 120

12.Quadratic Equation
#include &lt;stdio.h&gt;
#include &lt;math.h&gt;
int main() {
float a, b, c, d, r1, r2;
printf(&quot;Enter coefficients a, b, c: &quot;);
scanf(&quot;%f %f %f&quot;, &amp;a, &amp;b, &amp;c);
d = b*b - 4*a*c;
if (d &gt; 0) {
r1 = (-b + sqrt(d)) / (2*a);
r2 = (-b - sqrt(d)) / (2*a);
printf(&quot;Roots are real: %.2f and %.2f\n&quot;, r1, r2);
}
else if (d == 0) {
r1 = r2 = -b / (2*a);
printf(&quot;Both roots are equal: %.2f\n&quot;, r1);
}
else {
printf(&quot;Roots are imaginary.\n&quot;);
}

return 0;
}
output
Enter coefficients a, b, c: 1 -5 6
Roots are real: 3.00 and 2.00

13.Structure - Student Info
#include &lt;stdio.h&gt;
struct Student {
int roll;
char name[20];
float marks;
};
int main() {
struct Student s;
printf(&quot;Enter roll, name and marks: &quot;);
scanf(&quot;%d %s %f&quot;, &amp;s.roll, s.name, &amp;s.marks);
printf(&quot;Student Details:\n&quot;);
printf(&quot;Roll: %d\nName: %s\nMarks: %.2f\n&quot;, s.roll, s.name, s.marks);
return 0;
}
output
Enter roll, name and marks: 101 John 85.5
Student Details:
Roll: 101
Name: John
Marks: 85.50

14.Union Example
#include &lt;stdio.h&gt;
union Data {
int roll;
float marks;
};
int main() {
union Data d;
d.roll = 101;
printf(&quot;Roll = %d\n&quot;, d.roll);
d.marks = 89.5;
printf(&quot;Marks = %.2f\n&quot;, d.marks);
return 0;
}
output
Roll = 101
Marks = 89.50

15.Array of Structures

#include &lt;stdio.h&gt;
struct Student {
int roll;
char name[20];
};
int main() {
struct Student s[3];
int i;
for (i = 0; i &lt; 3; i++) {
printf(&quot;Enter roll &amp; name: &quot;);
scanf(&quot;%d %s&quot;, &amp;s[i].roll, s[i].name);
}
printf(&quot;\nStudent List:\n&quot;);
for (i = 0; i &lt; 3; i++) {
printf(&quot;%d %s\n&quot;, s[i].roll, s[i].name);
}
return 0;
}
output
Enter roll & name: 101 John
Enter roll & name: 102 Alice
Enter roll & name: 103 Bob

Student List:
101 John
102 Alice
103 Bob

16.Pointer Arithmetic
#include &lt;stdio.h&gt;
int main() {
int arr[5] = {10, 20, 30, 40, 50};
int *p = arr;
for (int i = 0; i &lt; 5; i++) {
printf(&quot;Value = %d\n&quot;, *(p + i));
}
return 0;
}
output
Value = 10
Value = 20
Value = 30
Value = 40
Value = 50

17.Basic File Operations
#include &lt;stdio.h&gt;
int main() {
FILE *fp;
char text[100];

fp = fopen(&quot;sample.txt&quot;, &quot;w&quot;);
fprintf(fp, &quot;Hello File!&quot;);
fclose(fp);
fp = fopen(&quot;sample.txt&quot;, &quot;r&quot;);
fgets(text, 100, fp);
printf(&quot;File Content: %s\n&quot;, text);
fclose(fp);
return 0;
}
output
File Content: Hello File!
