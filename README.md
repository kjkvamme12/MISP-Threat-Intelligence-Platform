# MISP Threat Intelligence Platform

## Objective

The Detection Lab project aimed to establish a controlled environment for simulating and detecting cyber attacks. The primary focus was to ingest and analyze logs within a Security Information and Event Management (SIEM) system, generating test telemetry to mimic real-world attack scenarios. This hands-on experience was designed to deepen understanding of network security, attack patterns, and defensive strategies.

### Skills Learned
[Bullet Points - Remove this afterwards]

- Understand the role of the Threat Intelligence Platform in a SOC
- Use the MISP Threat Intelligence Platform to search and investigate data from an alert for fast context gathering.
- Correlate data across disparate events for better threat environment context
- Collect and enter new threat intelligence data into the threat intelligence platform.
- Use MISP to search for indicators from an alert that match any prevously seen or downloaded threat intelligence data.
  
  

### Tools Used

- MISP

## Steps

You received an alert that a file with a known malicious hash was found on the hard drive of an employee machine. 
The hash: 
830207029d83fd46a4a89cd623103ba2321b866428aa04360376e6a390063570

1. Search this hash in MISP, enter in the filter box and filter all results


   ![Screenshot 2025-01-27 122010](https://github.com/user-attachments/assets/b5943c25-0e28-45d4-bda3-f1e412fc6531)


![Screenshot 2025-01-27 123445](https://github.com/user-attachments/assets/9b98d15b-1ff8-4d05-846a-e0bad4969df2)

This hash appears to be associated with North Korean attributed cyber-attacks
Scrolling down page we see an object with a URL that leads to cisa.gov
Now we are provided with more detail and severity of the hash. 

## Publish an alert to the MISP  platform

1. Create a new event
    - Threat Level: High
    - Analysis: Ongoing
    - Event INfo: Maui Ransomware
  
  

![Screenshot 2025-01-27 123958](https://github.com/user-attachments/assets/18ade122-1a99-4510-88bd-462a42e324ff)

![Screenshot 2025-01-27 124052](https://github.com/user-attachments/assets/a5527144-e916-4e79-bf34-2c2747c9c2fc)

2. Import attributes to the container.
   - We will add IOCs to the event by using the Freetext Import Tool.
  ![Screenshot 2025-01-27 125158](https://github.com/user-attachments/assets/60a2f3be-d599-45ed-925a-50d0134673c2)
we will now post our IOCs, one per line.


![Screenshot 2025-01-27 130818](https://github.com/user-attachments/assets/4209f8b0-b853-4a26-864a-173ab1158b18)

This is the result from our freetext import tool. There is a column called Similar Attributes which shows the MISP event 1252 contains the same indicators. We essential entered data that is already in the MISP instance so that we can see what it looks like when there is an IOC match across two different events. 


![Screenshot 2025-01-27 133000](https://github.com/user-attachments/assets/6a5a868d-4e21-4a07-8a1d-417abcd57f70)

After importing our Freetext, we see our entered attributes are recorded into the event. 



3. View Correlation Graph

   
![Screenshot 2025-01-27 144206](https://github.com/user-attachments/assets/d3f6654d-2442-408d-be65-bc1dea0a64e0)

Click and drag events and attributes to organize the correlation graph. 


![Screenshot 2025-01-27 144419](https://github.com/user-attachments/assets/489234c4-245c-41c9-814b-254d2dfd952d)



