## Quiz 1

### Q1

The data type of the variable PI is double.

```
#define PI 3.14
```

> False

### Q2

The source code of program is as follows:

```
int main(int argc, char *argv[])
{
...
}
```

The source code has been compiled to program hello, when you run it as follows, what argc will be?

./hello I LOVE CPP

> 4

## Quiz 2 

sizeof() is an operator.

## Quiz 3

size_t is similar to unsigned int. IS ALWATS GREATER THAN 0.

## Quiz 4

typedef is to create an alias for an existing data type, not used to create a new data type.

## Quiz 5

```
int num = 1;
int another = 2;
//You cannot change the value the p1 points to through p1
const int * p1 = &num;
*p1 = 3; //error
num = 3; //okay
//You cannot change value of p2 (address)
int * const p2 = &num;
*p2 = 3; //okay
p2 = &another; //error
//You cannot change either of them
const int* const p3 = &num;
```

### Q4

What's the output of the following code on your PC (64bit OS and CPU)?
```
int * numbers = new int[8];
cout << sizeof(numbers) << endl;
```

> 8

### Q5

What's the output of the following code?

```
    int * numbers = new int[8];

    char * pc = (char*) numbers;

    *numbers = 0x0A0B0C0D;

    cout << (int)pc[3] << endl;
```

> 10

### Q6

The following code can be compiled successfuly.

```
double value = 0.0;

double * const p = &value;

p[0] = 2.0;
```

> True

### Q7

The following code can be compiled successfuly.

```
double value = 0.0;

const double * p = &value;

value = 2.0;
```

> True

## Quiz 6

### Q1

What's the ouput of function sum()?

```
int main()
{
    int cookies[8] = {1, 2, 4, 8, 16, 32, 64, 128};
    int n = sum_arr(cookies, 3);
}
int sum_arr(int arr[], int n)
{
    std::cout << sizeof arr;
    return 0;
}
```

> 4 or 8

## Quiz 7

```
norm_ptr = norm_l1; //Pointer norm_ptr is pointing to norm_l1
norm_ptr = &norm_l2; //Pointer norm_ptr is pointing to norm_l2
float len1 = norm_ptr(-3.0f, 4.0f); //function invoked
float len2 = (*norm_ptr)(-3.0f, 4.0f); //function invoked
```

### Q2

> No default arguments in C. They are only in C++.

### Q3

If we have the following 3 functions, which will be called by "sum(3.0, 4);"?

```
int sum(int x, int y)
{
    cout << "sum(int, int) is called" << endl;
    return x + y;
}
float sum(float x, float y)
{
    cout << "sum(float, float) is called" << endl;
    return x + y;
}
double sum(double x, double y)
{
    cout << "sum(double, double) is called" << endl;
    return x + y;
}
```

> None of the above

### Q7

There is a function template. The specialization is correctly implemented in the following code.
```
template <typename T>
T sum(T x, T y)
{
     cout << "The input type is: " << typeid(T).name() << endl;
}

struct Point {
     int x;
     int y;
};

template
Point sum<Point>(Point pt1, Point pt2)
{
     cout << "The input type is: " << typeid(pt1).name() << endl;
     Point pt;
     pt.x = pt1.x + pt2.x;
     pt.y = pt1.y + pt2.y;
     return pt;
}
```

> False
> should be: template<> Point sum(Point pt1, Point pt2) {}

### Q8

If you forget to put a stopping rule in a recursive function, the function will repeatedly call itself, like a never-ending loop.

> False. It will lead to a stack overflow error because each function call will consume some stack memory and the stack size is limited.

### Q9

If you have a function template in C++, the generated program will create different functions based on the template when the program is executed.

> False. The functions can only be created during the compilation, not the program's execution.

## Quiz 8

### Q2

> Most mobile phones nowadays use ARM CPU.

### Q3

> The instruction set architecture for ARM processors is RISC.

### Q4

> ROI (Region of interest) in CvMat can be used to crop a region of a matrix/image without hard memory copy.

### Q5

> AVX is the SIMD extension to the x86 instruction set architecture.
> NEON is the SIMD extension to the ARM instruction set architecture.
> RVV is the SIMD extension to the RISC-V instruction set architecture.

## Quiz 9

### Q3

What's the output of the source code?

```
class Hello {
	float num;
	static int value;

public:
	int sum(int i, int j) { return i + j; }
	void setValue(int v) { value = v; }
	int getValue() { return value; }
};

int main()
{
	Hello h1, h2;
	h1.setValue(5);
	std::cout << h2.getValue() << std::endl;
}
```

> Link error.

## Quiz 10

```
    // prefix increment
    MyTime& operator++()
    {
        this->minutes++;
        this->hours += this->minutes / 60;
        this->minutes = this->minutes % 60;
        return *this; 
    }

    // postfix increment
    MyTime operator++(int)
    {
        MyTime old = *this; // keep the old value
        operator++();  // prefix increment
        return old; 
    }
```


### Q3 

Assignment operator '=' can be overloaded by a non-member function.

> False

## Quiz 11

### Q7

Please read the following code and choose correct answers:

```
class Person
{
    char * name;
  public:
    Person()
    {
        name = new char[128];
    }
    ~Person()
    {
        delete name;
    }
};


int main()
{
    Person p1;
    Person p2;
    p1 = p2;
    return 0;
}
```

> The code can be compiled without error.
> Runtime error.
> It can cause memory double free problem.
> It can cause memory leak.

## Quiz 14

### Q5

The following source code cannot be compiled successfully.

```
double gmean(double a, double b)
{
    if (a < 0 || b < 0)
        throw string("bad arguments");

    return std::sqrt(a * b);
}

int main()
{
    try{
        gmean(3, -3);
    }
}
```

> True

