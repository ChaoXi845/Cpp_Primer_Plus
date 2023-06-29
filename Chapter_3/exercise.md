# Chapter 3 Data Process

## 1 Convert *cm* to *m* and *cm*

```cpp
#include <iostream>
int main()
{
    using namespace std;
    const int para = 100;
    int height;
    cout << "Please enter your height: ";
    cin >> height;
    cout << "Your height is: " << height << "cm\n";
    int height_cm, height_m;
    height_cm = height % para;
    height_m = height / para;
    cout << "Your height is: " << height_m << "m " << height_cm << "cm";
    return 0;
}
```

## 2 Report BMI

```cpp
#include <iostream>
int main()
{
    using namespace std;
    double height_cm, height_m;
    const int para = 100;
    double weight, height, BMI;
    cout << "Enter your body's data: \n";
    cout << "First, enter your height of cm part: ";
    cin >> height_cm;
    cout << "Next, enter your height of m part: ";
    cin >> height_m;
    cout << "Finally, enter your weight(Kg): ";
    cin >> weight;
    height = height_m + height_cm / 100;
    BMI = weight / (height * height);
    cout << "Your BMI is: " << BMI;
    return 0;
}
```

## 3 Convert *degrees*, *minutes* and *seconds* to *degrees*

```cpp
#include <iostream>
const int para = 60;
int main()
{
    using namespace std;
    double degree, minute, second;
    double latitude;
    cout << "Enter a latitude in degrees, minutes, and seconds: \n";
    cout << "First, enter the degrees: ";
    cin >> degree;
    cout << "Next, enter the minutes of arc: ";
    cin >> minute;
    cout << "Finally, enter the seconds of arc: ";
    cin >> second;
    latitude = (second / 60 + minute) / 60 +degree;
    cout << degree << " degrees, " 
         << minute << " minutes, "
         << second << " seconds = " 
         << latitude << " degrees";
    return 0;
}
```

## 4 Convert *seconds* to *days*, *hours*, *minutes* and *seconds*

```cpp
#include <iostream>
const int DtH = 24;
const int time = 60;
const int DtM = DtH * time;
const int DtS = DtM * time; 
int main()
{
    using namespace std;
    long seconds;
    int day, hour, minute, second;
    cout << "Enter the number of seconds: ";
    cin >> seconds;
    day = seconds / DtS;
    hour = (seconds - day * DtS) / (time * time);
    minute = (seconds - day * DtS - hour * time * time) / time;
    second = (seconds % DtS) % time ;
    cout << seconds << " seconds = "
         << day << " days "
         << hour << " hours "
         << minute << " minutes "
         << second << " seconds.";
    return 0;  
}
```

## 5 Calculate the percentage of the US population in the global population

```cpp
#include <iostream>
int main()
{
    using namespace std;
    long double us_p, glo_p;
    double percentage;
    cout << "Enter the world's population: ";
    cin >> glo_p;
    cout << "Enter the population of the US: ";
    cin >> us_p;
    percentage = us_p / glo_p * 100;
    cout << "The population of the US is " << percentage << "% of the world population.";
    return 0;
}
```

## 6 Calculate fuel consumption per 100 KM

```cpp
#include <iostream>
const int para = 100;
int main()
{
    using namespace std;
    double kilemeter, liter, comsumption;
    cout << "Enter the kilemeter your car has run: ";
    cin >> kilemeter;
    cout << "Enter the fuel consumption of your car in liter: ";
    cin >> liter;
    comsumption = liter / (kilemeter / 100);
    cout << "The fuel comsumption per 100 KM is: " << comsumption << " L/KM.";
    return 0;
}
```

## 7 Convert *L/KM* to *mpg*

```cpp
#include <iostream>
const double para = 62.14 * 3.875;
int main()
{
    using namespace std;
    double lkm, mpg;
    cout << "Enter your fuel comsumption in L/100KM: ";
    cin >> lkm;
    mpg = para / lkm;
    cout << "The fuel comsumption: " << lkm << " L/100KM = " << mpg << " mpg.";
    return 0;
}
```
