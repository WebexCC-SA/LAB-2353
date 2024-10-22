<!DOCTYPE html>
<html>
<head>
    <title>Attendee Password Lookup</title>
    <style>
        #password {
            font-weight: bold;
            color: red;
        }
    </style>
</head>
<body>
    <h2>Attendee Password Lookup</h2>
    <label for="attendeeID">Select Attendee ID:</label>
    <select id="attendeeID" onchange="showPassword()">
        <option value="">Select an Attendee ID</option>
        <option value="101">101</option>
        <option value="102">102</option>
        <option value="103">103</option>
        <option value="104">104</option>
        <!-- Add more attendee IDs as needed -->
        <option value="132">132</option>
    </select>

    <p>Password: <span id="password"></span></p>

    <script>
        function showPassword() {
            var attendeeID = document.getElementById("attendeeID").value;
            var password = "";

            switch (attendeeID) {
                case "101":
                    password = "CJBU@1234";
                    break;
                case "102":
                    password = "CJBU@1235";
                    break;
                case "103":
                    password = "CJBU@1236";
                    break;
                case "104":
                    password = "CJBU@1237";
                    break;
                // Add more cases as needed
                case "132":
                    password = "CJBU@1265";
                    break;
                default:
                    password = "";
            }

            document.getElementById("password").textContent = password;
        }
    </script>
</body>
</html>
