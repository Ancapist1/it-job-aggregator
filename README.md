# it-job-aggregator
The idea is to create a project which scrapes the job data, analyses it and aggregates the technologies / experience / salary.
Then it shows them on the website.

FYI: this repo is only for showcase purpose. If it wasn't, i would've never put all of the code in a single monorepo - it would be a total mess!

It will look sth like this (since it's early stage it will most probably change): 

![image](https://user-images.githubusercontent.com/105131327/216625307-4cacf9ba-bf18-4811-a429-0388c7ece1fb.png)

Since scrappers will be written in Node, I'll make them separate, running in Docker (This way I'll make them run in parallel). The data will be then sent to RabbitMQ queue, then saved in the database. I could have mutliple mongodb instances, but it would require n calls to the services (where n is the number of scrapper instantions) each time I would want to get the data.
