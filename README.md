# Referral API Planning!

## Ideation
- As an employee of a company, I create a profile on this service, and it gives me a personalized link. I can share that link with anyone who wants a referral at the company I work for. When they click on that link, they can upload thier resume, say how they know me, personal info, and then a note or something. When they click submit, it'll show up on my list of referrals. I as a user can change the status of the referral (if it's done, etc)
- Input
  - Referree
    - Name, Email, Resume, notes-for-referrer
  - Referrer
    - Name, Email, Employer, List of referrees, Link for this referrals, Status of  referrals
- Action
  - Referree
    - Verify that the personalized link exists
    - Write to our database the infformation they submit
  - Referrer
    - Update list of referrals
    - Generate a link for them that is personalized
    - Allow them to be able to change the status of a referral
- Output
  - Confirmation path or something that shows it added sucessfully
- Tools we'll need
  - Java version installed
  - Postman
  - Database that is storing the info (optional)

## Classes
  - Referrer
    - Fields:
      - Name, Email, Resume, Employer, Hashmap of referees and the key is referee, and the value is list of info they sent or a nested list, Link for referees (name)
    - Paths:
      - /referrer/NAME?
        - Input: Post a request to this path with the following query:
          - Name, email, resume (a link to your resume that is a string), note 
        - Action: write to our database, add all 4 of those to the field called referees and then return that nested list
      - /referrer/NAME/referees
        - Input: a get request
        - Action: go to db and give me the nested list of all referees on this person
  - Referree
    - Fields:
      - Name, Email, Resume, Note 

## Building
- API Layer
- Database Layer
  - Mysql
    - Data
      - Referrer and all thier fields
- Client (Optional)

## Testing
- Postman
- Authorization Work