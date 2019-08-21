* Geocoding api call from java - https://stackoverflow.com/questions/12689084/how-to-use-google-geocoding-in-java

### response from google api - 

https://maps.googleapis.com/maps/api/geocode/json?address=india&key=custom-key
09:59:52.096 [main] DEBUG org.springframework.web.client.RestTemplate - HTTP GET https://maps.googleapis.com/maps/api/geocode/json?address=india&key=custom-key
09:59:52.110 [main] DEBUG org.springframework.web.client.RestTemplate - Accept=[text/plain, application/json, application/*+json, */*]
09:59:52.419 [main] DEBUG org.springframework.web.client.RestTemplate - Response 200 OK
09:59:52.436 [main] DEBUG org.springframework.web.client.RestTemplate - Reading to [java.lang.String] as "application/json;charset=UTF-8"
{
   "error_message" : "The provided API key is invalid.",
   "results" : [],
   "status" : "REQUEST_DENIED"
}

