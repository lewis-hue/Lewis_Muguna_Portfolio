# Projects - Lewis Muguna

This portfolio showcases my end-to-end expertise in Data Science, AI Engineering, and Data Infrastructure, featuring projects developed through professional engagements, academic research, and independent innovation. Each project highlights my ability to design scalable, cloud-native AI systems, perform data-driven analysis, and build intelligent automation solutions that solve real-world problems.

It serves as a living record of my achievements, technical growth, and certifications, and is regularly updated with new projects that reflect the latest advancements in Machine Learning, Generative AI, and MLOps.

📧 Email: lewiemuguna417@gmail.com

🔗 LinkedIn: www.linkedin.com/in/lewis-muguna-070080166

## Projects

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/Agentic-Viral-Video-Orchestrator/blob/main/AVVO%20System%20Overview.png"> **[Agentic Viral Video Orchestrator (AVVO)](https://github.com/lewis-hue/Agentic-Viral-Video-Orchestrator.git)**

**Agentic Viral Video Orchestrator (AVVO)** is a multi-agent **AI automation system** that autonomously discovers viral trends, generates short-form videos, and distributes them across multiple social media platforms.  
Built using **Python (FastAPI)** for the backend and **React + TypeScript** for the frontend, AVVO integrates **LangChain**, **Gemini 2.5-Flash**, and **FAISS** for intelligent content generation and retrieval.  
The system leverages **Celery** and **Redis** for task scheduling and parallel processing, **Cloudinary** for media storage and public video URLs, **Zapier Webhooks** for seamless automation triggers, and **Buffer API** for automated publishing workflows.  
Additional integrations with **OpenAI**, **Vertex AI Veo**, and **Google TTS** enable generative video synthesis and narration.  
The solution runs on **Dockerized infrastructure**, backed by **PostgreSQL**, and deploys via **AWS/GCP** with **CI/CD pipelines** managed through **GitHub Actions**.  
AVVO’s architecture is designed for **scalability**, **continuous optimization**, and **real-time feedback loops**, making it a **production-ready AI system** for teams aiming to scale viral content creation through automation and machine learning.
 



#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/Lewis_Data_Science_Profile/blob/main/download%20(1).jpg"> **[Agentic Plan Workbench: LLM-Powered Red Teaming for Function Calls](https://github.com/lewis-hue/Agentic-Plan-Workbench.git)**

This production-grade, full-stack web application serves as an interactive development environment (IDE) for building and validating complex AI agent behaviors. At its core, the application employs a multi-agent "red teaming" architecture where a Critic agent, powered by a high-speed LLM like Groq LLaMA 3, performs an adversarial analysis of user-defined function-calling plans. This process identifies subtle logical flaws, semantic errors, and schema violations, culminating in the automated generation of an optimized "Golden Plan" and preventing unreliable agent actions. The developer experience is centered around an interactive workbench featuring the Monaco Editor, providing a familiar, code-centric workflow for rapid iteration.
Architecturally, the system is built on an **asynchronous Python backend** using **FastAPI**, ensuring high-performance handling of concurrent **LLM API calls**. Data integrity and strict schema validation are enforced at the API boundary using Pydantic models, a critical practice for building reliable AI services. The framework is strategically designed as a powerful synthetic data generation engine, creating structured (**plan, critique, golden_plan**) triplets ideal for fine-tuning smaller, more specialized models. The entire application is containerized with Docker and designed for serverless deployment on platforms like **Google Cloud Run**, demonstrating expertise across a modern tech stack including **Python, FastAPI, Pydantic, JavaScript, the OpenAI SDK, and Docker for DevOps**. 

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/Lewis_Data_Science_Profile/blob/main/download%20(5).jpg"> **[Production-Grade Serverless RAG Application: A Full-Stack LLM System for Secure Document Analysis and Constitutional Compliance](https://github.com/lewis-hue/Qubiten-AI-Assistant.git)**

This production-grade, serverless web application is a proactive compliance advisor that translates complex constitutional law into actionable guidance for businesses, schools, and hospitals. At its core, the application uses a **Retrieval-Augmented Generation (RAG)** system powered by a **Groq LLaMA 3.1 LLM** to deliver citation-backed answers, preventing AI hallucinations. The user experience is enhanced with **real-time streaming responses** and hands-free query input via **Google Cloud Speech-to-Text** for voice transcription. 

Architecturally, it ensures user privacy and scalability through a **stateless backend** with **secure client-side document processing** in the browser using **IndexedDB**. The entire system is containerized with **Docker** and deployed serverlessly on **Google Cloud Run** with an **automated CI/CD pipeline**, demonstrating expertise across a modern tech stack including **Python, Flask, JavaScript, LangChain, Vector Databases (FAISS), and the full suite of Google Cloud and Docker for DevOps**. 

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/AI-Powered-Web-Scraper-Data-Extraction-Platform/blob/main/download%20(4).jpg"> **[AI-Powered Web Scraper and Data Extraction Platform](https://github.com/lewis-hue/AI-Powered-Web-Scraper-Data-Extraction-Platform.git)**

This project is a scalable, cloud-based application designed for web scraping and data export management. It features RESTful APIs for initiating and monitoring scraping jobs, as well as exporting and downloading data. Built with a Flask backend, MongoDB for scalable data storage, and Docker containers for seamless deployment, the application is optimized for performance and horizontal scaling. Future enhancements include the potential integration of Celery for task queue management. 

**Skills and tools:** Flask, MongoDB, RESTful APIs, Docker, Cloud Hosting (AWS, GCP, Heroku), CI/CD, Scalable Architecture, Asynchronous Processing, Performance Optimization, Task Queue Management (Celery).

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/LLMs-and-RAG/blob/main/download%20(3).jpg"> **[Qubiten Compliance Chatbot: An LLM-Powered RAG System](https://github.com/lewis-hue/LLMs-and-RAG.git)**

Qubiten Compliance Chatbot is a Retrieval-Augmented Generation (RAG) system leveraging Google Vertex AI’s text-bison\@001 model and embeddings. Built with a Python Flask backend and HTML/CSS/JavaScript frontend, it ingests compliance documents, performs FAISS-based similarity search, and assembles prompts for the LLM. 

**Skills and tools:** RAG, LLM fine-tuning, Vertex AI, Flask, Python, FAISS/Pinecone, RESTful APIs, and UI development, ensuring accurate, scalable regulatory guidance using a fine-tuned knowledge base and chat interface.

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/End-to-End-Data-Architecture-and-Analytics-Pipeline-on-AWS/blob/main/images.jpg"> **[End-to-End Data Architecture and Analytics Pipeline on AWS
](https://github.com/lewis-hue/End-to-End-Data-Architecture-and-Analytics-Pipeline-on-AWS.git)**

This project simulates the design of an end-to-end data engineering and analytics pipeline using AWS. It demonstrates the use of AWS services like Amazon EKS for container orchestration, Amazon S3 for data storage, AWS Glue for ETL processing, Amazon Athena for querying, Amazon SageMaker for machine learning, and Amazon QuickSight for data visualization. The pipeline simulates a scalable, secure architecture for ingesting, transforming, analyzing, and visualizing customer transactional data, providing business insights and predictive models in a telecommunications context.

**Skills & Tools:** Amazon Elastic Kubernetes Service (EKS), Amazon S3, AWS Glue, Amazon Athena, Amazon SageMaker, Amazon QuickSight, Apache Doris, data pipeline design and implementation, data ingestion, transformation, and feature engineering, scalable architecture creation, feature engineering, model development and training, predictive modeling for customer behavior analysis, secure and scalable cloud infrastructure design, end-to-end data pipeline integration and optimization, querying, reporting, business intelligence (BI) insights generation, and data-driven decision-making.

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/Lewis_Data_Science_Profile/blob/main/Snowflake.jpg"> **[Fraud Detection and Financial Transaction Analysis Using Snowflake, Machine Learning, and Tableau](https://github.com/lewis-hue/Fraud-Detection-Financial-Transaction-Analysis-Snowflake-.git)**

This project showcases advanced SQL, Snowflake, and Tableau skills to analyze financial transactions for fraud detection and customer insights. Using Snowflake for data warehousing and SQL for data transformation, I built a robust ETL pipeline to process and stage transaction data. Key analyses include customer segmentation, fraud risk scoring, and transaction breakdowns. I developed interactive Tableau dashboards to visualize customer spending behavior and fraud risks. This project optimized fraud prevention, enhanced customer targeting, and improved financial operations through actionable insights, leveraging advanced analytics, data visualization, and cloud data infrastructure.

**Skills & Tools:** Snowflake, Advanced SQL, Data Modeling, Data Warehousing, ETL Pipelines, Tableau Dashboards, Data Visualization, Business Intelligence, Customer Segmentation, Fraud Analytics, KPI Monitoring, Data-Driven Decision Making, Cloud Analytics Infrastructure, Performance Optimization, Transaction Analysis, Risk Scoring Frameworks


#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/Google_Ads_Analytics/blob/main/download.png"> **[Google Ads Campaign Optimization Using Amplitude Analytics](https://github.com/lewis-hue/Google_Ads_Analytics.git)**

This project utilizes Amplitude, a powerful product analytics tool, to optimize Google Ads campaigns through detailed analysis of user behavior and ad performance across platforms like Google, YouTube, and Google Display Network. By tracking key metrics such as clicks, conversions, cost, impressions, and interactions, we identify areas for improvement in targeting and engagement. The insights derived from Amplitude's marketing analytics enable better ad spend allocation, refined targeting strategies, and enhanced user journeys, ultimately improving conversion rates and maximizing customer lifetime value.

**Skills & Tools:** Product analytics, web analytics, Marketing analytics, Amplitude, and data visualisation.

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/Lewis_Data_Science_Profile/blob/main/Snowflake.jpg"> **[Fraud Detection and Financial Transaction Analysis Using Snowflake, Machine Learning, and Tableau](https://github.com/lewis-hue/Fraud-Detection-Financial-Transaction-Analysis-Snowflake-.git)**

This project showcases advanced SQL, Snowflake, and Tableau skills to analyze financial transactions for fraud detection and customer insights. Using Snowflake for data warehousing and SQL for data transformation, I built a robust ETL pipeline to process and stage transaction data. Key analyses include customer segmentation, fraud risk scoring, and transaction breakdowns. I developed interactive Tableau dashboards to visualize customer spending behavior and fraud risks. This project optimized fraud prevention, enhanced customer targeting, and improved financial operations through actionable insights, leveraging advanced analytics, data visualization, and cloud data infrastructure.

**Skills & Tools:** Snowflake, Advanced SQL, Data Modeling, Data Warehousing, ETL Pipelines, Tableau Dashboards, Data Visualization, Business Intelligence, Customer Segmentation, Fraud Analytics, KPI Monitoring, Data-Driven Decision Making, Cloud Analytics Infrastructure, Performance Optimization, Transaction Analysis, Risk Scoring Frameworks

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/Lewis_Data_Science_Profile/blob/main/Oracle.png"> **[Sales Forecasting and Marketing Optimization Using Python, Oracle, Machine Learning, and Power BI](https://github.com/lewis-hue/oracle-powerbi.git)**

This project showcases **data science** techniques and **business intelligence** strategies to optimize sales forecasting and marketing efforts using state-of-the-art tools and technologies. By leveraging **Python** for **Data Science**, **Machine Learning**, and **Oracle** for data storage and processing, the project develops an **end-to-end sales prediction pipeline**. The pipeline includes crucial steps such as **data preprocessing**, **feature engineering**, and **model training**, enabling market effectiveness.

**Skills & Tools:** Oracle Database, Python for Data Science, Pandas, NumPy, Scikit-learn, Machine Learning, Gradient Boosting, Predictive Modeling, Power BI, Data Visualization, ETL Pipelines, Advanced Analytics, Business Intelligence, Marketing ROI Optimization, Sales Forecasting, Hyperparameter Tuning, Regression Modeling.
##

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/lewis_page/blob/main/databricks.png"> **[Business Intelligence (BI): Sales Forecasting Dashboard (Databricks)](https://github.com/lewis-hue/BusinessIntelligence.git)**

This project demonstrates a comprehensive sales data analysis using **SQL** within **Databricks** on **Microsoft Azure**. The analysis covers product-level revenue, units sold, store performance, and geographic trends. A robust **ETL pipeline** was developed in Databricks to ingest and process transactional sales data across countries and stores. Key business insights were visualized via interactive dashboards to support strategic decision-making.

**Skills & Tools:** SQL, Databricks, Microsoft Azure, Business Intelligence, Data Visualization, Data Analysis, Sales Analytics, ETL Pipelines, Dashboarding, Retail Analytics

##

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/lewis_page/blob/main/Customer%20segmentation.png"> **[Data Analysis: Customer Segmentation and Behavior Analysis](https://github.com/lewis-hue/data_analysis.git)**

This project focuses on customer behavior analytics using **R** in **R Studio**, exploring the relationship between `TotalPurchase`, `Frequency`, and `Customer Lifetime Value (CLV)` through exploratory data analysis and correlation testing. Visualizations include bar graphs and scatterplots, supported by statistical metrics (correlation coefficients and p-values) to uncover actionable insights.


**Skills & Tools:** R, R Studio, Data Analysis, Correlation Analysis, Data Visualization, Customer Segmentation, CLV Modeling, Business Intelligence, Exploratory Data Analysis (EDA), Statistical Testing

##

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/Lewis_Data_Science_Profile/blob/main/BigQuery.jpg"> **[B2B SaaS Analysis Using Customer Data (BigQuery & Looker Studio)](https://github.com/lewis-hue/BigQuery.git)**

This project focuses on analyzing customer behavior, churn risk, and revenue generation for a B2B SaaS company using a variety of advanced data science techniques and tools. The objective is to uncover insights that can optimize customer acquisition, retention strategies, and revenue generation by leveraging the power of SQL, BigQuery, Looker Studio, and predictive modeling.

**Skills & Tools:** SQL, BigQuery, Looker Studio, Business Intelligence, Data Visualization, Data Analysis, Dashboarding
<br />

## Core Competencies


- **Methodologies**: Data Engineering, Data Analysis, Machine Learning, Deep Learning, Time Series Analysis, Natural Language Processing (NLP), ETL, ELT, Big Data Analytics
- **Languages**: Python (Pandas, Numpy, Scikit-Learn, Scipy, Keras, Matplotlib), R (Dplyr, Tidyr, Caret, Ggplot2), SQL (PostgreSQL, MySQL, BigQuery), Scala (Spark), C++
- **Tools**: Apache Spark, dbt, Docker, Kubernetes, Airflow, Tableau, Power BI, Looker Studio, Flask, PySpark, MS Excel, Google Sheets, AWS

## Certificates


- [IBM Data Engineering Specialization(IBM)](https://www.coursera.org/account/accomplishments/specialization/L2LPK72TSHIV)
- [AWS Cloud Solutions Architect(AWS)](https://www.coursera.org/account/accomplishments/professional-cert/certificate/YOI9L6540YBA)
- [Google Business Intelligence Specialization(Google)](https://www.coursera.org/account/accomplishments/specialization/2BO13KGKPD5V)
- [Python for Data Science, AI & Development (IBM)](https://www.coursera.org/account/accomplishments/verify/D433KOIGEMR5)
- [Machine Learning Models in Microsoft Azure (Microsoft)](https://www.coursera.org/account/accomplishments/verify/DM2KWMQBJ61M)
- [SQL and Relational Databases (IBM)](https://courses.cognitiveclass.ai/certificates/730619af9d6f4605abcf94d609d810d6)
- [Data Analysis with R Programming](https://www.coursera.org/account/accomplishments/verify/QBE3ZPA5Z7L0)
- [Scala (IBM)](https://courses.cognitiveclass.ai/certificates/7fa09c3eb5c94eaeaac9051512bc0870)
- [BigQuery for Data Analysts](https://www.coursera.org/account/accomplishments/verify/FXW8MAV2EWWJ)
- [Exploratory Data Analysis forMachine Learning (IBM)](https://www.coursera.org/account/accomplishments/verify/0M1V5IH0DPIM)
- [Data Analysis and Visualization with PowerBI](https://www.coursera.org/account/accomplishments/verify/1WJM24A7HZJ9)
- [Developing AI Applications withPython and Flask (IBM)](https://www.coursera.org/account/accomplishments/verify/E8KKQL3YJJIZ)
- [Modernizing DataLakes and Data Warehouses with Google Cloud](https://www.coursera.org/account/accomplishments/verify/IIR4VSGR470J)

<!--
**lewismuguna/lewismuguna** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on building scalable data pipelines with Apache Spark, BigQuery, and Python.
- 🌱 I’m currently learning more about advanced data engineering, cloud technologies, and machine learning optimization.
- 👯 I’m looking to collaborate on projects involving data analytics, machine learning, and cloud computing.
- 🤔 I’m looking for help with optimizing ETL workflows and advanced SQL querying techniques.
- 💬 Ask me about data analysis, data engineering, and cloud data technologies.
- 📫 How to reach me: via LinkedIn or email.
- 😄 Pronouns: He/Him
- ⚡ Fun fact: I love transforming raw data into actionable business insights!
-->
