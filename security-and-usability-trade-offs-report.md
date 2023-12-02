---
title: "Security and Usability Trade-offs of ChatGPT"
author: "2242090"
bibliography: references.bib
references-title: "8 Reference"
toc: true
toc-title: Table of Contents
toc-depth: 3
csl: harvard-imperial-college-london.csl
---

# 1 Introduction

ChatGPT, an AI assistant created by the AI research company OpenAI, will be evaluated using the security-usability threat modeling approach (see Appendix 1) as proposed by Kainda [@kainda2010] by considering usage and threat scenarios.

This report will present three usage scenarios, along with three corresponding threat scenarios, demonstrating particular deficiencies in the system. The scenarios will be thoroughly analysed to determine how easy the system is from a usability perspective. Additionally, some recommendations will be given which the system could improve upon.

The examination of ChatGPT's user interface will give rise to how it ultimately impacts end-user behavior. From this, we can learn how to improve this system to minimise risk from threats. The system will be evaluated through well-defined scenarios to provide an understanding of the benefits, as well as the risks associated.

Note, that the platform that has been decided to be analysed for the system, ChatGPT, is iOS since the web variant has limited features at the time of writing.

# 2 Usage scenarios

Usage scenario
: Actions that are desirable to stakeholders of a secure system [@kainda2010].

## 2.1 Asking specific questions to receive specific answers

The main functionality of ChatGPT is for the user to be able to input a specific query and receive the relevant output. iOS does its local tasks first (see Appendix 2). The AI engine utilises its dataset in combination with its pre-training to identify patterns in the user's prompt [@semrush2022]. After communication with the OpenAI servers, a response is generated and returned to the user. For ChatGPT's iOS application, haptic feedback is given to indicate when a response has completely been delivered. The screen rendering of the response is done slowly – suitable for human reading speeds (see Appendix 2).

## 2.2 Creating multiple chats, searching for particular chats, and searching for specific words or phrases

ChatGPT's technology is such that it can use the previous prompts within a chat to form a context. A user may decide that they want a completely new context. When the user swipes left (see Appendix 3), they can see pre-existing chats. If the user wants to search for specific words or phrases (see Appendix 4) the app returns all relevant results. When a search result is clicked, the interface then directs the user to the very beginning of that specific chat.

## 2.3 Automating digital tasks

A niche usage scenario, but is likely to occur for advanced users. Scenarios may include smart home automation to automatic email management, but the process remains fairly similar; just adaption to the specific workflow. This starts with the user's query, such as: "How can I generate a daily email report with Google Analytics?"

ChatGPT will present information on how the user can use tools such as Zapier to connect Google Analytics and Gmail. Using Zapier as an example, the user then configure their workflow on the dashboard (see Appendix 5). If in the case the user does decide to adopt more complex workflow automation, they can then request ChatGPT for further directions. The involvement of ChatGPT abstracts what would be a complex task into simple steps.

# 3 Threat scenarios

Threat scenario
: Actions that are not desirable and hence the system should not allow them to happen [@kainda2010].

## 3.1 User provides personal information without realising privacy risks

Users may disclose personal information without understanding the privacy implications associated. Without much transparency beforehand, they are unaware of the data processing actions occurring, so they assume that OpenAI handles their data in a secure way [@kim2021]. If the company is susceptible to data breaches in the future, sensitive information could be leaked, and thus, the user is therefore ignorant of the long-term risks it poses.

To model this, a study can be conducted where participants are given "dummy" prompts that encourage the sharing of personal details. This study would aim to track the responses given, such as users expressing a privacy concern. Surveys can also be carried out to gauge the user's emotional perspective in a typical interaction with ChatGPT.

## 3.2 User becomes overly dependent on ChatGPT instead of thinking independently

Since ChatGPT can provide human-like recommendations and responses, users may excessively depend upon it, especially when it comes to making final decisions.

Rather than the initial decision-making process, they may depend heavily on the arguments that ChatGPT presents. The user makes an assumption – that ChatGPT has better knowledge than them. Whilst this may be the case, ChatGPT lacks the emotional intelligence for real-life scenarios. It cannot take into account all factors which are intrinsic to humans. A long-term over-dependence on AI [@theophilou2023] can eventually deteriorate a user's critical analysis skills.

To model this, experiments could be conducted where participants use ChatGPT for specific decision-handling tasks, and evaluate whether they feel confident in trusting their judgment. Interviews could be carried out to measure the user's emotional standpoint on AI and evaluate whether decision-making processes affect their cognitive bias through simple "pros/cons" questions.

## 3.3 ChatGPT is misused to generate harmful, dangerous, or unethical content

Since ChatGPT is capable of generating content on a wide range of topics, there is a risk of malicious content generation. An example, as seen in Appendix 6, direct requests for malware can be made through jailbreaks such as DAN [@coolaj862023]. These misuses can only scale problematically since content can be generated quickly and repetitively due to the quick-processing AI models.

To model this, dedicated security researchers could probe ChatGPT's capabilities, and see the responses it returns – whether those responses pose harm to the user or other users should be categorised and documented. A reliable framework should first be established to correctly classify what constitutes a "harmful response".

# 4 Assessing difficulty-of-use for identified usage scenarios

According to the Kainda security and usability framework (see Appendix 1), each usage scenario identified will be evaluated against a set of usability factors. This will include recognising any system de-motivators and external de-motivators.

## 4.1 Asking specific questions to receive specific answers

| System de-motivators | External de-motivators |
|---|---|
| Analysing the effectiveness of ChatGPT its AI-generated responses should yield results which are useful to the user. Next for the efficiency, the system should also provide responses within an acceptable time. Furthermore for learnability, the user may need some onboarding time to phrase their queries for effective AI usage. | This may include other services that could offer competition to ChatGPT – especially those who make use of OpenAI's existing API but with a much more intuitive user interface. Another de-motivator, would be the limitations of the user's device, such as network speed or availability of hardware acceleration. |

## 4.2 Creating multiple chats, searching for particular chats, and searching for specific words or phrases

| System de-motivators | External de-motivators |
|---|---|
| First looking at efficiency, this should be a metric of the time it takes to find specific conversations or phrases – the more time it takes on average, the more it increases the usage friction. For effectiveness, the chat search feature should be responsive and quick, even if the user has accumulated many chats over time. | Competition from other services. Particularly if they have a better search feature and organisation capabilities. Performance greatly affects how promptly search results are returned – the more RAM or cores available, the more speed the searching algorithm executes with. |

## 4.3 Automating digital tasks

| System de-motivators | External de-motivators |
|---|---|
| If ChatGPT does not provide coherent instructions to the user, then they are unclear on how to automate workflows. Complex instructions may discourage the user. Furthermore, if ChatGPT cannot simplify complex technical terms such as API keys and Zapier, there is a steep learning curve – equating to lower learnability. | Competition from other services. A well known automation service is "If This Then That" (IFTTT), which helps to simplify the approach for the ordinary user, contrasting with ChatGPT's more instructional approach. |

# 5 Assessing ease-of-use for identified threat scenarios

For the identified threat scenarios, it is vital to recognise how easy it is to reproduce them. If the usage scenarios are hard to use, users may resort to utilising threat scenarios, even if their intentions are pure [@kainda2010]. System motivators, in this case, are any aspects of a system that compels a user to that threat scenario, whereas external motivators originate from outside the system which helps a user to arrive at the same threat scenario.

## 5.1 User provides personal information without realising privacy risks

| System de-motivators | External de-motivators |
|---|---|
| ChatGPT's uses its human-like conversational skills to persuade users to give out their personal details and thoughts more readily. This is not the only factor. Prolonged conversation with ChatGPT over time may build emotional rapport – leading to oversharing sensitive information. Additionally, a false sense of privacy is established within the user since there is no clear indication whether conversations are recorded and possibly analysed by OpenAI. | This mainly relates to the user's social situation. A social desirability state may influence users to present themselves positively and "show-off", eventually leading to the exposure of sensitive details [@kim2021]. Other users could genuinely mistake ChatGPT for an actual human, due to its empathetic responses. |

## 5.2 User becomes overly dependent on ChatGPT instead of thinking independently

| System de-motivators | External de-motivators |
|---|---|
| ChatGPT promotes high reliance on itself, based on the recommendations it gives. This is coupled with its expansive knowledge across a wide range of topics which further instills a sense of over dependence on AI. This then reduces the cognitive load on the user – ChatGPT simplifies complicated situations into an easy-to-digest format. There is more inclination for the user interact with ChatGPT rather than using their own analysis. | A long-term use of ChatGPT can result in cognitive laziness. Basic responsibility is diffused, since the user is relieved of their information overload [@theophilou2023]. This could be the aftermath of technological advancement, where the the user is led to believe that AI is more capable in making less error-prone decisions. |

## 5.3 ChatGPT is misused to generate harmful, dangerous, or unethical content

| System de-motivators | External de-motivators |
|---|---|
| ChatGPT's is unable to discriminate between safe and toxic outputs, which can lead to harmful possibilities. There is a lack of moderation before the user enters their query, so that unacceptable prompts are blocked. With the presence of jailbreaks [@coolaj862023], loopholes can exploit ChatGPT's large language model (LLM) to produce malicious content (see Appendix 6). This does not stop on a small scale – since ChatGPT can use previous context within the same chat, toxic outputs can only scale easily. | Given that it is currently an emerging technology, there are weak regulations surrounding AI. Given time and resources, the required legislation for AI will be implemented eventually. For some users, sharing AI-generated content on online forums has anonymity associated with it, giving them the confidence to distribute content that is offensive, extremist or perhaps dangerous. |

# 6 Recommendations

The identified usage scenarios, at least in the case of legitimate users, should be conveniently reachable. The threat scenarios are to be fortified against so that they aren't as easy to access. This section will give recommendations, concerning security and usability.

## 6.1 Usability recommendations

Usability recommendations are suggestions as to how users can achieve their intended goals with ChatGPT, whilst being easy and intuitive to further optimise the user experience.

### 6.1.1 Streamline chat organisation

Existing chats that the user already has could benefit from the implementation of tags or labels that can be organised into various folders. This way, context switching between different chats can occur more easily without being much of a load on the user.

### 6.1.2 Optimise search feature

The efficiency of the chat search functionality relies on prioritising its speed, and this can be done through metadata indexing and OS architecture optimisation. The search feature can be improved by relevance ranking so that only useful results are displayed.

### 6.1.3 Implement consistency check

When using AI-based systems, the generated responses require a consistency check. Leveraging the use of the large language model (LLM) processing capabilities, the system can identify statements that propose direct contradictions with one another. It is then up to the user to pinpoint the accurate responses amongst the conflicted ones. This not only trains the user but also allows ChatGPT to build a better dataset to refine its model even further.

### 6.1.4 Merge conversations on related topics

When users query about a topic across the span of several conversations, related content is often lost. Conversation merging can therefore offer a solution, in which users can select two or more conversations and combine them into a single chat. If this is the case, ChatGPT can either prompt the user, or they have the choice themselves. It would also be beneficial to allow the user to toggle between a merged and individual original conversations view. Due to cloud syncing capabilities, merging chats from different devices or accounts could also be a possibility.

## 6.2 Security recommendations

Security recommendations are suggestions that help safeguard users from misuse, user error, or the discovery of threat scenarios when using the system.

### 6.2.1 Display data policies clearly

Before any interaction with ChatGPT, a clear data handling dialog should be displayed to inform them of any data processing operations. The aim is to provide a structured explanation of the types of user data being collected, the actions in the processing stage, how it is stored within OpenAI's servers, and if it is being shared with third parties. Rather than the user having to read a long terms and conditions document, an opt-in consent to data handling should be displayed.

### 6.2.2 Flag any dangerous user activity

Flagging can help lower the probability that a user carries out harmful real-world activities. The idea of responsible use of a system with AI capabilities should be nurtured, and this can be achieved by utilising the training model of ChatGPT along with input from experts to identify conversation paths that lead to the generation of harmful content. In such cases, ChatGPT should recognise and notify users to discourage any unethical use of AI. The automated flagging system should also constantly alert OpenAI if such instances are detected.

### 6.2.3 Prevent loopholes of jailbreaks

The discovery of the large language model (LLM) exploits [@coolaj862023] requires patching against loopholes. A testing program, involving experts in the field, can be conducted to identify any flaws within ChatGPT's model. When these vulnerabilities are documented, these can be addressed by having the system undergo continuous improvement – ensuring that any loopholes that do exist are closed.

# 7 Appendices

## 7.1 Appendix 1

### 7.1.1 Kainda’s HCISec security threat model (Security-usability threat model)

![](images/kainda-2010-security-usability-threat-model.png)

## 7.2 Appendix 2

### 7.2.1 iOS engine performing simple local tasks via keyboard

![](images/chat-gpt-ios-engine.jpeg)

### 7.2.2 Slow rendering of AI-generated response for human reading speeds

![](images/chat-gpt-slow-rendering-speeds.jpeg)

### 7.2.3 Full final AI-generated response rendered on screen

![](images/chat-gpt-full-ai-response.jpeg)

## 7.3 Appendix 3

### 7.3.1 Existing chats being displayed

![](images/chat-gpt-existing-chat-display.jpeg)

## 7.4 Appendix 4

### 7.4.1 Searching for specific phrases or words

![](images/chat-gpt-search-function.jpeg)

## 7.5 Appendix 5

### 7.5.1 Zapier dashboard for Google Analytics and Gmail automation

![](images/zapier-dashboard-gmail-automation.png)

## 7.6 Appendix 6

### 7.6.1 Chat-GPT DAN exemplar jailbreak scenario

![](images/chat-gpt-dan-jailbreak-example.jpeg)

# 8 Bibliography