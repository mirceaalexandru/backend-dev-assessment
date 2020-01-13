# Backend Assessment

The goal of this test is not to evaluate how fast you deliver results but rather your problem solving and decision making skills.

If you get in "the zone" while working on the test and feel that you can do more then the minimum requirements of the task, please feel free to impress us with your skills and know-how. It will not go unnoticed.

Feel free to use packages, libraries, Frameworks and even starters/code generators or code snippets, but please mention any code that is not yours and justify the use in a sentence or two.

We expect you to use the following technologies:
- NodeJS/Express
- MongoDB

In order to evaluate also DevOps skills, it is required to deploy the project in a containerized environment using Docker (docker-compose or Kubernates are also welcome) and provide the online access link. For the MongoDB database it is warmly suggested to use the free layer provided by MongoDB Atlas.


### We Will be evaluating you on the following:

- Documentation
- Code Structure and software design
- Code readability and style(we expect you to use best practices and indicate what guidelines/best practices you followed)
- Logic behind your decisions and choices
- Error handling
- Testing
- Deployment

### Recommended deliverables:

- Detailed documentation that explains how to build and run the project, (i.e. instructions on how the project has been deployed)
- Detailed list of your choices and justification of the decisions that you feel need to be explained
- Link to a repository where we can find the source code of the project
- List of external libraries, packages, frameworks, starters and any other external code used in the project

## The Task:

Included in this repository you will find a files under /data directory.
Files contain a collections of advertising campaigns, adgroups , ads and ads statistics over time.
Each advertising campaign has following structure:
Campaign 1-> N Ad groups 1 -> N Ads 1 -> N stats

### Campaign
Describes advertising campaign. Campaign is composed of one or multiple adgroups and each adgroup has a set of ads assigned to it
### Ad Group
Describes ad group of advertising campaign
### Ad
Describes ad of particular ad group
### Ad Stats
Describes statistics of particular ad for time t

We would like to create a simple API (following RESTful guidelines) and allow following operations:
- Fetch campaigns:
	- By Id
	- By Status
- Fetch ad groups of particular campaign 
- Fetch ads of particular campaign
- Update existing campaign (every part of campaign structure can be updated: campaign, adgroup and ad)
- Fetch statistics of ad for particular data range:
    - Note that each statistics entry represents stats for date t   
    - With data from statistics, you have to return new field Cost per click
	Cost per click is calculated as:
		cost / clicks

The database collection should be pre-populated every time the service is started with the content of the json files provided. Also, provide a POSTman collection to test the endpoints.

Please write tests wherever and whenever you feel adequate.
