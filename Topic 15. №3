#include <string_view>
using namespace std;

bool NextToken(string_view& sv, char delimiter, string_view& token) {
    if (sv.empty()) {
        return false;
    }
    
    size_t pos = sv.find(delimiter);
    if (pos == string_view::npos) {
        token = sv;
        sv = string_view();
    } else {
        token = sv.substr(0, pos);
        sv.remove_prefix(pos + 1);
    }
    
    return true;
}
