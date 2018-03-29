# decrypt-cipher

This client can be used to decrypt already encrypted text.

Usages:<br />
-------------
WSO2 ciphertool allows to encrypt plain text values using the keystore provided in product. Sometimes we need to decrypt
these cipher text values for different troubleshooting purposes and check the plain text values. This project can be
used for that. <br />

How to run:<br />
-----------------
1. You can build the project from source or download the pre-built jar provided [here](prebuilt-jar/org.wso2.samples.decrypt-1.0-jar-with-dependencies.jar)  

If you are building from source, clone the repo locally and execute "mvn clean install" to build it. This will create a
executable jar called 'org.wso2.samples.decrypt-1.0-jar-with-dependencies.jar' in the target directory. <br />

2. You can execute org.wso2.samples.decrypt-1.0-jar-with-dependencies.jar in two ways. <br />
(i) Provide inputs as command arguments. <br />
Command for this is; <br />
**java -jar org.wso2.samples.decrypt-1.0-jar-with-dependencies.jar $CipherText  $KeystorePath  $KeystoreAlias
$KeystorePassword** <br />

eg:  java -jar org.wso2.samples.decrypt-1.0-jar-with-dependencies.jar
bBa173t6ThRLQOt6Z5BztDC56MXLAwb9cr6gHRJhWSbAGbIG7KaFxNjAuh9pVt/74tY06yKEt
/SIgL42QDMQMmMjMgmd9KP9VMtVTMw2EMdW55VETgwHmPzfAiL242M77bpZW/Y9/YTanPQk8KStOxIUI4iAM42lm2z3imbHVh0=
/home/dinusha/wso2is-5.3.0/repository/resources/security/wso2carbon.jks wso2carbon wso2carbon <br />

If it executed successfully, decripted value will be printed something similar to follows. <br />

*** Plain Text *** <br />
dinusha <br />
****************** <br />

(ii) Execute as interactive commandline inputs <br />
Command for this is (Inputs will be asked one by one); <br />
**java -jar org.wso2.samples.decrypt-1.0-jar-with-dependencies.jar** <br />

Encrypted Text : bBa173t6ThRLQOt6Z5BztDC56MXLAwb9cr6gHRJhWSbAGbIG7KaFxNjAuh9pVt/74tY06yKEt/SIgL42QDMQMmMjMgmd9KP9VMtVTMw2EMdW55VETgwHmPzfAiL242M77bpZW/Y9/YTanPQk8KStOxIUI4iAM42lm2z3imbHVh0= <br />
KeyStore file path : /home/dinusha/wso2is-5.3.0/repository/resources/security/wso2carbon.jks <br />
KeyStore alias : wso2carbon <br />
KeyStore password : wso2carbon <br />
*** Plain Text *** <br />
dinusha <br />
****************** <br />
