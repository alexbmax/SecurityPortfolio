# Security Incident Report #


# Section 1: Identify the network protocol involved in the incident #
HTTP protocol and DNS protocol 





# Section 2: Document the incident #
Users reported being prompted to update browser via download and noted that after download, they were redirected to a different website and computers running more slowly. 


Ran network protocol analyzer tcpdump tool and accessed website via sandbox environment. Logs showed successful DNS protocol connection to yummyrecipesforme.com. Download executed and then new DNS request sent for greatrecipes.com. 

After analyzing source original HTTP source code and comparing to current code, it appears javascript code was added to initiate download and redirect to other website. 

Admin tried to log in to admin account and could not. 

Appears to be a brute force attack. 

Recommend password policies be updated to ensure stronger passwords as well as using hashing or salting to increase password security. 




# Section 3: Recommend one remediation for brute force attacks # 
Stricter password policy 
Salting password 




