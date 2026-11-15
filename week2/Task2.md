Form & List UX Makeover





Level

★

Time box

1 week

Builds on

Your onboarding app (tables, Record Producer, Flow)

LinkedIn format

Before/after image (or a 2-image carousel)

Why this matters

The platform's default forms and lists work, but nobody enjoys them. On real projects clients judge an app in the first ten seconds of looking at a form. Making a form guide the user, by showing the right fields at the right time, explaining what's needed and stopping mistakes early, is the most basic UX skill a ServiceNow developer has.

The brief

Your stakeholders have used your app for a week, and the feedback is: "It works, but the form is overwhelming. I don't know which fields matter, and I keep getting rejected for missing information."

Redesign the forms and lists of your app's main table(s) so that a first-time user can fill them in correctly without help, and a fulfiller can scan a list and see what needs attention.

Requirements

Must have

[ ] Form layout: Fields grouped into logical sections (and tabs if it makes sense). Remove or hide anything a given user doesn't need.

[ ] Dynamic behaviour: At least 3 pieces of dynamic form logic, e.g. fields that appear, become mandatory or become read-only depending on other values.

[ ] Client-side scripting: At least 2 client scripts that do something a UI Policy cannot do on its own, e.g. validate a format, calculate a value, or show a contextual message under a field.

[ ] Server-side enforcement: Your key rules must also be enforced when a record is created or updated without the form (e.g. through a list edit, import or script).

[ ] Guidance: The user is told why something is needed, through field messages, annotations, hints or info messages.

[ ] Lists: The default list view shows the columns a fulfiller actually needs, sorted sensibly, with visual state indicators (e.g. colour or icon by state or priority).

[ ] Related lists: The right related records appear on the form, in a sensible order.

Should have

[ ] Different form views for different personas (requester vs. fulfiller).

[ ] Field labels and choice values rewritten in plain language, with no internal jargon.

[ ] The form also looks right in a Next Experience context (it doesn't have to be perfect yet; you'll come back to this in Week 7).

Stretch

[ ] A UI Action (button) that moves the record to its next logical state, with confirmation and validation.

[ ] Use a Data Policy and explain in your notes when you'd choose it over a Business Rule.

Constraints

Prefer no-code (UI Policies, Data Policies) over client scripts whenever the result is the same. Be ready to justify every script.

No GlideRecord in client scripts. If you need server data on the client, find the correct pattern.

Don't break the Record Producer or Flow from your onboarding task.

Acceptance criteria

[ ] A new user can create a valid record on the first attempt without asking anyone.

[ ] Setting a record into an invalid state is blocked both on the form and server-side.

[ ] Every client script has a clear reason for existing (written in your notes).

[ ] The list view lets a fulfiller pick out the most urgent record in under 5 seconds.

Deliverables

Updated app on your instance.

WEEK1-NOTES.md: a table of every UI Policy and script, what it does, and why you chose that mechanism.

Before and after screenshots: take the "before" ones first, before you change anything.

LinkedIn post.

LinkedIn brief

Format: One before/after composite image, or a 2–3 slide carousel.

Hook ideas: "Same data. Completely different experience." / "Users don't read forms. Here's how I made mine read them instead."

Show: The cluttered "before", the clean "after", and one dynamic behaviour as a short GIF if you can.

Say: One UX principle you applied and one technical thing you learned (e.g. UI Policy vs. Client Script).

Where to look

UI Policies · Client Scripts (onLoad / onChange / onSubmit) · g_form API · GlideAjax · Data Policies · Business Rules (before) · Form Designer · Form sections & views · Field Styles · Annotations · List Layout / List Control · Related Lists

Review questions (Friday)

When would you use a UI Policy instead of a Client Script, and the other way round?

Why isn't client-side validation enough on its own?

How did you get server data into a client script without GlideRecord?

What's the difference between a form section and a form view?

Which change made the biggest difference for users, and how do you know?

