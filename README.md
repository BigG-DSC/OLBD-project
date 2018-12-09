# SafeAir: find the best places to live in Madrid

## Use Cases

1. A family with two small children wants to move to a new place in Madrid. They are looking for a house in a specific neighbourhood. A requirement for them is a good air quality, especially since their children need to go to school every day. Currently, there is no open system in which they can assess the air quality around a school so they wil have to guess it using their own heuristics.

2. A daughter is looking for a home for her elderly mother in Madrid. She knows that here mother likes to be outside and hence she wants to take this aspect into account. As her mother is very sensitive to bad air, she wants to ensure that the neighbourhood her mom is going to live in will not pose any threads for her health. 

3. A government official of the Communidad de Madrid is tasked to improve the health of the citizens of his city. For this, he wants to assess the threats of different chemicals in the air and use this to rank districts of the city based on their health related risks. 


## The solution: SafeAir
The solution posed is SafeAir. SafeAir uses open linked data to present timed information on the presence of different chemicals in the atmosphere of Madrid. These measurements are linked to information on primary schools, elderly areas and public sports areas in the city. Specificaly these areas are chosen for they target the part of Madrid's population which is most vulnarable to these issues. 

The solution is introduced in the form a easy to use platform primarily consisting of a map architecture. A user is able to look for a specific civic structure in his neighbourhood. Clicking on this structure will reveal additional information of a specific chemaical in that area over time. Additionally, a user can, by specifying a month and chemical, see the impact of chemical on different regions of the Madrid residential area. Altogether, a user will quickly be able to assess the air quality of an area of interest and make well-formed decisions accordingly.


### Development
Development of the system is done as an assignment for the course Open Linked Big Data as part of the EIT Data Science master Exit Year on Universidad Politecnica de Madrid. With the implementation of the system, the authors aim at getting an introductory look at open linked data and how it can be used to create informative systems which can be used by a wide range of stakeholders.


#### Safeair provide a linked data client
The main application is a map created using a Mapbox object on which pointers are placed. The pointers are retrieved by the front-end application using SPARQL queries to the SPARQL endpoint in the back-end.

A user or developper may deploy our application by running the following steps:
- Download the files from the *site* folder and place them at a desired location.
- Run an arbitrary web server which points towards the folder containing the website.
- In your favourite web-browser, navigate to the base URL of the server to visit our landing page.
- Navigate to <url>/map.html to view the final application. Note, the map will only display data once the back-end server is correctly set-up.


#### Back-end
The back-end of the application holds the data used by the application. The back-end can be configured using the following steps:
- Download GraphDB (http://graphdb.ontotext.com/)
- Unpack the files on a desired location
- Install the software on your machine
- Navigate to the graphdb folder in a terminal
- Run the GraphDB endpoint by the command *bin/graphdb -Dgraphdb.workbench.cors.enable=true*
- Open a browser and navigate to *localhost:7200* which will open the GraphDB interface
- Create a new repository named "safeair" with baseurl *http://safeair.es/project/ontology/safeair#*
- Import the RDF files from the RDFs folder of this GIT repository with the Base IRI *http://safeair.es/project/ontology/safeair#*
- Run the front-end application. If all is set-up correctly, you will be able to show the data.


### Licenses
In the project, the following licenced pieces of data and software are used:
- Datos Abiertos Madrid: https://datos.madrid.es/portal/site/egob/menuitem.400a817358ce98c34e937436a8a409a0/?vgnextoid=b4c412b9ace9f310VgnVCM100000171f5a0aRCRD
- Wikidata: https://www.wikidata.org/wiki/Wikidata:Licensing
- Mapbox: https://www.mapbox.com/tos/
- GraphDB: http://graphdb.ontotext.com/documentation/free/


## Developers
Boy Raaijmakers - [@boyraaijmakers](https://github.com/boyraaijmakers) 
Gioele Bigini - [@BigG-DSC](https://github.com/BigG-DSC)

