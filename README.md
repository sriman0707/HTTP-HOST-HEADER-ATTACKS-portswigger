           HTTP Host header attacks

So In This report we are going to learn HTTP Host header attacks in simple way


What is mean by Http Host Header Attacks?

An HTTP Host Header Attack happens when a hacker manipulates the "Host" part of a web request.

Scenario:
Imagine you are visiting a banking website, like bank.com, to check your account balance. When your browser sends a request to the bank's server, it includes a Host header like this:
GET /account HTTP/1.1
Host: bank.com
This tells the server to send the correct page for bank.com.
Host Header Attack:
Now, an attacker discovers that the bank’s server doesn't check the Host header properly. They change the request by modifying the Host value to something else, like:
GET /account HTTP/1.1
Host: evil.com

If the bank’s server is vulnerable, it might accept this request and process it as if it were for evil.com, potentially:
1.	Redirecting users to a fake version of the banking site (evil.com), where they can steal login credentials.
2.	Sending a password reset link to a wrong or malicious site controlled by the attacker.
3.	Showing confidential data (like user accounts) to the attacker’s website.
Real-world outcome:
The attacker can trick the bank's server into:
●	Displaying sensitive info on evil.com instead of bank.com.
●	Redirecting legitimate users to a phishing site where their details can be stolen.
Solution:
The bank's server should check and ensure that the Host header is always bank.com and reject or correct any requests with other hostnames.
This is how a simple manipulation of the Host header can lead to major security risks if not properly handled!

So thats the example for It.
