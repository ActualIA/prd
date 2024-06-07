# The MVP

The goal of ActualIA's MVP is to bring the news to the user. To achieve it, it will integrate the following features :

- News provider selection over the main providers: RSS feeds, Google News and Telegram channels;
- Interest topic selection over a wide range of subjects;
- News summarization, on both news count and length;
- Audio reading, aiming for a one minute audio file.

ActualIA's MVP won't just be a black box that only provides the news, but it will also be able to tell where it comes from. To achieve this goal, ActualIA's MVP will feature :

- The original article for every summarized news, with a link to its original source;
- News context inspection, that can be used by simply taking a photo of an article to get the context around it. This feature is powered by OCR (*Optical Character Recognition*) and the same LLM used in the rest of the app. 

## Personas and Scenarios

ActualIA targets a demographic stuck between their want to stay informed on their interests and their lack of time. We offer them access to a customized briefing summarizing the important news of the day, automated and easy to skim. 

At ActualIA, we believe the news to have an important social aspect: that's why we offer ways to quickly share your transcripts to others, whether they are users of the app or not. We expect word of mouth to be a great adoption mechanism amongst our target demographics, such as students or office workers, since they tend to share interests and routines, and to find utility in the app. 

This is also why we have made the installation and onboarding aspect of the application as fast and lean as possible: when a potential user comes across an interesting news transcript shared by a friend, it is going to be very easy to follow the leads, install the app, and be an active user, at least for a period, to try it out.

The application will likely be used daily. Users will most likely set their alarms at two main times: 
 - In the morning, to wake up. This allows them to integrate the podcast in their morning routine, be it at home, while eating, or in their commute.
 - in the evening, after work or school, going back home.

## User Stories and Key Features

*"As a user, I want a fast to read recap of what happened yesterday such that I get updated regularly on the subjects that interest me."*

*"As a user, I want a short audio reading of yesterday's news such that I can not give my full attention to it."*

*"As a user, I want to customize my news feed such that I stay informed on the subjects I'm interested in and not be overwhelmed by other news."*

*"As a user, I want to retrieve the original source a transcript paragraph comes from, to verify its accuracy and get more information on it."*

*"As a user, I want to retrieve the context around an article such that I can be less biased and more informed in reading it."*

## Success Criteria

After MVP release, we aim for 1000 downloads in the first month, and 5000 downloads in the first three. For context, 5000 users is about the size of a small Swiss town.

After those 3 months, 10% of these 5000 users should be on the paid plan, DAU should be over 55%, MAU over 60%, the difference between MAU and DAU should not be bigger than 5%, and the retention rate should be over 80%. The app should have more than 4 stars on the Google Play Store.

DAU will be computed by totaling the number of users that made a news transcript request the last day, and dividing that by the number of users in our database since the launch of the MVP. MAU is computed by taking the number of users that have made a least two news transcript requests separated by at least one day without a request (this can be achieved by setting no alarm and doing the requests manually on the application). If we divide this MAU with the one from Google Analytics (the number of active users) we can obtain the percentage of users that uninstalled the app during the last 30 days, thus obtaining the retention rate.

If the difference between MAU and DAU is too big, it means that our audience is not interested in daily news but more on some news sometimes which might lead our strategy in a different direction.

Regarding feedback, we estimate that having a relatively big DAU is enough. In a next version, we will implement feedbacks on news transcript (users will be able to like or dislike a news) which will be useful for fine-tuning user preferences, as well as judging transcript usefulness amongst users. We will also add a more detailed feedback section on the app, so that users can suggest new features or improvements.

Another improvement that could be made would be direct collaboration with newspapers, in order to more cleanly use their articles as source. 

## Features Outside the Scope

News rating will not be implemented in the MVP. Being able to rate it is not hard (like / dislike) but having that kind of interaction taken into account would mean needing to update the prompt generating the news accordingly, requiring a whole prompt engineering process.

Setting a custom voice model from a recording, so it reads the news instead of the predefined voices, could be possible, but this comes at two main costs: 

 - the technical cost, since we would require a new AI model, and our backend would need to be modified in order to integrate it in its work flow. Doable, but it requires thought to properly implement;
 - the ethical cost, since would have to consider security and ethics issues, which is out of scope for a MVP.

In any case, being able to have it's partner or friend voice to read the news would be a great feature, and it will be considered when the time is right.

Additionally, one of the risks of such a closely customized news experience is amplifying pre-existing news biases in users, with their selection of news channels. This might lead to the [*filter bubble effect*](https://en.wikipedia.org/wiki/Filter_bubble). This is a phenomenon we need to keep in mind, but tackling the problem is currently impossible given our team composition: while we all have an interest in journalism, tackling this kind of bias requires a much deeper understanding of its causes and fixes, which is beyond the scope of our skills. This would require close collaborations with experts in media or journalism studies, or other similar fields.

We will also not consider any kind of social network-like feature, such as following profiles or other strict interaction between users, because we believe it to be outside of the spirit of the app. The engineering manpower we have is best used elsewhere to make the processes better, and the network aspect would clutter the streamlined onboarding and usage flows we have defined for our application. 