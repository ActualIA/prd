# Non-Functional Requirements

## Security, privacy, and data retention policies

Authentication is handled in two ways, either via the Google SSO or the Anonymous Sign-In function provided by Supabase. In both cases, the amount of information we store is minimal (just the user email, display name and profile picture link, in the case of a Google account), and it is kept by our Supabase instance.

We also require multiple authorizations from the user to access their device's hardware, notably:

- *Camera access*, for OCR article context inspection;
- *Storage access*, in order to write the generated contexts, transcripts and audios to cache in the device's storage;

## Adoptions, Scalability and Availability

We expect a majority of the users that set alarms to set them between 06:00 and 08:00, meaning that the bulk of audio/text generation will happen around early morning. Users that don't have an alarm set do not see any automatic transcript generation, so the transcript generation behavior is entirely dependent on their schedule. We conjecture that small peaks will appear at or around the most common "break" times, such as 10:00, 12:00, 16:00 and 18:00.

Given our model, and the predicted customer count, with a fairly priced paid plan we expect to be able to cover the automatic scaling in Supabase, such that peaks in requests shouldn't necessarily impact us too much. Additionally, no impact on service availability would take place, given that compute nodes are always available: at worst, latency will be impacted.
