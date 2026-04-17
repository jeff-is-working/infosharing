---
title: "Meeting brief — Open Government Meeting Knowledge"
purpose: "Talking points for a conversation with a communications specialist / independent government journalist"
audience: "Dual-role contact (comms + indie gov journalism)"
last_updated: 2026-04-17
---

# Open Government Meeting Knowledge — conversation brief

A pipeline that turns public government meeting recordings into a searchable, speaker-attributed knowledge base. Currently running on Thurston County (WA) Board of County Commissioners meetings.

## The problem it solves

Public meetings are technically public, but practically unsearchable. A 3-hour BOCC meeting on YouTube is a black box — you either watch the whole thing or miss it. Journalists and engaged residents end up relying on whatever the county chooses to summarize, which is not adversarial coverage.

## What it actually does

1. Pulls the meeting video from the county's public YouTube channel.
2. Transcribes it with Whisper (90%+ accuracy, runs locally — no audio leaves the machine).
3. Identifies who said what (speaker diarization, handles 14+ distinct voices).
4. Classifies segments by department and topic (15 departments, 12 topic areas).
5. Makes the whole corpus searchable in plain English — "what did Commissioner X say about the quiet zone?" returns the exact moment, with timestamp and video link.

## Why it's different from the usual options

- **Not Granicus / Legistar.** Those are $10K–$50K/year and designed for the agency, not the public watching the agency.
- **Not YouTube auto-captions.** No speaker attribution, no search across meetings, accuracy is poor on procedural language.
- **Not manual note-taking.** Scales to the full meeting record, not just the moments someone thought to watch.
- **Runs locally.** No meeting data sent to OpenAI, Google, or anyone else. Important for agencies; also important for source protection if a journalist feeds their own recordings through it.

## Current state

- Production pipeline processing Thurston County BOCC meetings.
- Searchable archive with semantic search, speaker-scoped queries, and per-meeting knowledge bases.
- Open source (source-available; BSL 1.1 → GPLv2 after 3 years).
- Designed so other counties / cities / school boards are a configuration change, not a rewrite.

## The story angle (for the journalist hat)

- **Replication.** Any county with a YouTube channel is a candidate. What does local accountability journalism look like when the 3-hour meeting is suddenly grep-able?
- **Asymmetry shift.** Right now the agency has the record and the public has the video. This flips that.
- **Open-source civic tech.** Independent, non-vendor tooling. What does that model mean for the long tail of small jurisdictions that will never get a Granicus budget?

## What I'd like from this conversation

**Comms specialist hat:**
- Does the pitch above land in under 60 seconds? Where does it lose a non-technical reader?
- Who should I be talking to first — agencies, journalists, civic orgs? What's the first credible external user look like?

**Journalist hat:**
- Honest read: is this interesting, or is it a tool in search of a story?
- What would make it genuinely useful in your workflow vs. a nice demo?
- Would you want to try it on a meeting you already covered, as a sanity check?

## Things I'm still figuring out (being upfront)

- How the community / free tier gets distributed publicly — not resolved yet, don't want to over-promise a download link.
- Whether the right first partner is a small county, a journalism outlet, or a civic nonprofit.
- What the right "proof it works" demo looks like for someone who isn't already a believer.

## Don't-ramble reminders

- Lead with the problem, not the tech stack.
- One concrete example (the BOCC quiet-zone search) beats five abstract capabilities.
- Stop talking after the ask. Let them react.
