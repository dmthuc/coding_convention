# C++ coding convention

This is based on the guideline from the book the C++ programming language by Bjarne Stroustrup -- https://www.amazon.com/C-Programming-Language-4th/dp/0321563840
## Bracing style
The open brace is always on the same line with the declaration except function.
```cpp
int main()
{
	for (int x = 0; x < 10; ++x) {
		cout << x << '\n';
	}
}
```
## User-defined type
User-defined type like class and enum have first letter capitalized. Name class with a noun. Words are separated by underscore. 
```cpp
class Customer_info {
public:
	enum class Package_type {standard, premium, luxury};
};
```
## Variable and Function
Variables and functions are named with first lower-case character. Words are separated by underscore. 
```cpp
class Customer_info {

};

std::string get_file_content(const std::string& filename) {
	std::string fake_content;
	return fake_content;
}

Customer_info parse_Customer_info(const std::string& filename) {
	Customer_info ret{};
	return ret;
}
```
## Namespace
Namespace are named with all lower-case characters. Words are separated by underscore.
```cpp
namespace category {
	class Category_classifier {
	
	};
}
```
## Macro
Marco are named with all upper-case characters. Words are separated by underscore.
```cpp
#define NUMBER_OF_DISKS 10
```
## Class member variable
Class member variables (not applied with struct) are named like normal variable and always ending with underscore.
```cpp
class Customer_info {
private:
	int age_;
};
```
## Comment
The following lines are from the book The C++ programming language chapter 9:

- A comment for each source file stating what the declarations in it have in common, references to manuals, the name of the programmer, general hints for maintanance, etc.

- A comment or each class, template, and namespace

- A comment for each class , template, and namespace

- A comment for each nontrivial function stating its purpose, the algorithm used (unless it is obvious), and maybe something about the assumptions it makes about its enviroment

- A comment for each global and namespace variable and constant

- A few comments where the code is nonobvious and/or nonportable

- Very little else
## General advice
Try to name thing as the way they are so other could understand your code easily. Long and unambiguous name is prefer over short name.
