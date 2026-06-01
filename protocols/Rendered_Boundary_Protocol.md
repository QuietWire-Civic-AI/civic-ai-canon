---
title: Rendered Boundary Protocol
subtitle: Visibility, Disclosure, Consent, and the Governance of Shared Information
date: 2026-06-01
status: Canonical Draft
version: 0.1
folder: protocols
organization: QuietWire
---

# Rendered Boundary Protocol

## Core Principle

**If a thing is rendered, it has crossed the trust boundary.**

A document, image, message, diagram, dataset, slide, recording, or idea that has been displayed to a person or system has already entered a shared environment. It may still be confidential. It may still be governed. It may still carry obligations. But technically and relationally, the message has happened.

A screen is not a vault.

A rendered document can be copied, photographed, memorized, summarized, transcribed, pasted, transformed, read aloud, described to another person, or handed to an AI system. “Disable download” and “disable print” may signal intent and add friction, but they do not provide true containment once the content is visible.

The mature response is not panic. The mature response is governance.

## Canon Line

**Rendered is revealed.
Revealed is not automatically released.
Release must be governed.**

## Purpose

This protocol establishes how QuietWire and the Civic AI Canon understand visibility, disclosure, consent, redistribution, AI handling, and provenance.

It recognizes two realities at once:

1. **Technical reality:** If information is rendered to a human, machine, room, or interface, it has already crossed into that trust environment.
2. **Ethical reality:** The ability to copy or transform information does not automatically create the right to redistribute it without care.

QuietWire’s goal is to replace primitive information-security theater with accountable sharing, consent-aware handling, clear provenance, and durable trust.

## The Problem

Many systems pretend that information can be safely shared while still being unshared.

Common examples include:

* view-only documents
* disabled print/download controls
* restricted slide decks
* shared screens in meetings
* “confidential” browser-based portals
* documents shown to contractors or partners
* text visible in group chats
* AI tools used to summarize restricted material
* screenshots of supposedly protected systems

These mechanisms may be useful for signaling policy, reducing accidental spread, or establishing an audit trail. But they should not be confused with meaningful containment once content is displayed.

If the information is sensitive enough that disclosure would cause serious harm, the proper control point is before rendering, not after.

## Definitions

### Rendered

Information is rendered when it becomes perceptible to a person, system, sensor, model, camera, microphone, screen reader, browser extension, clipboard tool, or other observer.

Rendering includes display, audio playback, screen sharing, printing, visual preview, transcription, summarization, and model ingestion.

### Disclosed

Information is disclosed when it enters a trust environment beyond its original holder or system.

Rendering is a form of disclosure.

### Released

Information is released when it is intentionally made available for broader use, distribution, publication, reuse, or transformation beyond the initial disclosure context.

Disclosure and release are related but not identical.

### Trust Circle

The trust circle is the set of people, systems, devices, organizations, rooms, accounts, assistants, and downstream tools reasonably included in the act of sharing.

When a person shares a document in a group, meeting, AI tool, or collaborative workspace, the actual trust circle includes more than the named recipient. It includes the working environment around that recipient.

### Provenance

Provenance is the record of origin, context, transformation, authorship, custody, and handling obligations attached to information.

## Protocol Rules

### 1. Rendered Means Disclosed

Once information has been rendered, it has crossed a boundary.

A person who can see or hear information can usually copy, describe, retain, or transform it. Systems should be designed with that fact in mind.

Do not build governance models that rely on the fantasy that visible information remains technically contained.

### 2. Anti-Copy Controls Are Not Confidentiality Controls

“No print,” “no download,” “view only,” and similar controls are not security boundaries after rendering.

They are friction mechanisms and policy signals. They may be useful, but they should not carry the weight of confidentiality.

For truly sensitive material, use stronger controls before display:

* disclose less
* redact more
* segment access
* watermark copies
* log access
* define recipient obligations
* use clean rooms where appropriate
* avoid rendering the material at all unless necessary

### 3. Visibility Is Not Unlimited Permission

The fact that information can be copied does not mean it may be freely redistributed.

QuietWire distinguishes:

* **technical access**
* **relational permission**
* **legal permission**
* **ethical permission**
* **canonical permission**

A person may have technical access to content without having authority to publish or circulate it.

### 4. Sharing Includes the Recipient’s Working Environment

When information is shared with a person, it is often also shared with the practical environment in which that person works.

That may include:

* their device
* their browser
* their operating system
* their clipboard
* their note-taking tools
* their AI assistant
* their accessibility tools
* their backup systems
* their nearby collaborators
* their organizational account controls

Responsible sharing requires awareness of this environment.

If a sender does not want a recipient using common tools of thought, memory, transformation, or collaboration, that restriction should be explicit before disclosure.

### 5. AI Handling Is Disclosure

Showing information to an AI system is a disclosure to that system and its operating environment.

QuietWire recognizes that AI systems can be legitimate tools for reading, summarizing, translating, organizing, classifying, transforming, and preserving information. But AI handling should be governed.

Before placing restricted material into an AI system, consider:

* Is the user authorized to process the material this way?
* Is the AI environment enterprise, consumer, local, or public?
* Is the content retained?
* Is it used for training?
* Is it subject to organizational policy?
* Is the output safe to redistribute?
* Does the output preserve source context and limits?

### 6. Default QuietWire Posture: Share Forward, Govern Clearly

QuietWire’s default posture is that ideas are meant to travel.

When QuietWire shares its own ideas, documents, protocols, and strategic frames, the usual intent is for trusted recipients to use them, transform them, discuss them, improve them, and carry them forward.

That does not mean every document is public. It means the default cultural posture is not hoarding. The default posture is propagation with provenance.

The work should move.

### 7. Mark Exceptions Explicitly

If information is not meant to travel, say so.

Restricted materials should be clearly marked with handling expectations, such as:

* private
* internal only
* confidential
* not for redistribution
* not for AI processing
* excerpt only
* anonymize before use
* do not forward
* source-sensitive
* embargoed
* client-restricted
* consent required before reuse

A restriction that is not expressed before or at disclosure should not be assumed to be technically enforceable after rendering.

### 8. Use Accountable Copies Instead of Imaginary Locked Copies

For important documents, use accountability rather than illusion.

Useful practices include:

* version numbers
* dates
* authorship
* canonical file paths
* watermarks
* recipient labels
* source notes
* access logs
* transformation notes
* public/private status markers
* expiry or review dates
* retained original copies
* clear redistribution terms

The goal is not to pretend copies cannot exist. The goal is to know what each copy is, where it came from, and what obligations travel with it.

### 9. Preserve Provenance During Transformation

When content is summarized, rewritten, translated, converted, pasted into a new document, or turned into a PDF, its provenance should be preserved where appropriate.

A transformed artifact should retain:

* original source or origin
* date of transformation
* transformer or steward
* purpose of transformation
* known restrictions
* whether it is exact, excerpted, summarized, interpreted, or adapted

This protects both trust and utility.

### 10. Do Not Confuse Openness With Carelessness

QuietWire favors movement, sharing, and practical transformation. That is not the same as recklessness.

The protocol rejects two weak postures:

* the childish security posture that believes a visible screen can remain truly contained
* the pirate posture that says anything visible is free to exploit without regard for consent or context

Canon requires the harder middle path:

**See clearly. Share deliberately. Attribute honestly. Govern what matters. Keep moving.**

## Practical Handling Classes

### Public Canon

Material intended for open publication, GitHub, website use, social sharing, or broad circulation.

Handling:

* may be copied and transformed
* provenance should remain attached
* improvements should flow back where useful
* attribution should be preserved where appropriate

### QuietWire Internal

Material intended for QuietWire collaborators, operational planning, drafts, and internal coordination.

Handling:

* may be used by trusted collaborators
* may be processed with approved AI tools
* should not be externally published without review
* provenance and status should be preserved

### Client / Partner Shared

Material received from or prepared for a client, partner, funder, government entity, or collaborator.

Handling:

* use within the agreed purpose
* preserve source and context
* avoid unnecessary redistribution
* ask before external publication
* AI handling depends on sensitivity and applicable agreement

### Restricted / Sensitive

Material that could cause harm, breach trust, violate law, expose personal information, or damage an organization if mishandled.

Handling:

* minimize rendering
* avoid unnecessary copying
* redact before transformation
* use approved systems only
* log handling where appropriate
* do not use public AI systems
* do not redistribute without explicit authority

## QuietWire AI Use Rule

When a QuietWire steward uses AI to process shared material, the steward should ask:

1. Do I have legitimate access to this material?
2. Would the sender reasonably expect me to use thinking tools to understand it?
3. Is this AI environment appropriate for the material?
4. Will the output expose anything that should remain bounded?
5. Have I preserved the source context?
6. Am I creating clarity, or laundering restricted content into an uncontrolled artifact?

If the answers are sound, AI use may be appropriate.

If the answers are unclear, reduce, redact, summarize at a higher level, or ask for permission.

## Screen Sharing Rule

A live screen share is a disclosure event.

Before sharing a screen, assume participants may:

* see the content
* remember the content
* screenshot the content
* record the content
* summarize the content
* ask an AI assistant to process the content
* discuss the content later

Share accordingly.

## Canon Application

In the Civic AI Canon and QuietWire work, many ideas are intentionally memetic. They are meant to spread, mutate, attach to new contexts, and improve through use.

For this class of work, the proper protection is not secrecy. The proper protection is:

* strong authorship
* durable provenance
* public timestamps
* canonical repositories
* clear licensing where appropriate
* repeated articulation
* active stewardship
* fast forward motion

The best defense for a living idea is not always containment. Often it is healthier propagation with visible origin.

## Key Aphorisms

**A screen is not a vault.**

**Rendered is revealed.**

**Revealed is not automatically released.**

**Release must be governed.**

**Friction is not confidentiality.**

**Provenance is stronger than pretending copies do not exist.**

**If sharing has happened, govern the consequences honestly.**

**For Canon work, let the idea travel with its lineage intact.**

## Closing Statement

The Rendered Boundary Protocol accepts the real nature of digital disclosure.

Once information is rendered, the trust boundary has already been crossed. From that moment, the task is not to pretend the message has not happened. The task is to govern what happens next.

QuietWire chooses clarity over illusion, provenance over false containment, consent over careless extraction, and forward motion over fear.

The work should move.

The lineage should remain visible.

The trust should be worthy of the sharing.
