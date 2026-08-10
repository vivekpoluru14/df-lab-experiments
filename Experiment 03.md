# Experiment 3: Password Capturing Using Wireshark

## Aim

To capture and analyze network packets using Wireshark and identify login credentials transmitted through HTTP traffic.

## Software Used

* Wireshark
* Windows or Linux Virtual Machine

## Introduction

Wireshark is a network packet capture and analysis tool. It can capture information transmitted over a network, including usernames, passwords, email addresses, and other personal information.

Wireshark can capture traffic from protocols such as:

* HTTP
* FTP
* Telnet

The captured network data can be used for troubleshooting network problems, but it can also be misused to obtain sensitive information.

In this experiment, Wireshark was used to capture network traffic and analyze HTTP packets to identify form data submitted during a login process.

## Procedure

### Step 1: Open Wireshark and Start Capture

Open **Wireshark** on Windows or in a Linux virtual machine.

Start capturing the network traffic.

In this experiment, the wireless network connection was selected for packet capture.

### Step 2: Enter Login Credentials

After starting the packet capture, open the required website.

Enter the login credentials on the website as part of the experiment.

The network traffic generated during the login process is captured by Wireshark.

### Step 3: Analyze the Captured Packets

After completing the login process, return to Wireshark.

Use appropriate display filters to identify the packets containing the login information.

Wireshark captures many different packets, so filtering is used to find the required HTTP traffic.

### Step 4: Filter HTTP Packets

In the Wireshark **Display Filter** bar, enter:

```text
http
```

This filter displays the captured HTTP packets.

The HTTP packets are then analyzed to find the form data submitted by the user.

### Step 5: Identify Form Submission Methods

Web forms such as login forms commonly use two methods for submitting data:

* **GET**
* **POST**

These methods can be filtered separately in Wireshark to analyze the captured HTTP requests.

### Step 6: Check GET Requests

To identify GET requests, enter the following filter in the Wireshark Display Filter bar:

```text
http.request.method == "GET"
```

Wireshark displays the captured GET packets.

The GET requests show requests for the login page, but the experiment did not find the submitted form data in the GET request.

### Step 7: Check POST Requests

Since the required form data was not found using GET, the POST method was checked.

Enter the following filter:

```text
http.request.method == "POST"
```

Wireshark displays the captured HTTP POST packets.

Select the packet containing the user information and examine the **HTML Form URL Encoded** section.

The submitted login form data can be viewed in this section.

### Step 8: View Captured Form Data

The captured form data showed the login information submitted through the website.

The captured form items were:

```text
Form item: "uname" = "vivek.m"
Form item: "pass" = "KALLU@W123"
```

These values matched the credentials entered during the login process.

## Result

The network traffic was successfully captured using **Wireshark**.

HTTP packets were filtered using the following display filter:

```text
http
```

GET requests were checked using:

```text
http.request.method == "GET"
```

Since the form data was not found in the GET request, POST requests were analyzed using:

```text
http.request.method == "POST"
```

The submitted form data was successfully identified in the **HTML Form URL Encoded** section of the captured HTTP POST packet.

## Output Screenshots
<img width="1917" height="1026" alt="Screenshot 2026-08-08 211221" src="https://github.com/user-attachments/assets/f75256ff-aa67-4465-b073-e8bfc7efec5d" />
<img width="1917" height="1078" alt="Screenshot 2026-08-08 224531" src="https://github.com/user-attachments/assets/7466e2c7-03d2-4248-b121-d04427e5d3fa" />
<img width="1917" height="1078" alt="Screenshot 2026-08-08 224546" src="https://github.com/user-attachments/assets/48a089c6-bc7b-48d9-a031-a4cf5aa5a787" />
<img width="1917" height="1078" alt="Screenshot 2026-08-08 224613" src="https://github.com/user-attachments/assets/89d6270e-f35c-4143-be7e-ece9013a2960" />


