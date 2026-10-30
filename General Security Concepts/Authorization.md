Based on your identification, what resources should you have access to ==🟢ex. assets in a particular department==

Once [[Authentication]] has proven who you are, authorization decides what you are allowed to do. An employee in HR should be able to open the HR files but not the finance files, even though both of them are logged in to the same company network. The general idea is to give each person only the access they need to do their job and nothing more, which is the principle of least privilege.

For large scalability this would be done via authorization models, which are typically assigned by roles, departments, organizations etc. This way, when a new person joins HR we can just place them in the HR role and they automatically get the correct access, instead of setting up every permission by hand.

> [!joke] Authentication gets you into the building, authorization decides if you can enter the CEO's office.

# Previous Topic
[[Authentication]]
# Previous Section
[[AAA Framework]]
# Next Topic
[[Accounting]]
