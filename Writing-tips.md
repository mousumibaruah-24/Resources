William Strunk's [Elements of Style](https://www.gutenberg.org/files/37134/37134-h/37134-h.htm) provides few key rules of writing clearly. See list below, and the hyperlinked text for details and examples. I would also add more to the list: write persuasively. 

> 8. Make the paragraph the unit of composition: one paragraph to each topic
> 9. As a rule, begin each paragraph with a topic sentence; end it in conformity with the beginning
> 10. Use the active voice
> 11. Put statements in positive form
> 12. Use definite, specific, concrete language
> 13. Omit needless words
> 14. Avoid a succession of loose sentences
> 15. Express co-ordinate ideas in similar form
> 16. Keep related words together
> 17. In summaries, keep to one tense
> 18. Place the emphatic words of a sentence at the end

## More tips (via GPT4)

* Plan Before You Write: Outline your main points to avoid meandering.
* Avoid Redundancies: For example, instead of "advance planning," just say "planning."
* Eliminate Filler Words: Words like "actually," "really," and "very" often don’t add value and can be omitted.
* Break Up Long Sentences: Aim for clarity. If a sentence seems too long, it probably can be broken into two or more sentences.
* Edit Ruthlessly: Once done, review your work and remove any unnecessary information.
* Choose Specific Words: E.g., instead of "a lot of people," say "75% of participants."
* Be Explicit: Make sure there's no ambiguity. If giving instructions or asking a question, be as clear as possible.
* Use Examples: They can illuminate a point and provide clarity.
* Stay On Topic: Ensure every sentence and paragraph relates back to your main point. Send separate emails for different themes/topics.
* Proofread: Mistakes can undermine your credibility and confuse readers. Make sure to review your work for clarity and accuracy.

## Examples:

* Questions should be clear and well defined. From Strunk: "Prefer the specific to the general, the definite to the vague, the concrete to the abstract."

Before: I am trying to match block names in dataset 1 with the those in dataset 2. 2501 got matched however 2477 are 100% matched and the rest 24 are 66% match using reclink. Any suggestions how to move ahead from here?

After: I am trying to match block names in dataset 1 with the those in dataset 2. There are XX unique blocks in dataset 1 and XX in dataset 2. I used -reclink- for fuzzy matching. I matched 1:1 on scode, dcode and bname. This leads to XX matched obs, leaving XX% unmatched. How should I proceed with matching the remaining XX unmatched blocks?

* Summaries should provide a succinct; attention is limited so you must condense info to focus only on the key highlights. From Strunk: "Vigorous writing is concise. A sentence should contain no unnecessary words, a paragraph no unnecessary sentences, for the same reason that a drawing should have no unnecessary lines and a machine no unnecessary parts."

Before: The eSewa portal serves as a vital interface, offering an integrated and seamless delivery of more than 400 citizen services including birth-death certificates, caste certificates, arms license registration by district administration. However, the absence of an option to update the mobile numbers within the ‘Update Profile’ section hinders and affects actors’ efficiency of service delivery. This brief document recommends the inclusion of a mobile number update feature to address these concerns.

After: The eSewa portal is a crucial interface that simplifies delivery of citizen services in Punjab. Currently, however, there is no option for the portal’s users (interchangeably referred to as “actors”) to update their mobile numbers. This limitation impacts the efficiency of the portal’s use and monitoring, as stale mobile numbers lead to inaccurate contact information preventing quick follow-up. It's imperative to take the necessary back-end measures to enable this feature enhancement.

* Blockers should be self-contained and provide all the necessary info to make an informed decision. 

Before: Uncertain about q19_assuredirrigatedland, as it represents total irrigated land (referencing the already written STATA/R code) and not assured irrigated land only. Also, in doubt about calculating total irrigated land following to earlier with q19_20_irrigated.

After: Can we be certain that q19_assuredirrigatedland refers to total irrigated land? I am confused because the name of the variable in the data is "totalirrigated". For context, there are three variables in the dataset: totalunirrigated, totalirrigated and otherirrigated. We also have three related questions in the survey: q18 total unirrigaged land; q19 with assured irrigation for two crops; q20 other irrigated land. Note: q19 and q20 are grouped under "total irrigated land". My question, therefore, is does totalirrigated refer to q19 + q20 or just q19 (or perhaps something else)? I am assuming totalunirrigated corresponds to q18 and otherirrigated corresponds to q20.

* Another example 

Before: Require clarification on defining labels for q16_ownvehicle, which has 5 sublevels ranging from 1-5, while the SECC questionnaire only has 2 sublevels (Yes or No).

After: I noticed that q16 has 5 values in the data, but in the questionnaire this is just a Yes/No question. Tabulating q16, I find that the values and their corresponding percentages are: val1 xx%, val2 xx% ... val5 xx% We can see that the values that most closely align with the options in the survey questionnaire are value X and value X. These account for XX% of the data, leaving YY% of the data assigned to values not in the questionnaire. How should I treat these YY% of the data?

