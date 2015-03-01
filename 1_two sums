#include<iostream>
using namespace std;

class Solution {
public:
    vector<int> twoSum(vector<int> &numbers, int target) {

    vector<int> result;
	map<int,int> Hash_map;

	for(int i = 0; i < numbers.size(); i++)
	{
		if(!Hash_map.count(numbers[i]))
		{
			Hash_map.insert(pair<int,int>(numbers[i], i+1));
		}

		if(Hash_map.count(target - numbers[i]))
		{
			int index_one, index_two;
		
			index_one = Hash_map[target - numbers[i]];
			index_two = i+1;
    
            if(index_one < index_two)
            {
			    result.push_back(index_one);
		    	result.push_back(index_two);
		    	
		    	return result;
            }
		}
    }
    
    return result;
    }
};
