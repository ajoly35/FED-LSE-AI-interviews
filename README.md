# FED/LSE AI Interviews Integration

A lightweight web bridge that connects Qualtrics surveys with ElevenLabs Conversational AI to conduct automated, context-aware academic research interviews.

## Overview

This project enables a seamless two-way workflow:
1. Qualtrics Part 1: The respondent answers initial demographic and technology questions.
2. Redirect with Context: Qualtrics redirects the respondent to this GitHub Pages site, passing survey answers as URL parameters.
3. ElevenLabs AI Interview: The respondent speaks with an AI academic research interviewer who personalizes questions based on the received business context.
4. Automatic Return: Upon completing the interview, the agent triggers a custom client tool that redirects the participant back to Qualtrics to log completion.

## Data Passed via URL Parameters

- response_id: Unique Qualtrics response ID
- business_age: Operational duration of the business
- employee_count: Total current staff
- client_base: Target market and client profile
- ai_tools_used: Current operational AI tools reported by the participant

## Deployment

1. Push index.html to the main branch of your GitHub repository.
2. In repository Settings, navigate to Pages and select Deploy from a branch (main).
3. In Qualtrics Survey Flow, add an End of Survey element with redirect to your GitHub Pages URL, appending the survey piped text variables as query parameters.
4. In index.html, update qualtricsReturnUrl with your Qualtrics completion survey link.ml, update qualtricsReturnUrl with your Qualtrics completion survey link.
