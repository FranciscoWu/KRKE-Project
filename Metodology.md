### **Methodology**

The methodology for this project combines the **Extreme Design (XD)** approach. This integrated approach provides an iterative and structured framework for the design of an ontology that models the interplay between paid, unpaid, and hybrid education systems. Additionally, **Large Language Models (LLMs)** and **Ontology Design Patterns (ODPs)** are incorporated to enhance concept generation and structural alignment.

------

### **1. Context and State-of-the-Art Literature**

This phase corresponds to **XD Task 1** and focuses on establishing a theoretical foundation for the ontology. The team reviewed literature in education theory, digital pedagogy, and sociology to understand the dynamics of modern educational systems. Key theories such as the **Zone of Proximal Development** and **Cognitive Load Theory** were used to inform the ontology's structure.

------

### **2. Large Language Models (LLMs)**

LLMs, such as ChatGPT, were employed to assist in the early stages of ontology design. Their role included:

- **Defining Core Concepts**: Generating definitions for terms like “informal learning” and “learner pathways.”
- **Scenario Creation**: Producing examples of educational decision-making, such as choosing between MOOCs and universities.
- Competency Questions: Extracting and formalizing questions to guide ontology development, such as:
  - “What factors influence learners to choose informal education?”
  - “How do cost and credibility vary across educational platforms?”

The LLM-generated competency questions were later translated into SPARQL queries for ontology validation.

------

### **3. Defining Classes and Class Hierarchy**

Based on the framework, key classes and hierarchies were defined:

- Core Classes
  - `FormalEducation`, `InformalLearning`, `NonFormalEducation`, `LearnerPathways`.
- Attributes
  - `Cost`, `Credibility`, `Flexibility`, and `Depth`.

These classes were iteratively refined to ensure alignment with the theoretical foundation and evolving competency questions.

------

### **4. Defining Properties and Relationships**

Properties were defined to capture the relationships between classes, ensuring the logical structure of the ontology. Examples include:

- Object Properties
  - `hasCost` (links `EducationSystem` to `Cost`).
  - `influencesCredibility` (links `LearningPlatform` to `Credibility`).
- Domain and Range
  - `hasCost`: Domain = `EducationSystem`, Range = `xsd:integer`.

Constraints such as cardinality and dependency relationships were also implemented, ensuring coherence and precision.

------

### **5. Modules Integration and Alignment**

Newly developed modules were integrated with the overall ontology structure using **Protégé**:

- Reuse of Existing Patterns
  - Ontology Design Patterns (ODPs) for `Credentialing` and `Cost Analysis` were adapted to solve design challenges.
- Alignment
  - Ensured semantic consistency across formal, informal, and hybrid education modules.

------

### **6. Creating and Refining Instances**

To make the ontology relevant to practical applications, instances of the defined classes are generated to represent real-world scenarios. This step bridges the gap between theoretical design and practical usage.

Afterward, the competency questions were converted into SPARQL queries and evaluated against the finalized ontology design using Protégé for validation.