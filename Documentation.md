# Documentation of SOHO

Chosen Methodology: Top-Down-Modelling using the SOHO, OCRA and DUL ontologies.

## 0. General Definitions
- Definition of "SocialRobot" as AutonomousAgent
- Definition of "NaturalRobot" as PhysicalAgent
- "SocialSkill" as subclass of "SocialCapability", which is a subclass of soho:AgentCapability. Each SocialSkill has only Functions as tasks
- "SocialMethod" and "SocialTask" as a subclass of Method with ProductionTask subclasses as subclasses of SocialTask
- "SocialAction" with "RobotAction", "JointAction" and "HumanAction" as subclasses
- "SocialPlan" with "Plan" as a superclass and "ProductionPlan" as a subclass

## 1. Introducing taxonomy: Regions
Based on an already established taxonomy on social robotics, the first major step in creating Sobots was the introduction of the taxonomic structures into the given parent domain of SOHO and OCRA, domain ontologies for human-robot collaboration. DUL differentiates in SocialObjects and Region, with the latter being some dimensional space serving as value ranges, e.g. for parameters.

Not all categories in the given taxonomy where regions, however, some could be reformulated as such, when there was an evident intention that they should serve as values not objects or qualities.

### User Context
- Age of the target group => AgeRegion and AgeInYears
- Expertise or target group => Exists within SOHO as ExpertiseLevelScale
- Physical Closeness => PhysicalCloseness region
- Ratio between number of robots and number of persons: ReatioRegion and HumanToRobotRatio

### Interaction Time
All three provided taxonomy categories were time-related dimensional spaces and thus introduced as such.

### Robot
- Human Likeliness => This is a dimensional space but it was mixed with other concepts in the taxonomy such as zoomorphism. It was solved by introducing two new regions (PurelyTechnical <-> Humanoid <-> Android) and (PurelyTechnical <-> Zoomorph). Both regions have PurelyTechnical as their intended origin value.
- Robot Type: While it is exclusive, this category is no dimensional space but a quality => not included as Region
- Interaction Type: Similar to Robot Type

### Interactivity
No regions discovered!

### Intelligence
- Autonomy: Already defined As AutonomyLevel in SOHO
- Adaptability: Defined analogously to Autonomy as Region

## 2. Introducing taxonomy: Context of Use
In Sobots, we define the Context of Use as a DUL:Situation under the class "SocialContext".
Inheriting members are:
- ApplicationArea
- InteractionPartner
- TargetGroup
- TaskContext
These classes were defined accordingly to the provided taxonomy

(!) Comments of the modeller: "Interaction partners are a state in context, but I don't understand how "environment" (de: Umwelt) fits here... Animals are also part of the environment! We exclude the environment for the time being, as it is a different concept, and already included elsewhere in SOHO..."

## 2. Introducing taxonomy: Qualities

Qualities serve as properties of an entity, that is, they cannot exist without an entity, but are not part of said entity. All dimensional spaces of the taxonomy are defined at this point, meaning this part focuses purely on the identification of qualities based on the remaining catgories.

- Appearance: The regions for human likeliness and zoomorphism where already defined, thus, the only quality of AgentAppearance as subclass of soho:AgentEmbodimentProperty was added.
- Type of robot: A subclass of a sobot:RobotProperty
- Mobility: A subclass of soho:AgentCapability. Categories fit the taxonomy
- Communication: Based on the types of communications (non-verbal, para-verbal etc.) communication capabilities were defined
- AgentAdaptability and AgentAutonomy were defined as subclasses of soho:AgentCapability

## 3. Introducing taxonomy: Communication

The taxonomy became very specific on the communication part. Most prominently, it splits communication into several four classes: non-verbal, verbal, paraverbal and extraverbal. Corresponding communication capabilities were already defined, however, the categories for each class within the taxonomy still remain. Since they are quite specific and describe clear functions of communication, the decision was made to attach this taxonomic tree to soho:Send and soho:Receive, both subclasses of soho:Communication, which is a subclass of soho:Function.

Additionally, the disjoint classes of SendCommunicationCapability and ReceiveCommunicationCapability were introduced.



