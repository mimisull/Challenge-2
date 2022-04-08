# Challenge-2 Repository
---
*Welcome to my Loan Qualifier App repository*
The Directory for this respoitory is:
[Summary](https://github.com/mimisull/Challenge-2/blob/main/README.md)
[Code](https://github.com/mimisull/Challenge-2/blob/main/app.py)
[TerminalHistory](https://github.com/mimisull/Challenge-2/blob/main/terminal_history.txt)
**Challenge activity 2 Loan Analyzer**
> Specifically, BizOps wants to know if this software can prompt the user to save the qualifying loans as a new CSV file.
*User Story*:
As a user, I need the ability to save the qualifying loans to a CSV file so that I can share the results as a spreadsheet.

*Acceptance Criteria*:
Given that I’m using the loan qualifier CLI, when I run the qualifier, then the tool should prompt the user to save the results as a CSV file.

Given that no qualifying loans exist, when prompting a user to save a file, then the program should notify the user and exit.

Given that I have a list of qualifying loans, when I’m prompted to save the results, then I should be able to opt out of saving the file.

Given that I have a list of qualifying loans, when I choose to save the loans, the tool should prompt for a file path to save the file.

Given that I’m using the loan qualifier CLI, when I choose to save the loans, then the tool should save the results as a CSV file.

## New Functionality Adds
New additions to the code include:
>'''def save_qualifying_loans(qualifying_loans):
    saves_loan = questionary.confirm("Do you want to save your qualifying loans?").ask()
    file_path = questionary.text("Enter a file path to save qualifying loans:").ask()
    file_path = Path(file_path)
    if not file_path.exists():
        sys.exit(f"Oops! Can't find this path: {file_path}")
    return save_qualifying_loans(file_path)'''

What this functionality serves is prompting the user for not only do they want to save their file, but where would they like to save it. This helps users organize themselves and makes sure the code doesn't just default to downloads like many applications do. This streamlines the process for the user.

## Usage
The project works by asking the user for their loan data, then asking for all the relevant information to pull any loans that they qualifier for based on their (bank_data, credit_score, debt, income, loan, home_value). Then, it prompts them to ask if they would like to save their file, and where they would like to save it.

## Contributors
Michael Sullivan
