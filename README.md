# max_in_array-0.0.1

#include "stdafx.h"
#include "iostream"
#include "sstream"

using namespace std;


int main()
{
	int max,i,a[10];


	for (string string; getline(cin, string) ; ) {
		istringstream stream(string);
		bool failure = false;
		for (int i = 1; i <= 10; ++i) {
			if (!(stream >> a[i])) {
				failure = true;
				break;
			}
		}

		max = a[1];

		if (!failure) {
			for (int i = 1; i <= 10; ++i) {
				if (a[i] > max) {
					max = a[i];
				}
			}
			cout << max << endl;
			break;
		}
		else {
			cout << "An error has occured while reading numbers from line" << endl;
		}
	}



	system("pause");
	cin.get();

    return 0;
}
