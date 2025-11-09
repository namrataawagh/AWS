# AWS
# Introduction to Cloud — Notes

> Source: Udemy lecture transcripts (introductory cloud computing)

---

## 1. Course intro

* This section is theory-focused — it explains **why the cloud is useful** and gives context before hands‑on work.
* Goal: understand traditional IT, how websites work, what servers contain, and why organizations moved to the cloud.

## 2. How websites work (high level)

* A website is served by a **server** hosted somewhere on the Internet.
* The **client** (web browser) and the server exchange data over a **network**.
* Communication uses **IP addresses** so each endpoint can send and receive data (analogy: postal mail with addresses).

## 3. What’s inside a server

* **Compute (CPU)**: performs calculations and runs code — like the brain performing computations.
* **Memory (RAM)**: very fast storage for temporary data and execution state.
* **Storage**: long‑term disk storage for files and persistent data.
* **Database**: structured storage that enables efficient querying.
* **Networking components**: routers, switches, DNS, etc.

These components together enable applications to run and be reachable over the network.

## 4. Traditional on‑premises IT (the old way)

* Early setups: servers in a garage or home → later moved to an office **data center**.
* Problems with this approach:

  * High upfront cost (buying hardware) and capital expenses (CAPEX).
  * Ongoing operational costs: rent, power, cooling, maintenance, staff.
  * Scaling is slow (ordering & installing hardware takes time), limited by space & budget.
  * Need for 24/7 staff for monitoring and repairs.
  * Risk from disasters (power outage, fire, earthquake).

**Key question:** Can we externalize hosting, operations, and maintenance? — **Yes: the cloud.**

## 5. What is Cloud Computing?

* **Definition:** On‑demand delivery of compute power, storage, databases, applications and other IT resources.
* Key ideas:

  * **On‑demand / self‑service:** provision resources when you need them (no long lead times).
  * **Pay‑as‑you‑go:** pay only for what you use; stop paying when you stop using.
  * Cloud providers maintain the physical infrastructure; users provision and consume resources via web consoles or APIs.

### Examples the user may already use:

* Gmail, Dropbox, Google Drive, iCloud, Netflix (streaming) — all are cloud services.

## 6. Cloud deployment models

* **Private Cloud:** Cloud resources dedicated to a single organization (may be managed by a third party). More control and tighter security.
* **Public Cloud:** Resources owned and operated by third‑party providers and delivered over the Internet (e.g., AWS, Azure, Google Cloud).
* **Hybrid Cloud:** Mix of on‑premises/private resources and public cloud — combine control for sensitive data with public cloud flexibility.

## 7. Five essential characteristics of cloud computing

1. **On‑demand, self‑service** — users provision resources without provider intervention.
2. **Broad network access** — available over the network, accessible in multiple ways.
3. **Resource pooling / multi‑tenancy** — physical resources shared among customers while maintaining isolation.
4. **Rapid elasticity / scalability** — automatically acquire or release resources as needed.
5. **Measured service** — usage is monitored, metered, and billed accordingly.

## 8. Six advantages of using cloud computing

1. Convert **CAPEX to OPEX** (rent instead of buy) → lower TCO.
2. **Economies of scale** delivered by large cloud providers reduce costs.
3. **No need to guess capacity** — scale based on real metrics.
4. **Speed & agility** — create, test, and deploy quickly.
5. **Reduced data center overhead** — no need to operate physical facilities.
6. **Global infrastructure available** — build worldwide applications quickly.

**Result:** More flexible, cost‑effective, scalable, elastic, highly available, and faster time‑to‑market.

## 9. Cloud service models (what you manage vs provider manages)

* **On‑premises:** You manage everything (apps, data, runtime, OS, virtualization, hardware, networking).

| Model                                  |                                          You manage | Provider manages                                                      |
| -------------------------------------- | --------------------------------------------------: | --------------------------------------------------------------------- |
| **IaaS (Infrastructure as a Service)** |         Applications, data, runtime, middleware, OS | Virtualization, servers, storage, networking                          |
| **PaaS (Platform as a Service)**       |                                  Applications, data | Runtime, middleware, OS, virtualization, servers, storage, networking |
| **SaaS (Software as a Service)**       | (Typically just user data and application settings) | Everything else — provider runs and manages the full product          |

* **IaaS examples:** Amazon EC2, DigitalOcean, Linode, Rackspace.
* **PaaS examples:** AWS Elastic Beanstalk, Heroku, Google App Engine.
* **SaaS examples:** Gmail, Dropbox, Zoom, and various managed AWS services (Rekognition used as a service).

### Pricing fundamentals (AWS examples)

* **Compute:** pay for actual compute time used.
* **Storage:** pay for the data stored.
* **Networking:** typically pay for data **egress** (data leaving the cloud); ingress often free.

## 10. AWS — short history & relevance

* Internal launch: 2002 (Amazon realized its IT stack could be offered externally).
* First public offering (SQS): 2004; expanded in 2006 with SQS, S3, and EC2.
* AWS is a market leader (Gartner Magic Quadrant leader for many years).
* As of 2023/2024 figures mentioned: large revenue (~$90B in 2023) and significant market share (~31% Q1 2024).
* Many large services run on AWS (Netflix, Dropbox, Airbnb, NASA, etc.).

## 11. AWS global infrastructure (concepts)

* **Regions:** Geographic areas (e.g., `us-east-1`, `eu-west-1`). Each region is isolated and contains multiple Availability Zones (AZs).
* **Availability Zones (AZs):** One or more discrete data centers within a region. AZs are isolated to avoid cascading failures but connected with high‑speed, low‑latency links.

  * Typical region: 3 AZs (minimum 3, can be up to 6 in some regions).
* **Edge locations / Points of Presence (PoPs):** >400 PoPs in many cities—used for content delivery (low latency) via services like CloudFront.

### Choosing a region — factors to consider

* **Compliance / Data residency** (legal requirements to keep data in a country).
* **Latency** (choose region closest to users for lower latency).
* **Service availability** (not all AWS services are available in every region).
* **Pricing differences** across regions.

## 12. AWS Console tips

* Top-right **Region selector**: pick a region close to you for lower latency.
* Services may be **global** (e.g., IAM, Route 53, CloudFront) or **region‑scoped** (e.g., EC2, Lambda; resources appear per selected region).
* **Recently visited services**, account health, cost & usage, and tutorial links are accessible from the Console Home.
* Use the region service availability table (AWS Regional Services) to verify if a service exists in your chosen region.

## 13. Shared Responsibility Model

* **Customer:** Responsible **for security *in* the cloud** — configuration, data, applications, access controls, OS, network/firewall rules.
* **AWS (provider):** Responsible **for security *of* the cloud** — physical infrastructure, hardware, and foundational services security.
* Important for exam questions: identify which side is responsible for what.

## 14. Policies & Acceptable Use

* Using AWS requires agreement to an **Acceptable Use Policy** (no illegal activity, no network abuse, no security violations, no spam/abuse, etc.).

## 15. Summary / Next steps

* The cloud provides on‑demand, scalable, pay‑as‑you‑go computing that solves many problems of traditional IT.
* Key takeaways: know the **service models** (IaaS/PaaS/SaaS), **deployment models** (public/private/hybrid), the **five characteristics**, and **shared responsibility** distinctions.
* Upcoming lectures will dive deeper into cloud types, AWS services, and hands‑on console work.

---

*Study tips:*

* Keep practicing the region/AZ concept and the shared responsibility split — these are common exam topics.
* Familiarize yourself with common services names (EC2, S3, RDS, Lambda) and which are global vs region‑scoped.
* Review the AWS region table when attempting hands‑on labs to ensure the services you need exist in your chosen region.
