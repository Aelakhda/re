#include <iostream>
#include <vector>

void splitList(const std::vector<int>& input, std::vector<int>& smaller, std::vector<int>& bigger) {
    int midpoint = input.size() / 2;

    for (int i = 0; i < midpoint; i++) {
        smaller.push_back(input[i]);
    }

    for (int i = midpoint; i < input.size(); i++) {
        bigger.push_back(input[i]);
    }
}

int main() {
    std::vector<int> input = {1, 2, 3, 4, 5, 6, 7, 8, 9};
    std::vector<int> smaller, bigger;

    splitList(input, smaller, bigger);

    std::cout << "Smaller list: ";
    for (int num : smaller) {
        std::cout << num << " ";
    }
    std::cout << std::endl;

    std::cout << "Bigger list: ";
    for (int num : bigger) {
        std::cout << num << " ";
    }
    std::cout << std::endl;

    return 0;
}
