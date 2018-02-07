Overview.

I. Problem Summary.

Having a rare disease or a family member who has a rare disease can be a huge challenge for all family members. The uncertainty that people face in this situation is very disheartening. Even on the internet, there is not a lot of information and resources about every existing disease. For that reason, the common problem that people face is unpreparedness for the financial toll that the disease can have on the family.

There are a lot of factors that should be accounted when looking at the cost of having a rare disease. They include direct healthcare costs like medication and treatments, indirect costs like the lost opportunity for the patient and the caregiver. Since most of the health insurance companies do not cover rare disease treatments and orphan drug costs there are very high costs associated with having a rare disease. Patients cannot rely on health insurance for such diseases.

For most rare diseases, there is little to no websites that can help patients and families learn about the disease cost and initial steps to take. For the few more common rare diseases there is some insight online, however, most of the information on costs comes from scholarly articles that are usually have been created overseas or a long time ago.

II. Goal.

- To inform rare disease patients and their families about the disease.\
- To give an accurate prediction of medical and non-medical financial costs of having a rare disease that is specific to the type of disease, stage, location, and age of the patient.\
- To predict the costs for 3 years in future.\
- To show that there are other financial costs associated with having a rare disease like the cost of lost opportunity.\
- To display the breakdown of costs and predictions.\
- To convey the sensitive information in a way that is friendly, non-frightening, accurate and easy to understand.

Design.

The Rare Disease Patient Portal is a web application. It was chosen because it is the most accessible for people with no knowledge in programming or access to mobile devices.

The initial user input was separated in a two-page story because the patients and their family will be under a lot of stress already and the portal will provide additional information on every page and explicit reasoning for why their data is being collected and how it affects the results. Similarly, the result page was separated into three pages. That ensures that the users will not see potentially traumatic information without their consent and willingness to see that information. For example, if the family only wants to see one-year cost prediction, they will be overwhelmed and stressed to see that the costs will only grow in three years.

On the backend, the portal has six data tables: disease, location, therapist, medicine, therapy requirement, and medicine requirement. The disease table will contain information about every disease in the system, including description, related links, additional information about current research being done and encouraging words for newly diagnosed patients. The location table contains all states of the United States of America, therapy and medicine cost factors for following three years for each state. The therapist and medicine tables have the name, description, and cost for each one of them. The therapy requirement and medicine requirement tables serve as connecting piece between the disease and their medicine and therapies that includes sessions per year and units per year.

The user will not see all of the underlying analytics and computations because that information can be repetitive and unnecessary especially when users are just trying to find out about such sensitive topic, nevertheless, the portal will still provide additional insight into what goes into the final results on every one of the result pages. The one-year and three-year prediction result pages will have a bar graph with insight under it, however, the cost of lost opportunity result page will only contain text explanation of how much extra care the patient will need and how much will be lost because of it.

    The overall design is focused less on telling the user how much money the disease will cost them, but rather highlight the causes for such costs and add additional support and information about the disease. The app lets the user know what therapies and medicines will be required, as well as, what is the amount of therapy sessions and medicine they will need for the particular rare disease.

Implementation.

I. Web Scraping.

    Any medical information is considered confidential and is usually highly hard to find on the internet. With rare diseases, the task of finding the dataset is even harder. With no dataset available for the Rare Disease Patient Portal, the data has been gathered from different sources to create new datasets.

    Diseases information was crawled from WebMD, Wikipedia, National Organization for Rare Diseases, PubMed and several scholarly articles. Medicine information was collected from Mayo Clinic, WebMD, Drugs.com. Therapists information was accumulated from Mayo Clinic, and salary information was gathered from Bureau of Labor Statistics and Salary.org. State-wise salary details were acquired from Wikipedia.

II. Cost of Rare Disease Estimation.

Cost of rare disease included the costs of therapies and medicines combined:

- Annual Therapy Cost = Session Cost * Therapy Location Cost Factor * Sessions Per Year\
- Annual Medicine Cost = Unit Cost * Medicine Location Cost Factor * Units Per Year\
- Annual Cost = Annual Therapy Cost + Annual Medicine Cost

The unit cost is the cost of medicine per dose, which generalized the cost independent of nature. The location cost factors are calculated based on basic unit/session price and scaled using each state's sales tax. Units per year and sessions per year are dependent on the disease and its requirements.

Furthermore, for the three-year prediction, different location cost factor has been used depending on each state's inflation rates, while the unit/session cost and the units/sessions per year remained static.

III. Lost Opportunity Estimation.

    To calculate the lost opportunity of the patient or the caretaker, we gathered the user input of their annual salary. Since there are 2080 hours in a year for an average full-time position, the annual salary was divided by 2080:

- Lost Opportunity = (Annual Salary / 2080) * Annual Hours of Therapy

    Here, the Annual Salary is what user will input initially or a default value of the national average of $60,000. A number of hours of therapy are calculated based on the suggested number of therapies annually.

IV. Front End.

The web portal consisted of seven pages.

1\. Homepage: This is the landing page for the rare disease patient, where the user is provided with general information about the portal and what it can do, as well as, the choice of rare diseases.\
2\. Disease information: After clicking on one of the diseases, the user will see the general knowledge of the disease, and will be prompted with two buttons for the stage of the disease: "Newly Diagnosed", "Already Known for a while". All of the chosen information by the user is saved as user input and sent to the result.\
3\. Query: Based on the stage of the disease, the user will see some information on either where to start and what to expect or recent research on the disease. Both stages will be recommended websites for their particular disease. Under all this text will be the user input fields: name, age, state, annual salary. Each one of these fields will have the reasoning behind those questions.\
4\. Results homepage: This page will provide information on medicine requirements and therapy requirements for the disease. Under it, there will be three buttons: "Get annual cost of treatment", "Get 3 years cost prediction", "Check Lost Opportunity".\
5\. Annual cost: This page will have a bar chart separated by medicine cost and therapy cost, under the graph there will be the breakdown of the cost.\
6\. Three-year prediction: Similarly to the annual cost page, this page will have a bar chart separated by medicine cost and therapy cost, however, this time there will be three times the bars. The breakdown of the cost by each year will be provided under the graph.\
7\. Lost opportunity: This page will have the number of hours required for therapy throughout the year and calculated cost of lost opportunity.

Results.

Overall, the Rare Disease Patient Portal achieved all of the stated goals of this project and effectively solved the problem.  This has been a successful proof of consent for cost prediction for rare disease based on various factors.

Future Work.

Even though all of the goals of the project has been met, there is still a lot of room for improvement and potential to be built upon. One of the biggest improvements that could be made is having a dataset and information about diseases.

If there is a possibility of having a better dataset, all of the potential rare diseases could be added to the database, as well as, their medicine and treatment requirements. This would add a bigger scope to the application and ensure that it's being used by real users. Currently, the app only provides information in US Dollars and bases the location on the United States. To create an accessible and internationally recognized application, the rare disease patient portal could have a bigger dataset of locations.

One of the other changes that could be made is tweaking the algorithm for lost opportunity prediction to also take into account the number of hours spent taking care of the patient outside of treatment. Currently, there was not enough information provided online on how much the caretakers spend on taking care of the patient and the portal couldn't expect the users to input this information since some of the patients were newly diagnosed.

Works Cited.

1\. List of U.S. states by income. (n.d.). In Wikipedia. Retrieved October 15, 2017, from https://en.wikipedia.org/wiki/List_of_U.S._states_by_income\
2\. Drugs. (n.d). In WebMD. Retrieved October 10, 2017, from https://www.webmd.com/drugs\
3\. Price Guide. (n.d). In Drugs.com. Retrieved October 10, 2017, from https://www.drugs.com/price-guide\
4\.

Spinraza. (n.d). Retrieved November 5, 2017, from https://www.spinraza.com\
5\. Bureau of Labor Statistics. (n.d.) Retrieved November 1, 2017, from https://www.bls.gov\
6\. Prescriptions. (n.d.). Retrieved November 5, 2017, from https://www.goodrx.com/\
7\. Salary. (n.d.). Retrieved October 15, 2017, from https://www.salary.com/\
8\. NORD. (n.d). Retrieved October 10, 2017,

form https://rarediseases.org/\
9\. Quittner, A., Goldbeck, L., Abbott, J., et al. Prevalence of depression and anxiety in patients with cystic fibrosis and parent caregivers: results of The International Depression Epidemiological Study across nine countries. Thorax, 2014; 69:1090-1097.\
10\. PubMed. (n.d.). Retrieved October 27, 2017, from https://www.ncbi.nlm.nih.gov/pubmed/\
11\. Venkatesan,  T., Tarbell, S., Adams, K., et al. A survey of emergency department use in patients with cyclic vomiting syndrome. BMC Emergency Medicine, 2010; 10:4