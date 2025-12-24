#include <iostream>
#include <string>
#include <vector>
#include <algorithm>
using namespace std;

int main() {
    vector<string> words;
    string word;
    
    while (cin >> word) {
        words.push_back(word);
    }
    
    if (words.empty()) {
        return 0;
    }
    
    vector<int> common_count(26, 0);
    
    for (char c : words[0]) {
        common_count[c - 'a'] = 1;
    }
    
    for (size_t i = 1; i < words.size(); ++i) {
        vector<int> current_count(26, 0);
        for (char c : words[i]) {
            current_count[c - 'a'] = 1;
        }
        
        for (int j = 0; j < 26; ++j) {
            common_count[j] = min(common_count[j], current_count[j]);
        }
    }
    
    for (int i = 0; i < 26; ++i) {
        if (common_count[i] > 0) {
            cout << char('a' + i);
        }
    }
    cout << endl;
    
    return 0;
}
