# AI-Scribble-Calculator
An AI-powered calculator that transforms scribbles into solutions 

![](https://github.com/Amjt11/AI-Scribble-Calculator/blob/main/images/ipados_18_calc_1718086821202.jpg)
**Apple's  Math  Notes**

## Problem Statement
Traditional calculators are limited to basic numerical operations, lacking context-aware calculations, natural language processing (NLP) for conversational inputs, and integration with dynamic data sources for real-time, contextual operations.

## Solution Approach
**Our AI Calculator** transforms digital interaction by allowing users to solve mathematical equations written as **scribbles** or drawings directly on a screen. 

Inspired  by  **Apple's  Math  Notes**  for  iPad,  this  system  combines advanced  AI  capabilities  with  a  user-centric  interface  to  provide  a  versatile platform  accessible  on  Android  and  PC.  The  proposed  system  focuses on overcoming  the  limitations  of  existing  mathematical  tools  by  integrating **handwriting recognition**, **real-time interaction**, and **cross-platform accessibility**.

![](https://github.com/Amjt11/AI-Scribble-Calculator/blob/main/images/9.png)

---

### Key Features: 

- **Scribble Input:** Supports handwritten equations or calculations using an input pen.  
- **Instant Solutions:** Instantly solves inputs in any format—equations, images, or drawings.  

### Unique Points: 
- Removes the need for keyboards or structured input.  
- Combines handwriting recognition with real-time calculations for seamless use.

---

## Workflow

![](https://github.com/Amjt11/AI-Scribble-Calculator/blob/main/images/Workflow.png)

**Frontend Interaction (React Application):**

- User draws on a canvas
- Clicks "**Calculate**" button
- The canvas is converted to a base64-encoded image
- The image and any predefined variables are sent to the backend via an axios POST request
- Backend Route Handling (**Fast API**):
- Receives the POST request with image data
- Decodes the base64 image string
- Converts the decoded data to a **PIL** (Python Imaging Library) Image object
- Calls the analyze image function with two parameters: a. The image object b. A dictionary of user-defined variables


**Image Analysis (Gemini AI)**

- Uses Google's Gemini 1.5 Flash model
- Receives a detailed prompt explaining how to interpret different types of mathematical problems:
- Simple mathematical expressions
- Systems of equations
- Variable assignments
- Graphical math problems
- Abstract concept detection
- Analyzes the image and attempts to solve the mathematical content
- Returns a list of dictionaries with results
- Response Processing:
- Parses the Gemini AI's response using ast.literal_eval()
- Adds an 'assign' flag to each response
- Returns the processed responses to the frontend

### AI Engine (Gemini API)
The  **Gemini  API**  is  the  core  component  responsible  for  solving  complex 
equations  and  performing  sophisticated  mathematical  tasks.  It  can  handle  a 
wide  range  of  calculations,  from  basic  algebraic  equations  to  advanced 
differential equations and symbolic calculations.

**Key Features** 

●  **Equation  Solving** :  Gemini  can  solve  algebraic,  trigonometric, and 
calculus-based equations and systems of equations. 
●  **Graphical  Rendering** :  It  can  also  generate  graphs  for  mathematical 
functions, which are returned to the front end for visual representation. 
●  **LaTeX  Rendering** :  Gemini  supports  the  rendering  of  equations  in  LaTeX 
format,  ensuring  that  complex  mathematical  expressions  are  displayed 
properly in the app. 

The  backend  layer  interacts  with  Gemini  through  an  API  request-response 
cycle,  where  the  user’s  input  equation  is  passed  to  Gemini,  and  the  result  is 
returned  to  the  user  in  an  easily  interpretable  format  (e.g.,  numerical  answers, 
LaTeX expressions, graphs). 

---


## Testing

### Functionality Testing Case 1:  Equation  Solving
**Test case 1**

- Input

![](https://github.com/Amjt11/AI-Scribble-Calculator/blob/main/images/1.png)

- Output

![](https://github.com/Amjt11/AI-Scribble-Calculator/blob/main/images/2.png)


**Test Case 2**

- Input

![](https://github.com/Amjt11/AI-Scribble-Calculator/blob/main/images/3.png)

- Output

![](https://github.com/Amjt11/AI-Scribble-Calculator/blob/main/images/4.png)


### Functionality Testing Case 2:  Diagram Problem  Solving

**Test Case 1**

- Input

![](https://github.com/Amjt11/AI-Scribble-Calculator/blob/main/images/5.png)

- Output

![](https://github.com/Amjt11/AI-Scribble-Calculator/blob/main/images/6.png)

**Test Case 2**

- Input

![](https://github.com/Amjt11/AI-Scribble-Calculator/blob/main/images/7.png)

- Output

![](https://github.com/Amjt11/AI-Scribble-Calculator/blob/main/images/8.png)


 ### Functionality Testing Case 3: Discovering  concepts  from  abstract  drawings
 
**Test Case 1**

- Input

![](https://github.com/Amjt11/AI-Scribble-Calculator/blob/main/images/10.png)


- Output

![](https://github.com/Amjt11/AI-Scribble-Calculator/blob/main/images/11.png)


**Test Case 2**

- Input and Output

![](https://github.com/Amjt11/AI-Scribble-Calculator/blob/main/images/12.png)

---

## Conclusion
The  AI-Powered  Calculator  App  successfully  meets  the  objectives outlined  for  the  project.  It  delivers  accurate,  real-time  calculations,  graphical visualizations,  and  LaTeX-rendered  expressions,  all  within  an intuitive  user interface.  The  integration  of  ReactJS,  FastAPI,  and  the  Gemini  API  ensures that  the  app  is  both  fast  and  scalable.  The  performance  benchmarks  and  user feedback  confirm  the  system’s  effectiveness in  providing  a  seamless experience for solving complex mathematical problems.



