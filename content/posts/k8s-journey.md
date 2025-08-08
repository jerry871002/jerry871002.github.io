---
date: "2025-08-08"
draft: false
title: "From Zero to CKA/CKAD: My Kubernetes Learning Journey"
summary: "From not knowing what a Pod was to passing both the CKAD and CKA exams, this post shares my Kubernetes learning journey and reflections."
toc: true
readTime: true
autonumber: true
---

Two years ago, I didn’t know what a Pod was.

Today, I’m proud to say I’ve passed both the **CKAD (Certified Kubernetes Application Developer)** and the **CKA (Certified Kubernetes Administrator)** exams.

This post is a personal reflection on my journey learning Kubernetes, from the initial confusion and imposter syndrome, to eventually earning two certifications that felt completely out of reach at the beginning.
If you're just getting started with Kubernetes or wondering how to approach learning it, I hope this can give you some perspective (and maybe save you some missteps along the way).

## Where It All Started

Back in early 2023, during my first year at Aalto University, I took a course called *Designing and Building Scalable Web Applications*.
[One of our projects](https://github.com/jerry871002/jodel-like-app) in the course was to deploy a web app that could auto-scale based on load, seemed straightforward enough, right?

Not quite.

Let me set the record straight about where I started.
I wasn't completely new to containers.
I had extensive experience using Docker and Docker Compose back then, so I was familiar with the containerization concept, but I never tried any container orchestration platform.

I remember having no clue what a **Pod** was, let alone more advanced concepts like **Deployment** and **Service**.
I somehow managed to complete the assignment by following tutorials, trial and error, and lots of Googling (ChatGPT wasn't that good back then 🤣).
The project worked and it scaled, but I knew I was just going through the motions without grasping the underlying concepts.
It felt like trying to solve a puzzle blindfolded.

Around the same time, there was another course called *Seminar in Computer Science*, designed to help us practice research and academic writing in preparation for our thesis.
My advisor offered several Kubernetes-related topics for us to explore: service mesh, cluster networking, and more.

I deliberately avoided them.

"That's way too complex," I thought. "I'll spend the whole semester just learning Kubernetes instead of doing actual research."

I remember during our checkpoint sessions, my friend presented his service mesh research, and I had absolutely no idea what he was talking about.
I felt a huge knowledge gap - not only did I not know Kubernetes, but there was this whole ecosystem of concepts I was completely unaware of.

Looking back, this avoidance probably made my later learning journey harder.
But sometimes we need to feel ready before we take the plunge.

## First Hands-On Exposure: Internship at Ericsson

In March 2023, I started my first internship in Finland.
The product I was working on ran entirely on Kubernetes.

No more avoiding it.
I had to learn fast.

I remember one particular incident that perfectly captured my knowledge gap.
I was writing a script that needed to read a secret from the cluster, but it kept failing.
I couldn’t figure out why and spent hours debugging until a kind colleague pointed out I didn’t have the right **Service Account** and **RBAC (Role-Based Access Control) permissions**.

(Yeah, looking back, the error message was probably clear, but when you know nothing, even the most obvious error message leaves you clueless.)

That was my first real-life lesson in Kubernetes security, and it was a humbling moment.
RBAC went from being an acronym I vaguely remembered to a crucial concept I had to respect.

Later that year, I was lucky enough that the company offered access to *Linux Foundation* training.
I enrolled in their *Kubernetes for Developers* and *Managing Kubernetes Applications with Helm* courses.
These courses provided me with a structured introduction to Kubernetes concepts with theoretical foundations that helped me understand the ecosystem more clearly, moving beyond the trial-and-error approach I'd been using.

I wasn’t fluent yet, but at least I was getting better at reading Kubernetes manifests without panicking.

## Slow Growth: Focusing on Thesis in 2024

2024 was relatively quiet on the Kubernetes front.
I was focusing on my master’s thesis, which was in the domain of **GitOps**.

Interestingly, while GitOps is primarily applied to Kubernetes-based applications, my thesis focused on applying GitOps principles in non-Kubernetes contexts.
Even so, understanding GitOps principles meant learning some of the most popular GitOps tools like Flux and ArgoCD.
I found myself learning about **Custom Resource Definition (CRD)** and **Custom Resource (CR)**, and the concept of closed-loop reconciliation - all fundamental to how Kubernetes controllers operate.

During this period, I also read *Kubernetes: Up and Running*.
(Shout out to Aalto University for providing access to the book.)
It’s an excellent resource for developing a mental model of how everything fits together.
It helped me understand not just how to use Kubernetes, but why it was designed the way it was.

I highly recommend it to anyone learning Kubernetes as it bridges the gap between hands-on experience and deeper architectural understanding.

## Setting a Goal: Getting Certified

After submitting my thesis in summer 2024, I decided it was time to get serious about Kubernetes.
With more free time on hand, I purchased both **CKAD** and **CKA** exams and set myself a deadline: pass them within a year.

However, just right after setting this ambitious goal, I completely paused my progress when I went back to Taiwan for vacation from October 2024 to January 2025.
Life had other plans.

Sometimes the biggest obstacle to learning isn't the complexity of the material, it's simply maintaining momentum.

## The CKAD Push

It wasn’t until February 2025 that I finally settled down and resumed serious study.

My main study resource was the *KodeKloud* courses, and I started with their CKAD course.
The hands-on labs were incredibly helpful, and the learning experience felt practical and immediately applicable.

Since I had all this prior experience from my internship and thesis work, preparing for CKAD felt more like a comprehensive review rather than learning something completely new.
The concepts I'd encountered in production finally clicked into place.

In March 2025, I passed the **CKAD** exam.
It felt great, but I knew the real challenge was yet to come.

## The Harder Climb

Success with CKAD gave me momentum, but then I started a new job.
Between getting used to new responsibilities and, honestly, just being lazy, I kept postponing the CKA exam preparation.

By June, reality kicked in.
I had already paid for the exam, and it wasn’t cheap.

(Thanks, Dad, by the way.
He funded both exams and has been incredibly supportive throughout my certification journey.
Even though I didn't pay for it myself, I still didn't want to let his investment go to waste.)

So I pushed myself to study consistently through June and July, focusing on elements that weren't covered in the CKAD exam: **cluster components**, **networking**, **scheduling**, **security**, and **troubleshooting**.
This exam is considerably harder than CKAD, especially the troubleshooting sections, which involve complex scenarios that require a deep understanding of Kubernetes internals.

In August 2025, I passed the **CKA exam**.

## Reflections and Advice

Looking back on this two-year journey, several key insights stand out:

### What I Learned About Learning Kubernetes

- **Understanding containers is crucial, but orchestration is a completely different beast.** Docker experience helps, but don't assume it prepares you for everything.
- **Real-world experience trumps everything.** Working with Kubernetes in production taught me more than any course could. Hands-on experience beats tutorials and reading materials every time.
- **Don't avoid complexity.** My early avoidance of Kubernetes topics probably slowed my learning. This has generally been my problem, and I'm still working on overcoming it.
- **Community and support matter.** Whether it's colleagues, family, or online communities, learning doesn't happen in isolation.
- **It's okay to not get everything at once.** I took many detours: vacations, thesis work, new jobs. But Kubernetes knowledge is cumulative, and every small exposure helps.

### Practical Advice for Certification Preparation

- **Choose your resources wisely.** Go with *KodeKloud* over *Linux Foundation* courses if you’re paying out of pocket. LF courses are expensive and don’t include lab environments. You need to bring your own GCP credits. KodeKloud provides an all-in-one environment with practical labs that mirror real exam scenarios.
- **Set realistic expectations.** The real exam is harder than KodeKloud's mock exams. Expect more steps per question and broader knowledge requirements. The Killer Shell exam simulator that comes with your exam purchase is much more realistic in this regard (you get one attempt for CKAD, two for CKA).
- **Prepare for time pressure.** Especially for CKA, you won't be able to complete every question if you're not fluent with kubectl commands. Practice until the commands become muscle memory.

## What's Next?

Even though I’ve passed both CKAD and CKA, I know I’m far from being a Kubernetes expert.
There’s always more to learn.

But for now, I’m proud of how far I’ve come.
This journey has been as much about personal growth as technical learning.
From not knowing what a Pod was to troubleshooting etcd issues and securing cluster roles, it's been a rewarding ride.

Next, I plan to work through the [Kubernetes The Hard Way](https://github.com/kelseyhightower/kubernetes-the-hard-way) tutorial, which has been widely praised for teaching deeper knowledge than even the CKA exam covers.
I'll probably pursue the **Certified Kubernetes Security Specialist (CKS)** someday, not just for the credential, but because having an exam deadline gives me the motivation to dive deep into the material.

The learning never really stops, but reaching these certification milestones has given me confidence that I can tackle complex technical challenges.
Now, when someone mentions service mesh or other Kubernetes-adjacent technologies, instead of feeling intimidated, I feel curious.

And that shift from fear to curiosity? That's perhaps the most valuable transformation of all.