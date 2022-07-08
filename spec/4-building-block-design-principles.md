# 4 Building Block Design Principles

## 4.1 Citizen-Centric

* Right to be forgotten: everything must be deletable
* User-centered design

The best tools evolve from empathizing, understanding and designing for the needs of end-users. Accordingly, we’ve identified a series of use cases and user journeys here: [InfoMed - RFIMPL\_Use Case Journeys.docx](https://docs.google.com/document/d/1zZwTdy1exWWpuIDcEzQ1B7h5Nr1vaF\_g/edit)

Each use case is composed of a collection of modules, or building blocks. As you can see, a relatively small set of these building blocks can be readily applied to a wide variety of applications in low-resource settings.

## 4.2 Open <a href="#_hj7wrge29nf5" id="_hj7wrge29nf5"></a>

* Based on open standards
* Based on Digital Development Principles, see [https://digitalprinciples.org/](https://digitalprinciples.org)  and  [https://digitalinvestmentprinciples.org](https://digitalinvestmentprinciples.org)[/](https://digitalinvestmentprinciples.org)
* Built on open-source software (where possible)
* Supports open development, see [https://standard.publiccode.net/](https://standard.publiccode.net)&#x20;
* No vendor lock-in
* Cloud native (Docker/Docker Compose/OCI containers)
* Code is openly developed and available to anyone, via Github or Gitlab

## 4.3 Sustainable <a href="#_5fv1ildee3ef" id="_5fv1ildee3ef"></a>

* Stewardship is critical, see [https://publiccode.net/codebase-stewardship/](https://publiccode.net/codebase-stewardship/)&#x20;
* Continuous funding for maintenance, development and evolution
* Attractive to ICT industry and individual developers in deployment environment (incentives must be aligned)
* Lower cost than commercial solutions due to shared development costs
* Uses microservices-based architecture instead of monolithic.
  * This increases interoperability, development and deployment speed and reliability.
  * From Wikipedia: a variant of the[ ](https://en.wikipedia.org/wiki/Service-oriented\_architecture)[service-oriented architecture](https://en.wikipedia.org/wiki/Service-oriented\_architecture) (SOA) structural style – arranges an application as a collection of[ ](https://en.wikipedia.org/wiki/Loose\_coupling)[loosely coupled](https://en.wikipedia.org/wiki/Loose\_coupling) services. In a microservices architecture, services are fine-grained and the protocols are lightweight.

## 4.4 Secure <a href="#_1tvbgx5xc0is" id="_1tvbgx5xc0is"></a>

* Blocks are audited and certified before being made available
* Development processes and standards enforce quality and security
* Different certification levels reflect level of standards-compliance
* Regular security scanning and auditing
* Public ratings and reviews
* Comprehensive logging and exception handling

## 4.5 Accessible <a href="#_64y5ys9r1wf3" id="_64y5ys9r1wf3"></a>

* Meets users where they are: web, mobile, SMS and/or voice. UI supports accessibility technologies, e.g. screen readers.
* SSO allows for signing in once for multiple services
* Shared ownership of code
* Deployment and development processes and standards are open to contributors
* Community-driven development tools for documentation and support
* Blueprints, templates and documentation

## 4.6 Flexible <a href="#_ul5nalat80jf" id="_ul5nalat80jf"></a>

* Blocks can be reused in multiple contexts
* Each block is autonomous
  * Blocks are interoperable
  * Easy to set up
* Standardized configuration and communications protocols connecting blocks
* Blocks can be provided as a service (ICT opportunity)

## 4.7 Robust <a href="#_jgyljayvwagf" id="_jgyljayvwagf"></a>

* Operates in low-resource environments:
  * Occasional power&#x20;
  * Low bandwidth
  * Low-reliability connectivity
* Easily scalable for high availability and reliability
* API-only based decoupling
* Asynchronous communications pattern decoupled through rooms is ideal
* Eventual consistency for data

***

Docker has become a bit proprietary. May I suggest that CRIO based container orchestration be adopted as it defines the open standard.

Seems sensible to me!

Or offline based systems.

Digital Registries BB is not working when there is no power. Can we fulfill this requirement with cloud?

As significant of part of population does not have access AT ALL to connectivity, workarounds must be in place when "NO bandwidth"

Can we consider that paper process is  a workaround?

If not enough bandwidth for classical apps, what exists could be leveraged already(ie edge/2G), then offline mode could be also used which means keep using digital solutions but have to move data physically (what’s used in elections, we can call it digital offline). Paper could be used also but it’s not better than digital offline and can be source of errors or fraud.

Digital Registries BB is not working when there is no power. Can we fulfill this requirement with cloud?
