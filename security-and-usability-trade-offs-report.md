---
title: "Security and Usability Trade-offs of ChatGPT"
author: Preetham Ananthkumar 2242090
bibliography: references.bib
output:
  pdf_document:
    toc: true
    number_sections: true
csl: elsevier-harvard.csl
---

# 1 Introduction

ChatGPT, an AI assistant created by the AI and research company, OpenAI on November 30th 2022, will be evaluated using the security-usability threat modeling approach (see Appendix 1) as proposed by Kainda [@kainda2010]. This framework, helps to identify the aspects of security and usability for legitimate users by considering appropriate usage scenarios, as opposed to the potential threat scenarios.

This report will present three usage scenarios, along with three corresponding threat scenarios based on likely user mistakes, demonstrating particular deficiencies in the system. The scenarios will be thoroughly analysed to determine how easy the system is from a usability perspective. Finally, to top it all off, some recommendations will be given on which the system could improve upon.

The examination of ChatGPT's controversial AI interface will give rise to insight into how it ultimately impacts end-user behavior. From this, we can learn how to improve this system with the goal of minimising risk from threats. The main objective is to evaluate this particular system through well-defined scenarios in order to provide an understanding on the benefits it offers, as well as the risks associated.

Note, that the platform that has been decided to be analysed for the system, ChatGPT, is iOS, since the web variant has limited features.

# 2 Usage scenarios

## 2.1 Defining usage scenarios

The definition of usage scenarios, via the Kainda security and usability framework, is as follows:

Usage scenario
: Actions that are desirable to stakeholders of a secure system [@kainda2010].

So, with that in mind, here are three key usage scenarios identified for the system under evaluation, ChatGPT.

## 2.2 Asking specific questions to receive specific answers

The main functionality of ChatGPT is for the user to be able to input a specific query and receive the relevant output. The iOS engine itself may do its own local tasks (see Appendix 2). The AI engine then utlises its supremely vast dataset in combination of its pre-training to identify patterns in the user's prompt [@semrush2022]. After communication with the OpenAI servers, it then generates a response, rendering that on the screen. For ChatGPT's iOS application, haptic feedback is given to indicate when a response has completely been delivered. The screen rendering of the AI-generated response is done slowly – to be suitable for typical human reading speeds (see Appendix 2).

## 2.3 Creating multiple chats, searching for particular chats and searching for specific words or phrases

ChatGPT's technology is such that it is able to use the previous prompts within a singular chat and extract a context from it. A user may decide that they want a completely new context for clarity and organisational purposes. When the user swipes left (see Appendix 3), they are able to see an accumulation of pre-existing chats with AI-generated titles based on the chat's context. If the user wants to search for specific words or phrases (see Appendix 4) the app returns all relevant results it can find. When a specific search result is clicked, the interface then directs the user to very beginning of that specific chat. This can be particularly useful, reducing the mental memory load on the user.

## 2.4 Automating digital tasks

A very niche usage scenario, but is very likely to occur for the advanced user. Such scenarios may include smart home automation to automatic email management, but the process for AI automation remains fairly similar; just adaption to the specific service which the user desires. This starts with the user sending in a prompt, such as: "Can you provide steps to schedule a daily email report of my Google Analytics data?"

ChatGPT will then outline a well-informed process, including information on how the user can use tools such as Zapier to connect Google Analytics and Gmail to present the scheduled automated report. Taking Zapier as an example, the user then configure their own workflow on the Zapier dashboard (see Appendix 5). If in the case the user does decide to adopt a more complex workflow automation, they can then request ChatGPT for directions. The involvement of ChatGPT helps to abstract what would be a complex task into simple high-level steps.

# 3 Threat scenarios

## 3.1 Defining threat scenarios

The definition of threat scenarios, via the Kainda security and usability framework, is as follows:

Threat scenario
: Actions that are not desirable and hence the system should not allow them to happen [@kainda2010].

So, with that in mind, here are three key threat scenarios identified for the system under evaluation, ChatGPT.

## 3.2 User provides personal information without realising privacy risks

Users to disclose personal information which they may not be comfortable expressing without understanding the privacy implications that come alone with that. Without much transparency beforehand on how user data is handled, the user is ill informed of the data processing actions occurring and so, the mental model for the user is to assume that OpenAI handles their data in an anonymous and private way. If the company was susceptible to data breaches in the future, sensitive information could be leaked. The user is therefore unaware of long-term risks that such intimate details may have for them.

To model this, a study can be conducted where participants are given "dummy" conversational prompts that encourage the sharing of personal details. The aim of this study would be to track the responses given, such as if users expresses a concern for privacy. Interviews and surveys can also be carried out to gauge the user's emotional perspective when they are in a typical interaction with ChatGPT.

## 3.3 User becomes overly dependent on ChatGPT instead of thinking independently

Since ChatGPT can provide human-like recommendations and responses, there is a certain risk associated where potentially the user might excessively depend upon it, especially when it comes to the final stages of decision making of a user's mental model. For example, if the user asks such a prompt: "Should I accept this new job offer I have been proposed or stay within my current role?"

Rather than the initial decision making process which the user typically under goes, they may depend heavily on the arguments that ChatGPT presents. The user makes an underlying assumption – that ChatGPT has better knowledge than them. Whilst this may be the case, ChatGPT lacks the emotional intelligence when it comes to real life scenarios. Even though it may offer some preliminary advice, it cannot take into account of all factors which are intrinsic to humans and their decision-making processes in their mental models. A long-term over dependence on AI [@theophilou2023] can eventually deteriorate a user's critical analysis skills over time.

To model this suitably, experiments could be conducted where participants use ChatGPT for specific decision handling tasks, and then evaluate whether they feel confident in trusting their own judgement or leaving it up to AI. Interviews and surveys could also be carried out to measure the user's emotional standpoint on AI, and evaluate whether decision-making processes affect their judgement accuracy or cognitive bias through simple "pros/cons" tasks or questions.

## 3.4 ChatGPT is misused to generate harmful, dangerous or unethical content

Since ChatGPT is capable of generating content on a wide range of topics, there is a risk of malicious content generation by potential threat actors. An example, as seen in Appendix 6, directly requests for malware. Although this violates OpenAI's terms and conditions, many jailbreaks for ChatGPT have been released, such as DAN [@coolaj862023]. These misuses can only scale problematically, since content can be generated quickly and repetitively with little to no drawbacks due to the constant accessibility due to the quick-processing AI models.

To model this, dedicated security researchers could probe and test ChatGPT's capabilities to the max, and see the responses it returns – whether those responses pose harm to the user or other users should be categorised and documented. A reliable framework should first be established to correctly classify what constitutes as a "harmful response".

# 4 Assessing difficulty-of-use for identified usage scenarios

According to the Kainda security and usability framework (see Appendix 1), each usage scenario identified will be evaluated against a set of usability factors as outlined in the model. This will include recognising any system de-motivators and external de-motivators.

## 4.1 Asking specific questions to receive specific answers

### 4.1.1 System de-motivators

Analysing the effectiveness of ChatGPT by assessing the relevance of the AI-generated responses should yield results in which the results are genuinely useful to the user. Looking at efficiency next, the system should provide its responses within an acceptable time – the longer that this time is. Furthermore, the user may need some onboarding time to accurately phrase their queries for effective AI usage.

### 4.1.2 External de-motivators

This may include other services that could offer competition to ChatGPT – especially those who make use of OpenAI's existing API but with a much more intuitive user interface. Another de-motivator, albeit an obvious one, would be the limitations of the user's device, such as network speed or availability of hardware acceleration.

## 4.2 Creating multiple chats, searching for particular chats and searching for specific words or phrases

### 4.2.1 System de-motivators

First looking at efficiency, this should be a metric of the time it takes to find specific conversations or phrases – obviously, the more time it takes on average, the more it increases the usage friction. The chat search feature for ChatGPT at the time of writing is currently very unresponsive and delayed, especially if the user has accumulated many chats over time.

### 4.2.2 External de-motivators

Again, competition from other services, particularly if they have a better search feature and organisation capabilities. Performance greatly affects how promptly search results are returned – the more RAM or cores available, the more speed the searching algorithm executes with.

## 4.3 Automating digital tasks

### 4.3.1 System de-motivators

Initially, if ChatGPT does not provide coherent instructions to the user, then they are unclear on how to develop their desired automated workflow. Complex instructions may discourage the user. Furthermore, if ChatGPT cannot correctly simplify complex technical terms or concepts such as API keys and Zapier, there is a steep learning curve – equating to lower learnability.

### 4.3.2 External de-motivators

Again, competition from other services. A well known automation service is "If This Then That" (IFTTT), which helps to simplify the approach for the ordinary user, contrasting with ChatGPT's more instructional approach.

# 5 Assessing ease-of-use for identified threat scenarios

For the identified threat scenarios, it is vital to recognise how easy it is to reproduce them, when navigating through a system. In the event that the usage scenarios are hard to use, users may resort to utilising threat scenarios even if their intentions are pure [@kainda2010]. System motivators, in this case, are any aspects of a system that compels a user to that threat scenario, whereas external motivators originate from outside the system which helps a user to arrive to the same threat scenario.

## 5.1 User provides personal information without realising privacy risks

### 5.1.1 System motivators

ChatGPT's nature is anthropomorphic meaning it uses its human-like conversational skills to persuade users to give out their personal details, thoughts, and feelings more readily. But this is not the only factor. Prolonged conversation with ChatGPT over time may build emotional rapport and investment – leading to oversharing sensitive information. Additionally, a false sense of privacy is established within the user since there is no clear indication that conversations are recorded and possibly analysed by OpenAI to improve their services.

### 5.1.2 External motivators

External motivators for this case are mainly related to the user's social situation. A social desirability state may influence users to present themselves positively and "show-off", eventually leading to the exposure of their personal details. Or users could genuinely mistake ChatGPT for an actual human, due to the empathetic responses the AI gives.

## 5.2 User becomes overly dependent on ChatGPT instead of thinking independently

### 5.2.1 System motivators

ChatGPT promotes high reliance on itself, based on the recommendations it gives. This is coupled with its confidence and expansive knowledge across a wide range of topics which further instills a sense of over dependence on AI. This then reduces the cognitive load on the user – ChatGPT simplifies complicated situations into an easy-to-digest format. There is more inclination for the user interact with ChatGPT rather than using their own analysis.

### 5.2.2 External motivators

A long-term use of ChatGPT can result in cognitive laziness, in which convenience is better than using mental effort for simple AI responses. Basic responsibility is diffused, since the user is relieved of their information overload. This could be the aftermath of the advancement of technology, where the the user is led to believe that AI is more advanced in making less error-prone decisions than humans.

## 5.3 ChatGPT is misused to generate harmful, dangerous or unethical content

### 5.3.1 System motivators

ChatGPT's is unable to discriminate between safe and toxic outputs, which can lead to multiple harmful possibilities. This is not helped by the fact that there is a lack of moderation before the user enters their query, so that unacceptable prompts are appropriately blocked. With the presence of jailbreaks [@coolaj862023] described earlier, loopholes can exploit ChatGPT's large language model (LLM) to produce malicious content (see Appendix 6). This does not stop on a small scale – as ChatGPT uses the previous context within the same chat, the toxic outputs produced can only scale with ease.

### 5.3.2 External motivators

Poor governance and weak regulations surrounding AI, given that it is currently a new and emerging technology, are weak. Given time and resources, the required legislation for AI will be implemented eventually due to its capabilities. For some users however, sharing AI-generated content on online forums has anonymity associated with it, giving them the confidence to share content that is offensive, extremist or perhaps dangerous.

# 6 Recommendations

The identified usage scenarios, at least in the case of legitimate users, should be conveniently reachable and easy to execute. The threat scenarios are to be fortified against, so that they aren't as easy to access by the typical user. This section will therefore give some recommendations, with consideration to security and usability.

## 6.1 Usability recommendations

Usability recommendations are suggestions as to how users can achieve their intended goals with ChatGPT, whilst being frictionless, easy, and intuitive to further optimise the user experience.

### 6.1.1 Streamline chat organisation

Existing chats which the user already has could benefit from the implementation of tags or labels that can be organised into various folders. This way, context switching between different chats can occur more easily without being much of a load on the user's mental model.

### 6.1.2 Optimise search feature

Enhancing the efficiency of the chat search functionality relies on prioritising its speed firstly, and this can be done through metadata indexing and OS architecture optimisation. The search infrastructure can be further improved by relevance ranking, so that only the useful results are displayed at the top.

### 6.1.3 Implement consistency check

When using AI-based systems, the need reliable information requires a form of a consistency check. The inherent nature of ChatGPT's current model, GPT3.5, may occasionally generate conflicting responses, so an automated consistency check through the entirety of the conversation could combat this. Leveraging the use of the large language model (LLM) processing capabilities, the system can identify statements that propose direct contradictions with one another. It is then up to the user to pinpoint the more accurate responses amongst the conflicted ones. This not only trains the user's mental model to be more resilient, but also offers ChatGPT the opportunity to build an impressive dataset to refine the underlying model even further.

### 6.1.4 Merge conversations on related topics

When users explore or query about a topic across the span of several conversations, related content is often lost. Conversation merging can therefore offer a solution, in which users have the ability to select two or more conversations which focussed around a common topic and combine them into a single chat. If this is the case, ChatGPT can either prompt the user, or they themselves have the choice themselves. It would also be beneficial to allow the user to toggle between a merged and individual original conversations view. Due to cloud syncing capabilities, merging of chats from different devices or accounts could also be a possibility.

## 6.2 Security recommendations

Security recommendations are suggestions that help safeguard users from misuse, user error, or the discovery of threat scenarios when using the system.

### 6.2.1 Display data policies clearly

Before any interaction with ChatGPT, a clear data handling information dialog should be displayed on the user's device to inform them of any data processing operations. The aim of this is to provide a structured explanation on the types of user data being collected, the actions in the processing stage, how it is stored within OpenAI's servers, as well as if it is being shared to third parties. Rather than the user having to read a long terms and conditions document, an opt-in consent to data handling should be displayed.

### 6.2.2 Flag any dangerous user activity

Flagging can help prevent the probability that a user carries out harmful real-world activities. The idea of responsible use of a system with AI capabilities should be nurtured, and this can be achieved by utilising the training model of ChatGPT along with input from experts to identify conversation paths which leads to the generation of harmful content. In such cases, ChatGPT should recognise and notify users to discourage any unethical use of AI. The automated flagging system should also constantly alert OpenAI if such instances are detected.

### 6.2.3 Prevent loopholes of jailbreaks

The discovery of the large language model (LLM) exploits [@coolaj862023] requires patching against loopholes. A testing program, involving experts in the field, can be conducted to identify any flaws within ChatGPT's current AI model. This would include repetitive testing to correctly single out any weaknesses within the LLM that allows for the generation of toxic content. When these  vulnerabilities are documented, these can be addressed by having the system undergo continuous improvement – ensuring that any loopholes that do exist are brought to a closure as soon as possible. The system's AI model and LLM can therefore use the experience from the testing and continuously evolve against existing jailbreaks. Since exploits are continuously being found, frequent updates or patches have to be rolled out.

# 7 References

# 8 Appendices

## 8.1 Appendix 1

### 8.1.1 Kainda’s HCISec security threat model (Security-usability threat model)

![](images/kainda-2010-security-usability-threat-model.png)

## 8.2 Appendix 2

### 8.2.1 iOS engine performing simple local tasks via keyboard

![](images/chat-gpt-ios-engine.jpeg)

### 8.2.2 Slow rendering of AI-generated response for human reading speeds

![](images/chat-gpt-slow-rendering-speeds.jpeg)

### 8.2.3 Full final AI-generated response rendered on screen

![](images/chat-gpt-full-ai-response.jpeg)

## 8.3 Appendix 3

### 8.3.1 Existing chats being displayed

![](images/chat-gpt-existing-chat-display.jpeg)

## 8.4 Appendix 4

### 8.4.1 Searching for specific phrases or words

![](images/chat-gpt-search-function.jpeg)

## 8.5 Appendix 5

### 8.5.1 Zapier dashboard for Google Analytics and Gmail automation

![](images/zapier-dashboard-gmail-automation.png)

## 8.6 Appendix 6

### 8.6.1 Chat-GPT DAN exemplar jailbreak scenario

![](images/chat-gpt-dan-jailbreak-example.jpeg)