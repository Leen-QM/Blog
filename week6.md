## **week 6: User centered design and quick prototyping, experiment with 3D models**

For my final assignment, I designed an interactive digital experience aimed at enhancing visitor engagement in a museum or exhibition. 
The system integrates an RFID wristband, 3D models, and audio guides to create a personalized journey through the exhibition.

### Steps to build this prototype:

#### 1. RFID Wristband Integration: 
This system relies on the RFID wristband, which is scanned by an RFID card reader. Each wristband contains a unique identifier linked to a list of visitors and their prefered language. When the wristband is scanned, it triggers the system to recognize the visitor and load their personalized content.

#### 2. Raspberry Pi Setup:
I used a Raspberry Pi as the central hub for this prototype. The Raspberry Pi communicates with the RFID reader and a small touchscreen display. It also serves as the server for hosting the website that contains all the 3D models and audio guides.

#### 3. Website with 3D Models and Audio Guides: 
Once the RFID wristband is scanned, the Raspberry Pi loads a website that displays a selection of 3D models related to the exhibits, which are fetched from the Sketchfab website and displayed using iframes. This allows for smooth integration and easy viewing of the models directly within the web interface. Additionally, audio guides in the language saved on the wristband are played, offering a personalized and interactive experience. This setup allows visitors to explore and learn about the artifacts in a dynamic way through both visual and auditory content.

#### 4. Language and Content Customization:
I used AI tools to convert text into speech, gathering detailed information about each artifact from QM's online collection. I then created an audio guide available in four languages: Arabic, English, Urdu, and French.


The final prototype successfully demonstrated the potential of combining RFID technology, interactive 3D models, and personalized audio guides to create a more engaging museum experience. Visitors could scan their wristbands to explore artifacts through interactive 3D models and hear detailed audio explanations in their preferred language.
![image](https://github.com/user-attachments/assets/64e39fc0-eb1a-4073-84b0-0595988a6233)

Throughout this project, I gained hands-on experience in integrating RFID technology with a Raspberry Pi to provide personalized experiences based on user interactions with wristbands. I also learned to create a web interface and insert 3D models with iframes, which helped me improve my grasp of web development and third-party content integration.
