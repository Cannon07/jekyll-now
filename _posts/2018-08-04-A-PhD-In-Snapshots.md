---
title: A PhD in Snapshots
published: true
layout: post
---

A PhD on average takes 5 to 6 years of time. For those who aren’t familiar with the academic world, this length of time often causes some confusion. What can you possibly keep learning for 5 years? To help answer this question, I’ve joined together progress reports I wrote up during various stages of my PhD. These reports were a condition of my funding from the Hertz foundation,which kindly supported me through 5 years of my PhD. The Hertz foundation requested that I provide reports of my research progress twice a year to demonstrate that I was making effective use of my scholarship. Each progress report below was written at the date indicated and has only been lightly edited, and consequently provides a glimpse into my thoughts as I progressed through the PhD. My progress reports started from the Spring of 2014, my second year in the program, so I’ve written a brief introduction for the 2012-2013 year to provide context. The reports were written for my scholarship committee and don’t discuss all my emotional highs and lows, but do provide an accurate snapshot of my progress and hopes through the degree.

## Prelude: Fall 2012 to Fall 2013
My first year in the program was mostly taken up by coursework. I took multiple classes on the theory and practice of machine learning, and various classes of algorithmic design. None of these classes particularly set my mind on fire, but machine learning was in the air, so I figured it was worth learning. I also “rotated” in various research groups. Stanford’s computer science department asked students to rotate between research groups, spending 3 months in each, to assess mutual fit between students and faculty. For those not familiar, the PhD is basically an extended apprenticeship between the student and their faculty advisor, so personal fit is absolutely critical. I rotated with two machine learning groups and a system software group. None of these particularly felt like a fit for me. The one bright spot in the year was landing the Hertz fellowship, which guaranteed five years of research support. With the fellowship in hand, I resolved to try researching things outside my core research competency of mathematical computer science. I took the summer off and visited family. I read the “Emperor of all Maladies” which got me very interested in the ideas around disease, so I resolved to talk to the computational biology faculty despite the fact that my last class in the life sciences had been in 9th grade. I talked to a dozen faculty or so, but felt drawn to the Pande group, which had worked for years on simulating proteins. Vijay (Pande) was interested in applying machine learning more systematically to the group’s work and encouraged me to hang around and spend time with his students. I ended up sticking around, and wrote a short paper on using Hidden Markov Models to analyze protein simulations in the fall of 2013, which we submitted to ICML (the international conference on machine learning).

## Hertz Report Spring 2014:
This quarter, I submitted a paper to NIPS (Neural Information Processing Systems) on the use of switching linear dynamical systems in analyzing protein simulation datasets. Our method analyzes these datasets by learning locally quadratic approximations to the protein’s energy landscape. These approximate energy landscapes can be used to reconstruct the protein’s dynamics. I used the algorithm to analyze datasets for the opioid growth factor met-enkephalin and the proto-oncogene Src-kinase. Our results show significant improvement in model fidelity over previous analysis methods.

The implementation required for this paper took up the majority of my time over the last few months. The method uses semidefinite programming to compute approximate dynamics for the protein. However, standard semidefinite solvers cannot efficiently solve the large problems needed for protein analysis. As a result, I implemented a new semidefinite solver based upon the Frank-Wolfe algorithm. Debugging and stabilizing this implementation was a major effort. In future work, I plan to extend this library to enable learning for even larger biological and quantum-mechanical datasets. [Note: this never ended up happening…]

I took and passed a class on optimization theory this spring quarter (for Credit/No-Credit). I also spent some time revising a paper submitted to ICML (the International Conference on Machine Learning) earlier this year. We had to make a few changes to the paper to satisfy the reviewers. The revised paper was accepted, and I will be attending ICML in Beijing this summer.

The remainder of my time was spent doing preparatory work for a new collaboration with Google. Another graduate student and I submitted a proposal this spring to the Google assisted science (GAS) team on using Google’s scalable deep learning systems for improving rational drug design. Standard approaches to virtual screening of proposed drugs depend upon simple similarity measures to identify possible new drugs. Deep learning provides a richer toolbox, which may enable the identification of novel families of drugs for infectious diseases. After a few meetings with the GAS team, our proposal was recently accepted, and our lab has started collaborating with Google. Over the last few weeks, we have performed some preliminary exploration and testing of deep learning methods on a Stanford cluster. I will intern at Google this summer to perform the necessary implementation and to run the required experiments on Google’s systems.

## Hertz Report Fall 2014:
I’ve spent the last six months working on a deep learning system to improve virtual screening  for drug discovery. The goal of this system is to enable the computational evaluation of the suitability of drug-like compounds for modulating biological targets. Our results show robust improvements over baseline algorithms for this task. We plan to submit our results to ICML (the International Conference on Machine Learning) in February.

This work has been performed in collaboration between the Pande lab and a team in Google research (Google Accelerated Science). I interned full-time with this team over the summer, and continued my internship on a part-time basis over the Fall quarter to continue working on this project. I plan to continue interning with Google research on a part-time basis till next Fall. We hope to collaborate with a pharmaceutical company to deploy our computational system on an actual drug discovery project.

Another major goal for the next few months is the curation of a large dataset of virtual screening information for the machine learning community. Dramatic progress in computer vision followed from the creation of the large-scale image dataset ImageNet. We hope that our dataset (code-named MoleculeNet) will trigger similar improvements in computational drug discovery. We have completed the majority of the curation work already. The remaining work requires the construction of clean metrics which accurately measure algorithmic progress. We anticipate releasing this dataset in June.

In other news, the paper I submitted to NIPS (Neural Information Processing Systems) in June 2014 on stable switching linear systems was rejected. The reviewers liked the technical depth of the work, but had some concerns. One reviewer felt the work focused too much on the biological application (protein modeling) and suggested I submit instead to a biological journal. Another reviewer wanted to see more quantitative analyses of the algorithm’s performance relative to baseline methods. I plan to de-emphasize the focus on proteins and add quantitative metrics before re-submitting the paper to a machine learning conference. Doing so will take about a month’s work, so I’ve decided to put this paper on the backburner while our collaboration with Google continues. I anticipate returning to this work late this year.

## Hertz Report Spring 2015:
Since my last progress report, I’ve continued work on my deep learning system for virtual screening in drug discovery. I wrapped up the previous stage of the project by releasing a paper on Arxiv in February. The paper was chosen to be featured on the Google Research blog, and attracted some attention from the broader biochemical research community. I was invited to give talks on the work to a few labs at Stanford, Memorial Sloan Kettering Cancer Center, and Schrodinger Inc. 

The feedback we received from the biochemical community about the work was positive. Biochemists appreciated the strengths of the system, but requested that we modify the system to directly predict IC50 values instead of our binary active/inactive classification. We received a number of offers for collaborative projects once we finish modifying the system.

The response from the machine learning community was more tepid. The work was rejected from ICML on the grounds that the work focused too much on biological applications. The reviewers would have liked to see deeper theoretical exploration of our system’s properties. After receiving these comments, I discussed the situation with my advisor and co-authors. We decided to leave the current paper on the Arxiv, and plan to submit follow-up papers to biochemical venues rather than to machine learning venues.

I’ve been working on a pair of follow-up projects since the completion of our earlier paper. The first expands the scope  of the original system to predict the requested IC50 values and also introduces a larger dataset, MoleculeNet, which we hope will serve as a standard benchmark for the field. We plan to submit this work to the Journal of Chemical Informatics in October. [Note: this paper took a number more years to come out]

The second project attempts to incorporate crystallographic data into our learning systems. The algorithm will accept co-crystal structures of proteins and ligands, and will attempt to predict the binding affinity of the complex. The goal of this work is to improve the accuracy of the current generation of “docking” software used by the computational chemistry community. This work should also be ready for submission around October (I haven’t yet decided on the venue). [Note: this paper also took a number more years to even make it to the Arxiv]

## Hertz Report Fall 2015:
Over the last six months, I’ve continued working on deep-learning methods for drug discovery. My primary research project focuses on creating an algorithm that uses the three-dimensional structures of proteins and drug-like compounds to predict the binding affinity of protein-drug complexes. This algorithm depends on using three-dimensional convolutional neural networks and adapts recent progress in computer vision to solve a generalized “visual” problem. The system has stabilized to the point where we see reasonable results (but which do not yet surpass our strong baseline algorithm). However, we are seeing steady improvements as we make tweaks, and we anticipate that the final method will be ready to submit to a good journal in April.  

The other major focus of my time has been creating a standard open-source package that computational drug discovery scientists can use to perform deep-learning and machine-learning on their datasets. The initial version of this package, deepchem, will be released in the next few weeks. Once we complete generating documentation and tutorials, the source and website will be made public. I have been using this package in a collaboration with researchers at Pfizer to analyze the BACE enzyme, and I will also present a tutorial on this package to Merck’s machine learning group at the beginning of February. 

In more procedural matters, our paper on using multitask deep-learning for drug discovery was rejected by ICML. The reviewers found the work to be too focused on biology and engineering for its audience. However, the computational drug discovery community has given our paper a good reception thus far (with 8 citations of the arxiv version in under a year). We’ve upgraded the system (in line with comments from biochemists) to directly predict IC50/Ki values for experiments rather than just predict binary activity/inactivity labels. We’re working on submitting this revised version of our paper to Nature Communications within the next few months.

Last quarter, I took a course on programming language theory to round out my breadth requirements. This quarter, I am currently TA’ing a course on convolutional neural networks to fulfill part of my departmental teaching requirements. I’ve also put together a qualifying examination committee, and anticipate finishing my qualifying exams by sometime this year. I plan to have all departmental requirements for graduation completed by early next year.

I attended the Gordon research conference on computer aided drug design in July and presented a poster on our multitask deep-learning work. I also recently gave talks on my work to computational chemistry researchers at the EPA, and to software engineers at twoXar and ParallelMachines (machine learning startups).

## Hertz Report Spring 2016:
The last few months also saw the submission of my first DeepChem powered paper. As I mentioned in my last progress report, I have been working with researchers at Pfizer to analyze the BACE-1 enzyme, a drug target potentially implicated with Alzheimer's. We harvested data from public sources, which we used to construct predictive models of ligand affinity to BACE-1. We compared DeepChem models to those generated by standard drug-discovery software packages, and found that DeepChem models provided significant boosts in predictive power. We’ve also open-sourced all analysis code, so that readers can recreate our results. The paper was submitted to JCIM (Journal of Chemical Informatics).

My current highest priority is another DeepChem powered analysis project with researchers at Merck. Unlike the Pfizer project, which was done on public datasets, the Merck collaboration works with Merck-internal datasets that are used in their day-to-day pipeline. Demonstrating that DeepChem can add value to their daily pipeline should raise the profile of the package and gain greater attention from the drug-discovery community. The lead researcher there is retiring at the end of the year, so we need to have our paper ready to go by September/October. To ensure that we meet this goal, I’ve had to put other projects on the backburner to give the Merck collaboration priority.

My project using three dimensional structures of proteins and proposed drugs to predict binding-affinity of protein drug complexes has made some progress. We achieved preliminary results which match or exceed strong baselines, but we discovered that reaching striking results would require significant software upgrades. Consequently my co-author and I have decided to put the project on hiatus for a few months, to allow me to finish my Merck collaboration and to allow my co-author to wrap-up some of his. We plan to start again in earnest by the end of summer.

In other news, I’ve spent the last six months working as a teaching assistant for two courses on deep-learning for computer vision and natural language processing. (I’m required to help teach two courses to graduate). The experience was fruitful, and I’ve learned a lot about how to work with students. I am somewhat relieved that I no longer have to teach until graduation, since my duties took up an enormous amount of time. That said, I’ve discovered that I enjoy mentoring, and I will be working with a pair of undergraduates this summer on exciting projects. I hope to see at least one of these projects reach a publishable endpoint.

Looking forward to the next six months, I have a pair of other collaborations with small Biotech companies lined up to use DeepChem in their day-to-day drug discovery efforts. I hope to publish these papers in the coming year, and I also hope to mature our three-dimensional algorithmic efforts and get out our first paper on the topic by winter. 

## Hertz Report Fall 2016:
The majority of my time has been spent on my open-source package, DeepChem (which aims to facilitate computational drug discovery). DeepChem has slowly started to pick up users in the pharmaceutical and research communities, and has crossed the milestone of 100 stars on Github. I anticipate spending the remainder of my thesis maturing and extending DeepChem to make deep-learning in drug discovery accessible to a larger audience.

The first DeepChem paper, a collaboration with Pfizer, was accepted and published in Journal of Chemical Information and Modeling. This paper demonstrated that basic machine-learning techniques could match or exceed traditional computational methods for drug modeling even in the presence of limited data.

I also made significant progress on a DeepChem collaboration with Merck. This collaboration aims to show that DeepChem can make multitask deep learning a practical tool for the pharmaceutical community. We analyzed a number of Merck’s internal datasets, and demonstrated under stringent conditions that multitask deep learning provides a performance improvement over basic machine learning techniques. I’ve completed a draft of our paper, “Is Multitask Deep Learning Practical for Pharma”. My Merck collaborators have requested a few revisions. After these revisions are complete, we will submit the paper to Merck’s legal review, hopefully by the end of the month.

I’ve also spent a significant amount of time mentoring younger students on research projects. I had two undergraduate research students over the summer. One of the students and I developed a new technique for adapting one-shot learning to drug discovery. This technique will enable us to use machine learning when only very limited amounts of experimental data are available (the technique transfers knowledge from related, but not identical, experiments to the experiment at hand). We have submitted this paper to ACS Central Science and have open-sourced the algorithms and data as part of DeepChem. We recently received comments back from reviewers, with mostly positive feedback and a request for some revisions. The other undergraduate student helped curate multiple new datasets which we are using in on-going projects.

Some other collaboration projects with junior students are also nearing completion. I’ve been working with a first year chemistry PhD student on developing a deep-learning system that models chemical synthesis. We reached a milestone recently with the construction of a prototype system that effectively models a small set of reactions. We hope to expand this prototype to model more reactions and write our first paper on the topic in the next few months. Another first year student has been working with me on developing a comprehensive set of benchmarks for machine-learning in chemistry. This set, MoleculeNet, will curate a number of existing datasets to offer solid benchmarking targets for algorithmic development. We have incorporated MoleculeNet into DeepChem and anticipate writing the associated paper soon.

I have also been working on a new type of deep-learning system for modeling molecular physics with a senior post-doc in the group. Our algorithm, the spatial-convnet, has achieved strong performance in predicting the binding free energy of large protein-ligand complexes. We anticipate that the spatial convnet has the potential to be widely applicable to problems in chemistry, biophysics, and materials science.

In a personal first, I co-organized the first conference on deep-learning in chemistry (http://deepchemworkshop.docking.org/). The conference was held at Stanford on November 11th. We had an enthusiastic turnout of about 150 researchers and students from industry and academia. I was a presenter in addition to being an organizer and gave a talk discussing DeepChem and our new one-shot learning algorithms. The conference helped spark a number of potential collaborations which I anticipate developing over the coming year.

I also recently passed my qualifying exam this October. I anticipate that once the papers I’ve mentioned above have been submitted, I should be ready to defend my thesis. I’m aiming to graduate by next year. I still need to find two additional members for my committee.

## Hertz Report Spring 2017:
Most of my time over the past six months has been spent on continuing development for DeepChem, my open source package for drug discovery. DeepChem now has 360 stars on Github and is the most popular open source drug discovery package (for small molecules) available online. I’ve started up a DeepChem User Group Meetup and had a healthy turn-out at the first iteration of the event. I plan to continue working to grow the DeepChem research and industrial communities over the next six months.

My recent paper on one shot learning paper was featured on the cover of ACS Central Science’s April Edition. The work was also picked up by press outlets including the Stanford Daily and IEEE Spectrum, and also by Huffington Post (the last due to some helpful outreach by the Hertz community).

The work I’ve been doing on a benchmarking suite, MoleculeNet, for molecular machine learning has matured. We released the first version of MoleculeNet onto Arxiv, and got good community feedback from other machine learning and computational biology researchers. We have revised, and completed a significantly expanded version of the paper with more datasets, models, and metrics. We have submitted this version of our paper to Chemical Science.

The first version of our paper on deep learning for chemical retrosynthesis just came out onto Arxiv. The paper demonstrates that machine learning technology developed for neural translation can be adapted for chemical retrosynthetic modeling (the task of identifying how to construct a desired molecule from simpler constituent subcomponents). The system currently performs as well as baselines based on rule-based transformations, but will hopefully be much simpler to extend and refine.

The first version of our paper on using deep learning for modeling protein-ligand binding pockets has been released onto Arxiv. This end-to-end deep learning system has accuracy approximately equal to that of a hand-tuned baseline which models chemistry which should be useful for understanding the dynamics of the binding pocket.

I also submitted my joint collaboration paper with researchers from Merck. This paper checks the ability of multitask learning to aid in tasks interesting for pharmaceutical drug discovery. We submitted the paper to Journal of Chemical Information and Modeling and received mostly positive feedback from the reviewers. I am currently working on revising the manuscript for resubmission.

This summer, I am mentoring an undergraduate student who will be working on a project applying deep reinforcement learning to the problem of protein folding. Following in the tradition of projects such as FoldIt, we hope that by using game-playing techniques, we will be able to accelerate the process of protein folding. I have also started a collaboration with another graduate student in the lab on the application generative adversarial networks to the problem of generating low energy ligand conformations. This problem is important for understanding the behavior of drug-like ligands in protein binding pockets. I have also started a project a first year grad student in the lab on the problem of using deep learning for protein 3D structure prediction. This project serves as a complement to the reinforcement learning approach to protein folding and uses a more classical approach based on directly predicting the residue-residue contacts in the lowest energy structure for the protein.

I recently passed my oral thesis proposal. In the Stanford CS department, the proposal is the last step before the thesis defense. My committee agreed with my proposal to defend my thesis this coming October.

## Hertz Report Fall 2017:
The most momentous occurrence of last few months was defending my thesis on December 12th. Most of fall quarter was spent preparing for the defense. Overall, the committee was quite happy with my research and passed me without any additional requests. I’m still working on polishing up my dissertation which should be submitted within the next month, formally concluding the PhD.

I’ve spent the last few months in winding down mode wrapping up some projects in the lab. I was a co-author on a recently submitted paper that used deep reinforcement learning to design RNA with desired folds. Our method outperforms the best alternative algorithm currently published, but doesn’t match the best human experts. We suspect that significantly greater computational power would be required to surpass human experts.

I’m also a co-author on a paper proposing a new deep learning approach to predicting protein-ligand binding affinity. This approach builds off some of my past work on applying deep learning to predicting binding free energies of protein-ligand structures. This paper will likely be submitted within the next few months.

A major part of my PhD was the creation of the deepchem.io open source project for deep learning in chemistry and biology. I want to make sure that this project and the growing open source community around it survive my PhD, so I’ve been investing significant time into ensuring that deepchem.io matures into a full fledged open source effort. In particular, I’ve worked with the other core developers to create a formal “technical steering committee” which will lead continued development of the project.

I’ve also spent a good chunk of time thinking about next steps after the PhD. After talking to many mentors and alumni, I decided that my efforts would be best spent working at a startup rather than in academia or a large research lab. I want to learn how to create a new engineering and research organization from the ground up, and co-founding a startup seems to be the best way to build this expertise. I’m currently working on a new startup in the blockchain space with a couple co-founders. This startup will be my full-time effort after the PhD is entirely concluded this quarter.

I’d also like to thank the Hertz foundation for all their support over the last few years. My work at the intersection of machine learning and science wouldn’t have been possible without your support!
