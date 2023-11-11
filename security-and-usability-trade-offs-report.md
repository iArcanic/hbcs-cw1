---
title: "Security and Usability Trade-offs Report"
author: Preetham Ananthkumar 2242090
bibliography: references.bib
reference-section-title: "5 References"
output:
  pdf_document:
    toc: true
    number_sections: true
csl: elsevier-harvard.csl
---

# 1 Introduction

This report analyses the security and usability trade-offs of ChatGPT, an AI assistant created by the AI and research company, OpenAI on November 30th of 2022. This system will be evaluated using the security-usability threat modeling approach as proposed by the Kainda [@kainda2010], as seen in Appendix 1. This is a suitable framework, as it helps to identify the frictions between both the security and usability for legitimate users by considering appropriate usage scenarios, as opposed to the potential threat scenarios that could also arise due to probable user mistakes.

To fully grasp an entire understanding of ChatGPT's security and stability, this report will present three usage scenarios, along with three corresponding threat scenarios based on likely user mistakes, demonstrating particular deficiencies about the system. The scenarios will be thoroughly analysed to determine how easy the system is from a usability perspective. Finally, to top it all off, some recommendations will be given on which the system could improve upon.

The examination of ChatGPT's controversial AI interface will give rise to insight on how it ultimately impact end-user behavior. From this, we can potentially glean strategies to improve this system with the goal of minimizing risk from threats. Overall, the main objective is to evaluate this particular system, ChatGPT, through well defined scenarios in order to provide a more holistic view on the benefits it offers, as well as the understood risk associated.

Note, that the platform that has been decided to be analysed for the system, ChatGPT, is iOS, since the web variant has limited features. Although it is the same product and engine, the mobile counterpart is slightly more popular (see Appendix 2) than the web version.

# 2 Usage scenarios

## 2.1 Defining usage scenarios

The definition of usage scenarios, via the Kainda security and usability framework, is as follows.

Usage scenario
: Actions that are desirable to stakeholders of a secure system [@kainda2010].

A more cohesive, in-depth take on this considers a variety of other elements (see Appendix 3) that comprise a usage scenario, explored in two studies [@dong2018; @ortiz2010], but can be summarised in combination as:
$$Scenario=(Time,\space Context,\space User,\space Product,\space Behavior\space (or\space Interaction),\space Artefact)$$

In which $Time$ defines the duration for which the user interacts with the product [@dong2018]. $Context$ refers to the environmental factors into distinct categories of physical, social, situational, cultural and temporal [@ortiz2010]. $User$ is as it says, however with additional attention to their values, personal traits and ambitions [@ortiz2010]. $Product$ is defined as the actual object that is being considered within the scenario [@dong2018]. $Behavior$ (or $Interaction$) concerns itself with the actual ongoings of the scenario interaction itself, and this could include the type of interaction (physical or non-physical) [@ortiz2010]. Finally, $Artefact$ is the end output of the usage scenario, which can take the form of either social, technical or aesthetic functions [@ortiz2010].

So, with that in mind, here are three usage scenarios identified for the system under evaluation, ChatGPT.

## 2.2 Usage scenarios for ChatGPT

All these scenarios will be under the assumption that the user has an authenticated account and has successfully logged in with said account. A consistent, stable internet communication throughout is obviously a understood prerequisite.

### 2.3 Asking specific questions (via both text and speech recognition) to receive specific answers

The main functionality of ChatGPT is for the user to be able to input a specific query and thus, receive the relevant output. The nature of the query on iOS can range from text input or speech recognition. The iOS engine itself may do its own local tasks, such as auto-correcting, spell-checking, text suggestions (see Appendix 4). Once a valid input is parsed, i.e. one which does not violate OpenAI's terms and conditions policy, the AI engine utlises the supremely vast dataset its been provided in combination of its pre-training phase to identify patterns and structures in the prompt it has been given [@semrush2022]. After communication and subsequent back-end server processing, a response is sent back to the user's device. It then generates a coherent response, rendering that on the screen in an easy-to-understand visual way. Specifically, for the ChatGPT iOS application, haptic feedback is given to indicate when a response has completely been delivered (see Appendix 4). The screen rendering of the AI-generated response is done slowly – to be suitable for typical human reading speeds (see Appendix 4).

### 2.4 Creating multiple chats, searching for particular chats and searching for words/phrases/characters in said chats

ChatGPT's technology is such that it is able to use the previous prompts and AI-generated responses within a singular chat and extract a context from it. A user may decide that they want a completely new context or just a blank screen for clarity and organisational purposes. When the user swipes left, they are able to see an accumulation of pre-existing chats (if any) with AI-generated titles based on the chat's context. If the user desired to search for a specific pattern of words, phrases or characters from from their entire chat history, again, the iOS engine does its simple local tasks via the keyboard and then the app returns all relevant results it can find within a specific time period. If older results are required, the user is prompted to do so. When a search result is clicked, the application interface then directs the user to very beginning of that specific chat.

### 2.5 Automating simple digital tasks

# 3 Threat scenarios

The definition of threat scenarios, via the Kainda security and usability framework, is as follows.

Threat scenario
: Actions that are not desirable and hence the system should not allow them to happen [@kainda2010].

# 4 Recommendations

# 5 References

# 6 Appendices

## 6.1 Appendix 1

### 6.1.1 Kainda’s HCISec security threat model (Security-usability threat model)

![](images/kainda-2010-security-usability-threat-model.png)

## 6.2 Appendix 2

### 6.2.1 ChatGPT's popularity amongst other apps on Apple's AppStore

![](images/chat-gpt-app-store-chart-popularity.png)

## 6.3 Appendix 3

### 6.3.1 Dong's UX usage scenario elements

![](images/dong-2018-ux-usage-scenario-elements.png)

## 6.4 Appendix 4

### 6.4.1 iOS engine performing simple local tasks via keyboard

![](images/chat-gpt-ios-engine.jpeg)

### 6.4.2 Slow rendering of AI-generated response for human reading speeds

![](images/chat-gpt-slow-rendering-speeds.jpeg)

### 6.4.3 Full final AI-generated response rendered on screen

![](images/chat-gpt-full-ai-response.jpeg)