Determine what kind of system you need
Do this once you have the requirements defined (Functional and NFR)

Types of applications

- Web Apps
	- Websites, the most common type of applications these days
	- JavaScript will likely be used
	- User initiated actions
	- Large scale
	- Short focused actions
	- User interface and UX required
- Web API
	- Similar to Web App but serves data intead of web pages
	- Exposes API that other applications and programs can use
	- REST is the most popular
		- URL + parameters + VERB
		- Can be used generically by all kinds of applications
	 - Very accessible
	 - Suited for client initiated actions
	 - Data retrieval and storage
	 - Short focused actions
- Mobile Apps
	- Runs on smart phones
	- Will connect with Web API's
	- User interactions (Games, social)
	- Location sensitive apps
- Console App
	- No fancy UI
	- Requires technical knowledge to run them
	- Limited interactions with user
		- Some options to run but not much interaction
	- Long running processes
	- Short actions by trained power users, familary with terminal commands
- Services
	- No UI at all
	- Managed by a service manager (such as in windows, service manager)
	- Long running processes
	- No user interactions
- Desktop applications
	- Run mainly on a PC
	- All resources on local PC
	- Might connect to the web
	- Works offline
	- UI should be great (MS Word is an example)
	- User centric actions
	- Heavy gaming

### Summary

There are more types now we have cloud computing such as Lambda functions in AWS or Azure Functions. There are various others.

We will usually need to mix and match from the application types and the full system will require more that one type to be a fully functional system.