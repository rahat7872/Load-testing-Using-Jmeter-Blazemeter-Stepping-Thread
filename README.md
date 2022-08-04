# Load-testing-Using-Jmeter

# **What Is Load Testing**
A load test enables us to measure response times, throughput rates, and resource-utilization levels, and to identify your application’s breaking point, assuming that the breaking point occurs below the peak load condition. Load Testing ensures that your application can perform as expected in production. Just because your application will pass a functional test, this does not mean that it can perform the same under a load. Load testing identifies where and when your application breaks, so you can fix the issue before shipping to production. 

# **Load testing by Jmeter**
JMeter Load Testing is a testing process done using a load testing tool named Apache JMeter which is open source desktop application based on Java. JMeter for load testing is a crucial tool that determines whether the web application under test can satisfy high load requirements or not. It also helps to analyse overall server under heavy load.

# **Execute a performance Test on Jmeter**
Before testing the performance of target demo web application "Blazedemo" We have determined-
- Normal Load: Average number of users visit your website
- Heavy Load: The maximum number of users visit your website
- What is your target in this test?

**Step1- recording test script:**
The BlazeMeter Chrome Extension allows us to test your web application by recording user actions and HTTP requests to create a unique test artifact that runs both JMeter and Selenium tests. By default, every test step you perform is being recorded to a “Test Case”, and it will be a monolithic script with a sequence of actions. On the JMX level, this will simply create a thread group consisting of these actions. The recorder, in fact, treats each step as a single transaction controller, so if you prefer, you may rename the label, and add additional labels to group subsequent actions under their own transaction controllers.
- Clicked the BlazeMeter icon in your Chrome browser toolbar:
- Loggged in to my BlazeMeter account. Verify that you see the “Hi [username]” greeting in the upper right-hand corner to confirm that the plugin is logged in.
- Gave our test a name.
- Clicked the Start recording button.
- Performed the actions in target application that wish to simulate in our test.
- When finished, clicked the Stop recording button.
- Download, edit, or run the test in the cloud.

**Step2- Added thread group**
- Start JMeter
- Select Test Plan on the tree
- Add Thread Group
<p float="left">
    <img src="https://user-images.githubusercontent.com/57935394/182814362-e1037543-981f-4046-a291-8c56b64b90b5.PNG" width="600" />
  </p>

- Number of Threads: 10 (Number of users connects to the target website: 100)
- Loop Count: 10 (Number of time to execute testing)
- Ramp-Up Period: 10

**Added stepping thread group for more details:**
In the stepping Thread Group control panel, we enter Thread Properties as follows:
<p float="left">
    <img src="https://user-images.githubusercontent.com/57935394/182818250-da3b4b3b-96af-4407-88a5-70b8292c60e5.PNG" width="600" />
  </p>

**Step3- Added jmeter config elements:**
Now we determine what JMeter elements in this test. The elements are
- HTTP Cookie Manager
- This element can be added by right-clicking on the Thread Group and selecting: Add -> Config Element -> HTTP Cookie Manager
<p float="left">
    <img src="https://user-images.githubusercontent.com/57935394/182821772-6273df5c-c4c8-46d2-89c8-cb9d75e7428e.png" width="600" />
  </p>
  
  
**Step-4 Added Jmeter assertions**
- Response assertions
<p float="left">
    <img src="https://user-images.githubusercontent.com/57935394/182822975-2a8875f0-3dfc-4558-8c87-37e564156689.PNG" width="600" />
  </p>

**Step-5: Added Jmeter Listener**
- View results tree
<p float="left">
    <img src="https://user-images.githubusercontent.com/57935394/182824494-d9c9675a-c386-4e96-a709-194fffda6b91.PNG" width="600" />
  </p>
  
- View results in Table

<p float="left">
    <img src="https://user-images.githubusercontent.com/57935394/182824485-52f914d6-f959-48be-919a-178c76de503c.PNG" width="600" />
  </p>
  
- Graph results

<p float="left">
    <img src="https://user-images.githubusercontent.com/57935394/182824479-d3c20d9c-63a5-4f0c-9684-ce3c593df93c.PNG" width="600" />
  </p>
  
- Assertion results

<p float="left">
    <img src="https://user-images.githubusercontent.com/57935394/182824500-9b533895-9bf9-4535-9cb0-6944211ef566.PNG" width="600" />
  </p>
  
- Active threads over time


<p float="left">
    <img src="https://user-images.githubusercontent.com/57935394/182824490-d2154df8-d21a-40c4-8ef2-85f8cf675a03.PNG" width="600" />
  </p>


