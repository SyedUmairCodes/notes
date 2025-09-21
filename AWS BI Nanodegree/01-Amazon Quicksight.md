# Amazon Quicksight

The rapid growth of Generative AI (GenAI) and Generative Business Intelligence (GenBI) is revolutionizing how organizations extract and understand insights from their data. Innovations in GenBI, like Amazon Q in QuickSight, are making data analysis accessible to everyone, even those without prior analytics experience, empowering them to make better decisions and improve customer service.

>[!NOTE]
GenBI simplifies data interaction and insight extraction to democratize data access and empower users to derive valuable insights efficiently.

Amazon QuickSight is a  versatile, cloud-based BI tool for diverse analytics needs, enabling actionable insights through features like automated dashboards and data visualizations. It Leverages AI to automate report generation and dashboard creation using natural language, significantly speeding up the process and identifying critical action items.

## Workflow and Visualizations

QuickSight is your cloud-based platform for democratizing data access. It serves as a "single source of truth" allowing users to create a variety of data visualizations and reports.

- Setup a dataset from the data you want to use, you can import any file such as a CSV or from Cloud Storage or third-party tools.
- Setup a refresh interval to keep the data upto date if you're working with real-time or current data.
- Create your dashboard using tabs (sheets) and different available components for visualizations and calculated fields.
- Publish your dashboard as an interactive view that others can use. The publish dashboard allows you to iterate and improve analyses without affecting the live dashboard.

>[!INFO]
>- Separating datasets allows them to be used for multiple dashboards without re-ingesting data, promoting efficiency.
>- Focus on who the users are and their specific needs.
>- Avoid overcomplicating or overloading dashboards with too many visuals, as this dilutes the message. Aim for a design that communicates clearly.
>- While QuickSight can do calculations, it's often best to perform complex computations in powerful database services like Amazon Redshift for efficiency.

**Visualization Tips:**
- Tables, traditional charts (pie, bar), gauges (for progress), geo-tagged maps. Experiment with different visual types to see what best conveys your data story.
- Place key performance indicators (KPIs) with directional trends at the top for quick viewing. Include more detailed visualizations lower on the page for users to drill down.
- Dynamic controls allow end-users to filter and slice visuals based on their specific needs based on parameters.

> [!NOTE]
> - QuickSight can automatically suggest recommended views.
> - You can import visuals from the HighCharts library by copying and pasting JSON code.

