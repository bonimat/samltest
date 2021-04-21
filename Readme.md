# Readme
https://medium.com/disney-streaming/setup-a-single-sign-on-saml-test-environment-with-docker-and-nodejs-c53fc1a984c9

passo 1 :
docker pull kristophjunge/test-saml-idp
passo 2 :
docker run --name=testsamlidp -p 8080:8080 -p 8443:8443 -e SIMPLESAMLPHP_SP_ENTITY_ID=saml-poc -e SIMPLESAMLPHP_SP_ASSERTION_CONSUMER_SERVICE=http://localhost:4300/login/callback -d kristophjunge/test-saml-idp              
5792aa9338d303cdcdc05c2eb7192a7625e9f04c3f4898f82183d345af188fd3
passo 3:
creare delle chiavi apposite
```
openssl req -x509 -newkey rsa:4096 -keyout certs\key.pem 
-out certs\cert.pem -nodes -days 900
```
passo 4:
cd /home/matteo/Workspaces/JavascriptProjects/samltest 
node index.js per avviare

|UID | Username | Password  | Group  | Email|
|----|----------|-----------|--------|------|
|1   | user1    | user1pass | group1 | user1@example.com |
|2   | user2    | user2pass | group2 | user2@example.com |