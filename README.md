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
