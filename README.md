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
- 
![image](https://github.com/user-attachments/assets/90e6802d-ea83-4f54-8732-3272fbf07061)


## Workflow

Frontend Interaction (React Application):

- User draws on a canvas
- Clicks "Calculate" button
- The canvas is converted to a base64-encoded image
- The image and any predefined variables are sent to the backend via an axios POST request
- Backend Route Handling (Fast API):
- Receives the POST request with image data
- Decodes the base64 image string
- Converts the decoded data to a PIL (Python Imaging Library) Image object
- Calls the analyze image function with two parameters: a. The image object b. A dictionary of user-defined variables
![image](https://github.com/user-attachments/assets/1ca2dd6a-5290-46f5-90f1-abb935dd3cda)


Frontend Interaction (React Application):
User draws on a canvas
Clicks "Calculate" button
The canvas is converted to a base64-encoded image
The image and any predefined variables are sent to the backend via an axios POST request
Backend Route Handling (Fast API):
Receives the POST request with image data
Decodes the base64 image string
Converts the decoded data to a PIL (Python Imaging Library) Image object
Calls the analyze image function with two parameters: a. The image object b. A dictionary of user-defined variables
![image](https://github.com/user-attachments/assets/2276f9cc-9239-4171-b226-0dfd0334474a)

