## Adding a new lab member

1. Create a new file in `people/`

   Example:
   `people/jane-doe.md`

2. Add front matter:

---
id: jane-doe
name: Jane Doe
role: Graduate Student
photo: jane-doe.jpg
email: jane.doe@lehigh.edu
---

Short bio here.

3. Add the ID to `_data/people.yml` in the desired display order:

- id: fujiwara
- id: cruz
- id: jane-doe

4. Add the photo to:

assets/img/people/jane-doe.jpg

5. Commit and push.