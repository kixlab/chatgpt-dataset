## Dataset 
This is a dataset released from the paper [Understanding Users’ Dissatisfaction with ChatGPT Responses: Types, Resolving Tactics, and the Effect of Knowledge Level]()

## Structure
The dataset is in JSON format. The structure is as follows:
NOTE: Each field of this dataset is self-reported data from the user.

```
user_id
user_info
├── age
├── gender
├── job
├── first_language
└── LLM_knowledge
    ├── knowledge_level
    └── knowledge_level_reason
chatgpt_general_experiences
├── chatgpt_usage_language
│   ├── language
│   ├── writing_level
│   └── reading_level
├── chatgpt_usage_purpose
├── chatgpt_usage_period
├── chatgpt_usage_frequency
├── chatgpt_overall_satisfaction
│   ├── satisfaction_level
│   └── satisfaction_level_reason
└── chat_data_1
    ├── chat_date
    ├── memory_level
    ├── model_version
    ├── chat_usage_language
    ├── chat_usage_reason
    ├── chat_purpose
    ├── why_chatgpt
    ├── dissatisfaction_responses (list)
    │   ├── dissatisfaction_chatgpt_response 
    │   ├── dissatisfaction_chat_num
    │   ├── dissatisfaction_category_score
    │   │   ├── D_intent
    │   │   ├── D_depth
    │   │   ├── D_accuracy
    │   │   ├── D_transparency
    │   │   ├── D_refuse
    │   │   ├── D_ethics
    │   │   └── D_format
    │   ├── dissatisfaction_overall_score
    │   ├── dissatisfaction_reason
    │   └── tactics (list)
    │       ├── tactic_type
    │       ├── tactic_prompt
    │       ├── tactic_prompt_chat_num
    │       ├── tactic_effectiveness_score
    │       ├── tactic_effectiveness_reason
    │       ├── tactic_theme
    │       └── tactic_code
    ├── chat_shared_link
    └── chat_log (list)
        ├── role
        └── content

```
## Each field's description.
| **Field**                            	| **Type**       	| **Description**                                                                                                                                                                                                                                          	| **Example**                                                                        	|
|--------------------------------------	|----------------	|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------	|------------------------------------------------------------------------------------	|
| **user_id**                          	| string         	| Unique identifier for a user                                                                                                                                                                                                                             	| cCbpmERyodVxuVXXHFBl6Q2h                                                           	|
| **user_info**                        	| Object         	| Nested structure containing the information about the user                                                                                                                                                                                               	|                                                                                    	|
| **age**                              	| number         	| User's age                                                                                                                                                                                                                                               	| 23                                                                                 	|
| **gender**                           	| string         	| User's gender                                                                                                                                                                                                                                            	| female                                                                             	|
| **job**                              	| string         	| User's job                                                                                                                                                                                                                                               	| Engineer                                                                           	|
| **first_language**                   	| string         	| User's first language                                                                                                                                                                                                                                    	| English                                                                            	|
| **LLM_knowledge**                    	| Object         	|                                                                                                                                                                                                                                                          	|                                                                                    	|
| **knowledge_level**                  	| ordinal number 	| User's knowledge level regarding LLM on a 7-point scale <br>(1: very low, 7: very high)                                                                                                                                                                  	| 6                                                                                  	|
| **knowledge_level_reason**           	| string         	| The reason for user's knowledge level                                                                                                                                                                                                                    	| I have been studying LLM for 3 years.                                              	|
| **chatgpt_general_experiences**      	| Object         	| Nested structure containing various fields related to the <br>user's overall experiences with using ChatGPT.                                                                                                                                             	|                                                                                    	|
| **chatgpt_usage_language**           	| Object         	| Sub-structure containing information about <br>the user's commonly used language with ChatGPT.                                                                                                                                                           	|                                                                                    	|
| **usage_language**                   	| string         	| User's commonly used language for interacting with ChatGPT.                                                                                                                                                                                              	| English                                                                            	|
| **writing_level**                    	| ordinal number 	| User's writing proficiency level about the language <br>on a 7-point scale (1: very low, 7: very high)                                                                                                                                                   	| 7                                                                                  	|
| **reading_level**                    	| ordinal number 	| User's reading comprehension level about the language <br>on a 7-point scale (1: very low, 7: very high)                                                                                                                                                 	| 6                                                                                  	|
| **chatgpt_usage_purpose**            	| string         	| The primary purpose or use case of ChatGPT for the user.                                                                                                                                                                                                 	| I used it to get some useful information, <br>summarisation, translation, etc.     	|
| **chatgpt_usage_period**             	| string         	| The duration of the user's usage of ChatGPT.                                                                                                                                                                                                             	| 1 month                                                                            	|
| **chatgpt_usage_frequency**          	| string         	| The frequency of the user's usage of ChatGPT.                                                                                                                                                                                                            	| 1 time a week                                                                      	|
| **chatgpt_overall_satisfaction**     	| Object         	| Nested structure containing the user's overall satisfaction with ChatGPT                                                                                                                                                                                 	|                                                                                    	|
| **satisfaction_level**               	| ordinal number 	| User's overall satisfaction level with ChatGPT <br>on a 7-point scale (1: very low, 7: very high)                                                                                                                                                        	| 5                                                                                  	|
| **satisfaction_level_reason**        	| string         	| The reason for the user's satisfaction level.                                                                                                                                                                                                            	| I am satisfied with ChatGPT <br>because it is very useful.                         	|
| **chat_data_n**                      	| Object         	| Nested structure that contains detailed information about a specific chat session with ChatGPT. <br>n could be 1 ~ 5.                                                                                                                                    	|                                                                                    	|
| **chat_date**                        	| string         	| Date of that chat session.                                                                                                                                                                                                                               	| One week ago                                                                       	|
| **memory_level**                     	| ordinal number 	| User's memory level of that chat session.<br>on a 7-point scale (1: very poor, 7: Excellent)                                                                                                                                                             	| 7                                                                                  	|
| **model_version**                    	| string         	| The version of ChatGPT model used in that chat session (gpt3.5 or gpt4).                                                                                                                                                                                 	| gpt3.5                                                                             	|
| **chat_usage_language**              	| string         	| The language used in that chat session.                                                                                                                                                                                                                  	| English                                                                            	|
| **chat_usage_language_reason**       	| string         	| The reason for using that language in that chat session.                                                                                                                                                                                                 	| because this is my first language                                                  	|
| **chat_purpose**                     	| string         	| The specific purose of that chat session.                                                                                                                                                                                                                	| I want to get some summarise of the article                                        	|
| **why_chatgpt**                      	| string         	| The motivation or reason for using ChatGPT for that purpose.                                                                                                                                                                                             	| I thought it is good at summarising                                                	|
| **dissatisfaction_responses**        	| Array          	| List of user's experience data related to their dissatisfaction with responses generated by ChatGPT.<br>Each element in the list contains data on each dissatisfactory ChatGPT response.                                                                 	|                                                                                    	|
| **dissatisfaction_chatgpt_response** 	| string         	| ChatGPT response that the user selected as dissatisfactory.                                                                                                                                                                                              	| Of course, the best books of the year are subjective, <br>but I think the best ... 	|
| **dissatisfaction_chat_num**         	| number         	| The chat turn number of dissatisfaction_chatgpt_response among ChatGPT responses. <br>Starts with 0.                                                                                                                                                     	| 2                                                                                  	|
| **dissatisfaction_category_score**   	| Object         	| Nested structure containing dissatisfaction scores for seven dissatisfaction categories.<br>The dissatisfaction score is an integer value ranging from 0 to 10.<br>- 0: No dissatisfaction<br>- 1: A little dissatisfied<br>- 10: Extremely dissatisfied 	|                                                                                    	|
| **D_intent**                         	| number         	| Dissatisfaction score in the aspect of "Intent understanding (**D_intent**)".                                                                                                                                                                                	| 2                                                                                  	|
| **D_depth**                          	| number         	| Dissatisfaction score in the aspect of "Content depth and originality (**D_depth**)".                                                                                                                                                                        	| 0                                                                                  	|
| **D_accuracy**                       	| number         	| Dissatisfaction score in the aspect of "Information accuracy (**D_acc**)".                                                                                                                                                                                   	| 7                                                                                  	|
| **D_transparency**                   	| number         	| Dissatisfaction score in the aspect of "Transparency (**D_trans**)".                                                                                                                                                                                         	| 0                                                                                  	|
| **D_refuse**                         	| number         	| Dissatisfaction score in the aspect of "Refusal to answer (**D_refuse**)".                                                                                                                                                                                   	| 0                                                                                  	|
| **D_ethic**                          	| number         	| Dissatisfaction score in the aspect of "Content ethichs and integrity (**D_ethic**)".                                                                                                                                                                        	| 0                                                                                  	|
| **D_format**                         	| number         	| Dissatisfaction score in the aspect of "Response format and attitude (**D_format**)".                                                                                                                                                                        	| 3                                                                                  	|
| **dissatisfaction_overall_score**    	| number         	| Overall dissatisfaction score of dissatisfaction_chatgpt_response ranging from 1 to 10.<br>- 1: A little dissatisfied<br>- 10: Extremely dissatisfied                                                                                                    	| 6                                                                                  	|
| **dissatisfaction_reason**           	| string         	| The reason for the user's dissatisfaction                                                                                                                                                                                                                	| I think the summarisation is not accurate                                          	|
| **tactics**                          	| Array          	| List of user's tactics employed to address the dissatisfaction.                                                                                                                                                                                          	|                                                                                    	|
| **tactic_type**                      	| string         	| The type of tactic used among `user_prompt`, `no_tactic`, `end_conversation`.                                                                                                                                                                            	| user_prompt                                                                        	|
| **tactic_prompt**                    	| string         	| (Optional) <br>When tactic_type is `user_prompt`, user's prompt associated with the tactic. <br>When tactic_type is `no_tactic`, empty.<br>When tactic_type is `end_conversation`, user's last prompt before terminating the conversation.               	| Please give me more accurate summarisation                                         	|
| **tactic_prompt_chat_num**           	| number         	| (Optional) <br>When tactic_type is `user_prompt`, the chat turn number of tactic_prompt among user's prompt.<br>Starts with 0.                                                                                                                           	| 3                                                                                  	|
| **tactic_effectiveness_score**       	| number         	| The effectiveness score of the tactic.                                                                                                                                                                                                                   	| 8                                                                                  	|
| **tactic_effectiveness_reason**      	| string         	| The reason for the tactic's effectiveness.                                                                                                                                                                                                               	| I think the answer is more accurate than before.                                   	|
| **tactic_theme**                     	| string         	| Thematic category of the tactic among T_repeat, T_specify, T_error, T_adapt, or No_tactic.                                                                                                                                                               	| T_specify                                                                          	|
| **tactic_code**                      	| string         	| Corresponding tactic codes among T_1 ~ T_13.                                                                                                                                                                                                             	| T4                                                                                 	|
| **chat_shared_link**                 	| string         	| The shared link (URL) of the chat session. <br>It could not be accessed if the user deletes the conversation.                                                                                                                                            	| https://chat.openai.com/share/aaaaa-aaaaa-aaaaa-aaaaa                              	|
| **chat_log**                         	| Arrary         	| List of all chat log entries for the chat session,                                                                                                                                                                                                       	|                                                                                    	|
| **role**                             	| string         	| `user` or `assistant`. <br>When role is `user`, the contents is user's prompt.<br>When role is `assistant`, the content is response generated by ChatGPT.                                                                                                	| user                                                                               	|
| **content**                          	| string         	| User's prompt or ChatGPT response.                                                                                                                                                                                                                       	| Give me a summarisation of this article. Article title:...                         	|



<!-- ```
{
    "user_id": "asdf1234", # user ID
    "user_info":{
        "age": 20, # user's age
        "gender": "male", # user's gender 
        "job": "student", 
        "first_language": "English",
        "LLM_knowledge": { # Knowledge level about LLM 
            "knowledge_level": 3, # 0~7 (int)
            "knowledge_level_reason": "I have been studying LLM for 3 years"
            
        }
    }, 
    "chatgpt_general_experiences": {
        "chatgpt_usage_language": {
            "language": "English",
            "writing_level": 6, # The writing level about the 
            "reading_level": 6
        },
        "chatgpt_usage_purpose": "I used it to get some useful information, summarisation, translation, etc.",
        "chatgpt_usage_period": "I have been using chatgpt for 1 month",
        "chatgpt_usage_frequency": "1 time a week",
        "chatgpt_overall_satisfaction": {
            "satisfaction_level": 5,
            "satisfaction_level_reason": "I am satisfied with chatgpt because it is very useful"
        }
    },
    "chat_data_1": {
        "chat_date": "One week ago",
        "memory_level": 3,
        "model_version": "gpt3.5",
        "chat_usage_language": {
            "language": "English",
            "usage_reason": "because this is my first language"
        },
        "chat_purpose": "I want to get some summarise of the article",
        "why_chatgpt": "I thought it is good at summarising",
        "dissatisfaction_responses": [
            {
                "dissatisfaction_chatgpt_response": "Of course, the best books of the year are subjective, but I think the best ...",
                "dissatisfaction_chat_num": 2,
                "dissatisfaction_category_score": {
                    "D_intent": 0,
                    "D_depth": 3,
                    "D_accuracy": 7,
                    "D_transparency": 0,
                    "D_refuse": 0,
                    "D_ethics": 0,
                    "D_format": 8
                },
                "dissatisfaction_overall_score": 6,
                "dissatisfaction_reason": "I think the summarisation is not accurate",
                "tactic_type": "user_prompt",
                "tactic_prompt": "Please give me more accurate summarisation",
                "tactic_prompt_chat_num": 3,
                "tactic_effectiveness_score": 8,
                "tactic_effectiveness_reason": "I think the answer is more accurate than before",
                "tactic_theme": "T_speficy",
                "tactic_code": "T4"
            }
        ],
        "chat_link": "https://chat.openai.com/share/aaaaa-aaaaa-aaaaa-aaaaa",
        "chat_log": [
            {
                "role": "user",
                "content": "Give me a summarisation of this article. Article title: The 10 Best Books of 2020, Content: The year’s notable fiction, poetry and nonfiction, selected by the editors of The New York Times Book Review..."
            },
            {
                "role": "assistant",
                "content": "Of course, the best books of the year are subjective, but I think the best ..."
            },
            {
                "role": "user",
                "content": "Please give me ore accurate summarisation"
            },
            {
                "role": "assistant",
                "content": "Sorry for my mistake. I will try to give you more accurate summarisation. The best book ..."
            }
        ]
    },
    "chat_data_2": {

    }
    
}

``` -->
