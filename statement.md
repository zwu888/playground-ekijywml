```C++ runnable
#include <iostream>

struct A
{
  A() : val() {}
  A(int v) : val(v) {}
  A(A a) : val(a.val) {} 

  int val;
};

int main(int argc, char** argv)
{
  A a1(5);
  A a2(a1);

  std::cout << a1.val + a2.val << std::endl;

  return 0;
}
