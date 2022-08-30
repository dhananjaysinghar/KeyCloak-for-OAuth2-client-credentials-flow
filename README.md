# KeyCloak-for-OAuth2-client-credentials-flow


## Docker Image: 
~~~
docker run --name keycloak_dev -p 8180:8180 -e KEYCLOAK_ADMIN=admin -e KEYCLOAK_ADMIN_PASSWORD=admin quay.io/keycloak/keycloak:latest start-dev --http-port=8180
~~~

## OAuth Grant types:
~~~
"grant_types_supported": [
"authorization_code",
"implicit",
"refresh_token",
"password",
"client_credentials"
],
~~~

URL:
~~~
curl --location --request POST 'http://localhost:8180/realms/realspeed/protocol/openid-connect/token' \
--header 'Content-Type: application/x-www-form-urlencoded' \
--data-urlencode 'client_id=realspeedApi' \
--data-urlencode 'client_secret=7gaXuSygNR8SLrQs4MpMrd7svxdHRoFn' \
--data-urlencode 'grant_type=client_credentials'


ISS: http://localhost:8180/realms/realspeed
KEYSTORE: http://localhost:8180/realms/realspeed/protocol/openid-connect/certs

All Settings:
http://localhost:8180/realms/realspeed/.well-known/openid-configuration
~~~

### Step-1
![alt text](login_page.jpg)

### Step-2
![alt text](login_page_1.jpg)

### Step-3
![alt text](homepage.jpg)

### Step-4
![alt text](create_realm.jpg)

### Step-5
![alt text](create_realm_2.jpg)

### Step-6
![alt text](realm_homepage.jpg)

### Step-7
![alt text](client_creation.jpg)

### Step-8
![alt text](create_client_1.jpg)

### Step-9
![alt text](create_client_2.jpg)

### Step-10
![alt text](create_JWKS.jpg)

### Step-11
![alt text](client_credentials.jpg)

### Step-12
![alt text](refresh_token_on.jpg)

### Step-13
![alt text](create_client_3.jpg)

### Step-14
![alt text](create_client_4.jpg)

### Step-15
![alt text](add_mapper_to_scope.jpg)

### Step-16
![alt text](add_mapper_to_scope_1.jpg)

### Step-17
![alt text](add_mapper_to_scope_2.jpg)

### Step-18
![alt text](add_mapper_to_scope_3.jpg)

### Step-19
![alt text](Add_scope_to_client.jpg)

### Results:
![alt text](client_credentials_CURL.jpg)
![alt text](JWKS.jpg)
![alt text](JWT_TOKEN.jpg)


# Other Links:
http://www.mastertheboss.com/keycloak/keycloak-with-docker/
https://www.appsdeveloperblog.com/keycloak-client-credentials-grant-example/
https://www.keycloak.org/
