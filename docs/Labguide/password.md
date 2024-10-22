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

            document.getElementById("password").textContent = password;
        }
    </script>
</body>
</html>
