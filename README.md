\\Учимся прогать на Git
#include <iostream>
#include <string>
using namespace std;
class Game
{
public:
	string name;
	void print() {

		cout << name << "dog run" << endl;
	};
private:
	string genre;
	void prinT() {
		cout <<  genre << "\tmmo" << endl;


	}
};

	enum Season {
		leto,//3
		zima,//1
		vesna,//2
		osen//4
	};
	class Seasons {
	public:
		Season s = leto;
		void SeasonsChange() {
			switch (s) {
			case leto: s = osen; break;
			case osen: s = zima; break;
			case zima: s = vesna; break;
			case vesna: s = leto; break;
			}
		}

		Season get_s() {
			return s;
		};
	};

	class ReverseSeasons : public Seasons {
	public:

		void SeasonsChange() {
			switch (s) {
			case leto: s = vesna;
				break;
			case vesna: s = zima;
				break;
			case zima: s = osen;
				break;
			case osen: s = leto;
				break;
			}
		}
	};