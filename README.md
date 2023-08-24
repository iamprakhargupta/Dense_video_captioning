# Exploring LLMs for Recipe summarization from Cooking Videos

As someone who loves cooking as well as making videos of them, it's
really painful writing step-by-step instructions for cooking. Also at
times we often try to look for a few points of how to make a dish
rather than watch the whole video which at times has filler content
leading us to watch it multiple times(honestly I have done this so
many times that I have lost track of it). I would like to use the
summarization power of these llms and explore this use case in detail.

Plan of Action:

Data Collection: Gather a diverse dataset of YouTube cooking videos
encompassing various cuisines - A dataset called You Cook 2 exists. I
am in talks with the authors for the videos. They already have the
annotations on the website

Preprocessing: Clean and format the collected data for training and
evaluation purposes. Since these videos have both audio and visual
clues associated with them I want to experiment with some networks
here using a speech-to-text network and feeding the result of them to
the chosen llm. Another experiment is to use an image-to-text model
like CLIP(currently experimenting with it) on frames of the video and
feed them to the LLM along with the combination of both speech and
visual clues

Model Selection and Fine-tuning: Experiment with llms (Llama2, Flan5)
models to identify the most suitable architecture for dense
captioning. So the short summary of this idea is that since llm are
really good in summary generation I want to use them for creating a
step-by-step recipe guide. The idea here is that the LLM can be
fine-tuned to summarise the critical idea from various modalities
provided to it. I would like to fine-tune my LLM at this step on the
preprocessed data.

Evaluation: Develop evaluation metrics to assess the quality and
accuracy of the generated recipe guide. Currently, I am exploring this
topic more and looking into the feasibility of using BLEU or ROUGE
metrics to test against the hand-annotated recipe

Iterative Refinement: Continuously refine the model and evaluation
process based on feedback and results from both my observation and
your guidance

Code will be committed once each part of the work in being done
