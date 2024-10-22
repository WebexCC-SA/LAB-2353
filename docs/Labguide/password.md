

<!-- BACKUP: 


<!DOCTYPE html>
<html>
<head>
    <title>Attendee Password Lookup</title>
    <style>
        #password {
            font-weight: bold;
            color: red;
        }
        #refreshBtn {
            margin-top: 10px;
            padding: 10px;
            background-color: #007BFF;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        #refreshBtn:hover {
            background-color: #0056b3;
        }
        .instruction {
            font-style: italic;
            color: gray;
        }
    </style>
</head>
<body>
    <h2>Attendee Password Lookup</h2>
    <p class="instruction">Please enter the attendee ID that you have been provided. <br>
    <i>(The ID is available on the desktop you are sitting on.)</i></p>
    
    <label for="attendeeID">Select Attendee ID:</label>
    <select id="attendeeID" onchange="showPassword()">
        <option value="">Select an Attendee ID</option>
        <option value="101">101</option>
        <option value="102">102</option>
        <option value="103">103</option>
        <option value="104">104</option>
        <option value="105">105</option>
        <option value="106">106</option>
        <option value="107">107</option>
        <option value="108">108</option>
        <option value="109">109</option>
        <option value="110">110</option>
        <option value="111">111</option>
        <option value="112">112</option>
        <option value="113">113</option>
        <option value="114">114</option>
        <option value="115">115</option>
        <option value="116">116</option>
        <option value="117">117</option>
        <option value="118">118</option>
        <option value="119">119</option>
        <option value="120">120</option>
        <option value="121">121</option>
        <option value="122">122</option>
        <option value="123">123</option>
        <option value="124">124</option>
        <option value="125">125</option>
        <option value="126">126</option>
        <option value="127">127</option>
        <option value="128">128</option>
        <option value="129">129</option>
        <option value="130">130</option>
        <option value="131">131</option>
        <option value="132">132</option>
    </select>

    <p>Password: <span id="password"></span></p>
    <button id="refreshBtn" style="display:none;" onclick="resetSelection()">Try Another ID</button>

    <script>
        function showPassword() {
            var attendeeID = document.getElementById("attendeeID").value;
            var password = "";

            switch (attendeeID) {
                case "101":
                    password = "Nf$#3cun";
                    break;
                case "102":
                    password = "t3d!nF7X";
                    break;
                case "103":
                    password = "T$M5Cxv9";
                    break;
                case "104":
                    password = "Zu54q6@w";
                    break;
                case "105":
                    password = "nkm8XL@P";
                    break;
                case "106":
                    password = "G7Hx@%4F";
                    break;
                case "107":
                    password = "f6kZx@8N";
                    break;
                case "108":
                    password = "A64rX!fn";
                    break;
                case "109":
                    password = "Fy#m7NDY";
                    break;
                case "110":
                    password = "J3pd6!4r";
                    break;
                case "111":
                    password = "TX26#4mv";
                    break;
                case "112":
                    password = "D%a2$d6m";
                    break;
                case "113":
                    password = "y5zV!eW6";
                    break;
                case "114":
                    password = "QG%d5rpC";
                    break;
                case "115":
                    password = "a%9F7vHt";
                    break;
                case "116":
                    password = "mCvJw%4s";
                    break;
                case "117":
                    password = "Txzt7e@U";
                    break;
                case "118":
                    password = "N3yPM7$9";
                    break;
                case "119":
                    password = "C#Nmz3TF";
                    break;
                case "120":
                    password = "MB3cnD%6";
                    break;
                case "121":
                    password = "g%9$nBNZ";
                    break;
                case "122":
                    password = "X3r@GSus";
                    break;
                case "123":
                    password = "HMY!4$mr";
                    break;
                case "124":
                    password = "R%f#6GzV";
                    break;
                case "125":
                    password = "A6%nUsy$";
                    break;
                case "126":
                    password = "a!7#W4Ud";
                    break;
                case "127":
                    password = "ubP3w!gt";
                    break;
                case "128":
                    password = "XsP43T$A";
                    break;
                case "129":
                    password = "Zv4%9A@p";
                    break;
                case "130":
                    password = "pH%5rQ42";
                    break;
                case "131":
                    password = "W6%ZMRg2";
                    break;
                case "132":
                    password = "c!Wx3bFa";
                    break;
                default:
                    password = "";
            }

            if (password) {
                document.getElementById("password").textContent = password;
                document.getElementById("attendeeID").disabled = true;
                document.getElementById("refreshBtn").style.display = "inline";
            }
        }

        function resetSelection() {
            document.getElementById("attendeeID").disabled = false;
            document.getElementById("attendeeID").value = "";
            document.getElementById("password").textContent = "";
            document.getElementById("refreshBtn").style.display = "none";
        }
    </script>
</body>
</html> -->



<!-- Latest:  -->



<script>
    function update() {
        them = Array.from(document.querySelectorAll("input")).reduce((acc, input) => ({...acc, [input.id + "_out"] : input.value}),{});
        Object.entries(them).forEach((entry) => {
            Array.from(document.getElementsByClassName(entry[0])).forEach((element, index) => {
                document.getElementsByClassName(entry[0])[index].innerHTML = entry[1];
            });
        });

        event.preventDefault();
        var attendeeID = document.getElementById("attendee").value;
        if (attendeeID !== "Your Attendee ID") {
            localStorage.setItem("attendeeID", attendeeID);
        }

        showPassword();
    }

    function showPassword() {
        var attendeeID = document.getElementById("attendee").value; // Get the attendee ID directly from the input field
        var password = "";

        switch (attendeeID) {
            case "101":
                password = "Nf$#3cun";
                break;
            case "102":
                password = "t3d!nF7X";
                break;
            case "103":
                password = "T$M5Cxv9";
                break;
            case "104":
                password = "Zu54q6@w";
                break;
            case "105":
                password = "nkm8XL@P";
                break;
            case "106":
                password = "G7Hx@%4F";
                break;
            case "107":
                password = "f6kZx@8N";
                break;
            case "108":
                password = "A64rX!fn";
                break;
            case "109":
                password = "Fy#m7NDY";
                break;
            case "110":
                password = "J3pd6!4r";
                break;
            case "111":
                password = "TX26#4mv";
                break;
            case "112":
                password = "D%a2$d6m";
                break;
            case "113":
                password = "y5zV!eW6";
                break;
            case "114":
                password = "QG%d5rpC";
                break;
            case "115":
                password = "a%9F7vHt";
                break;
            case "116":
                password = "mCvJw%4s";
                break;
            case "117":
                password = "Txzt7e@U";
                break;
            case "118":
                password = "N3yPM7$9";
                break;
            case "119":
                password = "C#Nmz3TF";
                break;
            case "120":
                password = "MB3cnD%6";
                break;
            case "121":
                password = "g%9$nBNZ";
                break;
            case "122":
                password = "X3r@GSus";
                break;
            case "123":
                password = "HMY!4$mr";
                break;
            case "124":
                password = "R%f#6GzV";
                break;
            case "125":
                password = "A6%nUsy$";
                break;
            case "126":
                password = "a!7#W4Ud";
                break;
            case "127":
                password = "ubP3w!gt";
                break;
            case "128":
                password = "XsP43T$A";
                break;
            case "129":
                password = "Zv4%9A@p";
                break;
            case "130":
                password = "pH%5rQ42";
                break;
            case "131":
                password = "W6%ZMRg2";
                break;
            case "132":
                password = "c!Wx3bFa";
                break;
            default:
                password = "Invalid Attendee ID";
        }

        document.getElementById("passwordDisplay").textContent = password;
    }
</script>

!!! tip "Please submit the form below with your Attendee ID in 3 digits long format (e.g. if your attendee ID is 51, please enter 051) and click Save. All configuration items in the lab guide will be renamed with that prefix."

    <script>
    document.getElementById("attendee").value = localStorage.getItem("attendeeID") || "Your Attendee ID"; 
    update();
    </script>
    <form id="attendee-form">
    <label for="attendee">Attendee ID:</label>
    <input type="text" id="attendee" name="attendee" onChange="update()" style="border: 2px solid black; padding: 5px; border-radius: 4px; background-color: orange;"><br>
    <br>
    <button type="button" onclick="update()" style="background-color: #4CAF50; color: white; padding: 10px 20px; border: none; border-radius: 5px; cursor: pointer; font-size: 16px;">Save</button>
    </form>

<h3>Your Password:</h3>
<p id="passwordDisplay" style="font-weight: bold; color: red;"></p>

<table>
  <tr>
    <td style="font-weight: bold;">Your Administrator Login</td>
    <td>wxcclabs+admin_ID<w class="attendee_out">AttendeeID</w>@gmail.com</td>
  </tr>
  <tr>
    <td style="font-weight: bold;">Your Agent Login</td>
    <td>wxcclabs+agent_ID<w class="attendee_out">AttendeeID</w>@gmail.com</td>
  </tr>
  <tr>
    <td style="font-weight: bold;">Your Supervisor Login</td>
    <td>wxcclabs+supvr_ID<w class="attendee_out">AttendeeID</w>@gmail.com</td>
  </tr>
  <tr>
    <td style="font-weight: bold;">Your Voice Entrypoint ID</td>
    <td>WX1_EP_<w class="attendee_out">AttendeeID</w></td>
  </tr>
  <tr>
    <td style="font-weight: bold;">Your Team1</td>
    <td><w class="attendee_out">AttendeeID</w>_Team1</td>
  </tr>
  <tr>
    <td style="font-weight: bold;">Your Team2</td>
    <td><w class="attendee_out">AttendeeID</w>_Team2</td>
  </tr>
  <tr>
    <td style="font-weight: bold;">Control Hub</td>
    <td><a href="https://admin.webex.com/">https://admin.webex.com/</a></td>
  </tr>
  <tr>
    <td style="font-weight: bold;">Agent Desktop</td>
    <td><a href="https://desktop.wxcc-us1.cisco.com/">https://desktop.wxcc-us1.cisco.com/</a></td>
  </tr>
  <tr>
    <td style="font-weight: bold;">Analyzer</td>
    <td><a href="https://analyzer-v2.wxcc-us1.cisco.com/analyzer">Analyzer</a></td>
  </tr>
  <tr>
    <td style="font-weight: bold;">Search Task API Documentation</td>
    <td><a href="https://developer.webex-cx.com/documentation/search/v1/search-tasks">Search Task API</a></td>
  </tr>
</table> -->

<!-- <h3>Your Password:</h3>
<p id="passwordDisplay" style="font-weight: bold; color: red;"></p>
 -->
