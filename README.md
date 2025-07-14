# IT-Helpdesk Insight
An interactive Power BI report analyzing support ticket data. Tracks key metrics like resolution time, satisfaction scores, SLA/TAT adherence, and priority-level performance across regions and channels. Includes drilldowns by country, city, and customer segment to identify areas of delay or dissatisfaction.

## [View the Dashboard](https://app.powerbi.com/view?r=eyJrIjoiYTM0MGE4NjAtMzUxZS00MTZiLTg5YzMtNjM3ZDdhZjU1NDg5IiwidCI6IjQ2NTRiNmYxLTBlNDctNDU3OS1hOGExLTAyZmU5ZDk0M2M3YiIsImMiOjl9)
<img width="720" height="1280" alt="Image" src="https://github.com/user-attachments/assets/997e7648-1fd9-46d4-bde6-56a2dc3d0232" />

---


## Introduction
IT Helpdesk Support plays a critical role in ensuring business continuity by resolving technical issues, managing service requests, and maintaining system stability.

From tracking ticket volumes and incident types to analyzing resolution times and customer satisfaction, helpdesk analytics empowers teams to identify bottlenecks, prioritize resources, and deliver faster, smarter support.

In this dashboard, I’ve visualized key metrics to drive efficiency, reduce SLA breaches, and enhance the overall user experience.

## Problem Statement
*"In this challenge, you’ll take on the role of an IT support analyst working with a dataset that looks like it came straight from a real service desk system, such as Jira Service Management. The goal is to explore and analyze support tickets to understand how the IT team handles different requests and how they can improve their performance.*

*This dataset includes over 10,000 IT support tickets. Each ticket is similar to what you'd see in a tool like Jira with details like:*

*Ticket ID, creation date, and resolution date, Subject and description of the issue or request, Response provided by the support team, Ticket priority (like High, Medium), queue, and type (e.g., Bug, Feature, Request), Tags for category, technical topic, and documentation, Country and location info for the requester*

*Your job is to dig into the data to find patterns that can help the IT team:*
* *Solve tickets faster*
* *Spot common or recurring issues*
* *Understand which requests take the most time or effort*
* *Improve workflows and customer satisfaction"*

## IT Helpdesk Support Dashboard Output

### Ticket Insight:
- The IT Helpdesk handled 11,923 tickets in total.

- Out of these, high-priority tickets were 4,571 (38.34%), while medium-priority tickets slightly led with 4,952 (41.53%). Low-priority tickets were 2,400 (20.13%).

- January consistently saw the highest number of tickets in both 2024 and 2025.

- February recorded the lowest ticket volume in both years.

- Q1 was the busiest quarter overall, indicating a strong start in both years.

- In 2024, ticket volume peaked in Q3 and dropped significantly in Q4.

- In 2025, Q1 showed high activity, but here's the catch — we don’t have data beyond June, so any full-year comparison would be incomplete.

#### Bottom line: ticket load is heaviest early in the year, especially with high-priority issues taking up a large share. But the trends shift as the year goes on — and partial data can easily skew the story.

###  Resolution Time & Priorities:
- Satisfaction rate is 38.34%, calculated based on tickets resolved within 2 days.
- The overall average resolution time is 2.82 days, reflecting a moderately efficient support process.
- General enquiry tickets take the longest to resolve, with an average of 3.43 days. The high resolution time for general enquiries is due to a high volume of low-priority tickets.
- Service outage and maintenance tickets have the shortest resolution time, averaging 2.43 days. The quicker resolution for service outage and maintenance tickets is due to a higher share of high-priority cases.
- Service outage and maintenance, technical support, and IT support queues handle the most high-priority tickets.
- The incident ticket category has the highest percentage of high-priority issues, at 43.56%.

- Request, change, and problem ticket categories mostly consist of medium-priority tickets.

#### Bottom line: The team is responsive to critical issues, but improving resolution time for low-priority tickets like general enquiries can enhance overall satisfaction.

### Location Based Analysis:
- Belgium reported the highest number of tickets, totaling 1,240. This signals a higher demand for support services in the region.
- Among Belgium's tickets, 41.61% were tagged as medium priority. Indicates recurring issues that require timely, but not urgent, resolution — a sign that processes or tools may need optimization to prevent escalation.

- Austria had the lowest ticket volume at 1,137. While this suggests fewer support needs, it’s important not to overlook quality and efficiency.
- Interestingly, Austria also had a high percentage of medium-priority tickets. This points to consistent but manageable issues that still need attention to maintain satisfaction.


## Files Included
### IT Support tickets .xlsx:
Contains raw data with details on tags, queue, pririty lebel, locatin based hostory, etc.

###  IT helpdesk.pbix:
Power BI report file with interactive dashboards and visualizations on tickets insight, geographical snapshot, and resolution time based on the dataset.

## Data Dictionary:

| Column Name        | Description                                         |
|--------------------|-----------------------------------------------------|
| Ticket ID          | Unique identifier for each ticket                  |
| Date               | Date the ticket was created                        |
| Resolution Date    | Calculated expected resolution date                |
| Subject            | Subject line of the support ticket                 |
| Body               | Main body of the ticket request or issue           |
| Answer             | Support response or follow-up provided             |
| Type               | Type of request (e.g., Request, Problem)           |
| Queue              | Support queue handling the ticket                  |
| Priority           | Priority level assigned to the ticket              |
| Primary Tag        | Primary classification of the ticket               |
| Secondary Tag      | Secondary classification for added context         |
| Category Tag       | General category tag for classification            |
| Technical Tag      | Specific technical classification tag              |
| Status Tag         | Status or nature of the issue                      |
| Resolution Tag     | Assigned resolution classification                 |
| Documentation Tag  | Documentation reference tag                        |
| Additional Tag     | Additional contextual or tagging info              |
| Country            | Country of origin for the ticket                   |
| Latitude           | Latitude of the originating location               |
| Longitude          | Longitude of the originating location              |

## Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a .xlsx file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in none of the columns errors & empty values were present.
- Step 5 : Create another 2 quaries by the name country and priority table.
- Step 6 : Update the header in 3 datasets as per requirement and load the dataset into Power BI.
- Step 7 : To calculate the Resolution time in days in column, write the formula - 

        = Duration.Days([Resolution Date] - [Date])


### Page Set up
- Step 8 :  To organise the report, at first text box is inseted in the report to write the TITLE of the page. Name the report as "IT Helpdesk Dashboard".

- Step 9 : In the report view, under the insert tab, using image option company's logo was added to the report design area at the left corner. Here is visual outcome:

 <img width="611" height="144" alt="Image" src="https://github.com/user-attachments/assets/10387674-8c60-454f-9e3f-fc150b45d968" /> 

- Step 10 : In order to navigate the report add the another three "Action" button as "Ticket Insight", "Resolution Time & Priority", and "Location based Ticket Analysis" vertically.

<img width="311" height="241" alt="Image" src="https://github.com/user-attachments/assets/663d409f-0d70-4739-8598-923d6bb6796c" />

- Step 11 : Make the duplicate of the page for three times to create the separate Canvas for each part.

### Creating Measure Table:
To develop a dynamic Power BI report on IT Helpdesh Support dashboard, I created a dedicated Measure Table to organize and centralize all the key DAX measures at one place. for creating new Measures Table Table following DAX expression was written;

    MeasuresTable = 
    SELECTCOLUMNS(
        FILTER(
            { (1) },
            FALSE()
        ),
        "Measure", [Value]
    )

#### *Step 12: Used DAX expression in Measures Table*
- To calculate *Total Ticket*:

        Total Tickets = COUNTROWS(Data)

- To calculate *Change Tickets*:

        Change Placed = 
        Var FilterChange = CALCULATE(COUNTROWS(Data), Data[Type] = "Change")
        Var TotalChange = COUNTROWS(Data)
        VAR percentage = DIVIDE(FilterChange, TotalChange)
        RETURN FORMAT(percentage, "0.00%")

- To calculate *Request Tickets*:

        Request Placed = 
        Var FilterRequest = CALCULATE(COUNTROWS(Data), Data[Type] = "Request")
        var TotalRequest = COUNTROWS(Data)
        VAR percentage = DIVIDE(FilterRequest, TotalRequest)
        RETURN FORMAT(percentage, "0.00%")

- To calculate *Incident Tickets*:

         Incident Placed = 
        Var FilterIncident = CALCULATE(COUNTROWS(Data), Data[Type] = "Incident")
        Var TotalIncident = COUNTROWS(Data)
        VAR percentage = DIVIDE(FilterIncident, TotalIncident)
        RETURN FORMAT(percentage, "0.00%")

- To calculate *Problem Tickets*:

        Problem Placed = 
        Var FilterProblem = CALCULATE(COUNTROWS(Data), Data[Type] = "Problem")
        var TotalProblem = COUNTROWS(Data)
        VAR percentage = DIVIDE(FilterProblem, TotalProblem)
        RETURN FORMAT(percentage, "0.00%")

- To calculate *"Satisfaction Rate"*:

        Satisfaction Rate = 
        VAR SatisfiedTickets = 
                CALCULATE(
                 COUNTROWS('Data'),
                 'Data'[Resolution Time (Days)] <= 2
                )
        RETURN 
        DIVIDE(SatisfiedTickets, [Total Tickets]) * 100

- To calculate *"SLA Breach"*:

        SLA Breach = 100 - [Satisfaction Rate]

- Set the Target limit gauge at 50 and Max limit at 100

- To calculate *"Highest Ticket Country"*:

        Highest Ticket Country = 
                CALCULATE(
                        SELECTEDVALUE('Data'[Country]),
                         TOPN(
                                1,
                                SUMMARIZE('Data', 'Data'[Country], "TicketCount", COUNT('Data'[Ticket ID])),
                                [TicketCount],
                        DESC
                 )
        )

- To calculate *"Lowest Ticket Country"*:

        Lowest Ticket Country = 
                CALCULATE(
                        SELECTEDVALUE('Data'[Country]),
                        TOPN(
                                1,
                                 SUMMARIZE('Data', 'Data'[Country], "TicketCount", COUNT('Data'[Ticket ID])),
                                [TicketCount],
                         ASC
                )
        )


