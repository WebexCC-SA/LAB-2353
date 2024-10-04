---
#icon: material/numeric-4-box-multiple
icon: material/folder-open-outline

title: Survey Insights
author: Gagarin Sathiyanarayanan
date: 2024-10-02
layout: post
---

!!! info "README"

    In this lab, we will make a test call to check the post-call survey feature using a pre-configured voice flow. We'll complete the survey as customers and then review/download the survey results from the administration portal. The steps for configuring the actual survey flow are at the end of this section but are not required to for this lab.

<script>
    function update(){them = Array.from(document.querySelectorAll("input")).reduce((acc, input) => ({...acc, [input.id + "_out"] : input.value}),{});
   Object.entries(them).forEach((entry) => {
    Array.from(document.getElementsByClassName(entry[0])).forEach((element,index) => 
    {
      console.log(document.getElementsByClassName(entry[0])[index].innerHTML); 
      document.getElementsByClassName(entry[0])[index].innerHTML = entry[1];
    })})

  event.preventDefault()
   if(document.forms["attendee-form"][1].value != "Your_Attendee_ID"){
    localStorage.setItem("attendeeID",document.forms["attendee-form"][1].value)
  }  
  }
</script>

## 7.1 Agent Login



!!! tip "Please submit the form below with your Attendee ID in 3 digits long format (e.g. if your attendee ID is 51, please enter 051) and click Save. All configuration items in the lab guide will be renamed with that prefix."

    <script>
    document.forms["attendee-form"][1].value = localStorage.getItem("attendeeID") || "Your Attendee ID"; 
    update();
    </script>
    <form id="attendee-form">
    <label for="attendee">Attendee ID:</label>
    <input type="text" id="attendee" name="attendee" onChange="update()" style="border: 2px solid black; padding: 5px; border-radius: 4px; background-color: orange;"><br>
    <br>
    <button type="button" onclick="update()" style="background-color: #4CAF50; color: white; padding: 10px 20px; border: none; border-radius: 5px; cursor: pointer; font-size: 16px;">Save</button>
    </form>
    <script>
    document.forms["attendee-form"][1].value = localStorage.getItem("attendeeID") || "Your Attendee ID";
    update();
    </script>

| **User Role** | **User email**                                                   | **Endpoint**   |
| ------------- | ---------------------------------------------------------------- | -------------- |
| Agent         | wxcclabs+agent\_<w class="attendee_out">AttendeeID</w>@gmail.com | WebRTC/Desktop |

> **Note**: To log in to the agent desktop, use either a different web browser or a new incognito web page. This will prevent the browser caching issues with admin and agent credentials.
>


- Navigate to **[Desktop](https://desktop.wxcc-us1.cisco.com/){:target="\_blank"}** in the chrome browser with the incognito mode.

- Enter the agent’s **email ID**.

- Enter the **Password** for the appropriate username.

- In the **_Station Credentials_** pane, select **"Desktop"**.

- Select the team **<w class="attendee_out">Your_Attendee_ID</w>\_Team1**.

- Click the **_Submit_** button. The browser may ask you to confirm the use the microphone from the browser.

- Make sure that you are successfully logged in to the Agent Desktop.

![Agent Sign In](../assets/images/AG-2.gif)

## 7.2 Provide a survey response

- Login to your Agent Desktop and make your state Available

- Dial  `+14402308301`  and enter your `Attendee ID` followed by `#`

- Accept the call from the agent desktop and disconnect the call by clicking the `End Call` button in agent desktop

     ![analyzer](../assets/images/Analyzer/survey1.gif)


- End the interaction from the Agent Desktop
- The customer voice call leg should now connect to the IVR survey flow. Follow the instructions and provice the survey rating

## 7.3 Access Survey Response Report

- From Control hub, access `Analyzer`

     ![analyzer](../assets/images/Analyzer/survey2.png)

- Navigate to Visualisation > search for `Survey Response` and open the report. 

     ![analyzer](../assets/images/Analyzer/survey3.png)

- Survey response that you provided in the previous section will take close to 20 minutes to show up in the report. However, you can view the historic survey responses in the report and explore the filter options

     ![analyzer](../assets/images/Analyzer/survey4.png)

## 7.4 Download Survey Response Report

- Navigate to `Surveys` section in control hub and click the download option against one of the configured surveys

     ![analyzer](../assets/images/Analyzer/survey5.png)

- Choose desired response time period and click `Download`

     ![analyzer](../assets/images/Analyzer/survey6.png)

## 7.5 [OPTIONAL] Configure new survey

- Click on Contact Center under Services from Control Hub
     
     ![analyzer](../assets/images/Analyzer/survey7.gif)

- Under Contact Center, click on Surveys
     
     ![analyzer](../assets/images/Analyzer/survey8.gif)

- Click the “Create new survey” button on the top-right corner of the Survey page

     ![analyzer](../assets/images/Analyzer/survey9.gif)

- Provide name for your survey as **Survey\_<w class="attendee_out">AttendeeID</w>** . Survey has to be named in this format for the flow to work. Select Language and click `Next`

     ![analyzer](../assets/images/Analyzer/survey10.png)

- Download the audio files : ![Click here to download](../assets/Survey_wav.zip)
  
- Upload `Welcome.wav` in the `Welcome note` section

     ![analyzer](../assets/images/Analyzer/survey11.gif)

- Add a desired survey question and upload `nps.wav` 

    ![analyzer](../assets/images/Analyzer/survey12.gif)

- Upload `Thankyou.wav` in the `Thank you note` section

    ![analyzer](../assets/images/Analyzer/survey13.gif)

- Review the audio files if required and click `Next`
    
    ![analyzer](../assets/images/Analyzer/survey14.png)

- Click `Save`
    
    ![analyzer](../assets/images/Analyzer/survey15.png)

## 7.6 [OPTIONAL] Add the feedback activity to your flow

- Navigate to `Flows` section in control hub and make a copy of the `Survey_Template` flow 
    
    ![analyzer](../assets/images/Analyzer/survey16.png)

- Search for the string `Copy_Survey` and open the flow

    ![analyzer](../assets/images/Analyzer/survey17.png)

- Edit the flow and rename it as **Survey\_<w class="attendee_out">AttendeeID</w>**

    ![analyzer](../assets/images/Analyzer/survey18.gif)

- Navigate to `Event Flow` , select `FeedbackV2` activity and under `Survey Method` select your respective survey created in the previous section

    ![analyzer](../assets/images/Analyzer/survey19.gif)

- Validate and publish the flow

    ![analyzer](../assets/images/Analyzer/survey20.gif)

- Map this flow to the respective Entrypoint DN assigned to you. 

- Navigate to `Channels` , lookup for **WX1_EP\_<w class="attendee_out">AttendeeID</w>** and select it. 

- Update `Routing Flow` as **Survey\_<w class="attendee_out">AttendeeID</w>** and `Version Label` as `Live` . Click Save.

    ![analyzer](../assets/images/Analyzer/survey21.gif)

- Login to your Agent Desktop and make your state Available

- Dial the respective DN assigned to your entrypoint  **WX1_EP\_<w class="attendee_out">AttendeeID</w>**  and enter your `Attendee ID` followed by `#`

- Accept the call from the agent desktop and disconnect the call by clicking the `End Call` button in agent desktop

     ![analyzer](../assets/images/Analyzer/survey1.gif)


- End the interaction from the Agent Desktop
- The customer voice call leg should now connect to the IVR survey flow. Follow the instructions and provice the survey rating

**Congratulations, you have completed this lab! You can continue with the next one.**
