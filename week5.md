

## **week 5: build an interactive copyright status assessment tool**

This week’s task was focused on creating an interactive online copyright assessment tool, aimed at helping users evaluate the copyright status of works within the context of two established frameworks: the QM’s EMu Copyright Documentation Guidelines and the GLAM-E Lab’s Copyright Clearance Handbook for Public Domain Publications of Digital Collections. The overall goal was to combine these two frameworks into a streamlined, user-friendly tool that will make copyright evaluations accessible for a wide range of users.

### Steps to Create the Tool:

#### 1. Understanding the Frameworks: 
The first step involved reading the two copyright assessment frameworks: QM’s EMu Copyright Documentation Guidelines and the GLAM-E Lab’s Copyright Clearance Handbook. I reviewed both documents carefully, identifying key questions, decision points, and guidelines in each framework.

#### 2. Creating Flowcharts with Mermaid: 
To visually represent the decision-making process involved in each framework, I created two detailed flowcharts using Mermaid language. These flowcharts would serve as a visual representation of the frameworks, helping users navigate through the copyright assessment process.

The first flowchart was based on QM’s EMu Copyright Documentation Guidelines, which focuses on assessing various aspects of a work's copyright status, including permissions, usage rights, and documentation.

```mermaid
flowchart TD
    A[Start: Emu Copyright Clearance] --> B{Is the artist alive?}
    B -->|Yes| C((work is under copyright protection))
    B -->|No| D{Did the artist die before 1975?}
    D -->|Yes| E((Work is in public domain))
    D -->|No| F((work remains under copyright protection))
  ```  


The second flowchart stemmed from the GLAM-E Lab’s Copyright Clearance Handbook, which emphasizes evaluating public domain works, clearing permissions, and understanding specific copyright conditions tied to digital collections.

glam-e lab flow chart.md


```mermaid
flowchart TD
    A[Start: GLAM-E Lab's Copyright Clearance] --> B{Is the underlying work eligible for copyright protection in your jurisdiction?}
    A --> 1{Is the underlying work eligible for copyright protection?}

    subgraph US 
    1 -->|Yes| 2{Was the underlying work published}
    1 --> |No| 3((the work is in the public domain. Proceed to Checklist 2))
    2 --> |No| 4[ remove the work for further review]
    2 --> |Yes| 5{date of publication}
    5 -->|on or before December 31, 1930| 6((work is in the public domain. Proceed to Checklist 2.))
    5 --> |after January 1, 1978| 7[work is in-copyright and remove the work for further review.]
    5 --> |between January 1, 1928,and January 1, 1978| 8{Is the underlying work a domestic or foreign work?}
    8 --> |Domestic Published in the US or within 30 days| 9{Does the work meet notice requirements?}
    8 --> |Foreign First published outside the US| 10[Refer to the copyright laws of the country of origin. Seek further advice if unsure]
    9 --> |Yes| 11{Does the work meet registration and renewal requirements?}
    9 --> |No| 12((the work is in the public domain. Proceed to Checklist 2.))
    11 -->|No| 14((the work is in the public domain. Proceed to Checklist 2.))
    11 -->|Yes| 15[the work is under copyright. Remove the work for further review.]
    end

    subgraph UK and EU Member States 
    B --Yes--> C{Do you know who created the underlying work?}
    B -- No -->D((The Work is in public domain. Proceed to checklist 2))
    C -->|No| E[Remove the work for further review]
    C --> |Yes| F{Is the work published?}
    F --> |No| G[Review Country Rules]
    F --> |Yes| H[Check Creator's death date]
    H --> I{Has the copyright expired?}
    I --> |Yes| J((The work is in public doman. Proceed to checklist 2))
    I -->|No| K[Remove work from open access program]
    I --> |Unsure| L(Is the work a foreign work?)
    L --> |Yes| M{Does the rule of shorter term apply?}
    M --> |Yes| N[Apply the shorter term for copyright expiration] 
    M --> |No| O[Apply the country’s original copyright term]
    O --> P{Has the copyright expired?}
    N --> P
    P --> |Yes| Q((The work is in the public domain. Proceed to Checklist 2.))
    P --> |No| R[Remove the work from the open access program.]
    end

    subgraph Checklist 2
    3 --> A2
    6 --> A2
    12 --> A2
    14 --> A2
    J --> A2
    D --> A2
    Q --> A2
    A2[Start: Checklist 2, The Digital Surrogate] --> B2{Is the digital surrogate a faithful reproduction of the underlying work?}
    B2 -->|Yes| C2((Public Domain - Proceed to Checklist 3))
    B2 -->|unsure| D2{Did digitization incorporate sufficiently create choices of the person who made it?}
    
    D2 -->|Yes| E2{Who made the digital surrogate?}
    D2 -->|No| F2((Public Domain - Proceed to Checklist 3))
    
    E2 -->|Organization made surrogate| G2((Organization owns copyright - Can release CC0 - Proceed to Checklist 3))
    E2 -->|Contractor made surrogate| H2[Review contract to determine rights]

    H2 -->|Rights assigned to organization| I2((Organization owns copyright - Can release CC0 - Proceed to Checklist 3))
    H2 -->|Rights retained by contractor| J2[Seek professional advice or remove work for further review]
    end

    
    subgraph Checklist 3
    C2 --> A3
    F2 --> A3
    G2 --> A3
    I2 --> A3
    A3[Start: Checklist 3, The Metadata] --> B3{What type of metadata is there?}
    B3 -->|Basic metadata| C3[not protected by copyright law, public domain - marked CC0]
    B3 -->|Expressive metadata| D3{Who created the more expressive metadata?}
    D3 -->|Organization created metadata| E3[Organization owns copyright - Marked CC0]
    D3 -->|Contractor created metadata| F3[Remove excessive metadata - publish the record with basic metadata - Marked CC0]
    end

```


#### 3. Building the Interactive Tool: 
The next step was to build an interactive assessment tool. Using pull-down menus, I designed the tool so users can input information about a work. These inputs will guide the user through the decision tree and determine whether a work is copyrighted, in the public domain, or if certain conditions apply.




What I Learned After Finishing the Task:

Mermaid for Visual Flowcharts: I gained practical experience in using Mermaid for creating flowcharts. The syntax is straightforward, and it’s an effective tool for visualizing decision-making processes. It helped me break down the complex copyright guidelines into manageable and easily digestible parts.

Interactive Design Principles: Designing an interactive tool brought me face-to-face with key considerations for user interface and user experience (UI/UX). I had to think critically about how to make the tool intuitive, engaging, and easy to use. Simple elements like pull-down menus and checkboxes made the process seamless for users, yet I also had to ensure that the tool maintained accuracy and clarity when presenting complex copyright rules.

Copyright Evaluation in Practice: Diving into the practical application of copyright evaluation frameworks helped deepen my understanding of copyright law, especially in the context of digital collections and public domain works. By translating abstract guidelines into an interactive format, I gained a more solid grasp of the challenges and nuances involved in assessing the copyright status of various works.

Combining Frameworks: One of the most insightful aspects of the task was combining two distinct frameworks into a single tool. It was fascinating to compare the nuances of both frameworks and see how they intersected or differed in terms of copyright evaluation. The side-by-side results feature was particularly valuable in understanding how the same work might be treated differently depending on the assessment method.

Conclusion: This week’s task allowed me to merge technical skills (like building an interactive tool) with legal concepts (like copyright law). The end result is not just a functional tool but also a deeper understanding of the complexities of copyright evaluation. I look forward to continuing the development and refining the tool further, but for now, it feels satisfying to have created something that can help others navigate the complex world of copyright with ease.
