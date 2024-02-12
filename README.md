## Inspiration
Going into a politically polarizing election year is a very daunting prospect. 2024 is set to have the greatest amount of electoral misinformation in history thanks to AI enhanced tools manipulating our social media and news sources. We decided that not only are relevant political news stories in high demand, but so is a technology to help analyze and remove their underlying biases more important than ever.
## What it does
Cito (named after the french word for citizen, citoyen), approximates a user's location by their zip code and assembles a list of important and relevant political news stories for their area. Then, using an ML classification model, rates the article writing for political polarization. Finally, a short summary is generated and given with a special emphasis made on highlighting the objective content. These news articles are sent to the user by notifications in a periodic fashion, with the original stories linked in the descriptions for fair comparison. We also have a chatbot to answer any questions users may have about the content they receive. 
## How we built it
The front end of our application was created using Javascript (React), Tailwind and SCSS. The back-end was assembled primarily through python and Next.js. We created a scraper that entered custom search parameters based on the user's location to google news searches. We also trained an ML model with sklearn on the Hyperpartisan News Detection dataset created for PAN @ SemEval 2019 Task 4, and used that to analyze the content of the scraped articles. We used SQLite to assemble tables to store our relevant data. 
## Challenges we ran into
We initially utilized an DistilBERT, a model for classification that didn't achieve the accuracy or loss results we wanted, and which took a very long time to train. We eventually migrated to an SVM later in the project as a result, which was much faster to train. It was also difficult to get Google News to respond to our specific search queries, as a lot of the key search operators were not as effective as stated. It was also hard having to scrape data from a variety of online formatting styles, and depending on the zip code there were less articles that fit our criteria of recent, political, and relevant. As well, the time crunch would have ideally been less severe 😅
## Accomplishments that we're proud of
We are proud of the completed web based app we developed, and its many interconnected features, which are all purposeful and sleek in the face of a minimalist front-end design. In the end our classification model achieved a 96.29% accuracy measurement across the validation/testing data we used. 
## What we learned
In the course of this project we learned a lot about a variety of libraries, languages, and programming techniques. A lot of our group members got some experience with website scraping, applied machine learning, and database assembly. We learned how to function in a collaborative environment and support the project and each other through constructive feedback and general helpfulness. We learned that while AI is poised to be overwhelming to the global political ecosystem, we as young developers have the capacity to push back against the trend with tools designed to help rather than harm. 
## What's next for cito
Full personalization, polishing, and eventually globalization.


## Usage
```
npm install
npm run dev
```
