Assume you oversee a small library and would like to develop a program that looks up books using their ISBNs. A list of books with their corresponding ISBN digits is in front of you. After the librarian inputs an ISBN, your software will look through the list to locate the relevant book.  The book's title and other details will be shown if the book is located. A notice stating that the book is not available in the library will appear if it cannot be located.

CODE:-

#include <iostream>
#include <map>
#include <string>

using namespace std;

class Library {
private:
    map<string, string> bookMap;

public:
    Library() {
      
        bookMap["9781449340377"] = "Learning Python";
        bookMap["9781491919538"] = "Python Cookbook";
        bookMap["9781492046287"] = "Fluent Python";
      
    }

    string searchBook(const string& isbn) {
        auto bookIterator = bookMap.find(isbn);
        if (bookIterator != bookMap.end()) {
            return bookIterator->second;
        } else {
            return "Book not available in the library.";
        }
    }
};

int main() {
    Library library;
    string inputISBN;

    cout << "Welcome to the Library!" << endl;
    cout << "Enter the ISBN of the book you want to find: ";
    cin >> inputISBN;

   
    string bookTitle = library.searchBook(inputISBN);
    
    
    cout << "Result: " << bookTitle << endl;

    return 0;
}
