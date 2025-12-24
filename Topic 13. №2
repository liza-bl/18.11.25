#include <iostream>
#include <string>
#include <map>
#include <set>
#include <vector>
#include <algorithm>
using namespace std;

int main() {
    int n;
    cin >> n;
    
    map<int, set<string>> page_words;
    
    for (int i = 0; i < n; ++i) {
        string word;
        int page;
        cin >> word >> page;
        page_words[page].insert(word);
    }
    
    for (const auto& entry : page_words) {
        cout << entry.first;
        for (const auto& word : entry.second) {
            cout << " " << word;
        }
        cout << endl;
    }
    
    return 0;
}
