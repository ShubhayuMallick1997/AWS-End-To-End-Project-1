<div align = center style="width: 100%; font-family: Arial, sans-serif; margin: auto;">

  <div style="text-align: center;">
    <h1 style="font-size: 32px; color: #d62828;">🔴 <u>AWS End-to-End Project Execution</u></h1>
    <h2 style="font-size: 24px; color: #003049;">Retail Domain | S3 + Glue + Athena | CSV, Parquet, JSON</h2>
  </div>

  <p style="font-size: 16px; text-align: justify;">
    Welcome to this hands-on <b>AWS Big Data Project</b> where we build a complete <b>retail data pipeline</b>
    using <b>Amazon S3</b>, <b>AWS Glue Visual Editor</b>, and <b>Amazon Athena</b> — all <i>without writing a single line of code</i>!
  </p>

  <hr/>

  <h3 style="text-align: center; color: #264653;">🚀 Project Overview</h3>

  <p style="text-align: justify;">
    In this mini end-to-end project, we demonstrate how to process <b>Retail domain data</b> from raw ingestion
    to structured querying using <b>AWS analytics services</b>.
  </p>

  <table style="width: 100%; border-collapse: collapse; font-size: 16px;" border="1">
    <tr style="background-color: #eaeaea;">
      <th style="text-align: left; padding: 10px;">📥 Source Files</th>
      <td style="padding: 10px;">
        <ul>
          <li><code>customer_data.csv</code></li>
          <li><code>sales_data.csv</code></li>
        </ul>
        Uploaded to <code>s3://your-bucket-name/raw/</code>
      </td>
    </tr>
  </table>

  <br/>

  <h3 style="text-align: center; color: #264653;">🔹 Step-by-Step Execution</h3>

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
  </table>

  <br/>
</div>
  <h3 style="text-align: center; color: #264653;">📂 Output Directory Structure</h3>

  <pre style="background: #f4f4f4; padding: 30px; border-left: 30px solid #888; font-size: 16px;">
s3://your-bucket-name/cleaned-data/
    ├── parquet/   (partitioned by country/sales_date)
    ├── json/
    └── csv/
  </pre>
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

  <div style="text-align: center; font-size: 16px;">
    📌 <b>Like 👍 | Share 📤 | Subscribe 🔔</b> for more hands-on AWS and Data Engineering content!
  </div>

</div>
</div>
