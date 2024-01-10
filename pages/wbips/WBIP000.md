# WBIP000 — WBIP Intro

`draft`

## What is a WBIP?

WBIP stands for WebBtc Improvement Proposal and is inspired by other improvement proposal initiatives (e.g. BIPs, NIPs). Rather than adding a new standard and convention—adding to the burden of choice—WBIPs aim to build upon the WebBTC protocol.

_This WBIP and following WBIPs SHOULD use RFC-2119 language for accuracy._

## Motivation

The motivation behind the WBIPs primarily stems from a need to standardize and improve the functionality of Bitcoin wallet APIs, making them more accessible and easier to use for developers. This initiative aims to provide a unified interface for Bitcoin and various layer 2 solutions. The overarching goal is not only to reduce redundancy and the complexities prevalent with the existing solutions but also to provide a flexible foundation that can easily integrate new use-cases.
The motivation for WBIPs comes after the wake of Ordinal theory allowing inscriptions to the Bitcoin chain. This has encouraged more developers to build on Ordinals and Bitcoin, which led to many new different APIs and protocols. The wide variety can make it cumbersome for developers to work with everything. The improvement proposal approach is meant to make building in the web-enabled Bitcoin ecosystem more user-friendly and democratic.

## Why not CAIP?

Adding proposals as CAIPs (Chain Agnostic Improvement Proposals) was discussed, but was found to potentially complicate the developers workflow and experience. Rather, WBIPs are designed for simplicity and adaptability, inspired by the NIPs (Nostr Implementation Possibilities) of the Nostr community. The proposed approach leans towards shorter, focused improvement proposals. These offer a foundation for future development and can be easily discarded if needed. Without imposing CAIP, the development of Bitcoin-enabled websites becomes more user-driven and straightforward for developers.

## A Good WBIP

An effective WBIP embodies several characteristics:

- **Future-Proof**: The best WBIPs are drafted with an eye towards potential future developments and innovative concepts. They are constructed in a way that allows for simple adaptation and extension in light of upcoming updates and novel ideas.
- **Flexible Rule Set**: The rules specified in a WBIP should not be rigid, but instead allow for modifications as the technological landscape, particularly around privacy, security, and usability, continues to evolve. The acknowledgment that circumstances change and rules may need revision is inherent to the process.
- **Clarity & Conciseness**: An effective WBIP is not a promotional document but a clear and concise blueprint for implementation. It should avoid unnecessary jargon and fluff, focusing instead on providing the essential information in a straightforward manner.
- **Privacy & Security**: WBIPs should err on the side of privacy/security and address potential issues. If in doubt NOT returning information, which might leak information about the user. As privacy is a pivotal aspect in the world of blockchain technology, any potential privacy concerns arising from the implementation of a WBIP should be thoroughly addressed and solutions proposed.
- **Justified Choices**: A well-crafted WBIP does not only prescribe solutions but also provides the reasoning behind the choices made. If multiple approaches or conventions are possible, a strong WBIP will explain why one was selected over the others.
- **Invites Collaboration**: WBIPs should also foster a sense of community and collaboration. Encouraging input from various stakeholders can help to refine and improve the proposals, leading to more robust and widely accepted standards.

> By adhering to these guidelines, WBIPs can serve as effective vehicles for improving and enhancing the WebBTC protocol while ensuring broad acceptance and ease of implementation.

Todo: Motivation

Todo: get inspiration from other IPs
Nostr, bip, caip

## Tags

Tags are used to categorize WBIPs. They are formatted as space-separated words in backticks (markdown code). Tags are the first things listed in a WBIP after the title (markdown H1).

`draft`, `accepted`, `rejected` — WBIPs are tagged with `draft` until they are accepted by the community. Once accepted, they are tagged with `accepted`. If a WBIP is rejected, it is tagged with `rejected`. If these tags are used the WBIP should have some acceptance criteria.

## Fields

An "author" field is optional. If the author or multiple authors are specified, these SHOULD be listed near the top of the WBIP, similar to tags.
