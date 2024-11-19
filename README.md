<h1>Dynamic-Form-Generator</h1>

## Overview

The Dynamic Form Generator is a tool that allows users to create forms dynamically based on JSON schemas. It simplifies the process of form creation, validation, and data handling.
 ### Background
 - Create a dynamic form generator that takes a JSON schema and generates a styled, functional form in real-time. The application should display the JSON editor and the generated form side by side.

### Main Interface
 1. Create a split-screen interface with:
    - Left side: JSON editor
      - Syntax highlighting for JSON
      - Real-time JSON validation
      - Error messages for invalid JSON
    - Right side: Generated form preview
      - Updates in real-time as JSON is edited
      - Responsive form layout
      - Proper error states and validation

2. Technical Requirements:
   - Use TypeScript for type safety
   - Create proper interfaces for the JSON schema
   - Handle JSON validation gracefully
   - Real-time form generation and validation
   - Proper error boundaries for both editor and form
   - Mobile-responsive layout (stack editor and preview on smaller screens)
   
### Form Features
 - The generated form should:
    - Support all field types from the schema
    - Show proper validation messages
    - Have loading states where appropriate
    - Submit data to console.log()
    - Show success message after submission
    - Be styled consistently using Tailwind CSS

 ### Testing Requirements
  - Write tests using Playwright and Jest:
    - Test JSON validation
    - Test real-time form generation
    - Test form validation and submission
    - Test responsive layout
    - Test error scenarios

  ### Technical Stack
   - React 18+
   - TypeScript
   - Tailwind CSS
   - React Hook Form
   - Playwright for E2E testing
   - Jest for unit testing

  ### Evaluation Criteria
  
   1. Code Quality:
      - TypeScript usage and type safety
      - Component structure and reusability
      - Error handling
      - Code organization
   2. User Experience:
      - Real-time updates
      - Form responsiveness
      - Error messages
      - Mobile compatibility
  3. Testing:
      - Test coverage
      - Edge case handling
 ### Bonus Points
  - Add a "Copy Form JSON" button
  - Implement form field validation preview
  - Add dark mode support
  - Add ability to download form submissions as JSON

## Setup Instructions

To get started with the Dynamic Form Generator, follow these steps:

### Prerequisites

- Node.js (version 14 or later)
  ```bash
  https://www.geeksforgeeks.org/installation-of-node-js-on-windows/
- npm (Node package manager)
  ```bash
  npm install npm --global // Updates the ‘CLI’ client

### Installation

1. Clone the repository & like new folder:

   ```bash
   CMD: npx create-react-app dynamic-form-generator --template typescript
   cd dynamic-form-generator
   
2. Get started with Tailwind CSS:
   ```bash
   https://tailwindcss.com/docs/installation
   package :
   npm install -D tailwindcss postcss autoprefixer
   npm install tailwindcss react-hook-form
   npm install tailwindcss react-json-view
   
3. Install the required dependencies:
   ```bash
   npm install

4. Start the development server:
   ```bash
   npm start
The application should now be running at http://localhost:3000.   

## Example JSON Schemas
Here are a couple of example JSON schemas to demonstrate how to define forms:

    ```json
    {
      "formTitle": "Project Requirements Survey",
      "formDescription": "Please fill out this survey about your project needs",
      "fields": [
        {
          "id": "name",
          "type": "text",
          "label": "Full Name",
          "required": true,"placeholder": "Enter your full name"
        },
        {
          "id": "email",
          "type": "email",
          "label": "Email Address",
          "required": true,
          "placeholder": "you@example.com",
          "validation": {
                "pattern": "^[^\\s@]+@[^\\s@]+\\.[^\\s@]+$",
                "message": "Please enter a valid email address"}
        },
        {
          "id": "companySize",
          "type": "select",
          "label": "Company Size",
          "required": true,
          "options": [
          { "value": "1-50", "label": "1-50 employees" },
          { "value": "51-200", "label": "51-200 employees" },
          { "value": "201-1000", "label": "201-1000 employees" },{ "value": "1000+", "label": "1000+ employees" }]
        },
        {
          "id": "industry",
          "type": "radio",
          "label": "Industry",
          "required": true,
          "options": [
          { "value": "tech", "label": "Technology" },
          { "value": "healthcare", "label": "Healthcare" },
          { "value": "finance", "label": "Finance" },
          { "value": "retail", "label": "Retail" },
          { "value": "other", "label": "Other" }]
        },
        {
          "id": "timeline",
          "type": "select",
          "label": "Project Timeline",
          "required": true,
          "options": [{ "value": "immediate", "label": "Immediate (within 1 month)" },
          { "value": "short", "label": "Short-term (1-3 months)" },
          { "value": "medium", "label": "Medium-term (3-6 months)" },
          { "value": "long", "label": "Long-term (6+ months)" }]
        },
        {
          "id": "comments",
          "type": "textarea",
          "label": "Additional Comments",
          "required": false,
          "placeholder": "Any other details you'd like to share..."
        }]
      }

## Local development guide

    npm test

## Building for Production
To build the application for production, use the following command:
     
     npm run build

## Final output

<img align="center" alt="Output" src="https://raw.githubusercontent.com/harish5108/Dynamic-Form-Generator/refs/heads/main/Screenshot%202024-11-19%20094435.jpg">

