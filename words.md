# Words

How Agama writes its text, from button labels to error messages, and where
the rules come from. It applies [the principles](principles.md), above all
[plain words, in every language](principles.md#7-plain-words-in-every-language).

## At a glance

- [Sources](#sources): the SUSE style guide first, then the Inclusive Naming
  Initiative, then PatternFly, and Agama's own rules on top.
- [Inclusive language](#inclusive-language): a term that excludes or
  distracts is replaced by one that says what happens.
- [Example: "abort"](#example-abort): why Agama never uses it, and what it
  says instead.
- [Agama's own rules](#agamas-own-rules): buttons say what they do, reports
  what will happen, links where they go, all in plain words that translate
  well.

## Sources

When a wording question comes up, look for the answer in this order:

1. **The [SUSE Documentation Style Guide][suse-style]** for language:
   spelling, capitalization, terminology and inclusive language.
2. **The Inclusive Naming Initiative's [evaluation framework][ini-framework]**
   for any term the SUSE guide does not cover. The guide itself sends
   readers there.
3. **PatternFly's [content design guidelines][pf-content]** for UI text the
   SUSE guide does not cover, such as button labels or empty states.
4. **[Agama's own rules](#agamas-own-rules)** on top, kept to what is
   specific to an installer.

*Why:* SUSE has worked on how its products speak for many years, and it
already covers SUSE software: it asks for sentence case in it, as Agama does.
Following it saves the team from settling the same questions again, and
keeps Agama reading like the rest of SUSE.

## Inclusive language

Replace a term that is charged outside technology, needlessly violent, or
less clear than a plain word, as the [evaluation framework][ini-framework]
asks. A term that fails the first test is replaced, whatever else speaks for
it. The initiative's [word lists][ini-lists] record the terms already
evaluated.

*Why:* the right word costs nothing, and the wrong one pushes people away
from a tool they are about to trust with their machine.

## Example: "abort"

The initiative lists [abort][ini-abort] among the terms to replace: its
meaning outside technology is direct and charged, and it adds no clarity a
plainer word lacks. So Agama names what actually happens instead:

| Situation | Say | Not |
| --- | --- | --- |
| The user stops something they started | Cancel | Abort |
| Something is running and can be stopped | Stop | Abort, Kill |
| The installation cannot go on | Installation failed | Installation aborted |
| The outcome of the user stopping it | Canceled by user, Interrupted by user | Aborted by user |
| Leaving a dialog without doing anything | Close | Abort |

"Kill" is no replacement either: the initiative lists it as unsuitable.

## Agama's own rules

- **Short labels inside a form, full ones on their own.** "Name", not
  "Connection name", inside a connection form. Breadcrumbs, links and row
  buttons name their object: "Edit connection", "Configure sda".
- **Controls instruct, reports describe:** "Delete" on the button, "To be
  deleted" in the report, never worded as already done. Each act has one verb
  and one noun everywhere ("actions", never "changes").
- **A link is named after where it goes,** not after what it reports: "Go to
  storage settings" on an alert about storage, not "Invalid settings". Danger
  color goes on the statement, not on the link.
- **A control that shows more names what it shows:** "Show technical
  details", "Show 3 subvolume actions". Avoid a bare "Show more" wherever
  possible: a screen reader user moving from control to control hears it
  with no context, and can't tell several of them apart.
- **Every place a sentence names is a link to it,** like "Uses" and "Used by"
  between devices.
- **Repeat only when it helps:** to keep the user oriented (a side panel
  repeats the name of its row), to spare remembering (a summary in the list,
  the details in the panel), or for a different task. Repetition hurts when
  it adds noise, shows one action twice, can drift out of sync, or makes a
  screen reader say the same thing twice. No intro paragraph restates the
  table below it.
- **Error messages say what is wrong with that field,** next to it, and are
  tied to it so a screen reader reads them with the field. "Required" and
  "wrong format" are different messages, and a format error shows an example
  ("e.g. 20 GiB"). The label, the help and the errors use the same word.
- **A control's accessible name includes its visible label, word for word,**
  so voice control finds it by what the user sees. Added context, such as
  "Hostname" in "Hostname mode", goes around the label, never in place of
  it.
- **Plain words, not symbols or internals.** "At least 5 GiB", not "≥". No
  internal names ("space policy"). Outcomes rather than mechanisms. Never
  "the control below".
- **Text in another language is marked with its language,** such as each
  entry in the language list.
- **Sentence case.** Whole sentences, never stitched together from pieces.
- **Titles don't end in a period.** Headings, dialog titles and alert titles
  alike. A question mark stays when it matters.
- **A note for translators on every string:** what it is, and where it shows
  up.
- **A string freeze is never dodged by reusing a string from another
  context.** A string is reused only where it means the same thing in the
  same place. New text waits, tracked as a follow-up, and strings that will be
  needed are reserved early.

*Standards:* WCAG [1.3.3], [2.4.4], [2.5.3], [3.1.2], [3.3.1], [3.3.3];
SUSE style guide [Biases and inclusiveness][suse-bias],
[Capitalization of headings and titles][suse-capitalization] and
[User interface items][suse-ui]; PatternFly [Punctuation][pf-punctuation].
See also Sara Soueidan on [text labels][ss-labels].

[1.3.3]: https://www.w3.org/WAI/WCAG22/Understanding/sensory-characteristics.html "Sensory Characteristics"
[2.4.4]: https://www.w3.org/WAI/WCAG22/Understanding/link-purpose-in-context.html "Link Purpose (In Context)"
[2.5.3]: https://www.w3.org/WAI/WCAG22/Understanding/label-in-name.html "Label in Name"
[3.1.2]: https://www.w3.org/WAI/WCAG22/Understanding/language-of-parts.html "Language of Parts"
[3.3.1]: https://www.w3.org/WAI/WCAG22/Understanding/error-identification.html "Error Identification"
[3.3.3]: https://www.w3.org/WAI/WCAG22/Understanding/error-suggestion.html "Error Suggestion"
[ini-abort]: https://inclusivenaming.org/word-lists/tier-1/abort/ "Inclusive Naming Initiative: abort"
[ini-framework]: https://inclusivenaming.org/handbook/evaluation-framework/ "Inclusive Naming Initiative: Evaluation framework"
[ini-lists]: https://inclusivenaming.org/word-lists/ "Inclusive Naming Initiative: Word lists"
[pf-content]: https://www.patternfly.org/content-design/overview "PatternFly content design"
[pf-punctuation]: https://www.patternfly.org/content-design/grammar/punctuation "PatternFly Punctuation"
[ss-labels]: https://www.sarasoueidan.com/blog/accessible-text-labels/ "Accessible Text Labels For All"
[suse-bias]: https://documentation.suse.com/style/current/html/style-guide-db/sec-language.html#sec-bias "SUSE Documentation Style Guide: Biases and inclusiveness"
[suse-capitalization]: https://documentation.suse.com/style/current/html/style-guide-db/sec-language.html#sec-capitalization "SUSE Documentation Style Guide: Capitalization of headings and titles"
[suse-style]: https://documentation.suse.com/style/current/html/style-guide-db/index.html "SUSE Documentation Style Guide"
[suse-ui]: https://documentation.suse.com/style/current/html/style-guide-db/sec-language.html#sec-ui-item-language "SUSE Documentation Style Guide: User interface items"
