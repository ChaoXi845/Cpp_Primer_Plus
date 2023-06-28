# Chapter 2  Start Learning C++

This is my solution about exercises of each chapter  

## 1 Display your name and address

```c++
#include <iostream>

int main()
{
    using namespace std;
    cout << "My name is Li Zongrui, a master student of robotics." << endl;
    cout << "My address is Guiyang, Guizhou Province, China.";
    return 0;  
}
```

## 2 Input a distance in *long* and convert it to yard (one *long* = 220 yards)

```cpp
#include <iostream>
double Convert(double);

int main()
{
    using namespace std;
    double distance;
    cout << "Please input a distance in long: ";
    cin >> distance;
    double conv_distance;
    conv_distance = Convert(distance);
    cout << distance << " Long = " << conv_distance << " Yards";
    return 0;
} 

double Convert(double dis)
{
    return 220 * dis;
}
```  

## 3 Use 3 function defined by self and print these below

> Three blind mice  
> Three blind mice  
> See how they run  
> See how they run

And one of the function should be used twice to output the top two lines,
the another function is used twice to output others.

```cpp
#include <iostream>
void FirstFunc();
void SecondFunc();

using namespace std;

int main()
{
    FirstFunc();
    FirstFunc();
    SecondFunc();
    SecondFunc();
    return 0;
}

void FirstFunc()
{
    cout << "Three blind mice" << endl;
}

void SecondFunc()
{
    cout << "See how they run" << endl;
}
```

## 4 Input an age and output how many months are contained of this age

```cpp
#include <iostream>
int main()
{
    using namespace std;
    int age;
    cout << "Enter your age: ";
    cin >> age;
    int mon;
    mon = 12 * age;
    cout << endl << "This age means " << mon << " months";
    return 0;
}
```

## 5 Convert Celsius degree to Fahrenheit degree

```cpp
#include <iostream>
double CtoF(double);

int main()
{
    using namespace std;
    int Cd;
    int Fd;
    cout << "Please enter a Celsius value: ";
    cin >> Cd;
    Fd = CtoF(Cd);
    cout << endl << Cd << " degrees Celsius is " << Fd << " degrees Fahrenheit.";
    return 0;
}

double CtoF(double value)
{
    return 1.8 * value + 32.0;
}
```

## 6 Convert *light year* to *astronomical unit*

```cpp
#include <iostream>
double LYtoAU(double);

int main()
{
    using namespace std;
    double LY;
    double AU;
    cout << "Enter the number of light years: ";
    cin >> LY;
    AU = LYtoAU(LY);
    cout << endl << LY << " light years = "<< AU << " astronomical units.";
    return 0;
}

double LYtoAU(double value)
{
    return 63240 * value;
}
```

## 7 Combine hour and minute into time

```cpp
#include <iostream>
int main()
{
    using namespace std;
    int hour;
    int minute;
    cout << "Enter the number of hours: ";
    cin >> hour;
    cout << "Enter the number of minutes: ";
    cin >> minute;
    cout << "Time: " << hour << ":" << minute;
    return 0;
}
```
