# kanban-readme

## How to run ui / backend

I'm not sure if there a "pip install -r requirements" or "virutal environemnts" in nodejs like in python. I've seen that you just needed to do `npm install` in the directory where the package.json is.

1) run kanban api with `npm start`:
    - this should show a localhost with a port number.;
2) run kanban ui with `npm start`;
    - This should start up react!;


## Overall Architecture

In order to try and make myself as familiar with the tech-stack, I decided to challenge myself and try to mimic the way ~pensieve~ was doing it. So the backend is constructed with express and hits a mongo database with mongoose.

1) Backend
    - Database: MongoDB
    - Language: Express.js
2) FrontEnd
    - Language: React
    - Env: Node.js


Details:

- To put it into a bit of detail, the frontend consists of four major components: (Dashboard, Columns, Post, Header). The header isnt fully functional on the backend but I at least wanted to make the webpage look a little better and filled rather than having a singular kanban dashboard. The dashboard represents the overall table while each column holds the column title and multiple posts that are tied to the column_title such as "to-do". I've also added a settings sign that I wanted to allow for adding and deleting columns;however, due to the essense of time, thought it would be better to move on.

- The backend similarly has four different major routes/tables. Because I was very unfamiliar with utilizing a document database, it was very difficult to wrap my head around how to design the "documents." Usually in sql you would store a one-to-many relationship such as posts to columns as posts referencing the column. Instead, because this is document-based, there lies the perk of storing both data into one document. I checked multiple videos on "best practices" but each case had its own pros and cons. Hence, thinking about scaling, I thought it was best to have "references" or kind of like a join between each document.


Thoughts:
- If given more time, I would have tried to 1) split off the queries for each component (columns component -> columns query) instead of having to go down the reference road between documents and just doing one full query. (this might prove to fix a bug of not refreshing once updated.)

- Set up a settings to add/edit/or delete columns

Lessons Learned:
- Trying a new tech stack + on a time crunch makes you try and cut corners.
- The way you design documentDBs is kinda like the opposite of a sql relational database.
- React's kinda neat!
- Learning is stressful but fun :')
- Not sure if i enjoy mongodb ;;






