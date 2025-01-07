### Perspectivisation Competency Questions  
#### Competency Questions and SPARQL Queries on Second-Level Modelling  

Based on user scenarios created in collaboration with LLMs, we derived the following competency questions to address the perspectives and influences surrounding educational systems. These questions guided the formulation of SPARQL queries, ensuring the ontology effectively meets the informational needs identified during scenario analysis.  

---

#### Prefixes  
To use the SPARQL queries below, the following prefixes must be included:  

```sparql
PREFIX edu: <http://www.semanticweb.org/ontologies/2024/EDU/>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
```  

---

### Competency Questions and Corresponding Queries  

1. **Which individuals have an external viewpoint regarding educational systems?**  
   **SPARQL Query:**  
   ```sparql
   SELECT ?person ?viewpoint
   WHERE {
     ?person rdf:type edu:Learner .
     ?person edu:hasViewpoint edu:ExternalViewpoint .
   }
   ```

2. **Which individuals have a negative attitude towards paid education systems?**  
   **SPARQL Query:**  
   ```sparql
   SELECT ?person 
   WHERE {
       ?person rdf:type edu:Learner .
       ?person edu:hasAttitude edu:NegativeAttitude .
       ?paidSystem rdf:type edu:PaidEducationSystem .
       ?person edu:choosesEducationalPath ?paidSystem .
   }
   ```

3. **What factors influence negative attitudes in educational systems?**  
   **SPARQL Query:**  
   ```sparql
   SELECT ?system ?influence ?content
   WHERE {
     ?system rdf:type edu:EducationalSystem .
     ?system edu:hasInfluencingFactors ?influence .
     ?influence edu:influences edu:NegativeAttitude .
     ?influence edu:hasContent ?content .
   }
   ```

4. **What factors contribute to positive attitudes in educational systems?**  
   **SPARQL Query:**  
   ```sparql
   SELECT ?system ?influence ?content
   WHERE {
     ?system rdf:type edu:EducationalSystem .
     ?system edu:hasInfluencingFactors ?influence .
     ?influence edu:influences edu:PositiveAttitude .
     ?influence edu:hasContent ?content .
   }
   ```

5. **What are the perspective shifts that occur in educational systems?**  
   **SPARQL Query:**  
   ```sparql
   SELECT ?system ?perspectiveShift ?content
   WHERE {
     ?system rdf:type edu:EducationalSystem .
     ?system edu:hasPerspectiveShift ?perspectiveShift .
     ?perspectiveShift edu:hasContent ?content .
   }
   ```

6. **What stereotypes are associated with paid educational systems?**  
   **SPARQL Query:**  
   ```sparql
   SELECT ?paidSystem ?stereotype ?content
   WHERE {
     ?paidSystem rdf:type edu:PaidEducationSystem .
     ?paidSystem edu:triggersStereotype ?stereotype .
     ?stereotype rdf:type edu:Stereotype .
     ?stereotype edu:hasContent ?content .
   }
   ```

7. **What are the attitudes held by participants in free education systems?**  
   **SPARQL Query:**  
   ```sparql
   SELECT ?freeSystem ?participant ?attitude
   WHERE {
     ?freeSystem rdf:type edu:FreeEducationSystem .
     ?participant rdf:type edu:Learner .
     ?participant edu:choosesEducationalPath ?freeSystem .
     ?participant edu:hasAttitude ?attitude .
   }
   ```

---

#### Data Property Visualization  

To visualize the content of entities such as `Influence`, `PerspectiveShift`, or `Stereotype`, include the `edu:hasContent` data property in the query.  

Example:  
```sparql
SELECT ?system ?perspectiveShift ?content
WHERE {
  ?system rdf:type edu:EducationalSystem .
  ?system edu:hasPerspectiveShift ?perspectiveShift .
  ?perspectiveShift edu:hasContent ?content .
}
```

---

These modified competency questions and SPARQL queries now align with the ontology structure and instance data, enabling researchers to analyze perspectives, attitudes, influences, and stereotypes associated with both free and paid education systems. Each query has been tested to ensure it returns meaningful results from the provided dataset.