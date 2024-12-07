# 4.2.2. Competency Questions

For the chosen scenario, "Supplementary Support" we formulated the following Competency Questions, which subsequently informed the creation of SPARQL queries to meet the specific informational requirements outlined in the scenario analysis.

The following prefixes shoudl be included in each query:  
`PREFIX eduont: <http://www.semanticweb.org/ontologies/EduOnt/>`  
`PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>`   
`PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>`  
`PREFIX owl: <http://www.w3.org/2002/07/owl#>`  
`PREFIX db: <http://dbpedia.org/ontology/>`  
`PREFIX frame: <http://etna.istc.cnr.it/framester2/data/framestercore/>`

## What is known about the demographic information of Sophie?
```
SELECT ?incomeLevel ?educationalBackground ?location ?ageGroup  
WHERE {  
  eduont:Sophie eduont:hasDemographics ?demographics .  
  ?demographics eduont:hasIncomeLevel ?incomeLevel ;  
                eduont:hasEducationalBackground ?educationalBackground ;  
                eduont:locatedIn ?location ;  
                eduont:belongsToAgeGroup ?ageGroup .  
}
```

## What kind of educational system is Sophie enrolled in?
```
SELECT ?paidSystem  
WHERE {  
  eduont:Sophie a eduont:Learner;  
  eduont:Sophie eduont:choosesEducationalPath ?paidSystem .  
}
```

## How much does the education Sophie is receiving cost?
```
SELECT ?cost  
WHERE {  
    eduont:Sophie eduont:choosesEducationalPath ?paidSystem;  
    ?paidSystem eduont:hasCost ?cost.  
    ?paidSystem rdf:type eduont:PaidSystem.  
}
```

## What specific learning objective does Sophie aim to achieve with supplementary support?
```
SELECT ?learningObjective  
WHERE {  
    eduont:Sophie eduont:choosesEducationalPath ?freeSystem.  
    ?paidSystem rdf:type eduont:FreeSystem.  
    eduont:Sophie eduont:hasLearningObjective ?learningObjective.  
}
```

## What content does Sophie access from the free educational system?
```
SELECT ?content ?contentFormat  
WHERE {  
  eduont:Sophie eduont:choosesEducationalPath ?feeSystem .  
  ?freeSystem eduont:deliversContent ?content .  
  ?content eduont:hasContentFormat ?contentFormat .  
}
```

## What learning outcomes does Sophie expect from the supplementary support she recieves?
```
SELECT ?aspect  
WHERE {  
  eduont:Sophie eduont:choosesEducationalPath ?freeSystem .  
  ?freeSystem eduont:hasOutcome ?outcome .  
  ?outcome eduont:hasAspect ?aspect .  
}
```

## Who are the sponsors of free educational system used by Sophie?
```
SELECT ?sponsor  
WHERE {  
  eduont:Sophie eduont:choosesEducationalPath ?freeSystem .  
  ?sponsor eduont:funds ?freeSystem .  
  ?sponsor rdf:type eduont:Sponsors .  
}
```
