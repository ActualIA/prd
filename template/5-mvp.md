# The MVP

ActualIA's MVP will bring news to user. To achieve so it will integrate the following features :

- News provider selection on the main providers (RSS flows, google news, ...)
- Topic selection over a wide range of subjects
- News summarization, on both number of news and length of them
- Audio reading, aiming a one minute audio file

ActualIA's MVP mustn't be a black box that only provides news, but also tell where it comes from. To achieve this goal, ActualIA's MVP will feature :

- The original article for every summarized news, with a link to its location
- News context inspection, that can be used by simply taking a photo of an article to get the context around it

## Personas and Scenarios

ActualIA doesn't have a key audience, it targets all citizens since everyone should keep track of the actuality.

Being well informed on recent events is a encouraged in society, and since being informed with ActualIA takes no time (without counting the download of the app and the onboarding) many people would like to download only by hearing about it.

Moreover, the application offers a way to share the transcript to other people, through the app and on other medias. When someone will have an interesting news that he wants to share, he will recommand the application to another potential user.

The application will be used daily, since it produces a news recap every day, with an alarm set by the user to set up a routine. The alarm will most likely be set for the morning when awakening, to here the news while getting dress up (before going to work at least), or for the evening, when coming back home. It could also be set for a break during the day.

## User Stories and Key Features

"As a user, I want a fast to read recap of what happened yesterday such that I get updated regularly on the subjects that interest me."

"As a user, I want a short audio reading of yesterday's news such that I can not give my full attention to it."

"As a user, I want to customize my news feed such that I stay informed on the subjects I'm interested in and not be overwhelmed by other news."

"As a user, I want to retrieve the orginal source a transcript paragraph comes from such that I can verify it and get more information on it."

"As a user, I want to retrieve the context around an article such that I can be less biased and more informed when reading it."

## Success Criteria

We aim for 5000 downloads three months after MVP's release, 1000 after one month (5000 is the population of a small town).

After those 3 months, 10% of these 5000 downloads should use the paid plan, DAU should be over 55%, MAU over 60%, the difference between MAU and DAU should not be bigger than 5%, and the retention rate should be over 80%. The app should have more than 4 stars on playstore.

DAU will be computed by summing the number of users that made a news transcript request the last day (and dividing by the number of created users in our database since the launch of the MVP). MAU is computed by taking the number of user that have made a least two news transcript requests separated by at least one day without a request (this can be achieved by setting no alarm and doing the requests manually on the application). If we divide this MAU with the one from Google Analytics (the number of active users) we can obtain the percentage of users that uninstalled the app during the last 30 days, thus obtaining the retention rate.

If the difference between MAU and DAU is too big, it means that our audience is not interested in daily news but more on some news sometimes which might lead our strategy in a different direction.

Concerning feedback, we estimate that having a relatively big DAU is enough. In a next version, we will implement feedbacks on news transcript (users will be able to like or dislike a news) which will be usefull for fine-tuning users preferences but also seeing if overall users find the news usefull or note. We will also publish a survey on the app, so that users can suggest new features or improvements.

A very nice improvement would be to work with regular newspapers like [*The Times*](https://www.thetimes.com/), where we could provide a news transcript every day on their site using only their articles, or to develop a fine-tune version of our app for their journalists so they are kept updated everyday.

## Features Outside the Scope

News rating will not be implemented in the MVP. Being able to rate it is not hard (like / dislike) but taking it in account would mean that the app has to update the prompt generating the news accordingly, which involves a whole prompt engineering proces.

Being able to record voice so it reads the news would maybe possible today, however the server would have to integrate a new AI model, and we would have to consider security and ethics issues, which is out of scope for a MVP. But being able to have it's partner or firend voice to read the news would be a great feature.

Currently, ActualIA only fetches news from user provided sources. This leads to a [*filter bubble effect*](https://en.wikipedia.org/wiki/Filter_bubble) which puts the user in a state of intellectual isolation. ActualIA has to tackle this problem, but it needs reflection with experts on how to fetch from other sources that are considered as objective to cross-check facts, but with actuality it's not trivial to find an objective news provider.
