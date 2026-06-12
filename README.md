Prompt Engineering Internship – Week 1
Project 1: Zero-Shot & Few-Shot Data Extraction
Overview

This project demonstrates the application of Prompt Engineering techniques to extract structured information from unstructured resume text and convert it into a valid JSON format.

The prompt was designed to perform deterministic data extraction using delimiters, few-shot examples, JSON schema enforcement, and temperature control.

Objective

To design a prompt that can extract candidate information from unstructured text and return it in a structured JSON format while maintaining consistency, accuracy, and proper handling of missing values.

Information Extracted

The prompt extracts the following fields:

{
  "candidate_name": "",
  "education_field": "",
  "skills": [],
  "experience": "",
  "desired_role": "",
  "contact_number": null
}
Prompt Engineering Techniques Used
1. Delimiter Usage

Used ### delimiters to clearly separate instructions from raw input data.

2. Few-Shot Prompting

Two Input/Output examples were provided before the final test case:

Rahul Sharma – Computer Science Engineering Student
Anjali Nair – Electronics and Communication Engineering Student

These examples helped the model learn the expected extraction pattern.

3. JSON Schema Enforcement

The model was instructed to generate only valid JSON output without explanations or conversational filler.

4. Null Handling

Missing values are returned as null instead of being guessed.

5. Deterministic Formatting

The output follows a consistent schema for every input.

6. Temperature Control

Temperature was set to 0 to reduce randomness and improve output consistency.

Final Test Case
Input
RAW_TEXT:

Hi, My name is Ardra, an Electronics and Communication student.
Skilled in Embedded, Python, SQL and Matlab.
Completed a 2 week internship in IOT.
I would like to work as an AI Intern and my contact number is 9447575893.
Generated Output
{
  "candidate_name": "Ardra",
  "education_field": "Electronics and Communication",
  "skills": ["Embedded", "Python", "SQL", "Matlab"],
  "experience": "2 week internship in IOT",
  "desired_role": "ai intern",
  "contact_number": "9447575893"
}
Results

The model successfully extracted all required fields from the unstructured resume text and generated a valid JSON output while maintaining schema consistency and deterministic formatting.

Tools Used:
- Google AI Studio
- GitHub
- Google Drive

link: https://aistudio.google.com/app/prompts?state=%7B%22ids%22:%5B%221Z89eY-RlP-O5PP275g_0uAfQs65BqGdU%22%5D,%22action%22:%22open%22,%22userId%22:%22117155938400731026692%22,%22resourceKeys%22:%7B%7D%7D&usp=sharing

Output:
The prompt successfully extracts candidate details and returns structured JSON output.

