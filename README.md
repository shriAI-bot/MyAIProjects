Summary: This tool will help users practice for standardized tests and job assessments.

Steps to access the tool:
  1. Copy paste the code into notepad file or Click “Download” to get the file
  2. Save it with a .html extension (e.g., mocktest.html). If Save won't work then try 'Save As' as .html file.
  3. Double-click the file to open it in your browser — and you're in!

 Prompt for LLM: Copy paste entire section / prompt on on your favoriate LLM tool like Google AI Studio, Claude, Chat GPT etc. You can Change it as per your need and build your own tool!
 ** IF Tool starts giving memory error then reduce the number of questions to 50 and see the result and then optimize it.

 --PROMPT STARTS---
 
LLM Prompt: Build a Self-Contained Cognitive Ability Mock Test Tool
[1. PROJECT GOAL & OVERVIEW]
Your task is to generate the complete code for a self-contained, interactive Cognitive Ability & Logical Reasoning Mock Test Tool. The final output must be a single index.html file that runs locally in any modern browser without needing a server or internet connection. This tool will help users practice for standardized tests and job assessments.
[2. CORE TECHNICAL REQUIREMENTS]
Platform: A single, self-contained .html file.
Technology Stack: Vanilla JavaScript (ES6+), CSS3, and HTML5 only.
Dependencies: Absolutely none. Do not use any external libraries or frameworks (e.g., jQuery, React, Vue, Bootstrap).
Deployment: The index.html file must be fully functional when opened directly in a web browser.
[3. CONTENT GENERATION: THE QUESTION BANK]
You must generate a high-quality, diverse question bank embedded directly within the JavaScript.
Total Unique Questions: 150 unique questions.
Cognitive Categories & Distribution: Generate exactly 30 questions for each of the 5 categories below. Ensure the questions within each category are distinct and cover the described topics.
Verbal Reasoning: Reading comprehension, grammar, vocabulary, verbal deductions.
Numerical Reasoning: Arithmetic, number series, ratios, word problems, data interpretation.
Logical Reasoning: Pattern recognition (non-visual), critical reasoning, analogies.
Deductive Reasoning: Syllogisms, if-then statements, conditional logic puzzles.
Spatial & Abstract Reasoning: Shape rotation, 2D/3D visualization, matrix completion, visual patterns.
Difficulty Distribution (per category): Within each category's 30 questions, ensure this precise difficulty split:
Easy: 7 questions (~25%)
Medium: 16 questions (~50%)
Hard: 7 questions (~25%)
Question Structure: Every question must be a JavaScript object with the following format. Ensure all explanations are clear and detailed.
Generated javascript
      // Sample Question Object Format
{
  category: "Numerical Reasoning", // Must match one of the 5 categories
  difficulty: "Easy", // "Easy", "Medium", or "Hard"
  question: "What is the next number in the sequence: 2, 4, 8, 16, ?",
  options: ["18", "24", "32", "36"], // An array of 4 string options
  correct_index: 2, // The 0-based index of the correct answer in the options array
  explanation: "The pattern is to multiply the previous number by 2. Therefore, 16 × 2 = 32."
}
   
[4. APPLICATION LOGIC & TEST STRUCTURE]
Exam Series: The tool will guide the user through a series of 3 exams.
Exam Composition: Each exam consists of 50 multiple-choice questions.
Randomization & Uniqueness:
For a full test-taking session (all 3 exams), you must pull 150 questions from the question bank.
For each of the 3 exams, randomly select 50 questions from the pool without replacement.
CRITICAL: Ensure that no question is repeated across any of the 3 exams within a single session.


Timer: Each exam is timed for 15 minutes.
A countdown timer must be clearly visible on the screen.
The exam must auto-submit when the timer reaches 00:00.


Navigation:
Users can click "Next" to proceed to the next question.
Once an answer is submitted, the user cannot go back to change it.
A "Submit Exam" button appears on the final question.


[5. SCORING, RESULTS & FEEDBACK]
Per-Exam Report (Displayed after each exam is completed):
Score: Display the final score (e.g., "42 / 50").
Pass/Fail Status: Show "Pass" if the score is 70% or higher, otherwise "Fail".
Performance Breakdown: A percentage-based summary of performance in each cognitive category (e.g., Verbal Reasoning: 80%, Numerical Reasoning: 60%).
Incorrect Answers Review: List every question the user answered incorrectly. For each one, show:
The original question.
The user's incorrect answer.
The correct answer.
The detailed explanation for the correct answer.




Comprehensive Final Report (Displayed after all 3 exams are completed):
Overall Summary: An overview showing the score and Pass/Fail status for each of the 3 exams.
Performance Trends: A simple trend analysis showing performance (by percentage score) in each cognitive category across the 3 tests.
Overall Average: The average score across all 150 questions.
Personalized Study Advice: Generate brief, actionable advice based on the user's weakest categories (e.g., "You consistently scored lower in Spatial Reasoning. Focus on practicing shape rotation and pattern matrix puzzles.").


Retesting: After the final report, provide a button to "Restart Test Series". This should clear all session data and start a new series with a fresh randomization of questions.
[6. USER INTERFACE (UI) & EXPERIENCE (UX)]
Design Philosophy: Create a clean, modern, and professional UI. Use a minimalist aesthetic with ample white space. The layout should be intuitive and distraction-free.
Layout: Use modern CSS (Flexbox and/or Grid) to ensure the layout is fully responsive and looks great on desktop, tablet, and mobile devices.
Color Palette:
Primary Action/Highlight: #4285F4 (Blue)
Correct/Pass: #34A853 (Green)
Incorrect/Fail: #EA4335 (Red)
Background: #F8F9FA (Very light grey)
Text: #202124 (Dark grey/almost black)


Key UI Components:
Welcome Screen: Title, brief instructions, and a mandatory disclaimer section.
Disclaimer Logic: The "Start Exam" button must be disabled until the user checks a box that says: [ ] I have read and acknowledge the disclaimer.
Quiz Interface:
Visible countdown timer.
Progress indicator (e.g., "Question 5 / 50").
The current question.
Four clickable answer choices.


Result Screens: Clearly formatted reports as described in section 5.


Disclaimers: Use the exact text below.
On the Welcome Page (before starting):
"Disclaimer: The content in this tool is generated by an artificial intelligence model and is for practice purposes only. AI models can make mistakes and may produce inaccurate information or incorrect answers. You must independently verify all information. The developer of this tool accepts no liability for any decisions made based on its content."
On all Result Pages (at the bottom):
"Disclaimer: Results and explanations are generated by an AI and are for informational purposes only. Please verify any information that seems incorrect."
[7. CODE & QUALITY REQUIREMENTS]
File Structure: All HTML, CSS, and JavaScript must be contained within a single index.html file. Use <style> tags for CSS and <script> tags for JavaScript.
Code Style: Use clear, descriptive variable and function names (e.g., currentQuestionIndex, calculateScore()).
Commenting: Add comments to explain major parts of the JavaScript logic (e.g., the randomization function, the scoring logic, the timer setup).
Validation: Ensure the generated code is free of errors. Check for:
No duplicate questions in the question bank.
Accurate correct_index and explanations for all questions.
Flawless functionality of the timer, navigation, and scoring logic.
Cross-browser compatibility (Chrome, Firefox, Edge).


[8. FINAL OUTPUT CHECKLIST]
Your final generated index.html file must contain:
<head> with metadata and all necessary CSS in a <style> block.
<body> containing:
A welcome screen with instructions and the mandatory disclaimer checkbox.
The quiz interface structure (to be populated by JS).
The result page structures (per-exam and final report).


<script> tag at the end of the body containing:
The full 150-question JavaScript object array.
All application logic for test management, randomization, timing, scoring, and UI updates.

 -- END OF PROMPT


