#include <iostream>
#include <vector>
#include <algorithm>
#include <iterator>

using namespace std;

int main() {
    int n;
    int a, b;
    int m, maxm = 0;
    bool flag = true;
    vector<int> vector1;
    vector<int> vector0, vector0max;
    vector<vector<int >> vector2;
    cin >> n;
    for (int i = 0; i < n; ++i) {
        cin >> a >> b;
        vector1.push_back(a);
        vector1.push_back(b);
        vector2.push_back(vector1);
        vector1.clear();
    }
    sort(vector2.begin(), vector2.end());
    auto iterator2 = vector2.begin();
    while (iterator2->front() <= vector2.begin()->back()) {
        vector0.push_back(iterator2->front());
        vector0.push_back(iterator2->back());
        int q = iterator2->back();
        m = 1;
        for (vector<int> x:vector2) {
            if (x.front() >= q) {
                vector0.push_back(x.front());
                vector0.push_back(x.back());
                q = x.back();
                m++;
            }
        }
        if (maxm <= m) {
            maxm = m;
            vector0max = vector0;
        }
        vector0.clear();
        iterator2++;
    }
    cout << maxm << endl;
    for (int x:vector0max) {
        cout << x;
        if (flag) {
            cout << "-";
            flag = false;
        } else {
            cout <<endl;
            flag = true;
        }
    }
    return 0;
}
