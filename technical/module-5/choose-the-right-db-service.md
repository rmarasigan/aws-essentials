# Choose the Right Database Service

### AWS database services
AWS has a variety of database options for different use cases. The following table provides a quick look at the AWS database portfolio.

<table>
  <thead>
		<tr>
      <th>Database Type</th>
      <th>Use Cases</th>
      <th>AWS Service</th>
    </tr>
  </thead>
  <tbody>
		<tr>
      <td>Relational</td>
      <td>Traditional applications, ERP, CRM, e-commerce</td>
      <td>Amazon RDS, Amazon Aurora, Amazon Redshift</td>
    </tr>
		<tr>
      <td>Key-value</td>
      <td>High-traffic web apps, e-commerce systems, gaming applications</td>
      <td>Amazon DynamoDB</td>
    </tr>
		<tr>
      <td>In-memory</td>
      <td>Caching, session management, gaming leaderboards, geospatial applications</td>
      <td>Amazon ElastiCache for Memcached, Amazon ElastiCache for Redis</td>
    </tr>
		<tr>
      <td>Document</td>
      <td>Content management, catalogs, user profiles</td>
      <td>Amazon DocumentDB (with MongoDB compatibility)</td>
    </tr>
		<tr>
      <td>Wide column</td>
      <td>High-scale industrial apps for equipment maintenance, fleet management, and route optimization</td>
      <td>Amazon Keyspaces (for Apache Cassandra)</td>
    </tr>
		<tr>
      <td>Graph</td>
      <td>Fraud detection, social networking, recommendation engines</td>
      <td>Amazon Neptune</td>
    </tr>
		<tr>
      <td>Time series</td>
      <td>IoT applications, DevOps, industrial telemetry</td>
      <td>Amazon Timestream</td>
    </tr>
		<tr>
      <td>Ledger</td>
      <td>Systems of record, supply chain, registrations, banking transactions</td>
      <td>Amazon QLDB</td>
    </tr>
  </tbody>
</table>

## Breaking up applications and databases

As the industry changes, applications and databases change too. Today, with larger applications, you no longer see just one database supporting it. Instead, applications are broken into smaller services, each with their own purpose-built database supporting it. This shift removes the idea of a one-size-fits-all database and replaces it with a complimentary database strategy. You can give each database the appropriate functionality, performance, and scale that the workload requires.

## Resources
* [Databases on AWS](https://aws.amazon.com/products/databases/)
* [AWS Database Blog](https://aws.amazon.com/blogs/database/?nc=sn&loc=4)
* [Database Freedom](https://aws.amazon.com/products/databases/freedom/?nc=sn&loc=5)