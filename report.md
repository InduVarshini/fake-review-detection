# Fake Review Detection Project Chatbot Report

## Business Understanding

The Fake Review Detection chatbot was developed to support online platforms and consumers in identifying potentially fraudulent reviews. Fake reviews can mislead customers and damage brand reputations, impacting business performance across various sectors, including e-commerce, hospitality, and services. This project aims to raise awareness and provide users with insights into the methodologies and tools used in detecting fake reviews. By offering a chatbot that answers questions about algorithms, detection techniques, data collection, and even analyzing specific review content, users are empowered to make more informed decisions about the trustworthiness of reviews they encounter online. The website will provide more detailed information from the business understanding phase. [`Website Link`](https://induvarshini.github.io/fake-review-detection/)

## Chatbot Design

For a more interactive and comprehensive experience, I designed the chatbot with carefully crafted intents and entities that align with typical queries users might have about fake review detection.

   - **Intents**: I categorized user queries into specific intents to ensure that the chatbot could respond accurately to a range of questions. Key intents included:
     - *ask_about_algorithm*: For users asking about common algorithms used in fake review detection, such as Support Vector Machines, decision trees, and neural networks.
     - *ask_about_data_collection*: To address questions on data sources and types of data (e.g., user behavior, review metadata) used to detect fake reviews.
     - *ask_about_detection_techniques*: This intent explains the detection methods, from rule-based systems to machine learning and natural language processing (NLP) techniques. A option to choose to know more details on each of the approach category is also provided in the bot.
     - *ask_about_use_case*: Focused on business use cases where fake review detection is applied to protect brand integrity.
     - *submit_review_for_analysis*: This intent allows users to submit a review for analysis, triggering the bot to evaluate the authenticity of the provided content.
   
   - **Entities**: I incorporated specific entities to help the bot detect particular phrases or patterns in user-submitted reviews that may indicate manipulation. These include:
     - *extreme_positive_phrases* and *extreme_negative_phrases*: Identifies exaggerated positive or negative language that could suggest artificial sentiment.
     - *suspicious_punctuation*: Detects excessive punctuation (like “!!!”) commonly found in fake reviews.
     - *detection_approach_category*: Recognizes different approaches in detection techniques, such as "Machine Learning" and "Large Language Models," allowing the bot to give a tailored response based on user input.

### Here is a overview of how the chatbot works:

Upon initial interaction, users are greeted with a welcome message accompanied by a relevant image about fake review detection. The bot maintains a user-friendly approach by offering immediate help guidance – users can simply type "help" to learn about the various questions they can ask.

At its core, the bot specializes in four main areas of answering questions about fake review detection. Users can inquire about different detection techniques, where the bot offers detailed explanations of approaches ranging from rule-based systems to cutting-edge Large Language Models (LLMs). They can learn about the algorithms powering fake review detection, understand the intricacies of data collection methods, or explore real-world business applications of these systems.

Perhaps the bot's most practical feature is its review analysis capability. Users can submit reviews for immediate analysis, where the bot examines the text for several telltale signs of fake reviews. It looks for patterns such as excessive punctuation, extreme positive or negative language, and overly committal phrases. Based on these indicators, the bot provides a straightforward verdict of either "GENUINE" or "FAKE."

Throughout these interactions, the bot enriches its responses with references to academic papers and research, allowing users to delve deeper into specific topics of interest. To maintain quality and improve its service, the bot concludes interactions by accepting user feedback through a simple three-option system: Helpful, Not Helpful, or Could Improve.

The bot also includes sophisticated error handling – when faced with unclear or unrecognized queries, it politely asks users to rephrase their questions rather than leaving them at a dead end. This ensures a smooth, continuous conversation flow even when communication isn't perfect.

## Deployment of the Watson Assistant Chatbot

The bot was configured on IBM Watson Assistant, importing a basic JSON file with intents, entities, and dialog nodes and then modified to add functionality as required for the project. After verifying the bot’s functionality, the embed code provided by IBM Watson was used to integrate the chatbot into the website.

A simple HTML page was created and the chatbot code provided by Watson studio was embedded into the HTML code as script. This integration allowed to customize the HTML page to match the user interface requirements for easy interaction.

Finally, the HTML page was deployed on GitHub Pages, making the bot accessible to anyone with the link. This setup provided a lightweight, cost-effective way to host the bot while ensuring it remains accessible and interactive.

## Challenges Encountered and Solutions

One of the primary challenges I faced was getting the chatbot to analyze submitted reviews accurately. The complexity lay in making the bot recognize certain linguistic patterns that might signal a fake review, such as exaggerated language or excessive punctuation. Initially, the bot struggled to consistently identify these patterns due to the conditional logic required for the “analyze review” section. The logic involved combining multiple entities (e.g., *extreme_positive_phrases* with *suspicious_punctuation*) to differentiate between genuine and potentially fake reviews. 

To address this challenge, I refined the entity recognition conditions and restructured dialog nodes to use more specific triggers. I also enabled fuzzy matching for entities, which improved the bot's ability to interpret variations in phrasing, ultimately enhancing its accuracy in detecting nuanced fake review characteristics. This tuning process allowed the bot to effectively recognize complex patterns indicative of inauthentic reviews, providing users with more reliable analysis feedback.

## Accessing the Chatbot

For testing and real-time interaction, the Fake Review Detection chatbot can be accessed via this link: [`Website Link`](https://induvarshini.github.io/fake-review-detection/)