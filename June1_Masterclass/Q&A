Here are the questions and answers provided during the Masterclass. Please also refer to https://docs.snowflake.com/ for more information. Finally, please connect with your Snowflake team for more answers.

Question 1: Will this work with python 3.9?
Answer: Snowpark today (as you might have seen in our docs) requires python 3.8 today.  Python 3.9 is officially planned to go open public preview by the end of this week. Python 3.10 is planned to go out into open public preview toward the end of June

Question 2: Do you have plans to Provide IDE inside snowflake account ?
Answer: We currently have python worksheets inside the snowsight UI. Please tune in to Summit at the end of the month for news around upcoming Python features!

Question 3: How it is going to help in managing cost compared to running a  Python code in cloud managed instance?
Answer: In a cloud managed instance it will require data movement between the storage and the compute memory. Snowpark is meta data driven and keeps the data in place, which reduces costs. You also benefit from the fully elastic Snowflake compute that can spin up and down in seconds, so you won’t need to run and pay for compute for longer than you need it.

Question 4: in this schematic where is streamlit located?
Answer: You can use Snowpark and the features in this schematic via a Streamlit-built UI in order to work with the data and/or build a data application.

Question 5: We are currently evaluating DBT Cloud as a potential transformation tool for our data lake in Snowflake. Could Snowpark be considered an alternative to something like DBT Cloud?
Answer: dbt is terrific - and is one of the most popular data transformation tools today. And until recently, dbt has been entirely a SQL-based transformation tool.  However, it now allows for python based models that leverage Snowpark.  So it isn’t really an either/or.  Good example here https://www.phdata.io/blog/python-models-in-dbt/

Question 6: Will it be possible to work with different Python library versions for differente modules?
Answer: Yes, by leveraging our integration with Anaconda, your are able to select various versioning of packages you need.

Question 7: Do we have any inbuilt facility to automate data pipeline in Snowpark(Workflow management) ...such as tools like Airflow,Autosys etc
Answer: You are able to call Python functions with Tasks within Snowflake itself when you’re working with data in Snowflake. If you need to orchestrate ingestion from sources outside of Snowflake, you’ll need to leverage something like Airflow for that.

Question 8: Why is Snowpipe preferred to COPY command/External Table with SQL ingest for ingesting files? Is there a comparative study showing pros and cons and when to use what with why?
Answer: Snowpipe essentially automates the COPY command using very cost effective compute that is ‘serverless’ (doesn’t use your defined warehouses) at 1.8 the cost of an XS.  It can listen for new files as they arrive in cloud bucket storage and load automatically.  https://docs.snowflake.com/en/user-guide/data-load-snowpipe-intro. There are also integrations with streaming services like Kafka to effectively address streaming use cases.  I’d use a COPY command for one off loads, but for anything you want automated, Snowpipe is the way to go.

Question 9: We have a curated Anaconda repository.  Will we be able to point to that?
Answer: Don’t believe you’ll be able to point to that directly, however, you can load any packages you need that aren’t already in Snowflake’s curated repository. It’s very possible that everything you need is already in the Snowpark curated repository, since we have 4000+ of the most popular packages in there. If you’re already a Snowflake customer, work with your SE to determine if this is the case.

Question 10: In the How it Works slide, is it preferable to use the SQL approach on the right rather than the Dataframe approach on the left?
Answer: The approach on the right was the Python Secure sandbox. What this does is spin up a Python environment to run Python on a Snowflake cluster and leverages the packages in Snowflake anaconda environment for that. Think spinning up a sandbox to run Scikit-Learn packages to train a model. 
The dataframe is a metadata-only pointer to the data in Snowflake that you can use for low-footprint, fast, and secure transformations.  You would work with a dataframe in a Jupyter notebook or an Airflow-orchestrated script in order to run transformations for Data Engineering/Feature Engineering. Data would not leave Snowflake.

Question 11: Whether DBT (data transformation capabilities) be implemented via Snowpark?
Answer: Until recently, dbt has been entirely a SQL-based transformation tool.  However, it now allows for python based models that leverage Snowpark.  So it isn’t really an either/or.  Good example here https://www.phdata.io/blog/python-models-in-dbt/

Question 12: can I conda install?  Pip can sometimes break my anaconda instance.
Answer: Yes, conda install will also work. See https://docs.snowflake.com/en/developer-guide/snowpark/python/setup#installation-instructions. We recommend conda installing to a particular snowflake conda repo so that the versioning matches what is on your snowflake account

Question 13: will openai library work?
Answer: Yes, it’s one of the packages in the curated Anaconda environment.

Question 14: Is the code in VS-code running on Daniel’s laptop or is the VS-code connected to the remote snowpark warehouse or compute instance?
Answer: When Daniel makes the connection at the beginning with session.create(), it connects his kernel to his snowflake account. So his local kernel is pushing down code to his snowflake account. This will become more clear when he registers a python sproc in a second. See how Daniel connects his kernel local on his laptop.

Question 15: Does snowpark share the compute? or it is dedicated per customer? How are we ensuring the data security?
Answer: Snowpark and Snowflake compute are both handled the same way. It’s a hot pool of compute available to customers. Two customers won’t be using the same nodes at the same time. This pooled compute architecture has HIPPA/PCI/FedRAMP certifications and is securely used for the most sensitive data.

Question 16: How do we execute this code on a schedule?
Answer: All of this work can be stored as a stored procedure on snowflake, and executed via SQL calls. Please see this link to learn more about Snowflake tasks https://docs.snowflake.com/en/user-guide/tasks-intro

Question 17: When Daniel imports nltk and other modules, do you have to pre-load these same modules on the snowflake account?
Answer: A large number of modules are in the snowflake anaconda repo, nltk included (https://repo.anaconda.com/pkgs/snowflake/). You can upload any that are not there, but this makes managing things easier on you

Question 18: Can we just use Snowpark Python Notebook instead of the VS code?
Answer: At this time, there is no in-built notebook in Snowflake. There are just the Python Worksheets in Snowflake that run Python code but is not cell-based. Stay tuned for Summit announcements for more info on what’s to come. However, you can use any IDE to run the Snowpark package. Hex or Jupyter notebooks are favorites among customers.

Question 19: In case I don't want to write the processed data back in Snowflake, but instead say write it in an external Graph database ... what are my options to connect to the graph db, or I will need to exchange the data as files and trigger an external process to load it?
Answer: The most secure way would be to use trusted external functions/established ELT process, but you are free to move the data onto your local machine and push it wherever you want from the python kernel

Question 20: Hi, is there any integration with IBM watson explorer with snowflake/snowpark to run their ML libraries with data in snowflake
Answer: You may have seen this, but from a data source standpoint it is easy to connect data to Watson Query.  Hope that helps!

Question 21: Can snowpark scripts be used by airflow to orchestrated them?
Answer: Yes. Snowflake Scripts are SQL callable, so it works seamlessly with airflow. You are able to deploy python code as stored procedures and / or functions. So those can be used in sql just like standard stored procedures. You run the procedure or udf using sql syntax if you prefer.

Question 22: So, no direct external connections allowed? Any plans to be able to do so?
Answer: That feature is currently in private preview called Direct External Access PrPr. Please connect with your Snowflake rep to learn more.

Question 23: How about CICD implementation using Azure DevOps pipelines?
Answer: However your python kernel is accessing your CI/CD processes. The sprocs will be deployed from the python kernel and written to snowflake as a sql callable object. Whatever is pushing that code to snowflake will maintain the CI/CD

Question 24: Writing snowpark code using snowflake python worksheet or connecting through any IDE like anaconda.. Which one would you suggest?
Answer: We allow you to work where you are most comfortable. use whichever makes you most productive and leverage the same Snowflake power behind the scenes

Question 25: Can you talk about the use of snowpark in data validation of Snowflake as a destination vs a source DB like sql server, how can this be implemented and automated
Answer: If you’re asking about running Python functions to output data quality analytics, then this is absolutely possible. Assuming you have Python code that can scrub the data and identify data quality issues, you can run that using a Snowflake task in an automated fashion. Can be run as data is ingested into Snowflake using Streams as well.

Question 26: Can you use get_ddl() to get the python function ddl?
Answer: You can get the udf code with get_ddl, but its stored as byte code in binary and if code is over a certain size its saved to a stage.

Question 27: What is the scope of udf, is it global?
Answer: Can you please give some more context? The UDF will be limited to the RBAC of the role that created the UDF.

Question 28: What kind of ML algorithms does this provide? Does it provide detail hyperparameter tunings?
Answer: This link contains all of the packages pre-loaded and available: https://repo.anaconda.com/pkgs/snowflake/. You can train any of the models these support. You are able to run hyperparameter tuning in Snowflake as well: https://medium.com/snowflake/parallel-hyperparameter-tuning-using-snowpark-53cdec2faf77

Question 29: Does snowpark still use snowflake cloud services to do syntax check on database view/table/column names etc
Answer: Are you meaning serverless? If so, yes.

Question 30: Can you please share the documentation for functions that are supported by Snowpark dataframe?
Answer: These are some good references: 
https://docs.snowflake.com/ko/developer-guide/snowpark/reference/python/api/snowflake.snowpark.DataFrame.html
https://docs.snowflake.com/en/developer-guide/snowpark/python/working-with-dataframes
https://docs.snowflake.com/developer-guide/snowpark/reference/python/index.html

Question 31: Do you have plans for a  webinar to go over snowflake-ml-modeling?
Answer: We will likely run another Masterclass focused on ML modeling with Snowflake. For now, please see https://quickstarts.snowflake.com/guide/machine_learning_with_snowpark_python/index.html?utm_cta=website-workload-data-science-resources-ml-with-snowpark-python-quickstart#0

Question 32: Any insights on availability for group_by().apply_in_pandas() function?
Answer: Please see https://docs.snowflake.com/ko/developer-guide/snowpark/reference/python/index.html

Question 33: Converting snow spark dataframe to pandas would make it to be loaded in memory locally?
Answer: If you were to run it on your local laptop correct. however in this situation, you would deploy the code as a stored procedure inside snowflake and the data would be local to the “Snowflake Compute Cluster”… so it would never leave the snowflake platform. The benefit of this approach is you dont have a code migration effort.

Question 34: does it supports virtual environment creation by user to separate concerned packages?
Answer: Sure, you can create a virtual environment using conda or the like.

Question 35: Do you have any migration tool to migrate the existing Azure Databricks codes to Snowpark ?
Answer: Yes, please connect with your Snowflake account team to learn more.

Question 36: Is there any possibility of decrypt a encrypted file(it is in cloud lake) and load the data into snowflake?
Answer: Yes you can. You can run any supported library against a file that would be download from a stage to the /tmp folder on the compute cluster.

Question 37: can snowparc run pythton byte-code?
Answer: You can run the byte code by uploading to a stage - and then running as a python udf - there’s an example here https://docs.snowflake.com/en/developer-guide/udf/python/udf-python-creating and https://docs.snowflake.com/en/developer-guide/udf/python/udf-python-creating#creating-a-python-udf-with-code-uploaded-from-a-stage

Question 38: Is there any ability to constrain a "untrusted" library so it has no ability to reach out to the internet even in the event it did contain malicious code?
Answer: Packages are not able to access network at this time, security is built in from start

Question 39: Joe - regarding your message "can be done on ANY python Kernel", can you elaborate please?
Answer: Regardless of which vendor or computer you run the model training on. as long as you leverage supported libraries, the model file can be uploaded to snowflake and run from within snowflake. this means we dont force you to train your model on snowflake to be able to use it in our platform

Question 40: if we have existing python scripts that run data validation of datasource (sql server) against the migrated data in snowflake, how can we leverage snowpark to implement an automated data validation process that runs faster
Answer: You could run those python scripts as sprocs on snowflake. 

Question 41: is Snowpark a good tool to encrypt decrypt files and SFTP ingest/upload? We do this using Airflow/base python so should we consider bringing that inside Snowflake instead?
Answer: When you load files into Snowflake, they are automatically encrypted and decrypted for querying/reverse ETL. Snowflake could absolutely be a good landing spot for the SFTP and you may be able to leverage data sharing to send data out as needed.
