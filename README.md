<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>High-Level Architecture Overview</title>
</head>
<body>

<h1>High-Level Architecture Overview</h1>

<img src="https://imgur.com/RvJ41Cu" alt="High-Level Architecture">

<h2>Overview</h2>
<p>This repository contains a high-level architecture diagram for our web application hosted on AWS. The architecture leverages various AWS services to ensure scalability, security, and high availability.</p>

<h2>Architecture Components</h2>
<ul>
    <li><strong>Users</strong>: The end-users who interact with the application.</li>
    <li><strong>Amazon Route 53</strong>: Provides domain name system (DNS) web services.</li>
    <li><strong>AWS WAF</strong>: A web application firewall that helps protect the web applications from common web exploits.</li>
    <li><strong>Amazon CloudFront</strong>: A content delivery network (CDN) that distributes content to end-users with low latency.</li>
    <li><strong>Elastic Load Balancing (ELB)</strong>: Distributes incoming application traffic across multiple targets, such as EC2 instances.</li>
    <li><strong>Amazon EC2 Web Servers</strong>: Hosts the web server instances in a web subnet, with auto-scaling enabled for handling varying loads.</li>
    <li><strong>Amazon EC2 Application Servers</strong>: Hosts the application server instances in an application subnet, also with auto-scaling.</li>
    <li><strong>Amazon ElastiCache</strong>: Provides caching to improve the performance and scalability of the application.</li>
    <li><strong>Amazon Aurora</strong>: A MySQL and PostgreSQL-compatible relational database.</li>
    <li><strong>Amazon Aurora Replica</strong>: Provides high availability and read scalability for the Aurora database.</li>
    <li><strong>NAT Gateway</strong>: Allows instances in a private subnet to connect to the internet or other AWS services, but prevents the internet from initiating connections with those instances.</li>
    <li><strong>Elastic File System (EFS)</strong>: Provides scalable file storage for use with Amazon EC2.</li>
</ul>

<h2>Network Structure</h2>
<ul>
    <li><strong>VPC (Virtual Private Cloud)</strong>: Isolates the network environment for the application.</li>
    <li><strong>Public Subnet</strong>: Contains the NAT Gateways.</li>
    <li><strong>Web Subnet</strong>: Hosts the Amazon EC2 web server instances.</li>
    <li><strong>App Subnet</strong>: Hosts the Amazon EC2 application server instances.</li>
    <li><strong>DB Subnet</strong>: Hosts the Amazon Aurora and Aurora Replica instances.</li>
</ul>

<h2>Security</h2>
<ul>
    <li><strong>AWS WAF</strong>: Protects against web exploits and attacks.</li>
    <li><strong>Security Groups</strong>: Act as a virtual firewall for the instances to control incoming and outgoing traffic.</li>
    <li><strong>Network Access Control List (NACL)</strong>: Provides an additional layer of security for the VPC.</li>
</ul>

<h2>How to Use</h2>
<p>To deploy the architecture, follow these steps:</p>
<ol>
    <li>Clone the repository.</li>
    <li>Review the architecture diagram and familiarize yourself with the components.</li>
    <li>Use the provided CloudFormation templates or Terraform scripts to set up the environment (scripts provided in the repository).</li>
</ol>

<h2>Contribution</h2>
<p>Feel free to contribute to the repository by opening issues or submitting pull requests.</p>

<h2>License</h2>
<p>This project is licensed under the MIT License.</p>

</body>
</html>
