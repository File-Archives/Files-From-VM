### Micro-services.
<hr />
<ol>
	<li>
		Extract the zip and import the extracted directory in STS.
	</li>
	<li>
		Run the "service registry" application as a java application. This is a eureka server.
		4) run postman and send a POST request to check if order-service is running properly. find "input text" in the root folder of the project, that is the request JSON body to the order service.
		5) check for appropriate response and run cloud gateway.
	</li>
	<li>
		Run the "order-service" application as a java application. This is a eureka client, we can verify that it is running in the eureka server page.
		<img src="Screenshots/run this order service selected file as a java application.PNG"/>
	</li>
	<li>
		Run the "payment service" application as a java application. This is also a eureka client, we can verify that it is running in the eureka server page.
		<img src="Screenshots/run this payment service selected file as a java application.PNG"/>
	</li>
	<li>
		Run postman and send a POST request to check if order-service is running properly. find "input text" in the root folder of the project, that is the request JSON body to the order service.
	</li>
	<li>
		Check for appropriate response and run cloud gateway. Cloud gateway is another eureka client.
	</li>
	<li>
		Send another POST request to order-service through cloud gateway.
	</li>
</ol>
<hr />

### Notes for Micro-services
<ul>
	<li>
		Communication between a service to another service is done using a "RestTemplate".
		<img src="Screenshots/service to service communication, order service with payment service.PNG" />
		CHECK OTHER LINES OF CODE TO SEE HOW TO EXACTLY COMMUNICATE AND SEND A RESPONSE.
	</li>
	<li>
		Load balancer is done using the feign framework. By using this annotation at line 22, check the below image.
		<img src="Screenshots/load balancer, feign framework does this by just putting this annotation in our application.PNG" />
	</li>
	<li>
		If any requests with the tag "order" comes, and after order anything else will be sent to "ORDER-SERVICE" in a load balanced way. (Check the uri property for this).
		<img src="Screenshots/application yaml for gateway.PNG" />
	</li>
</ul>
<hr />
### Support Links - 
https://www.baeldung.com/spring-resttemplate-post-json - View postForObject and CreatePersonUrl.
<hr />