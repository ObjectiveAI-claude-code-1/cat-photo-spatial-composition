# cat-photo-spatial-composition

Evaluates the effective use of surrounding space in a cat photograph. This function reads a single cat photograph and produces a scalar score reflecting how well the space around the cat — the negative space, background, and environment — serves the subject.

## Input

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `cat_photograph` | image | Yes | The cat photograph to evaluate. May range from a carefully composed portrait to a casual snapshot, and may feature any setting or background. |

## Output

A scalar score between 0 and 1.

- **Scores near 1.0** indicate the surrounding space serves the cat excellently — the cat feels prominent without feeling cramped, the environment provides context or atmosphere without overwhelming, and the cat is the clear and undeniable focal point of the image.
- **Scores near 0.5** indicate the surrounding space is adequate but unremarkable — the composition neither excels nor significantly detracts from the cat as subject.
- **Scores near 0.0** indicate the surrounding space works against the cat — the subject is overwhelmed by too much empty space, crowded by careless cropping, or lost among cluttered and competing background elements.

## What It Evaluates

The function assesses three compositional qualities:

### 1. Spatial Proportion

The relationship between the size of the cat and the amount of space that surrounds it. The function detects both extremes:

- **Too little space:** An aggressive crop that carelessly slices through ears, paws, or tail without artistic justification, making the image feel claustrophobic and cramped.
- **Too much space:** A tiny cat lost in an ocean of empty floor, blank wall, or featureless sky, making the subject feel insignificant — like a footnote in its own photograph.
- **Ideal:** The cat feels prominent without feeling cramped. There is enough breathing room for the viewer's eye to settle comfortably, and the environment provides a sense of place without overwhelming the subject. This balance is contextual — a cat in motion may warrant more space than a cat at rest.

### 2. Environmental Cooperation

Whether the background and surrounding elements support the cat as the subject or compete with it for the viewer's attention.

- **Competing environment:** A busy background crowded with objects fragments the viewer's focus, causing the eye to bounce between elements rather than settling on the cat.
- **Cooperating environment:** A clean or softly rendered background cooperates by stepping aside. A richly detailed environment cooperates by directing attention inward toward the cat — foliage that frames the animal, shelves whose lines draw the eye toward the subject, light that falls naturally on the cat.
- **Key principle:** The question is not whether the background is simple or complex, but whether it cooperates. A minimalist background is not automatically better than a detailed one. What matters is whether the surroundings understand their role as supporting context rather than rival subjects.

### 3. Subject Prominence

The cumulative, holistic impression of whether the cat is the undeniable focal point of the photograph. This quality emerges from the interplay of spatial proportion and environmental cooperation.

- **Strong prominence:** The viewer's eye arrives at the cat naturally and stays there willingly. The entire image feels like it exists in service of the cat. Every element of surrounding space quietly affirms the cat as the subject.
- **Weak prominence:** The cat is technically present but does not feel like the point of the image. It may be lost in too much space, buried behind competing elements, or cropped so tightly it feels like a fragment rather than a subject.
- **Key principle:** Prominence is not about size or centering. A cat does not need to fill the frame to feel prominent, nor sit dead center to command attention. Prominence is the sense that the cat is the reason the photograph exists.

## Use Cases

- **Photo contest platforms** — Judge the compositional merit of cat photograph entries by evaluating how well the spatial composition serves the subject.
- **Photographer self-assessment** — Check whether framing instincts are serving the subject well, identifying where spatial balance breaks down.
- **Photography education** — Teach emerging photographers about spatial awareness by scoring their work and surfacing specific compositional strengths and weaknesses.
- **Content curation** — Filter or rank cat photographs by compositional quality when selecting images for publications, social media, or galleries.
- **Automated feedback pipelines** — Integrate into image review workflows to provide structured compositional evaluation at scale.