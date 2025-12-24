#include <iostream>
#include <string>
#include <map>
#include <vector>
#include <algorithm>
#include <cctype>
using namespace std;

int main() {
    int k;
    cin >> k;
    cin.ignore();
    
    map<string, int> freq;
    string word;
    
    while (cin >> word) {
        for (char& c : word) {
            c = tolower(c);
        }
        freq[word]++;
    }
    
    vector<pair<string, int>> words(freq.begin(), freq.end());
    
    sort(words.begin(), words.end(), [](const pair<string, int>& a, const pair<string, int>& b) {
        if (a.second != b.second) {
            return a.second > b.second;
        }
        return a.first < b.first;
    });
    
    for (int i = 0; i < min(k, (int)words.size()); ++i) {
        cout << words[i].first << "\t" << words[i].second << endl;
    }
    
    return 0;
}
