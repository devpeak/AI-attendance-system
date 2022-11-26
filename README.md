<html>
<head>
</head>
<body>
<h2>AI-Attendance-System</h2>
<p align = "center">
<img src = "https://user-images.githubusercontent.com/100518568/197471002-d915c95d-b78a-4d97-9824-1eabca7f3e00.png" width = "210mm" height ="300mm" alt = "AWSomeify Hackathon"/>
</p>
We are building a cloud-based solution built using <strong>Amazon Web Services (AWS)</strong> for <em>automatically recording and tracking classroom attendance</em> using facial recognition.
<br>

<h3>♦ Motivation ♦</h4>
<ul>
<li>Physical Attendance is time consuming process.</li>
<li>Reducing human effort by automatic facial recognition.</li>
<li>No more loss of productivity.</li>
<li>Preventing fake Roll Calls.</li>
<li>Potential to benefit other environments e.g. Workplace. </li>
</ul>
<h3>♦ Introduction ♦</h3>
  The project will consist of three main components ⇝
 <dl>
 <dt> 🔵 AWS Facial Rekognition</dt>
 <dd> ➼ The facial recognition component will be responsible for recognizing students. </dd>
 <dt>🔵 A web based environment for Attendance Management System </dt>
 <dd>➼ Faculties: To maintain the attendance record of students mark via facial recognition system.</dd>
 <dd>➼ Student: can check attendance of multiple lectures. </dd>
 <dt>🔵 Camera:</dt>
 <dd>➼ Responsible for uploading classroom images to AWS for processing. </dd>
 </dl>
 <h3> ♦ Flowchart ♦ </h3>
 <img src = "https://user-images.githubusercontent.com/100518568/197422492-c2e775ab-023d-4b07-89df-f5dd558ebc39.png" alt = "flowchart">
 <br>
 <h2>Overview of Face Detection and Face Comparison </h2>
 <p> There are two primary applications of <b>machine learning</b> that analyze images containing faces: <em>face detection</em> and <em>face comparison</em>.</p>
 <p>A face detection system is designed to answer the question: <strong>is there a face in this picture?</strong><p>
 <ul>
 <li>A face detection system determines the presence, location, scale, and (possibly) orientation of any face present in a still image or video frame.</li>
 <li>This system is <strong><em> designed to detect the presence of faces</em></strong> regardless of attributes such as gender, age, and facial hair.</li>
 </ul>
 <br>
 <p>A face comparison system is designed to answer the question: <strong>does the face in an image match the face in another image?</strong></p>
 <ul>
 <li>A face comparison system takes an image of a face and makes a prediction about whether the face matches other faces in a provided database.</li>
 <li>Face comparison systems are <strong><em>designed to compare and predict potential matches of faces</em></strong> regardless of their expression, facial hair, and age.</li>
 </ul>
 <br>
 <h3>Comparing faces in images</h3>
 <p>To compare a face in the <em>source</em> image with each face in the <em>target</em> image, use the CompareFaces operation.</p>
 
 <h2>Set up the AWS CLI and AWS SDKs </h2>
 
 <ol>
 <li>Download and install the AWS CLI and the AWS SDKs that you want to use.</li>
 <li>Create an access key</li>
 
 <ol type="a">
 <li>Sign in to the AWS Management Console and open the IAM console</li>
 <li>In the navigation pane, choose Users.</li>
 <li>Choose the name of the user you created </li>
 <li>choose the Security credentials tab.</li>
 <li>Choose Create access key. Then choose Download .csv file to save the access key ID and secret access key to a CSV file on your computer.</li>
 </ol>
 <li>navigate to your home directory, in my case it is C:\Users\hp and create an <strong>.aws</strong> directory.</li>
 
 <li>In the <strong>.aws</strong> directory, create a new file named <b>credentials</b>.</li>
 
 <li>[default]<br>
aws_access_key_id = your_access_key_id<br>
aws_secret_access_key = your_secret_access_key</li>

<li>Save the <strong>Credentials</strong> file and delete the CSV file.</li>

<li>In the <bold>.aws</bold> directory, create a new file named <bold>config</bold>.</li>

<li>Open the <bold>config</bold> file and enter your <bold>region</bold> in the following format.</li>

<li>[default]<br>
region = your_aws_region</li>
<pre>Note: If you don't select a region, then us-east-1 will be used by default.
</pre>
</li>

<li>Save the config file.</li>
</ol>

<h2>Using Rekognition with an AWS SDK</h2>

<p>AWS software development kits (SDKs) are available for many popular programming languages. Each SDK provides an API, code examples, and documentation that make it easier for developers to build applications in their preferred language.</p>

<p>We are using AWS SDK for Python (Boto3) for our project</p>
<p>The SDK is composed of two key Python packages: Botocore (the library providing the low-level functionality shared between the Python SDK and the AWS CLI) and Boto3 (the package implementing the Python SDK itself).</p>
 <hr>
<h3> Steps needed to install the AWS SDK for Python.</h3>

<dl>
<dt>&#x1F4A1 Install Boto3</dt>
<dd><pre>pip install boto3</pre></dd>
</dl>
<dl>
<dt>&#x1F4A1 Using the AWS Common Runtime (CRT)</dt>
<dd>The AWS CRT is a collection of modular packages that serve as a new foundation for AWS SDKs. Each library provides better performance and minimal footprint for the functional area it implements. Using the CRT, SDKs can share the same base code when possible, improving consistency and throughput optimizations across AWS SDKs.
<pre>
<strong>pip install boto3[crt]</strong>
</pre>
</dd>
</dl>

 
 
 
 
 
 
 
 <h3>References </h3>
 <ul>
 <li>https://scholarworks.gvsu.edu/cistechlib/340/</li>
 <li>https://aws.amazon.com/rekognition/faqs/</li>
 <li>https://aws.amazon.com/lambda/faqs/ </li>
 <li>https://aws.amazon.com/rds/faqs/ </li>
 <li>https://aws.amazon.com/ec2/faqs/ </li>
 </ul>
</body>
</html>
