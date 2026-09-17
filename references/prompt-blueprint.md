# Prompt Construction Blueprint

## Input Defaults

Infer missing choices conservatively:

- Platform: generic image-to-video prompt compatible with Grok.
- Aspect ratio: follow the source image; use 9:16 for portrait marketing content when unspecified.
- Voice: young adult female Mandarin.
- Audio: no music; quiet synchronized process and laboratory Foley.
- Subtitles: Simplified Chinese, bottom safe area, white with a thin dark outline, synchronized phrase by phrase.
- Product selection: one clearest foreground/central luminaire.

Ask a question only when a missing choice would materially change the result and cannot be inferred from the image or conversation.

## Semantic Storyboarding

Map the copy clause by clause, not keyword by keyword. One dominant visual per claim is usually enough.

1. Product identification → immediate potting or a product macro that includes real potting.
2. Material property → standardized specimen test or close-up physical behavior.
3. Environmental protection → assembled-luminaire lab test.
4. Call to action → completed, illuminated product hero shot.

Do not add unrelated tests simply because they are available. If the script says waterproof and damp-proof, show a water-jet scene and a controlled humidity scene. If it says elongation, show a tensile specimen rather than a water test.

## Duration and Speech

Keep the supplied copy exact. Estimate whether it can be spoken clearly, then distribute phrases so the final word lands near the end.

- Start narration around 0.1 seconds.
- End the last word around duration minus 0.1 seconds.
- Use short natural breath pauses between clauses.
- Never instruct the model merely to “finish within” the duration; that often causes rushed speech. State that the narration should occupy almost the whole video and provide approximate phrase windows when pacing has previously failed.
- If the copy is clearly too long, say so briefly and offer a shorter alternative, but still provide the requested prompt unless the user asks for rewriting only.

Suggested visual density:

- 6 seconds: 2–3 major visual beats.
- 10 seconds: 4–5 major visual beats.
- 15 seconds: 5–7 major visual beats with longer material behavior or test shots.

Prefer movement within a shot over unnecessary cuts. Use match cuts, highlight wipes, object-shape transitions, and focus pulls to preserve continuity.

## Opening Graphics

When the user wants an opening technology graphic:

- Overlay it on active potting rather than delaying the action.
- Use the product name plus no more than three concise benefits.
- Use restrained cyan/white translucent lines, scanning arcs, tracking points, and small particles.
- Keep it in the upper or middle safe area, away from the dispensing action and bottom subtitles.
- Fade it cleanly at the requested time. Do not let it reappear.

## Complete Prompt Order

Write the final prompt in this order:

1. Format, duration, aspect ratio, genre.
2. Reference-image identity lock and one-target rule.
3. Exact voice-over, pronunciation, start/end timing, and phrase pacing.
4. First-frame action and opening graphic.
5. Claim-aligned scenes in narration order.
6. Camera motion and transitions.
7. Subtitles and sound.
8. Negative constraints targeted to likely failures.
9. Highest-priority summary.

The prompt should be self-contained. Do not tell the user to splice separate fragments together.

## Negative Constraints Worth Reusing

Select only those relevant to the current prompt:

- no product redesign, changing LED count, moving screws, or changing tray geometry;
- no simultaneous filling of multiple trays;
- no filling a detached cover;
- no localized blob when the cavity must be fully filled;
- no overflow beyond seals or cavity walls;
- no bubbles, milkiness, yellow tint, water-like splashing, or impossible flow;
- no cured-layer stringing, slime, tall peaks, or adhesion to a hand;
- no invented certifications, values, report numbers, or pass marks;
- no male voice, music, subtitle errors, random logos, QR codes, or watermarks;
- no rushed narration or silent tail when the user wants speech to end with the video.

## Revision Rule

Every user correction produces a new full prompt with all earlier accepted requirements preserved. Do not answer with only the changed paragraph.
