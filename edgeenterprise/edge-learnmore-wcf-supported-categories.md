---
title: "Supported categories for Web Content Filtering (WCF)"
ms.author: ssatti
author: dan-wesley
manager: vesesha
ms.date: 07/10/2024
audience: ITPro
ms.topic: reference
ms.service: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom:
description: "How web content is categorized and the currently supported categories for Web Content Filtering (WCF)."
---

# Supported categories for Web Content Filtering

This article describes how web content is categorized and lists the categories that are currently supported.

## Introduction

 Proprietary categorization technology and processes are used to categorize websites, IPs, and detect anonymous proxy use in real-time. Coupled with machine learning-driven AI, our automated technology is context aware through comprehensive sentiment analysis, entity recognition, and topic modeling. Over 250 content analysis engines review text (in more than 200 languages) and images for URL categorization. Worldwide human review teams also perform physical website inspections to ensure accuracy and cultural relevance.

## Supported categories

The following table lists the supported categories, gives a description for each category, and gives examples.

| Category |  Category string  | Description | Example |
| --- | --- | --- | --- |
| **Adult content** | | | |
| Cults | *cults* | Sites related to groups or movements whose members demonstrate passion for a belief system that is different from those that are socially accepted | N/A |
| Gambling | *gambling* | Online gambling and sites that promote gambling skills and practice. | irpoker.com |
| Nudity | *nudity* | Sites that provide full-frontal and semi-nude images or videos, typically in artistic form, and might allow the download or sale of such materials. | roystuart.net |
| Pornography / Sexually explicit | *pornography_or_sexually_explicit* | Sites containing sexually explicit content in an image-based or textual form. Any form of sexually oriented material is also listed here. | xhamster.com |
| Sex education | *sex_education* | Sites that discuss sex and sexuality in an informative and nonvoyeuristic way, including sites that provide education about human reproduction and contraception, sites that offer advice on preventing infection from sexual diseases, and sites that offer advice on sexual health matters. | tradesexualhealth.com |
| Tasteless | *tasteless* | Sites oriented towards content unsuitable for school children to view or that an employer would be uncomfortable with their staff accessing, but not necessarily violent or pornographic. | specialfriedrice.net |
| Violence | *violence* | Sites that display or promote content related to violence against humans or animals | peacefulpillhandbook.com |
| **High bandwidth** |  |  |
| Download sites | *download_sites* | Sites whose primary function is to allow users to download media content or programs, such as computer programs. | download.com, dropbox.com |
| Image sharing | *image_sharing* |  Sites that are used primarily for searching or sharing photos, including those that have social aspects. | flickr.com, tumblr.com |
| Peer-to-peer | *peer_to_peer* | Sites that host peer-to-peer (P2P) software or facilitate the sharing of files using P2P software. | utorrent.com, hostgator.com |
| Streaming media & downloads | *streaming_and_downloads* | Sites whose primary function is the distribution of streaming media, or sites that allow users to search, watch, or listen to streaming media. | youtube.com, spinninrecords.com |
| **Legal Liability** |  |  |
| Child abuse images | *child_abuse_images* | Sites that include child abuse images or pornography. | N/A |
| Criminal activity | *criminal_activity* | Sites that give instruction on, advice about or promotion of illegal activities. | fakepassport.info, terroristwebsites.info |
| Hacking | *hacking* | Sites that provide resources for illegal or questionable use of computer software or hardware, including sites that distribute copyrighted material that has been cracked. | mirror-h.org |
| Hate & intolerance | *hate_and_intolerance* | Sites promoting aggressive, degrading, or abusive opinions about any section of the population that could be identified by race, religion, gender, age, nationality, physical disability, economic situation, sexual preferences or any other lifestyle choice. | N/A |
| Illegal drug | *illegal_drug* | Sites that sell illegal/controlled substances, promote substance abuse, or sell related paraphernalia | weedmaps.com |
| Illegal software | *illegal_software* | Sites that contain or promote the use of malware, spyware, botnets, phishing scams, or piracy & copyright theft | anonymizer.com, 123freemovies.net |
| School cheating | *school_cheating* | Sites related to plagiarism or school cheating | N/A |
| Self-harm | *self_harm* | Sites that promote self-harm, including cyberbullying sites that contain abusive and/or threatening messages towards users | N/A |
| Weapons |*weapons* | Any site that sells weapons or advocates the use of weapons, including but not limited to guns, knives, and ammunition. | ammo.com |
| **Leisure** |  |  |
| Chat | *chat* | Sites that are primarily web-based chat rooms. | lingr.com |
| Games | *games* | Sites relating to video or computer games, including sites that promote gaming through hosting online services or information related to gaming. | piratesarena.net, rustguides.com |
| Instant messaging | *instant_messaging* | Sites that can be used to download instant messaging software or client based instant messaging | aim.com |
| Professional network | *professional_network* | Sites that provide professional networking services. | linkedin.com |
| Social networking | *social_networking* | Sites that provide social networking services | facebook.com, match.com, blogger.com |
| Web-based email | *web_based_email* | Sites offering web-based mail services. | gmail.com |
| **Other** |  |  |
| None | *none* | This category doesn't block any URLs. Having none as the only blocked category is equivalent to not blocking any category. | N/A |

## See also

- [Configure Web Content Filtering on Edge](microsoft-edge-web-content-filtering.md)
- [Microsoft Edge management service](/deployedge/microsoft-edge-management-service)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)