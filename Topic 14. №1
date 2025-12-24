#include <vector>

template <typename T>
void Duplicate(std::vector<T>& v) {
    size_t original_size = v.size();
    v.reserve(v.size() * 2);
    for (size_t i = 0; i < original_size; ++i) {
        v.push_back(v[i]);
    }
}
