## **week 6: User centered design and quick prototyping, experiment with 3D models**

For my final assignment, I designed an interactive digital experience aimed at enhancing visitor engagement in a museum or exhibition. 
The system integrates an RFID wristband, 3D models, and audio guides to create a personalized journey through the exhibition.

### Steps to build this prototype:

#### 1. RFID Wristband Integration: 
he core of this system relies on the RFID wristband, which is scanned by an RFID card reader. Each wristband contains a unique identifier linked to a list of visitors and their prefered language. When the wristband is scanned, it triggers the system to recognize the visitor and load their personalized content.

#### 2. Raspberry Pi Setup:
I used a Raspberry Pi as the central hub for this prototype. The Raspberry Pi communicates with the RFID reader and a small touchscreen display. It also serves as the server for hosting the website that contains all the 3D models and audio guides.

#### 3. Website with 3D Models and Audio Guides: 
Once the RFID wristband is scanned, the Raspberry Pi loads a website that displays a selection of 3D models related to the exhibits and plays audio guides in the language saved on the wristband. This allows visitors to explore and learn about the artifacts through interactive and personalized content.

#### 4: Language and Content Customization:
I used AI tools to convert text into speech, gathering detailed information about each artifact from QM's online collection. I then created an audio guide available in four languages: Arabic, English, Urdu, and French.


This week, I gained practical experience in using Mermaid for creating flowcharts. The syntax is straightforward, and it’s an effective tool for visualizing decision-making processes.




