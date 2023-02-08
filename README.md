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

## Building
- API Layer
- Database Layer
- Client (Optional)

## Testing
- Postman
- Authorization Work