## Installation : Success

### [Prerequsites](https://aios.readthedocs.io/en/latest/get_started/installation.html#prerequsites) : Met 

* Anaconda 

* Python: 3.9-3.11 :: 3.11

* Git : Y


### Build from source[#](https://aios.readthedocs.io/en/latest/get_started/installation.html#build-from-source "Permalink to this heading")

```bash
# Prep: Git Enabled
# ---
(base) dp@P920:~/Documents/GitHub/AIOS$ ll
total 20
drwxrwxr-x 3 dp dp 4096 Aug 24 17:48 ./
drwxrwxr-x 3 dp dp 4096 Aug 24 17:45 ../
drwxrwxr-x 8 dp dp 4096 Aug 24 17:45 .git/
-rw-rw-r-- 1 dp dp   66 Aug 24 17:45 .gitattributes
-rw-rw-r-- 1 dp dp  137 Aug 24 17:49 installation_with_ollama.md
```

Git clone AIOS repository

```bash
# Created conda environment
# ---
(base) dp@P920:~/Documents/GitHub/AIOS$ conda create -n aios python=3.11
...
Preparing transaction: done
Verifying transaction: done
Executing transaction: done
#
# To activate this environment, use
#
#     $ conda activate aios
#
# To deactivate an active environment, use
#
#     $ conda deactivate

# Cloned source resository
# ---
(base) dp@P920:~/Documents/GitHub/AIOS$ git clone https://github.com/agiresearch/AIOS.git
Cloning into 'AIOS'...
remote: Enumerating objects: 3110, done.
remote: Counting objects: 100% (872/872), done.
remote: Compressing objects: 100% (367/367), done.
remote: Total 3110 (delta 649), reused 557 (delta 501), pack-reused 2238 (from 1)
Receiving objects: 100% (3110/3110), 3.24 MiB | 12.03 MiB/s, done.
Resolving deltas: 100% (1682/1682), done.

(base) dp@P920:~/Documents/GitHub/AIOS$ ll
total 24
drwxrwxr-x  4 dp dp 4096 Aug 24 17:57 ./
drwxrwxr-x  3 dp dp 4096 Aug 24 17:45 ../
drwxrwxr-x 12 dp dp 4096 Aug 24 17:57 AIOS/
drwxrwxr-x  8 dp dp 4096 Aug 24 17:45 .git/
-rw-rw-r--  1 dp dp   66 Aug 24 17:45 .gitattributes

## Activated conda
(base) dp@P920:~/Documents/GitHub/AIOS$ conda activate aios
```

Install from requirements-cuda.txt if you have cuda environment
```
(aios) dp@P920:~/Documents/GitHub/AIOS$ cd AIOS/
(aios) dp@P920:~/Documents/GitHub/AIOS/AIOS$ pip install -r requirements-cuda.txt
Collecting google-generativeai (from -r requirements.txt (line 1))
  Using cached google_generativeai-0.7.2-py3-none-any.whl.metadata (4.0 kB)
Collecting openai==1.20.0 (from -r requirements.txt (line 2))
  Using cached openai-1.20.0-py3-none-any.whl.metadata (21 kB)
  ...
  ...
ferencing-0.35.1 regex-2024.7.24 requests-2.32.3 rpds-py-0.20.0 rsa-4.9 safetensors-0.4.4 sentencepiece-0.2.0 six-1.16.0 sniffio-1.3.1 starlette-0.38.2 sympy-1.13.2 tiktoken-0.7.0 tokenizers-0.19.1 torch-2.4.0 torchvision-0.19.0 tqdm-4.66.5 transformers-4.44.2 triton-3.0.0 typing-extensions-4.12.2 tzdata-2024.1 uritemplate-4.1.1 urllib3-2.2.2 uvicorn-0.30.6 uvloop-0.20.0 vllm-0.5.4 vllm-flash-attn-2.6.1 watchfiles-0.23.0 websockets-13.0 xformers-0.0.27.post2 xxhash-3.5.0 yarl-1.9.4 zipp-3.20.0
(aios) dp@P920:~/Documents/GitHub/AIOS/AIOS$  
```

## Quickstart

### Use with ollama
```

### Using with Ollama
```bash
(aios) dp@P920:~/Documents/GitHub/AIOS/AIOS$ ollama serve
2024/08/24 19:29:05 routes.go:1125: INFO server config env="map[CUDA_VISIBLE_DEVICES: GPU_DEVICE_ORDINAL: HIP_VISIBLE_DEVICES: HSA_OVERRIDE_GFX_VERSION: OLLAMA_DEBUG:false OLLAMA_FLASH_ATTENTION:false OLLAMA_HOST:http://127.0.0.1:11434 OLLAMA_INTEL_GPU:false OLLAMA_KEEP_ALIVE:5m0s OLLAMA_LLM_LIBRARY: OLLAMA_MAX_LOADED_MODELS:0 OLLAMA_MAX_QUEUE:512 OLLAMA_MODELS:/home/dp/.ollama/models OLLAMA_NOHISTORY:false OLLAMA_NOPRUNE:false OLLAMA_NUM_PARALLEL:0 OLLAMA_ORIGINS:[http://localhost https://localhost http://localhost:* https://localhost:* http://127.0.0.1 https://127.0.0.1 http://127.0.0.1:* https://127.0.0.1:* http://0.0.0.0 https://0.0.0.0 http://0.0.0.0:* https://0.0.0.0:* app://* file://* tauri://*] OLLAMA_RUNNERS_DIR: OLLAMA_SCHED_SPREAD:false OLLAMA_TMPDIR: ROCR_VISIBLE_DEVICES:]"
time=2024-08-24T19:29:05.776-04:00 level=INFO source=images.go:782 msg="total blobs: 0"
time=2024-08-24T19:29:05.776-04:00 level=INFO source=images.go:790 msg="total unused blobs removed: 0"
time=2024-08-24T19:29:05.777-04:00 level=INFO source=routes.go:1172 msg="Listening on 127.0.0.1:11434 (version 0.3.6)"
time=2024-08-24T19:29:05.778-04:00 level=INFO source=payload.go:30 msg="extracting embedded files" dir=/tmp/ollama903725205/runners
time=2024-08-24T19:29:13.543-04:00 level=INFO source=payload.go:44 msg="Dynamic LLM libraries [cpu cpu_avx cpu_avx2 cuda_v11 rocm_v60102]"
time=2024-08-24T19:29:13.543-04:00 level=INFO source=gpu.go:204 msg="looking for compatible GPUs"
time=2024-08-24T19:29:13.747-04:00 level=INFO source=types.go:105 msg="inference compute" id=GPU-f14cca0f-a072-da5f-cb18-c6e58dd9e7b0 library=cuda compute=8.6 driver=12.2 name="NVIDIA RTX A4000" total="15.7 GiB" available="13.9 GiB"
[GIN] 2024/08/24 - 19:30:07 | 200 |     134.814µs |       127.0.0.1 | HEAD     "/"
time=2024-08-24T19:30:09.228-04:00 level=INFO source=download.go:175 msg="downloading 6a0746a1ec1a in 47 100 MB part(s)"

```

```bash
(aios) dp@P920:~/Documents/GitHub/AIOS/AIOS$ ollama pull llama3:8b
pulling manifest 
pulling 6a0746a1ec1a...   1% ▕█                                    ppulpulling manifppulling manifest  pulling pulpulling mapulling manifest 
pulling 6a0746a1ec1a... 100% ▕████████████████████████████████████████████████████████████▏ 4.7 GB                         
pulling 4fa551d4f938... 100% ▕████████████████████████████████████████████████████████████▏  12 KB                         
pulling 8ab4849b038c... 100% ▕████████████████████████████████████████████████████████████▏  254 B                         
pulling 577073ffcc6c... 100% ▕████████████████████████████████████████████████████████████▏  110 B                         
pulling 3f8eb4da87fa... 100% ▕████████████████████████████████████████████████████████████▏  485 B                         
verifying sha256 digest 
writing manifest 
removing any unused layers 
success 
(aios) dp@P920:~/Documents/GitHub/AIOS/AIOS$ 

```

```bash
(aios) dp@P920:~/Documents/_POCs/AIOS/AIOS$ python main.py --llm_name ollama/llama3:8b --use_backend ollama --max_gpu_memory '{"0": "24GB"}' --eval_device "cuda:0" --max_new_tokens 256
[🤖ollama/llama3:8b] AIOS LLM successfully loaded.

Traceback (most recent call last):
....

[Scheduler] example/academic_agent is executing. 

[🤖ollama/llama3:8b] example/academic_agent is switched to executing.

[example/cook_therapist] Initialized. 

[example/cook_therapist] Develop a low-carb, keto-friendly dinner that is flavorful and satisfying.

[example/cook_therapist] Generated workflow is: [{'message': 'Gather user input on desired ingredients, dietary restrictions, or cuisine type.', 'tool_use': []}, {'message': 'Create a detailed recipe, including ingredients, measurements, and step-by-step instructions.', 'tool_use': []}, {'message': 'Generate an image of the final dish.', 'tool_use': ['text_to_image']}, {'message': 'Present the recipe, including image, instructions, and nutritional information.', 'tool_use': []}]

[Scheduler] example/academic_agent is executing. 

[🤖ollama/llama3:8b] example/academic_agent is switched to executing.

[example/academic_agent] At step 1, Let's start with gathering research topics and keywords.

**Research Topic:** I'm going to focus on "Emerging Technologies in Education" as it's a relevant and current theme that can be explored further.

**Keywords:**

* EdTech
* Innovative Learning Methods
* AI-powered Educational Tools
* Gamification in Education
* Personalized Learning

These keywords will serve as a foundation for searching and finding relevant research papers on arXiv, the next step!

Your turn! What would you like to explore within this topic?

[Scheduler] example/cook_therapist is executing. 

[🤖ollama/llama3:8b] example/cook_therapist is switched to executing.

[example/academic_agent] At step 1, **Step 1: Gather research topic and keywords**

To gather relevant research papers on the impact of social media on mental health in adolescents, I'll define a clear research topic and extract relevant keywords.

Research Topic: "The Impact of Social Media on Mental Health in Adolescents"

Keywords:

* Social media
* Mental health
* Adolescents (or teenage years)
* Online behaviors
* Anxiety
* Depression
* Self-esteem
* Peer relationships

These keywords will help me search for papers that focus on the relationship between social media use and mental health outcomes in adolescents.

Next step: Search for relevant papers on arXiv!

**Tool used:** None (just thinking)

Let me know when you're ready for me to proceed to the next step!

[Scheduler] example/academic_agent is executing. 

[🤖ollama/llama3:8b] example/academic_agent is switched to executing.

[example/cook_therapist] At step 1, Let's gather some information from you.

**Low-Carb, Keto-Friendly Dinner Preferences**

To create a personalized recipe for you, please share your preferences:

1. **Dietary Restrictions:**
        * Gluten-free
        * Dairy-free (or can tolerate dairy)
2. **Cuisine Type:** (Choose one or more)
        * Italian
        * Mexican
        * Asian-inspired
        * Mediterranean
3. **Meat Preferences:** (Select one or more)
        * Beef
        * Pork
        * Chicken
        * Seafood (e.g., salmon, shrimp)
4. **Vegetable Preferences:** (Choose your top 2-3 favorite vegetables)
5. **Spice Level:** (Scale of 1-5, where 1 is mild and 5 is very spicy)
6. **Specific Ingredient Requests:** (Any ingredients you'd like to include or avoid)

Please share your preferences, and I'll create a unique recipe for you!

[Scheduler] example/academic_agent is executing. 

[🤖ollama/llama3:8b] example/academic_agent is switched to executing.

[example/academic_agent] At step 2, [Action]: I will call the arxiv with the params as {'query': 'EdTech OR Innovative Learning Methods OR AI-powered Educational Tools OR Gamification in Education OR Personalized Learning'}. [Observation]: The output of calling the arxiv tool is: Published: 2023-09-05
Title: Personalization, Cognition, and Gamification-based Programming Language Learning: A State-of-the-Art Systematic Literature Review
Authors: Kashif Ishaq, Atif Alvi
Summary: Programming courses in computing science are important because they are often
the first introduction to computer programming for many students. Many
university students are overwhelmed with the information they must learn for an
introductory course. The current teacher-lecturer model of learning commonly
employed in university lecture halls often results in a lack of motivation and
participation in learning. Personalized gamification is a pedagogical approach
that combines gamification and personalized learning to motivate and engage
students while addressing individual differences in learning. This approach
integrates gamification and personalized learning strategies to inspire and
involve students while addressing their unique learning needs and differences.
A comprehensive literature search was conducted by including 81 studies that
were analyzed based on their research design, intervention, outcome measures,
and quality assessment. The findings suggest that personalized gamification can
enhance student cognition in programming courses by improving motivation,
engagement, and learning outcomes. However, the effectiveness of personalized
gamification varies depending on various factors, such as the type of
gamification elements used, the degree of personalization, and the
characteristics of the learners. This paper provides insights into designing
and implementing effective personalized gamification interventions in
programming courses. The findings could inform educational practitioners and
researchers in programming education about the potential benefits of
personalized gamification and its implications for educational practice.

Published: 2021-04-18
Title: Co-Creation of Innovative Gamification Based Learning: A Case of Synchronous Partnership
Authors: Nicholas Dacre, Vasilis Gkogkidis, Peter Jenkins
Summary: In higher education, gamification offers the prospect of providing a pivotal
shift from traditional asynchronous forms of engagement, to developing methods
to foster greater levels of synchronous interactivity and partnership between
and amongst teaching and learning stakeholders. The small vein of research that
focuses on gamification in teaching and learning contexts, has mainly focused
on the implementation of pre-determined game elements. This approach reflects a
largely asynchronous approach to the development of learning practices in
educational settings, thereby limiting stakeholder engagement in their design
and adoption. Therefore, we draw on the theory of co-creation to examine the
development process of gamification-based learning as a synchronous partnership
between and amongst teaching and learning stakeholders. Empirical insights
suggest that students gain a greater sense of partnership and inclusivity as
part of a synchronous co-creation gamification-based learning development and
implementation process.

Published: 2020-04-07
Title: Computers in Secondary Schools: Educational Games
Authors: Margarida Romero
Summary: This entry introduces educational games in secondary schools. Educational
games include three main types of educational activities with a playful
learning intention supported by digital technologies: educational serious
games, educational gamification, and learning through game creation.
Educational serious games are digital games that support learning objectives.
Gamification is defined as the use of "game design elements and game thinking
in a non-gaming context" (Deterding et al. 2011, p. 13). Educational
gamification is not developed through a digital game but includes game elements
for supporting the learning objectives. Learning through game creation is
focused on the process of designing and creating a prototype of a game to
support a learning process related to the game creation proc

[Scheduler] example/cook_therapist is executing. 

[🤖ollama/llama3:8b] example/cook_therapist is switched to executing.

[example/academic_agent] At step 2, [Action]: I will call the arxiv with the params as {'query': '((social media) AND (mental health) AND (adolescents OR teenage years)) AND NOT ((video games) OR (gaming))'}. [Observation]: The output of calling the arxiv tool is: Published: 2017-04-30
Title: Quantifying Mental Health from Social Media with Neural User Embeddings
Authors: Silvio Amir, Glen Coppersmith, Paula Carvalho, Mário J. Silva, Byron C. Wallace
Summary: Mental illnesses adversely affect a significant proportion of the population
worldwide. However, the methods traditionally used for estimating and
characterizing the prevalence of mental health conditions are time-consuming
and expensive. Consequently, best-available estimates concerning the prevalence
of mental health conditions are often years out of date. Automated approaches
to supplement these survey methods with broad, aggregated information derived
from social media content provides a potential means for near real-time
estimates at scale. These may, in turn, provide grist for supporting,
evaluating and iteratively improving upon public health programs and
interventions.
  We propose a novel model for automated mental health status quantification
that incorporates user embeddings. This builds upon recent work exploring
representation learning methods that induce embeddings by leveraging social
media post histories. Such embeddings capture latent characteristics of
individuals (e.g., political leanings) and encode a soft notion of homophily.
In this paper, we investigate whether user embeddings learned from twitter post
histories encode information that correlates with mental health statuses. To
this end, we estimated user embeddings for a set of users known to be affected
by depression and post-traumatic stress disorder (PTSD), and for a set of
demographically matched `control' users. We then evaluated these embeddings
with respect to: (i) their ability to capture homophilic relations with respect
to mental health status; and (ii) the performance of downstream mental health
prediction models based on these features. Our experimental results demonstrate
that the user embeddings capture similarities between users with respect to
mental conditions, and are predictive of mental health.

Published: 2024-08-04
Title: Representation Bias of Adolescents in AI: A Bilingual, Bicultural Study
Authors: Robert Wolfe, Aayushi Dangol, Bill Howe, Alexis Hiniker
Summary: Popular and news media often portray teenagers with sensationalism, as both a
risk to society and at risk from society. As AI begins to absorb some of the
epistemic functions of traditional media, we study how teenagers in two
countries speaking two languages: 1) are depicted by AI, and 2) how they would
prefer to be depicted. Specifically, we study the biases about teenagers
learned by static word embeddings (SWEs) and generative language models (GLMs),
comparing these with the perspectives of adolescents living in the U.S. and
Nepal. We find English-language SWEs associate teenagers with societal
problems, and more than 50% of the 1,000 words most associated with teenagers
in the pretrained GloVe SWE reflect such problems. Given prompts about
teenagers, 30% of outputs from GPT2-XL and 29% from LLaMA-2-7B GLMs discuss
societal problems, most commonly violence, but also drug use, mental illness,
and sexual taboo. Nepali models, while not free of such associations, are less
dominated by social problems. Data from workshops with N=13 U.S. adolescents
and N=18 Nepalese adolescents show that AI presentations are disconnected from
teenage life, which revolves around activities like school and friendship.
Participant ratings of how well 20 trait words describe teens are decorrelated
from SWE associations, with Pearson's r=.02, n.s. in English FastText and
r=.06, n.s. in GloVe; and r=.06, n.s. in Nepali FastText and r=-.23, n.s. in
GloVe. U.S. participants suggested AI could fairly present teens by
highlighting diversity, while Nepalese participants centered positivity.
Participants were optimistic that, if it learned from adolescents, rather than
media sources, AI could help mitigate stereotypes. Our work offers an
understanding of the ways SWEs and GLMs misrepresent a developmenta

[Scheduler] example/academic_agent is executing. 

[🤖ollama/llama3:8b] example/academic_agent is switched to executing.

[example/cook_therapist] At step 2, Based on your input, I've created a delicious low-carb, keto-friendly dinner recipe for you. Here it is:

**Recipe:** Balsamic Glazed Pork Chops with Roasted Brussels Sprouts and Cauliflower

**Servings:** 4

**Nutritional Information (per serving):**

* Calories: 540
* Protein: 43g
* Fat: 42g
* Carbohydrates: 6g
* Fiber: 2g
* Net Carbs: 4g

**Ingredients:**

For the pork chops:

* 4 pork chops (6 oz each)
* 1/4 cup balsamic glaze (make your own or use store-bought)
* 2 tbsp olive oil
* 2 tsp garlic powder
* Salt and pepper, to taste

For the roasted Brussels sprouts and cauliflower:

* 1 lb Brussels sprouts, trimmed
* 1 head of cauliflower, broken into florets
* 2 tbsp olive oil
* 1 tsp salt
* 1/2 tsp black pepper
* 1/4 cup grated Parmesan cheese (optional)

**Instructions:**

1. Preheat your oven to 400°F (200°C).
2. In

[Scheduler] example/academic_agent is executing. 

[🤖ollama/llama3:8b] example/academic_agent is switched to executing.

[example/academic_agent] At step 3, Based on the papers I found using the arXiv tool, here are the key findings summarized:

**Paper 1: "Personalization, Cognition, and Gamification-based Programming Language Learning: A State-of-the-Art Systematic Literature Review"**

* Personalized gamification can enhance student cognition in programming courses by improving motivation, engagement, and learning outcomes.
* The effectiveness of personalized gamification varies depending on factors such as the type of gamification elements used, the degree of personalization, and the characteristics of the learners.

**Paper 2: "Co-Creation of Innovative Gamification Based Learning: A Case of Synchronous Partnership"**

* Co-creation of gamification-based learning can foster greater levels of synchronous interactivity and partnership between teaching and learning stakeholders.
* Students gain a greater sense of partnership and inclusivity as part of a synchronous co-creation gamification-based learning development and implementation process.

**Paper 3: "Computers in Secondary Schools: Educational Games"**

* Educational games include serious games, gamification, and game creation, all with the intention to support learning objectives.
* Gamification can be used in non-game contexts to engage students and promote learning.

These papers highlight the potential benefits of using personalized gamification and co-creation

[Scheduler] example/cook_therapist is executing. 

[🤖ollama/llama3:8b] example/cook_therapist is switched to executing.

[example/academic_agent] At step 3, **Step 3: Summarize key findings of selected papers**

Based on the search results from arXiv, I've selected two papers that seem relevant to our research topic. Here's a summary of their key findings:

Paper 1: "Quantifying Mental Health from Social Media with Neural User Embeddings"

* The authors propose a novel model for automated mental health status quantification using user embeddings learned from Twitter post histories.
* They demonstrate that the user embeddings capture similarities between users with respect to mental conditions, and are predictive of mental health.
* The study suggests that machine learning-based approaches can be used to estimate mental health prevalence at scale, providing near real-time estimates.

Paper 2: "Representation Bias of Adolescents in AI: A Bilingual, Bicultural Study"

* The authors investigate how teenagers are depicted by AI models and compare these with the perspectives of adolescents living in the U.S. and Nepal.
* They find that English-language static word embeddings (SWEs) associate teenagers with societal problems, while Nepali SWEs show less bias.
* The study highlights the disconnect between AI presentations and teenage life, suggesting that AI could be used to present a more positive and diverse representation of teenagers.

Key findings:

1. Social media can provide valuable

[Scheduler] example/academic_agent is executing. 

[🤖ollama/llama3:8b] example/academic_agent is switched to executing.

[example/cook_therapist] At step 3, [Action]: I fail to call any tools.. [Observation]: The tool parameter {'prompt': 'Balsamic Glazed Pork Chops with Roasted Brussels Sprouts and Cauliflower on a plate, garnished with fresh parsley and a drizzle of balsamic glaze.', 'path': '/home/dp/Documents/_POCs/AIOS/AIOS/pyopenagi/agents/example/cook_therapist/output/generated_image.png'} is invalid.

```

## Next Steps:
### @TODO: LLM Classes
