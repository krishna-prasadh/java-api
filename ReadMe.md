{\rtf1\ansi\ansicpg1252\deff0\deflang1033{\fonttbl{\f0\fnil\fcharset0 Calibri;}{\f1\fnil Consolas;}}
{\colortbl ;\red0\green0\blue255;\red127\green0\blue85;\red0\green0\blue0;\red42\green0\blue255;\red63\green127\blue95;\red0\green0\blue192;}
{\*\generator Msftedit 5.41.21.2510;}\viewkind4\uc1\pard\sa200\sl276\slmult1\lang9\f0\fs22  # Agile CRM Java API\par
\par
Agile CRM is a an new breed CRM. You can sign up here - {\field{\*\fldinst{HYPERLINK "http://agilecrm.com"}}{\fldrslt{\ul\cf1 http://agilecrm.com}}}\f0\fs22\par
\par
Requirements\par
============\par
Java 1.5 and later.\par
\par
\par
Installation\par
============\par
You'll need to manually download the following JARs:\par
\pard\sa200\sl276\slmult1{\field{\*\fldinst{HYPERLINK "http://www.java2s.com/Code/Jar/j/Downloadjerseyclient115jar.htm"}}{\fldrslt{\ul\cf1 http://www.java2s.com/Code/Jar/j/Downloadjerseyclient115jar.htm}}}\f0\fs22\par
{\field{\*\fldinst{HYPERLINK "http://www.java2s.com/Code/Jar/j/Downloadjsonjar.htm"}}{\fldrslt{\ul\cf1 http://www.java2s.com/Code/Jar/j/Downloadjsonjar.htm}}}\f0\fs22\par
{\field{\*\fldinst{HYPERLINK "http://www.java2s.com/Code/Jar/j/Downloadjacksoncoreasl192jar.htm"}}{\fldrslt{\ul\cf1 http://www.java2s.com/Code/Jar/j/Downloadjacksoncoreasl192jar.htm}}}\f0\fs22\par
\par
* jersey-client-1.15.jar\par
* jersey-core-1.15.jar\par
* jersey-json-1.15.jar\par
* jackson-core-asl-1.9.2.jar\par
* jackson-mapper-asl-1.9.2.jar\par
* json.jar\par
\par
\pard\sa200\sl276\slmult1  Usage\par
=====\par
\par
TestAgile.java\par
\par
\cf2\b\f1\fs20 import\cf3\b0  java.util.List;\cf0\par
\par
\cf2\b import\cf3\b0  com.agilecrm.api.APIManager;\cf0\par
\cf2\b import\cf3\b0  com.agilecrm.api.ContactAPI;\cf0\par
\cf2\b import\cf3\b0  com.agilecrm.stubs.Contact;\cf0\par
\par
\cf2\b public\cf3\b0  \cf2\b class\cf3\b0  TestAgile\cf0\par
\cf3\{\cf0\par
\cf3     \cf2\b public\cf3\b0  \cf2\b static\cf3\b0  \cf2\b void\cf3\b0  main(String[] args)\cf0\par
\cf3     \{\cf0\par
\cf3\tab\cf2\b try\cf0\b0\par
\cf3\tab\{\cf0\par
\cf3\tab     String baseUrl = \cf4 "{\field{\*\fldinst{HYPERLINK "https://<Your"}}{\fldrslt{\ul\cf1 https://<Your}}}\f1\fs20  Domain>.agilecrm.com/dev"\cf3 ;\cf0\par
\cf3\tab     String userName = \cf4 "AgileCRM username"\cf3 ;\cf0\par
\cf3\tab     String apiKey = \cf4 "AgileCRM apikey"\cf3 ;\cf0\par
\par
\cf3\tab     \cf5 // Create a connection to Agile CRM\cf0\par
\cf3\tab     APIManager apiManager = \cf2\b new\cf3\b0  APIManager(baseUrl, userName, apiKey);\cf0\par
\par
\cf3\tab     \cf5 // Get the Contact API with configured resource\cf0\par
\cf3\tab     ContactAPI contactApi = apiManager.getContactAPI();\cf0\par
\par
\cf3\tab     \cf5 // --------------------- Get contacts -----------------------------\cf0\par
\cf3\tab     List<Contact> contacts = contactApi.getContacts();\cf0\par
\cf3\tab     System.\cf6\i out\cf3\i0 .println(\cf4 "All contacts.. "\cf3  + contacts);\cf0\par
\cf3\tab\}\cf0\par
\cf3\tab\cf2\b catch\cf3\b0  (Exception e)\cf0\par
\cf3\tab\{\cf0\par
\cf3\tab     System.\cf6\i out\cf3\i0 .println(\cf4 "Exception message.. "\cf3  + e.getMessage());\cf0\par
\cf3\tab     e.printStackTrace();\cf0\par
\cf3\tab\}\cf0\par
\cf3     \}\cf0\par
\cf3\}\cf0\f0\fs22\par
\par
See [TestContact.java] for more examples.\par
}
 