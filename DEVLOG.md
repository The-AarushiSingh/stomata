Day 1 — User Model & Understanding Backend Design
What I Built

Started the backend for Campus Runner and created the first database model: User.

The goal of this model is to store all users of the platform, including:

Students creating delivery requests
Student runners accepting deliveries
Admins managing the platform

Created:

src/
└── models/
    └── user.model.ts

The model currently stores:

Name
Email
Password
Mobile Number (optional)
Role (user, deliveryBoy, admin)

I also enabled automatic timestamps so MongoDB tracks when a user is created and updated.

What I Learned

Today I learned that designing a model starts with understanding the problem, not writing code.

Before writing the schema, I need to ask:

What information do I need to store?
Which fields are required?
Which fields must be unique?
Which fields should have limited values?

For the User model:

Email should be unique because it identifies a user.
Password is required because users need authentication.
Mobile can be optional.
Role should only allow predefined values.

I also learned the difference between:

Interface

Used by TypeScript to provide type safety while coding.

Schema

Used by Mongoose to enforce database structure and validation.