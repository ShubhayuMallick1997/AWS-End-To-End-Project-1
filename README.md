<div align = center style="width: 100%; font-family: Arial, sans-serif; margin: auto;">

  <div style="text-align: center;">
    <h1 style="font-size: 32px; color: #d62828;">🔴 <u>AWS End-to-End Project Execution</u></h1>
    <h2 style="font-size: 24px; color: #003049;">Retail Domain | S3 + Glue + Athena + Power BI | CSV, Parquet, JSON</h2>
  </div>

  <p style="font-size: 16px; text-align: justify;">
    Welcome to this hands-on <b>AWS Big Data Project</b> where we build a complete <b>retail data pipeline</b>
    using <b>Amazon S3</b>, <b>AWS Glue Visual Editor</b>, and <b>Amazon Athena</b>, <b>Power BI</b> — all <i>without writing a single line of code</i>!
  </p>

  <hr/>

  <h2 style="text-align: center; color: #264653;">🚀 Project Overview</h2>

  <p style="text-align: justify;">
    In this mini end-to-end project, we demonstrate how to process <b>Retail domain data</b> from raw ingestion
    to structured querying using <b>AWS analytics services</b>.
  </p>

  <table style="width: 100%; border-collapse: collapse; font-size: 16px;" border="1">
    <tr style="background-color: #eaeaea;">
      <th style="text-align: left; padding: 10px;">📥 Source Files</th>
      <td style="padding: 10px;">
        <ul>
          <li><code>customer.csv</code></li>
          <li><code>sales.csv</code></li>
        </ul>
        Uploaded to <code>s3://your-bucket-name/raw/</code>
      </td>
    </tr>
  </table>

  <br/>

  <h2 style="text-align: center; color: #264653;">🔹 Step-by-Step Execution</h2>

  <table style="width: 100%; border-collapse: collapse; font-size: 16px;" border="1">
    <tr>
      <td style="width: 5%; text-align: center;">1️⃣</td>
      <td>Upload raw <code>.csv</code> data files to S3</td>
    </tr>
    <tr>
      <td style="text-align: center;">2️⃣</td>
      <td>Create a Glue ETL Job using Visual Editor</td>
    </tr>
    <tr>
      <td style="text-align: center;">3️⃣</td>
      <td>Read Customer and Sales data from S3 using Glue</td>
    </tr>
    <tr>
      <td style="text-align: center;">4️⃣</td>
      <td>
        Apply transformations:
        <ul>
          <li>Join on <b>customer ID</b></li>
          <li>Remove <b>nulls</b></li>
          <li>Eliminate <b>duplicate records</b></li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align: center;">5️⃣</td>
      <td>
        Write transformed data back to S3 in 3 formats:
        <ul>
          <li>CSV</li>
          <li>Parquet</li>
          <li>JSON</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align: center;">6️⃣</td>
      <td>Partition data by <code>country</code> and <code>sales_date</code></td>
    </tr>
    <tr>
      <td style="text-align: center;">7️⃣</td>
      <td>Create a Glue Database and connect to Athena</td>
    </tr>
    <tr>
      <td style="text-align: center;">8️⃣</td>
      <td>Create an External Table in Athena using Parquet folder and partition projection</td>
    </tr>
    <tr>
      <td style="text-align: center;">9️⃣</td>
      <td>Run SQL queries in Athena for analytics and validation</td>
    </tr>
    <tr>
      <td style="text-align: center;">9️⃣</td>
      <td>Power BI Inegration to build Interactive Dashboard from output CSV</td>
    </tr>
  </table>

  <br/>
</div>

<table align="center" style="width: 100%; border-collapse: collapse; font-size: 16px;">
  <tr>
    <td style="width: 50%; vertical-align: top; text-align: center; font-weight: bold; padding: 20px;">
      <h3 align = center > 📂 Output Directory Structure </h3>
    </td>
    <td style="width: 65%; padding: 20px;">
      <pre style="background: #f4f4f4; padding: 20px; border-left: 6px solid #888; font-size: 16px; margin: 0;">
s3://your-bucket-name/cleaned-data/
    ├── parquet/   (partitioned by country/sales_date)
    ├── json/      (partitioned by country/sales_date)
    └── csv/       ((partitioned by country/sales_date)
    └── csv/       (Not Partitioned / Single File Output for Power BI Integration)
      </pre>
    </td>
  </tr>
  <tr>
    <td style="width: 35%; vertical-align: top; text-align: center; font-weight: bold; padding: 20px;">
      <h3 align = center> 📊 Power BI Integration </h3>
    </td>
    <td style="width: 65%; padding: 20px;">
      After the ETL process, the <code>CSV</code> file (without partitioning) stored in S3 was accessed locally.
      Using <b>Power BI Desktop</b>, the file was imported directly from the S3 bucket via a pre-signed URL / AWS connector.
      <br/><br/>
      Key dashboards created:
      <ul>
        <li>💰 <b>Total Sales by Country</b></li>
        <li>📆 <b>Sales Trend Over Time</b></li>
        <li>🛒 <b>Top Products by Region</b></li>
        <li>👤 <b>Customer Segmentation</b></li>
      </ul>
      These dashboards were built offline in Power BI using locally cached data and refreshed periodically.
    </td>
  </tr>
</table>
</table>

<table align="center" style="width: 100%; border-collapse: collapse; font-size: 16px;">
  <tr>
    <td style="width: 50%; vertical-align: top; text-align: center; font-weight: bold; padding: 20px;">
    <h3 align = center > 📂 ETL Pipeline on Glue Visual Editor </h3>
    </td>
    <td style="width: 65%; padding: 20px;">
      <pre style="background: #f4f4f4; padding: 20px; border-left: 1px solid #888; font-size: 16px; margin: 0;">
      <img src = "https://github.com/ShubhayuMallick1997/AWS-End-To-End-Project-1/blob/main/Screenshot%202025-07-15%20031408.png" width = "90%">
    </td>
  </tr>
    <tr>
    <td style="width: 50%; vertical-align: top; text-align: center; font-weight: bold; padding: 20px;">
    <h3 align = center > 📂 Athena Query to fetch filtered Data from External Table </h3>
    </td>
    <td style="width: 65%; padding: 20px;">
      <pre style="background: #f4f4f4; padding: 20px; border-left: 1px solid #888; font-size: 16px; margin: 0;">
      <img src = "https://github.com/ShubhayuMallick1997/AWS-End-To-End-Project-1/blob/main/Screenshot%202025-07-15%20004526.png" width = "90%">
    </td>
  </tr>
   </tr>
    <tr>
    <td style="width: 50%; vertical-align: top; text-align: center; font-weight: bold; padding: 20px;">
    <h3 align = center > 📂 Power BI Dashboard from Output CSV Data </h3>
    </td>
    <td style="width: 65%; padding: 20px;">
      <pre style="background: #f4f4f4; padding: 20px; border-left: 1px solid #888; font-size: 16px; margin: 0;">
      <img src = "https://github.com/ShubhayuMallick1997/AWS-End-To-End-Project-1/blob/main/Screenshot%202025-07-15%20024847.png" width = "70%">
      <img src = "https://github.com/ShubhayuMallick1997/AWS-End-To-End-Project-1/blob/main/Screenshot%202025-07-15%20024903.png" width = "70%">
      <img src = "https://github.com/ShubhayuMallick1997/AWS-End-To-End-Project-1/blob/main/Screenshot%202025-07-15%20024947.png" width = "70%">
      <img src = "https://github.com/ShubhayuMallick1997/AWS-End-To-End-Project-1/blob/main/Screenshot%202025-07-15%20025002.png" width = "70%">
    </td>
  </tr>
</table>


      

<div align = center>
  <br/>

  <h3 style="text-align: center; color: #264653;">🎯 What You’ll Learn</h3>

  <table style="width: 100%; border-collapse: collapse; font-size: 16px;" border="1">
    <tr>
      <td>✅</td><td>Build visual ETL pipelines using AWS Glue Studio</td>
    </tr>
    <tr>
      <td>✅</td><td>Handle multiple file formats: <code>CSV</code>, <code>JSON</code>, and <code>Parquet</code></td>
    </tr>
    <tr>
      <td>✅</td><td>Implement multi-level partitioning in Glue and Athena</td>
    </tr>
    <tr>
      <td>✅</td><td>Create and query external Athena tables on S3 data</td>
    </tr>
    <tr>
      <td>✅</td><td>Apply joins, deduplication, and null filtering in Glue jobs</td>
    </tr>
    <tr>
      <td>✅</td><td>Understand practical Retail domain data flow in cloud</td>
    </tr>
  </table>

  <br/>


</div>
</div>
