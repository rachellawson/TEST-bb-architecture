# 5 Cross-Cutting Requirements

Building blocks are responsible for meeting all cross-cutting requirements or specifying why specific requirements do not apply. Govstack compliance and certification processes will validate these requirements.

## 5.1 APIs MUST Return a Response within 60 Seconds

## 5.2 MUST follow TM Forum Specification REST API Design Guidelines Part 1 <a href="#_wyofs1ddrlgk" id="_wyofs1ddrlgk"></a>

See: [https://drive.google.com/file/d/1lpl1IzLGzvbXALW4jqDxLAKqfwuJyeXy/view?usp=sharing](https://drive.google.com/file/d/1lpl1IzLGzvbXALW4jqDxLAKqfwuJyeXy/view?usp=sharing)

## 5.3 SHOULD follow TM Forum Specification REST API Design Guidelines Parts 2-7 <a href="#_19suuzwtdje" id="_19suuzwtdje"></a>

See [https://drive.google.com/drive/u/2/folders/1eS20wt\_PP7CoJEOvzagYDTTMCfmv3y6l](https://drive.google.com/drive/u/2/folders/1eS20wt\_PP7CoJEOvzagYDTTMCfmv3y6l)

## 5.4 EOL MUST be at Least 5 Years <a href="#_fo8til974qj2" id="_fo8til974qj2"></a>

Nothing SHALL be used in a block that has an EOL of less than 5 years.&#x20;

## 5.5 MUST Only Use TIOBE Top 25 Languages

See [https://www.tiobe.com/tiobe-index/](https://www.tiobe.com/tiobe-index/)

Should it avoid languages promoted by individual companies?

## 5.6 MUST Use API-only Based Decoupling <a href="#_8vqx9ylj3l5" id="_8vqx9ylj3l5"></a>

## 5.7 SHOULD Follow the Amazon API Mandate&#x20;

See https://api-university.com/blog/the-api-mandate/

1. All teams will henceforth expose their data and functionality through service interfaces.&#x20;
2. Teams must communicate with each other through these interfaces.&#x20;
3. There will be no other form of interprocess communication allowed: no direct linking, no direct reads of another team’s data store, no shared-memory model, no back-doors whatsoever. The only communication allowed is via service interface calls over the network.&#x20;
4. It doesn’t matter what technology is used \[ed: internally]. HTTP, Corba, Pubsub, custom protocols — doesn’t matter.&#x20;
5. All service interfaces, without exception, must be designed from the ground up to be externalizable. That is to say, the team must plan and design to be able to expose the interface to developers in the outside world. No exceptions.&#x20;
6. Anyone who doesn’t do this will be fired. Is this enforcable?

## 5.8 APIs MUST be Idempotent&#x20;

Paraphrased from Wikipedia: APIs can be called multiple times without changing the result beyond the initial application.

## 5.9 Stateless APIs SHOULD be Used Wherever Possible to Enhance Scalability

## 5.10 Regular Security and Code Quality Audits MUST be Run&#x20;

Thse should be run across the code base and dependencies, e.g. [https://www.sonarqube.org/](https://www.sonarqube.org) and/or [https://snyk.io/](https://snyk.io) .

## 5.11 MUST Include Integration Test Coverage&#x20;

## 5.12 MUST Include Support for a Log Sink&#x20;

## 5.13 Data Models MUST Include Version Numbers

## 5.14 APIs MUST be Versioned&#x20;

As shown here: e.g. /api/v1 and /api/v2&#x20;

## 5.15 API Calls MUST Include Transaction/Trace/Correlation IDs&#x20;

## 5.16 MUST Use Semantic Versioning See https://semver.org/

## 5.17 MUST Provide Configuration Only through the Environment&#x20;

No configuration in code, use environment variables wherever possible&#x20;

## 5.18 MUST Include Clearly-Defined Key Rotation Policies&#x20;

Some blocks may require the use of security keys. Those that do must have clearly defined key rotation policies to enhance security

## 5.19 Documentation MUST be Generated from Code and/or Checked in Alongside Source Code

## 5.20 MUST Not Use Shared Database/Filesystem/Memory interconnection uses APIs only

## 5.21 Databases MUST Not Include Business Logic&#x20;

This means no triggers/stored procedures shall be used.

## 5.22 MUST Enforce Transport Security&#x20;

HTTPS with TLS 1.3 and insecure cyphers disabled.&#x20;

## 5.23 MUST Only Use Unicode for Text&#x20;

## 5.24 MUST Use ISO8601/UTC for Timestamps

## 5.25 MUST Follow REST Design Principles&#x20;

MUST not include PII/session keys in URLs - use POST or other methods for this&#x20;

MUST support caching/retries&#x20;

* Resource identification in requests Individual resources are identified in requests, for example using [URIs ](https://en.wikipedia.org/wiki/Uniform\_resource\_identifier)in RESTful Web services. The resources themselves are conceptually separate from the representations that are returned to the client. For example, the server could send data from its database as [HTML](https://en.wikipedia.org/wiki/HTML), [XML ](https://en.wikipedia.org/wiki/XML)or as [JSON](https://en.wikipedia.org/wiki/JSON)—none of which are the server's internal representation.&#x20;
* Resource manipulation through representations When a client holds a representation of a resource, including any [metadata ](https://en.wikipedia.org/wiki/Metadata)attached, it has enough information to modify or delete the resource's state.&#x20;
* Self-descriptive messages Each message includes enough information to describe how to process the message. For example, which parser to invoke can be specified by a [media type](https://en.wikipedia.org/wiki/Media\_type).&#x20;

See https://en.wikipedia.org/wiki/Representational\_state\_transfer for more.

## 5.26 MUST be Asynchronous First&#x20;

* When entities change, they publish events, allowing loosely-coupled solutions to be assembled without changing existing APIs. \
  Supports occasional connectivity/low bandwidth&#x20;

## 5.27 MUST Support Both SAAS and Do-It-Yourself&#x20;

* Many new governments prefer cloud-based deployments&#x20;
* SAAS is preferred to make it easy for companies to provide new services
* Anyone should be able to test/deploy building blocks by themselves&#x20;

## 5.28 MUST be Autonomous&#x20;

Each block must be capable of running independently.&#x20;

## 5.29 MUST be Open-source Only with No Vendor Lock-in&#x20;

Each block must be composed of open-source software unless there are no alternatives.

## 5.30 MUST be Cloud Native&#x20;

* Each block MUST be ready to be deployed as independent Docker images, with complete source code and build instructions committed to GitHub.&#x20;
* A block may be composed with Kubernetes or docker compose. All build files must be included alongside the source code.&#x20;

## 5.31 MUST Closely Model the Organization/Roles Being Automated&#x20;

See [https://en.wikipedia.org/wiki/Conway%27s\_law](https://en.wikipedia.org/wiki/Conway's\_law)

5.32 MUST Use Standardized Configuration&#x20;

* Configuration MUST only happen through environment variables or secrets&#x20;
* Allows visual construction of blocks, perhaps with domain modeling tools&#x20;

5.33 MUST Use Standardized Data Formats for Interchange&#x20;

JSON is used for data models/services. See [https://www.json.org/json-en.html](https://www.json.org/json-en.html)

## 5.34 MUST Use Existing Standards for Data Interchange, Where Available&#x20;

If an existing standard is available, it should be used, e.g. DICOM/Hl7/FHIR for healthcare. TMForum has a large library of standardized APIs and data models that can be used.

## 5.35 I/O Sanitization MUST be Used&#x20;

* See an example [https://json-schema.org/ ](https://json-schema.org)for JSON data.&#x20;
* Follows Postel’s law: be liberal in what you consume but strict in what you emit

## 5.36 MUST Include Machine-Readable API descriptions&#x20;

* Each block’s service APIs are defined using a standardized machine-readable language. External APIs are described using the OpenAPI 3.0 specification for APIs: [https://swagger.io/docs/specification/about/](https://swagger.io/docs/specification/about/)

## 5.37 MUST Provide a Compliance Test Kit&#x20;

Must provide a runnable [https://www.postman.com/](https://www.postman.com) to ensure compliance&#x20;

Part of building block design

## 5.38 MUST Use Web Hooks for Callbacks

## 5.39 MUST be Internationalizable

## 5.40 MUST Follow Best Practices for Public Code&#x20;

See [https://standard.publiccode.net/](https://standard.publiccode.net) and practices outlined here:&#x20;

* [Code in the Open](https://standard.publiccode.net/criteria/code-in-the-open.html)&#x20;
* [Bundle Policy and Source Code ](https://standard.publiccode.net/criteria/bundle-policy-and-code.html)
* [Create Reusable and Portable Code ](https://standard.publiccode.net/criteria/reusable-and-portable-codebases.html)
* [Welcome Contributions](https://standard.publiccode.net/criteria/open-to-contributions.html)&#x20;
* [Maintain Version Control ](https://standard.publiccode.net/criteria/version-control-and-history.html)
* [Require Review of Contributions  ](https://standard.publiccode.net/criteria/require-review.html)
* [Document Your Objectives ](https://standard.publiccode.net/criteria/document-objectives.html)
* [Document your code ](https://standard.publiccode.net/criteria/documenting.html)
* [Use plain English ](https://standard.publiccode.net/criteria/understandable-english-first.html)
* [Use open standards](https://standard.publiccode.net/criteria/open-standards.html)&#x20;
* [Use continuous integration ](https://standard.publiccode.net/criteria/continuous-integration.html)
* [Publish with an open license ](https://standard.publiccode.net/criteria/open-licenses.html)
* [Use a coherent style ](https://standard.publiccode.net/criteria/style.html)
* [Pay attention to codebase maturity](https://standard.publiccode.net/criteria/advertise-maturity.html)

## 5.41 MUST Follow Strict Requirements Around NTP/RTC Synchronization&#x20;

## 5.42 If an API Response will Take Longer than 5 Seconds, you SHOULD Return a Ticket with a Suggested Callback Time that is Resolved by Polling

## 5.43 MUST use STDOUT/ERR for Logging, to be Captured by the Docker/Container Environment&#x20;

* Each block MUST be ready to be deployed as independent Docker images, with complete source code and build instructions committed to GitHub&#x20;
* A block may be composed with Kubernetes or docker compose. All build files must be included alongside the source code.

## 5.44 SHOULD Include Kubernetes or Ansible Scripts&#x20;

In addition to Docker Compose for more efficient and scalable deployments. This will make individual components of the building block independently scalable and make building blocks less monolithic and more efficient,&#x20;

## 5.45 SHOULD Comply with GDPR Principles&#x20;

Include the right to be forgotten account deletion), privacy requirements to protect the rights of individuals, etc. Note that these requirements may vary by region.

## 5.46 MUST Implement Existing Standards Where Possible&#x20;

Building blocks and building block solutions MUST leverage existing standards, especially those listed in the Standards section below.
