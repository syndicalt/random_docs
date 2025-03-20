### Understanding Boolean Logic Basics
Boolean logic is a system of representing statements or conditions as either **True** or **False**, often used in programming, mathematics, and decision-making. The two primary operators we'll focus on are:
- **AND**: All conditions must be True for the result to be True.
- **OR**: At least one condition must be True for the result to be True.

Additionally, we can use parentheses to group conditions, creating complex expressions with multiple layers of logic.

---

### Step-by-Step Guide to Translating Statements

#### 1. Identify the Key Conditions
Break the statement into its individual parts (conditions) that can be evaluated as True or False. These are typically nouns, verbs, or phrases that describe a state or requirement.

- Example: "I will go to the park if it is sunny and I have free time."
  - Condition 1: "It is sunny" → Let’s call this **S**.
  - Condition 2: "I have free time" → Let’s call this **F**.

#### 2. Determine the Logical Relationships
Look for words that indicate how the conditions connect:
- **AND**: Words like "and," "both," "as well as," or "plus" mean all conditions must be True.
- **OR**: Words like "or," "either," "one of," or "alternatively" mean at least one condition must be True.

- From the example: "sunny **and** I have free time" → Use **AND**.

#### 3. Assign Variables
Give each condition a simple variable (e.g., A, B, S, F) to make the logic easier to write and read.

- "It is sunny" = **S**
- "I have free time" = **F**

#### 4. Write the Boolean Expression
Combine the variables with the appropriate operators (AND, OR) based on the relationships:
- Example: **S AND F**
  - This means both "It is sunny" AND "I have free time" must be True for "I will go to the park" to be True.

#### 5. Handle Multiple Groups (Complex Statements)
For statements with multiple parts or conditions grouped together, use parentheses to clarify the order of operations. Boolean logic follows a precedence similar to arithmetic: AND is evaluated before OR, unless parentheses specify otherwise.

- Example: "I will go to the park if it is sunny and I have free time, or if my friends are going."
  - Condition 1: "It is sunny" = **S**
  - Condition 2: "I have free time" = **F**
  - Condition 3: "My friends are going" = **G**
  - Relationship: "sunny AND free time" is one group, connected by OR to "friends are going."
  - Boolean Expression: **(S AND F) OR G**
    - This means either "sunny AND free time" OR "friends are going" must be True.

#### 6. Test the Expression
Evaluate the expression with different True/False combinations to ensure it matches the original statement’s intent:
- **S = True, F = True, G = False**: (True AND True) OR False = True → Go to the park.
- **S = False, F = True, G = False**: (False AND True) OR False = False → Don’t go.
- **S = False, F = False, G = True**: (False AND False) OR True = True → Go to the park.

---

### Examples of Translation

#### Simple Statements
1. **Statement**: "The system works if the power is on and the battery is charged."
   - Conditions: "Power is on" = **P**, "Battery is charged" = **B**
   - Relationship: AND
   - Expression: **P AND B**

2. **Statement**: "I’ll eat dinner if I’m hungry or if it’s 6 PM."
   - Conditions: "I’m hungry" = **H**, "It’s 6 PM" = **T**
   - Relationship: OR
   - Expression: **H OR T**

#### Complex Statements with Groups
3. **Statement**: "I’ll travel if I have money and a passport, or if my boss approves and I get a free ticket."
   - Conditions:
     - "I have money" = **M**
     - "I have a passport" = **P**
     - "My boss approves" = **B**
     - "I get a free ticket" = **T**
   - Relationships:
     - "money AND passport" = one group
     - "boss approves AND free ticket" = another group
     - These two groups are connected by OR
   - Expression: **(M AND P) OR (B AND T)**

4. **Statement**: "The alarm triggers if the door is open and the system is armed, but not if it’s daytime."
   - Conditions:
     - "Door is open" = **D**
     - "System is armed" = **S**
     - "It’s daytime" = **T**
   - Relationships:
     - "door is open AND system is armed" = one group
     - "not if it’s daytime" = negate the daytime condition (using NOT)
     - Combine with AND
   - Expression: **(D AND S) AND (NOT T)**

---

### Tips for Complex Logic
- **Parentheses Matter**: Use them to group conditions clearly. Without parentheses, AND takes precedence over OR.
  - Example: **A AND B OR C** = **(A AND B) OR C**, not **A AND (B OR C)**.
- **Negation (NOT)**: Words like "not," "isn’t," or "unless" indicate a NOT operator.
  - Example: "I’ll go unless it rains" → "I’ll go if NOT raining" → **NOT R**.
- **Implied Conditions**: Sometimes conditions are implicit. "If it’s sunny" might imply "and it’s not raining" depending on context—clarify with the user if needed.
- **Break It Down**: For very long statements, split them into smaller parts, translate each, then combine.

---

### Practice Problems
Try translating these into Boolean expressions:
1. "I’ll buy a car if it’s red or blue and it’s under $20,000."
2. "The game starts if all players are ready and the referee is present, or if it’s past 3 PM."
3. "I’ll attend the event if I’m invited and it’s not raining, or if my friend insists."

#### Answers:
1. **(R OR B) AND U**
   - R = "It’s red," B = "It’s blue," U = "It’s under $20,000"
2. **(P AND R) OR T**
   - P = "All players are ready," R = "Referee is present," T = "It’s past 3 PM"
3. **(I AND (NOT R)) OR F**
   - I = "I’m invited," R = "It’s raining," F = "My friend insists"
