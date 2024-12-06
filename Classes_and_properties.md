# 4.2.3. Classes and Properties
Classes and properties from the first level modelling phase.

The theoretical framework provided the foundational knowledge necessary for identifying the key entities to be represented as classes and properties within the ontology. This understanding is vital as it shapes the scope and level of detail of the ontology. The ontology designer begins by defining the core classes that encapsulate the fundamental concepts of the domain, ensuring each class is clearly and relevantly defined. Following this, object properties are identified to represent the relationships between these classes, while data properties are used to capture specific attributes of the classes.

The designer ensures that each class and property is thoroughly defined and organized in a logical manner to support accurate representation and reasoning. This involves specifying clear definitions, formulating expressions and constraints for the properties, and establishing appropriate hierarchies and relationships between classes. Consistency is maintained throughout the ontology. The final result is a well-organized framework that facilitates effective knowledge sharing, integration, and interoperability within the domain.

## Classes
- <span style="background-color: #a9a9a9; color: #333333; padding: 2px 6px; border-radius: 4px; font-family: monospace;">EducationalSystem</span>  
A structured and organized framework within which formal education is delivered. It encompasses the institutions, policies, curricula, programs, and resources that collectively shape the educational experience and outcomes for learners. It is designed to facilitate the acquisition of knowledge, skills, and competencies in a structured and regulated environment, often guided by national or regional educational standards and goals. The educational system also involves the interaction of teachers, students, administrators, and other stakeholders, all working together to achieve educational objectives.  
    - <span style="background-color: #a9a9a9; color: #333333; padding: 2px 6px; border-radius: 4px; font-family: monospace;">PaidSystem</span>: an educational framework or program that requires learners to pay for access to its services, resources, or content.
    - <span style="background-color: #a9a9a9; color: #333333; padding: 2px 6px; border-radius: 4px; font-family: monospace;">FreeSystem</span>: an educational framework or program that does not require learners to pay for access to its services, resources, or content.
- <span style="background-color: #a9a9a9; color: #333333; padding: 2px 6px; border-radius: 4px; font-family: monospace;">People</span>
    - Learner: an individual engaged in the process of acquiring knowledge, skills, and competencies through formal or informal education. This can include students at various educational levels, from primary to higher education, who participate in structured learning activities within the system.
- <span style="background-color: #a9a9a9; color: #333333; padding: 2px 6px; border-radius: 4px; font-family: monospace;">Agent</span>
    - <span style="background-color: #a9a9a9; color: #333333; padding: 2px 6px; border-radius: 4px; font-family: monospace;">EducationalProviders</span>: organizations or entities that offer educational services, resources, and programs to learners
    - <span style="background-color: #a9a9a9; color: #333333; padding: 2px 6px; border-radius: 4px; font-family: monospace;">Sponsors</span>: individuals, organizations, or entities that provide financial or other forms of support to educational programs or systems
- <span style="background-color: #a9a9a9; color: #333333; padding: 2px 6px; border-radius: 4px; font-family: monospace;">Outcome</span>  
measurable results or achievements that learners attain as a result of their engagement in educational activities.
    - <span style="background-color: #a9a9a9; color: #333333; padding: 2px 6px; border-radius: 4px; font-family: monospace;">NetworingOpportunities</span>: represents the networking opportunities that the learner acquires during and as a result of the educational process.
    <span style="background-color: #a9a9a9; color: #333333; padding: 2px 6px; border-radius: 4px; font-family: monospace;">PersonalGrowth</span>: represents the development of a learner's emotional, social, and intellectual capabilities, resulting from the educational process.
    - <span style="background-color: #a9a9a9; color: #333333; padding: 2px 6px; border-radius: 4px; font-family: monospace;">ImpactOnCareer</span>: represents the influence that education has on an individual's professional trajectory, including career advancement, job opportunities, employability, and the ability to meet industry-specific demands.
    - <span style="background-color: #a9a9a9; color: #333333; padding: 2px 6px; border-radius: 4px; font-family: monospace;">SkillDevelopment</span>: represents the acquisition and enhancement of specific abilities or competencies, such as technical, cognitive, or interpersonal skills, that enable learners to perform tasks effectively and excel in their personal or professional lives.
- <span style="background-color: #a9a9a9; color: #333333; padding: 2px 6px; border-radius: 4px; font-family: monospace;">SocietalPerception</span>  
Reflects how society views the value, credibility, and effectiveness of different educational systems or approaches.
- <span style="background-color: #a9a9a9; color: #333333; padding: 2px 6px; border-radius: 4px; font-family: monospace;">Credibility</span>  
Represents the degree to which an educational system or resource is regarded as legitimate and capable of delivering quality learning outcomes
- <span style="background-color: #a9a9a9; color: #333333; padding: 2px 6px; border-radius: 4px; font-family: monospace;">Certification</span>  
Represents an official document or credential awarded to a learner upon successfully completing an educational program, demonstrating their
competence or knowledge in a specific area.
- <span style="background-color: #a9a9a9; color: #333333; padding: 2px 6px; border-radius: 4px; font-family: monospace;">Content</span>  
The materials, resources, and information provided within an educational system to facilitate learning, such as lessons, textbooks,
videos, or exercises.
- <span style="background-color: #a9a9a9; color: #333333; padding: 2px 6px; border-radius: 4px; font-family: monospace;">LearningObjective</span>  
A specific goal or intended outcome that an educational activity aims to achieve, describing what learners are expected to know
or be able to do by the end of the process.
- <span style="background-color: #a9a9a9; color: #333333; padding: 2px 6px; border-radius: 4px; font-family: monospace;">LearnerDemographics</span>  
The characteristics and attributes of a learner population, such as age, educational background, income level, and location,
which influence their educational needs and experiences.

## Properties
- **isUsedBy (EducationalSystem --> Learner)**: Links an educational system to a learner (indicating that the educational system is used by the learner).
- **hasSocietalPerception (EducationalSystem --> SocietalPerception)**: Links an educational system to societal perception it has.
- **choosesEducationalPath (Learner --> FreeSystem, PaidSystem)**: Links a learner to an educational path, indicating the system (free or paid) they have chosen to pursue their education.
- **hasDemographics (Learner --> LearnerDemographics)**: Associates a learner with their demographic information, such as age, location, income level, and educational background.
- **hasLearningObjective (Learner --> LearningObjective)**: Connects a learner to a specific learning objective, defining the goals they aim to achieve through the educational process.
- **deliversContent (FreeSystem, PaidSystem --> Content)**: Links an educational system (free or paid) to the content it provides to learners, such as course materials or resources.
- **hasOutcome (FreeSystem, PaidSystem --> Outcome)**: Connects an educational system to the outcomes it generates, such as skill development, personal growth, or career impact.
- **offeredBy (Certification --> FreeSystem, PaidSystem)**: Links a certification to the educational system (free or paid) that offers it as part of its programs or courses.
- **hasCredibility (PaidSystem --> Credibility)**: Associates a paid educational system with its credibility, indicating its perceived reliability and quality by stakeholders.
- **provides (EducationalProviders --> FreeSystem, PaidSystem)**: Connects educational providers to the systems (free or paid) they offer, indicating their role in delivering educational services.
- **funds (Sponsors --> FreeSystem)**: Links sponsors to a free educational system, indicating financial or other forms of support provided by the sponsors.

- <span style="color:green;">**hasQualityMetrics**</span> **(Content --> rdfs:Literal)**: A functional property that specifies the quality metrics associated with educational content. It has a domain of Content and a range of literal values.
- <span style="color:green;">**hasDeliveryMethod**</span> **(Content --> rdfs:Literal)**: A functional property that defines the method by which the educational content is delivered (e.g., online, in-person). It has a domain of Content and a range of literal values.
- <span style="color:green;">**hasContentFormat**</span> **(Content --> rdfs:Literal)**: A functional property that indicates the format of the educational content (e.g., video, text, PDF). It has a domain of Content and a range of literal values.
- <span style="color:green;">**hasContentLanguage**</span> **(Content --> rdfs:Literal)**: A functional property that specifies the language in which the educational content is presented. It has a domain of Content and a range of literal values.

- <span style="color:green;">**hasCost**</span> **(FreeSystem, PaidSystem --> rdfs:Literal)**

- <span style="color:green;">**belongsToAgeGroup**</span> **(LearnerDemographics --> rdfs:Literal)**: A functional property that specifies the age group to which a learner belongs. It has a domain of LearnerDemographics and a range of literal values.
- <span style="color:green;">**locatedIn**</span> **(LearnerDemographics --> rdfs:Literal)**: A functional property that indicates the geographical location of a learner. It has a domain of LearnerDemographics and a range of literal values.
- <span style="color:green;">**hasEducationalBackground**</span> **(LearnerDemographics --> rdfs:Literal)**: A functional property that describes the prior educational background of a learner. It has a domain of LearnerDemographics and a range of literal values.
- <span style="color:green;">**hasIncomeLevel**</span> **(LearnerDemographics --> rdfs:Literal)**: A functional property that denotes the income level of a learner. It has a domain of LearnerDemographics and a range of literal values.

- <span style="color:green;">**hasAccessibility**</span> **(EducationalSystem --> rdfs:Literal)**: A functional property that describes the level of accessibility of an educational system, such as its availability or ease of access for learners. It has a domain of EducationalSystem and a range of literal values