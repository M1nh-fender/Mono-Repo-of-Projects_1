[What is Spring Security really all about? Java Brains Brain Bytes (youtube.com)](https://www.youtube.com/watch?v=sm-8qfMWEV8&list=PLqq-6Pq4lTTYTEooakHchTGglSvkZAjnE)

- OS, JVM, App Server Security is mostly already taken care of (according to the YouTube)
- So we have to build our own application security
- Threats are always evolving

# Spring Security Introduction
---
- A framework for application security
	- Login and logout functionality
	- Allow/block access to URLs to logged in users
	- Allow/block access to URLs to logged in users AND with certain roles
- Handles common vulnerabilities
	- Session fixation
	- clickjacking
	- click site request forgery
- What it can do
	- Username/password authentication
	- SSO/Okta/LDAP
	- App level Authorization
	- Intra App Authorization like OAuth
	- Microservice security (tokens, JWT)
	- Method level security


# Spring Security 5 Concepts
---
- Authentication -> who are you?
	- ways to check if user is valid is a username and password
		- This is 'knowledge based authentiation'
- Authorization -> Can user do this
- Principal -> Info of logged in user
- How does authorization occur?
	- This is done via 'Granted Authority'
- Roles are a group of authorities....
# Spring Security More Details
---
- 