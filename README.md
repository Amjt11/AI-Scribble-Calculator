# AI-Scribble-Calculator
An AI powered calculator that transforms scribbles into solutions 

## Problem Statement
Traditional calculators are limited to basic numerical operations, lacking context-aware calculations, natural language processing (NLP) for conversational inputs, and integration with dynamic data sources for real-time, contextual operations.

## Solution Approach
**Our AI Calculator** transforms digital interaction by allowing users to solve mathematical equations written as scribbles or drawings directly on a screen.  

### Key Features: 

- **Scribble Input:** Supports handwritten equations or calculations using an input pen.  
- **Instant Solutions:** Instantly solves inputs in any format—equations, images, or drawings.  

### Unique Points: 
- Removes the need for keyboards or structured input.  
- Combines handwriting recognition with real-time calculations for seamless use.


## Workflow

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

![image](https://github.com/user-attachments/assets/68e5b91c-126b-4bac-b9d3-456854fb56d5)


**Image Analysis (Gemini AI):**

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

 ![image](https://github.com/user-attachments/assets/2a855d8f-a52c-4d55-b06f-2671260574fa)




