### New Classes and Properties for Educational Perspectives  

Classes and properties derived from the second-level modeling process.  

In the second-level modeling of our ontology, the elemental framework was refined by aligning it with the **PERSPECTIVISATION ontology** developed by Aldo Gangemi. Special attention was given to classes such as **Background**, **Cut**, **Lens**, **Eventuality**, and **Attitude** to incorporate a nuanced understanding of how perspectives within the field of education evolve and interact. This phase systematically introduced new classes and properties, enabling a richer representation of educational viewpoints, societal influences, and institutional dynamics.  

By employing punning for viewpoints and attitudes, we ensure dual interpretations that enable elements to function both as abstract classes and specific instances. This enhances the versatility of the ontology, supporting both theoretical analysis and practical application. For example, viewpoints and attitudes can serve as abstract classes for general reasoning or as individuals for analyzing real-world cases. This dual treatment makes the ontology effective for abstract conceptualization and instance-based application.  

---

### Classes  

**ExternalViewpoint**  
Represents the perspective of individuals or institutions outside the educational system, such as parents, policymakers, or media entities.  

- Disjoint with InternalViewpoint.  

**InternalViewpoint**  
Represents the self-perception and experiences of individuals within the educational system, such as students, teachers, and administrators. This class includes how these individuals perceive their roles, relationships, and goals within the system.  

**Influence**  
Covers the various factors that shape perspectives and attitudes toward education. This includes influences such as:  
- **Institutional factors**: Policies, funding, or curriculum changes.  
- **Cultural factors**: Societal values, norms, and expectations regarding education.  
- **Media portrayal**: Representations of education in news, movies, and social media.  
- **Personal experiences**: Individual interactions with the educational system.  

**PerspectiveShift**  
Captures changes in perceptions about education over time. For instance, shifts in societal attitudes toward online education, inclusion of marginalized groups, or the importance of interdisciplinary learning.  

**Stereotype**  
Represents common generalizations or misconceptions about education, educators, or students. For instance:  
- “STEM fields are for men.”  
- “Art degrees have no real-world value.”  
These stereotypes often shape public attitudes and can influence educational policies and practices.  

**PositiveAttitude / NegativeAttitude / NeutralAttitude**  
Classes representing evaluative stances toward education or specific aspects of it.  
- **NegativeAttitude**: Often linked to stereotypes or dissatisfaction (e.g., “School is outdated and rigid”).  
- **NeutralAttitude**: A balanced mix of positive and negative views.  
- **PositiveAttitude**: Often tied to recognition of moral or societal value (e.g., “Education is the key to equality”).  

---

### Properties  

**hasViewpoint (People -> InternalViewpoint/ExternalViewpoint)**  
Links a person to their perspective on education.  
- **isViewpointOf**: Inverse property linking a viewpoint to a person.  

**hasAttitude (People -> NegativeAttitude/NeutralAttitude/PositiveAttitude)**  
Connects individuals to their evaluative stance on education.  
- **isAttitudeOf**: Inverse property linking attitudes back to people.  

**influencedBy (NegativeAttitude/NeutralAttitude/PositiveAttitude -> Influence)**  
Indicates the factors influencing a particular attitude. For instance:  
- A **PositiveAttitude** toward remote learning may be influenced by **CulturalFactors** promoting flexibility.  

**triggersStereotype (EducationSystem -> Stereotype)**  
Relates stereotypes to the educational system they generalize.  

**isCharacterisedBy (ExternalViewpoint/InternalViewpoint -> PerspectiveShift)**  
Links viewpoints to shifts in perspective, capturing changes such as:  
- Students shifting from a negative to positive outlook on education after experiencing inclusive teaching practices.  

**expressedVia (PositiveAttitude/NegativeAttitude/NeutralAttitude -> Stereotype/MoralValue)**  
Denotes that attitudes toward education are shaped by stereotypes or moral values.  

**determines (ExternalViewpoint/InternalViewpoint -> NegativeAttitude/NeutralAttitude/PositiveAttitude)**  
Captures how external or internal viewpoints influence attitudes toward education.  

**hasPerceptionOf (NotParticipant -> EducationSystem)**  
Links individuals not directly involved in the education system (e.g., policymakers) to their perception of it.  

**hasInfluencingFactors (EducationSystem -> Influence)**  
Connects the education system to the factors shaping its perception.  

**hasPerspectiveShift (EducationSystem -> PerspectiveShift)**  
Links the educational system to shifts in societal or individual perceptions about it.  

---

### Application in the Project Context  

These classes and properties are tailored to explore and analyze educational perspectives, fostering insights into how attitudes toward education evolve due to societal, cultural, and institutional influences. By integrating nuanced representations of viewpoints, attitudes, and stereotypes, the ontology allows for a deeper understanding of the dynamics at play within the educational system.  

This approach not only facilitates theoretical research but also supports practical applications, such as identifying factors influencing public perceptions, improving inclusivity, or addressing stereotypes in education.  
