# Endpoint-Investigation--Redline

![image](https://github.com/user-attachments/assets/9ad283ea-a638-4233-bf88-028b2b208d0c)



## Personal Project: Endpoint Investigation - Memory Analysis

### Scenario

As part of my role as a Junior SOC Analyst, I was presented with a situation where a Senior Accountant named Charles reported that he could no longer access the spreadsheets and other files he had been working on. Additionally, he mentioned that his wallpaper had been changed to display a message indicating that his files had been encrypted—a clear sign of a ransomware attack. My task was to perform a memory analysis on the compromised host to investigate the incident and provide answers to specific questions regarding the attack.
Task

I was instructed to navigate to a folder titled Endpoint Investigation on my desktop and load the AnalysisSession1.mans file into Redline for analysis. Below are the detailed steps I followed, along with my findings.

#### Question 1: Can you identify the product name of the machine?

![image](https://github.com/user-attachments/assets/14bd1c23-6f40-4173-98e1-2a8e0a0e842d)

Explanation: After loading the analysis file from the Endpoint Investigation folder, I navigated to the "System Information" section on the left side of Redline's interface. This section provides a summary of the system's hardware and software details. I looked specifically for any mention of the product name of the machine.

Answer: Windows 7 Home Basic


#### Question 2: Can you find the name of the note left on the Desktop for “Charles”?

Explanation: Initially, I explored the File Downloaded History tab but did not find any relevant information. I decided to investigate the contents of Charles' desktop. To do this, I accessed the File System section on the left-hand side of Redline, expanded the menu until I reached the desktop directory, and found a suspicious .txt file. By double-clicking on it, I was able to see the file details and copy the filename.

![image](https://github.com/user-attachments/assets/1d054a33-caf9-4950-a87c-2d185ff39aa0)

Answer: R_E_A_D___T_H_I_S___AJYG1O.txt

#### Question 3: Find the Windows Defender service; what is the name of its service DLL?

Explanation: To locate the Windows Defender service, I navigated to the Windows Services tab. I used the search function to look for "Windows Defender," which yielded one result. By double-clicking on this service, I accessed the details where the service DLL was listed.

![image](https://github.com/user-attachments/assets/4641d9bc-cfca-474d-a854-7ec5204224f2)

Answer: MpSvc.dll


#### Question 4: The user manually downloaded a zip file from the web. Can you find the filename?

Explanation: I started by checking the File Downloaded History tab and used the search function, but this did not yield the desired results. I then sorted the entries by the "Download Type" column, where I found a manual download entry. I realized that my initial search had been restricted to the "Target Directory" column. Once I corrected my approach, I identified the filename.


Answer: eb5489216d4361f9e3650e6a6332f7ee21b0bc9f3f3a4018c69733949be1d481.zip


#### Question 5: Provide the filename of the malicious executable that got dropped on the user’s Desktop.

Explanation: I revisited the desktop directory, where I discovered an .exe file that appeared suspicious. This was identified as the dropped malicious executable.


Answer: Endermanch@Cerber5.exe


#### Question 6: Provide the MD5 hash for the dropped malicious executable.

Explanation: Initially, I attempted to retrieve the MD5 hash by using the URL found in the File Download History and checking it on VirusTotal, but this led to no results. I then searched for the .zip file on VirusTotal, which again proved unfruitful. Finally, I switched to the Timeline tab, where I found entries containing MD5 hashes. By searching for the .exe file in this tab, I found the correct MD5 hash.

![image](https://github.com/user-attachments/assets/fe9aa8be-5266-412f-8b53-745b70d81a43)


Answer:60a95b2c2d77cd5d232296a7fa4

#### Question 7: What is the name of the ransomware?

Explanation: I submitted the MD5 hash of the malicious executable to VirusTotal. In the "Details" tab of the VirusTotal report, the name "Cerber" appeared multiple times. To confirm, I conducted a quick search online, which verified that Cerber is indeed a type of ransomware.

 fe1bc![Screenshot from 2024-09-01 22-28-39](https://github.com/user-attachments/assets/ae0fb0e2-3c2f-4b09-9c34-7ac4dadd96c9)

Answer: Cerber


#### Conclusion

This project involved performing a memory analysis on a compromised host using Redline to investigate a ransomware attack. I encountered various challenges, primarily related to the slow performance of the analysis tool, which tested my patience and focus. However, the experience was highly rewarding, as it provided me with practical exposure to tools and techniques used in real-world cybersecurity investigations.


#### Experience Gained

  Tool Proficiency: I became more proficient in using Redline for memory analysis, learning how to navigate its interface to extract critical information.
  
  Analytical Thinking: This project enhanced my analytical thinking, particularly in tracing the steps of a ransomware attack and identifying key artifacts.
  
  Use of External Resources: I improved my skills in leveraging external resources like VirusTotal and online search engines to validate my findings.


#### Benefits

  Practical Experience: Gained hands-on experience with a real-world scenario, which is crucial for a career in cybersecurity.
  
  Problem-Solving: Developed problem-solving skills by troubleshooting and finding alternative ways to gather information when initial methods did not work.
  
  Confidence Boost: Successfully completing this investigation has increased my confidence in handling similar incidents in the future.


This project was a significant step forward in my journey as a SOC Analyst, reinforcing the importance of persistence, attention to detail, and a methodical approach in cybersecurity investigations.


