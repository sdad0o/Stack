#include <iostream>
using namespace std;
template <class type>
class stack
{
private:
	type* element;
	int top, size;
public:
	stack(int size)
	{
		element = new type[size];
		top = -1;
		this->size = size;
	}
	bool IsFull()
	{
		return (top == size - 1);
	}
	bool IsEmpty()
	{
		return(top == -1);
	}
	int GetSize()
	{
		return size;
	}
	void push(type e)
	{
		if (IsFull())
		{
			cout << " STACK IS FULL !!\t";
				assert(0);
		}
		++top;
		element[top] = e;
    }
	type pop()
	{
		if (IsEmpty())
		{
			cout << " STACK IS EMPTY !! \t";
			assert(0);
		}
		return element[--top];
	}
	type getTop()
	{
		if (IsEmpty())
		{
			cout << " STACK IS EMPTY !! \t";
			assert(0);
		}
		return element[top];
	}
	~stack()
	{
		delete[]element;
	}
};
int main()
{
	return 0;
}
