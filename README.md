# MQTT_OMRON_PLC_Datasheet
Sysmac Studio MQTT

AWS Setup:

Reference: http://www.osdes.com/oms/sample/navi/AWS1.html

Step 1: Create an AWS account

1-1. Create an account



Step 2: Create Policy

2-1. Open IoT Core

![image](https://github.com/junxian428/MQTT_OMRON_PLC_Datasheet/assets/58724748/2810d272-e53a-4eaa-b779-de834a206a7b)

2-2. Open Policy

![image](https://github.com/junxian428/MQTT_OMRON_PLC_Datasheet/assets/58724748/d714d2b0-d17b-4333-96f8-49b1f38d2b9d)

2-2. Create a policy

![image](https://github.com/junxian428/MQTT_OMRON_PLC_Datasheet/assets/58724748/6419b163-2bae-4898-991e-bad37e24d0b2)

Policy name (arbitrary)

Policy action = *

Policy resource = *

Enter the above and press the [Create] button

Here, the policy action and policy resource are set loosely, but please set them according to the actual operation


Step 3: Create Certificate

3-1. Add certificate

![image](https://github.com/junxian428/MQTT_OMRON_PLC_Datasheet/assets/58724748/de5e7c2f-330c-4f8e-94bb-c473f20628d7)


3-2. Create a certificate


![image](https://github.com/junxian428/MQTT_OMRON_PLC_Datasheet/assets/58724748/8fad3332-3d71-4def-ba69-6dfd3dc0b116)

3-3. Download certificate and key


![image](https://github.com/junxian428/MQTT_OMRON_PLC_Datasheet/assets/58724748/5dd365f6-a384-43f0-b654-add8a3b50638)

Step 4: Attach certificate and policy

4-1. Attach Policy

![image](https://github.com/junxian428/MQTT_OMRON_PLC_Datasheet/assets/58724748/a5d90b57-c5e0-4bdd-9ad2-b54f0ac148f9)

![image](https://github.com/junxian428/MQTT_OMRON_PLC_Datasheet/assets/58724748/91602d48-f86d-45cb-8b89-eb14fd752c35)

![image](https://github.com/junxian428/MQTT_OMRON_PLC_Datasheet/assets/58724748/f136f4dc-f8e9-49e7-aaf6-df1fc48ede34)

![image](https://github.com/junxian428/MQTT_OMRON_PLC_Datasheet/assets/58724748/cb28478a-c170-4a55-9c3e-04632b33d3e5)


_____________________________________________________________________________________________________________________________


PLC



1-Set PLC to Program mode

2- Execute the "Secure socket setting command" shortcut in the C:\ProgramData\Omron\Sysmac Studio\StartMenu\Sysmac Studio\Tools folder (or C:\ProgramData(
x86)\Omron\Sysmac Studio\StartMenu\Sysmac Studio\Tools )

3- Transfer certificate and key files to PLC
C:\ProgramData\Omron\Sysmac Studio\StartMenu\Sysmac Studio\Tools\TLSSettingTool>tlsconfig setSessionInfo /id 0 /key "C:\private\xxx-private.pem.key " /cert "C:\certs\xxx-certificate.pem.crt" /ip:192.168.10.201 /f
(xxx-private.pem.key and xxx-certificate.pem.crt are the downloaded files (If the file name is long, you can change it.)

![image](https://github.com/junxian428/MQTT_OMRON_PLC_Datasheet/assets/58724748/9808382f-2ab6-471f-9dfc-a3109855ce2d)


Version Software update log: 

https://automation.omron.com/en/ca/support/resources/software-revision-change-history/change-history-of-sysmac-studio

![image](https://github.com/junxian428/MQTT_OMRON_PLC_Datasheet/assets/58724748/e6a9a195-22f6-4b60-9416-b69271592381)

Solution:

![image](https://github.com/junxian428/MQTT_OMRON_PLC_Datasheet/assets/58724748/86ef69ce-be4a-4524-ba73-7084a17da181)
