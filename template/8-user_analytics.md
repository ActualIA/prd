# User Analytics and Acceptance

In order for our MVP to have a meaningful usefulness in product direction, we will need to implement some sort of tracking. This will allow us to gauge adoption of new features in terms of UIUX choices, as well as identify bugs and pain points that need improvement. We could implement:

### Metrics

- User engagement: average duration per app visit, as well as/as a function of navigation paths;
- Feature adoption: taps on key feature buttons;
- User retention: conversions from free to paid plan user, average subscription length in months; onboarding/customization drop-off rate;

### Success criteria

As success criteria, we consider (other than smooth operation of the app, which is a given), not necessarily high levels of adoption, but retention. What we have is a product that responds to a need, sure, but we also have a new workflow, a pipeline which might not fit everyone on earth, no matter how streamlined it is. Therefore, we are more interested in high **retention rates in paid plan users**: using the free plan as a "launch platform" for users to decide it's for them, we can retain loyal users for the paid plan.

### User Analytics

Supabase allows easy anonymous data collection, and we plan to closely monitor it to measure the metrics we specified in the *Metrics* section. This kind of data collection refers to collections of users and their general behavior as a trend, and is therefore easily anonymized, in order to comply with privacy laws.

### AB Testing

AB testing could be particularly useful in seeing how easy to use the app is, by measuring click through rate through key feature paths (such as the onboarding, settings, or main panes) depending on different UIUX choices.
