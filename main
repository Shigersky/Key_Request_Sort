#include <iostream>
#include <vector>
#include <set>
#include <queue>

std::string myString1 = "abcdf pqoeipwoeqop";
std::string myString2 = "1234 pqoei323232op";
std::string myString3 = "eueue oeiiweepwoe";
std::string myString4 = "1234 pqoei323232op";
std::string myString5 = "1235 pqoei323w32op";
std::string myString6 = "eueue oeiiweepwoe";


std::vector<std::string> requests = { myString1, myString2, myString3, myString4, myString5, myString6 };
std::multiset<std::string, std::string> sortedRequests;


std::vector<std::string> compareKey(std::vector<std::string> request)
{
	std::multiset <std::string> prime;
	std::queue <std::string> basic;

	size_t requestSize = request.size();

	
	for (size_t i = 0; i < requestSize; i++)
	{


		if (request[i][0] >= 97 && 120 >= request[i][0])
			prime.insert(request[i]);

		else
		{
			
			basic.push(request[i]);

		}
	}
		
	std::vector<std::string> allRequests;
	allRequests.reserve(request.size());

	auto it = prime.begin();
	

	while (it != prime.end())
	{
		allRequests.emplace_back(*it);
		it++;
	}

	while (!basic.empty())
	{
		
		allRequests.emplace_back(basic.front());
		basic.pop();
	}

	
	return allRequests;

}

int main()
{



	std::vector<std::string> result = compareKey(requests);
	
	for (std::string& str : result)
		std::cout << str << '\n';


	return 0;
}
