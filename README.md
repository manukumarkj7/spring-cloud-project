# spring-cloud-project

currency conversion application which it has three projects currency conversion, Eureka naming server, forex service. 

request coming from zuul api gateway that  is redirecting to feign client which is implemented in currency conversion  calls the forex service internally and ribbon client included in currency conversion micro service to handling load balancing in round robin fashion.

Both the currency conversion and forex services which is registered in eureka server, It helps to  find the forex service through currency conversion

currency conversion calls the forex service to find the currency conversion and add the quantity to the conversion value.finally send the response 

application built  as maven project  

example to test the application:

GET mapping request  to http://localhost:8000/currency-exchange/from/EUR/to/INR/quantity/10000
