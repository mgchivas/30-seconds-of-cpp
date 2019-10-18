# begin

**Description:**  The find function looks for a matching key in the map container. If matching key is found, the returning value is an iterator with the matching key and corresponding value. If no match is found, the end iterator is returned.

**Example**
```cpp

#include <iostream>
#include <map>

int main(){
    std::map<char,int> sampleMap;

    // insert key-value pairs
    sampleMap['a'] = 1;
    sampleMap['b'] = 2;
    sampleMap['c'] = 3;

    // Look for a matching key
    // if not found, find returns the end of the iterator 
    auto result = sampleMap.find('a');

    // check what was stored in result
    if(result != sampleMap.end()) {
        // result will have the key and the corresponding value if a matching key is found
        std::cout << "Found a match! " << result->first << " " << result->second << "\n";
    }
    else {
        std::cout << "Match was not found\n";
    }

    // Looking for a key not defined
    auto result2 = sampleMap.find('f');
        if(result2 != sampleMap.end()) {
        // result will have the key and the corresponding value if a matching key is found
        std::cout << "Found a match! " << result2->first << " " << result2->second << "\n";
    }
    else {
        std::cout << "Match was not found\n";
    }

}
```
**[See Sample Code](snippets/map/find.cpp)**
**[Run Code](https://rextester.com/DBUQE78443)**