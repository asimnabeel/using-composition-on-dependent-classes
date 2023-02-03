# using-composition-on-dependent-classes
using composition on dependent classes
composition using #C++
#include<iostream>
#include<string>
using namespace std;
class Time
{
int hr, min;
public:
Time()
{
hr = 0;
min = 0;
}
Time(int h, int m)
{
hr = h;
min = m;
}
void set_time(int h,int m)
{
hr = h;
min = m;
}
int get_hr()
{ 
return hr;
}
int get_min()
{
return min;
}
void Time_display()
{
cout << "Time:" << hr << ":" << min << endl;
}
};
class Date
{
int day, mon, year;
public:
Date()
{
day = 0;
mon = 0;
year = 0;
}
Date(int d,int mon,int y)
{
day = d;
mon = mon;
year = y;
}
void set_Date(int d, int m1, int y)
{
day = d;
mon = m1;
year = y;
}
int get_day()
{
return day;
}
int get_mon()
{
return mon;
}
int get_year()
{
return year;
}
void Date_display()
{
cout << "Date:" << day << "/" << mon << "/" << year << endl;
}
};
class Event
{
string event_Name;
Time event_time;
Date event_date;
public:
Event(string name, int h, int m, int d, int m1, int y)
{
event_Name = name;
event_time.set_time( h, m);
event_date.set_Date(d, m1, y);
}
void event_display()
{
cout << "Event Name:" << event_Name << endl;
event_time.Time_display();
event_date.Date_display();
}
};
int main()
{
Event E("Eid", 8,56, 9, 6, 2024);
E.event_display();
}
