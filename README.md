# decrypt-cipher

This client can be used to decrypt already encrypted text.

Usages:
WSO2 ciphertool allows to encrypt plain text values using the keystore provided in product. Sometimes we need to decrypt
these cipher text values for different troubleshooting purposes and check the plain text values. This project can be
used for that.

How to run:
1. You can build the project from source or download the pre-built jar provided in https://github
.com/dinusha-dilrukshi/decrypt-cipher/blob/master/prebuilt-jar/org.wso2.samples.decrypt-1.0-jar-with-dependencies.jar.

If you are building from source, clone the repo locally and execute "mvn clean install" to build it. This will create a
executable jar called 'org.wso2.samples.decrypt-1.0-jar-with-dependencies.jar' in the target directory.

2. You can execute org.wso2.samples.decrypt-1.0-jar-with-dependencies.jar in two ways.
(i). Provide inputs as command arguments.
Command for this is;
java -jar org.wso2.samples.decrypt-1.0-jar-with-dependencies.jar <CipherText> <KeystorePath> <KeystoreAlias>
<KeystorePassword>

eg:  java -jar org.wso2.samples.decrypt-1.0-jar-with-dependencies.jar
bBa173t6ThRLQOt6Z5BztDC56MXLAwb9cr6gHRJhWSbAGbIG7KaFxNjAuh9pVt/74tY06yKEt
/SIgL42QDMQMmMjMgmd9KP9VMtVTMw2EMdW55VETgwHmPzfAiL242M77bpZW/Y9/YTanPQk8KStOxIUI4iAM42lm2z3imbHVh0=
/home/dinusha/wso2is-5.3.0/repository/resources/security/wso2carbon.jks wso2carbon wso2carbon

If it executed successfully, decripted value will be printed something similar to follows.

*** Plain Text ***
dinusha
******************

(ii). Execute as interactive commandline inputs
Command for this is (Inputs will be asked one by one);
java -jar org.wso2.samples.decrypt-1.0-jar-with-dependencies.jar

Encrypted Text : bBa173t6ThRLQOt6Z5BztDC56MXLAwb9cr6gHRJhWSbAGbIG7KaFxNjAuh9pVt/74tY06yKEt/SIgL42QDMQMmMjMgmd9KP9VMtVTMw2EMdW55VETgwHmPzfAiL242M77bpZW/Y9/YTanPQk8KStOxIUI4iAM42lm2z3imbHVh0=
KeyStore file path : /home/dinusha/wso2is-5.3.0/repository/resources/security/wso2carbon.jks
KeyStore alias : wso2carbon
KeyStore password : wso2carbon
*** Plain Text ***
dinusha
******************