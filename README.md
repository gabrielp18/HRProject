# Why do people leave a company?
One of the problems that many companies face is the dismissal of employees. But why does this happen?
- [View our thought process!]()

To answer this question, we will work with a consultancy specialized in promoting the growth of
companies. The contracting company is facing a problem regarding the dismissal of employees and would like to
that we investigate why this happens and, if possible, predict who will leave the company.

## Let's think: how does a layoff affect a business?
When an employee leaves a company, the cost of time spent on a new hire until his independence from his
function takes time, which can vary between 4 to 12 months. During this period, a supervisor starts to use his/her time
to teach this new employee, which may compromise their role. In addition, there is a probability of falling
of quality of the functions, since the new employee will not reproduce the same resourcefulness as the old employee,
since it is not trained enough.

## How can we help our customer?
The first step is to analyze the entire database provided by the customer, with an exploratory data analysis we can highlight the main reasons for the departure of employees.
But as everything in life is not easy, we will have to process this data, see if there are null data, do a statistical analysis of all the data.
After that, we can move on to the data visualization, where we will be able to see the distribution of this data as well as its dependency.

Based on this information, we can provide our client with a report of the **top reasons their employees leave your company**.
# ![](https://user-images.githubusercontent.com/95098504/150886733-afea992b-4431-4bb1-83a9-1c409f264f07.png)
As expected, one item is decisive for leaving the company: **salary**.

In addition, we can see which departments experience the highest employee loss
# ![](https://user-images.githubusercontent.com/95098504/150887153-28d7e4b1-3d98-409e-9fd7-c09492614c06.png)

As noted, the department with the highest exit rate is sales. But why does this happen? In the vast majority of companies, salespeople do not have a fixed salary.
(if they do, it is quite low) being basically remunerated by commissions. If the seller doesn't sell, he doesn't receive, basically that's it. As a result, this may be one of the reasons
related to the greater departure of employees in this sector.

A curious part of this data is in relation to the number of projects and layoffs. It is expected that the more projects a person has, the more this employee is related to the company,
more trust the company has in this employee and a greater delivery and salary this employee can receive, but is this what happens?
# ![](https://user-images.githubusercontent.com/95098504/150887497-64cfe0d4-c15c-421e-8135-4fb020777287.png)
We can see in this graph that the most "busy" employees - with 6 and 7 projects - left the company. Next to them, people who carried out only 2 projects.

Let's look at people who performed 6 to 7 projects, what is their salary?
# ![](https://user-images.githubusercontent.com/95098504/150887903-27329b35-2868-459e-a279-0550d435ad6a.png)
We see that the majority are classified as low salary, that is, this brings us to our first topic addressed for people leaving a company: **the salary**

## More projects = more salary?
This hypothesis is expected based on the premise that more work leads to a higher salary. However, it can be noted that employees who have less than 3 projects earn higher salaries than people who have more than 5 projects.
# ![1](https://user-images.githubusercontent.com/95098504/154844788-1142b229-1183-4758-82e9-f56122a5feaf.png)
# ![2](https://user-images.githubusercontent.com/95098504/154844807-0dc3cd0a-dc3f-4fb3-8297-92d4655af889.png)

## The happiest employees are whose those recived more salary?
This hypothesis can be observed, since people who evaluated the company with a level of satisfaction greater than 75% of the average, have a higher salary.
# ![3](https://user-images.githubusercontent.com/95098504/154844812-b0e913ca-34d9-40c2-bfa3-96c6e0274ea3.png)
# ![4](https://user-images.githubusercontent.com/95098504/154844816-a94ae5d8-4050-4900-972d-af6253924a7c.png)

## Hypoteshis test about the influence of salary in churn
Taking into account the assumption that salary is the main influence for employees to leave the company, let's statistically validate this.
Our null hypothesis is that the salary directly influences the departure of employees from the company, and the alternative hypothesis is that there is no proven influence.
In addition, we will test whether the level of satisfaction also influences the departure of these employees.
For this, the chi square test was used, where a relationship between a continuous variable and a category can be established.
The result obtained from p-value fails to reject the null hypothesis, that is, salary and satisfaction, in isolation, do not directly influence the exit of employees.

## Predict the future?
Almost everyone wants to predict the future, and our client is no different. He would like us to provide a system that could assess whether or not the employee will leave the company.
based on data submitted to the program.

### How do we do it?
For this, our Machine Learning team thought of testing some algorithms such as: LogisticRegression, LGBMClassifier, DecisionTree and RandomForest. The customer in conversation with
our Product Owner specified that he would like 4 algorithms and that he would decide which one to use.
The Machine Learning team decided to improve the LogisticRegression and LGBMClassifier hyperparameters with *roc_auc_score* and *gp_minimize* and for DecisionTree and RandomForest they used *cross_validate* and *KFold*.

The best result found by the team was with the LGBMClassifier with parameter optimization by Bayesian Optimization (*gp_minimize*), resulting in:
# ![5](https://user-images.githubusercontent.com/95098504/154844842-cac791e0-b97b-46bd-a6a8-4d06835cd432.png)
