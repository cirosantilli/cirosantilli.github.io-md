# Artificial intelligence

↑ **Parent:** [Machine learning](machine-learning.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Artificial_intelligence)

**Table of contents**

- [AI by capability](#ai-by-capability)
  - [Artificial general intelligence](#artificial-general-intelligence)
    - [Principles of AGI](#principles-of-agi)
      - [The missing link between continuous and discrete AI](#the-missing-link-between-continuous-and-discrete-ai)
      - [Intelligence is hierarchical](#intelligence-is-hierarchical)
      - [AGI architecture](#agi-architecture)
        - [Elements of AGI](#elements-of-agi)
          - [Common sense](#common-sense)
          - [Instrumental goal](#instrumental-goal)
            - [Instrumental convergence](#instrumental-convergence)
    - [AGI research](#agi-research)
      - [History of AGI research](#history-of-agi-research)
        - [AGI blues](#agi-blues)
          - [AGI excitement](#agi-excitement)
        - [Moravec's paradox](#moravec-s-paradox)
        - [AI winter](#ai-winter)
        - [AI boom](#ai-boom)
        - [AGI research has become a taboo in the early 21st century](#agi-research-has-become-a-taboo-in-the-early-21st-century)
      - [AGI interest group](#agi-interest-group)
        - [AGI House](#agi-house)
        - [AGI conference](#agi-conference)
          - [Open AGI Summit](#open-agi-summit)
      - [Journal of Artificial General Intelligence](#journal-of-artificial-general-intelligence)
      - [AGI research entity](#agi-research-entity)
        - [Amazon AGI team](#amazon-agi-team)
        - [Giotto.ai](#giotto-ai)
        - [Kyutai](#kyutai)
        - [mit quest for intelligence](#mit-quest-for-intelligence)
        - [safe superintelligence inc.](#safe-superintelligence-inc)
        - [Steven Byrnes](#steven-byrnes)
        - [Astera Institute](#astera-institute)
          - [Hipster research institute](#hipster-research-institute)
            - [Topos institute](#topos-institute)
          - [Astera Institute person](#astera-institute-person)
            - [Michael Nielsen](#michael-nielsen)
        - [FutureAI](#futureai)
          - [BrainSimII](#brainsimii)
          - [Sallie (FutureAI)](#sallie-futureai)
          - [Charles Simon](#charles-simon)
        - [GoodAI](#goodai)
          - [AI People](#ai-people)
          - [Marek Rosa](#marek-rosa)
        - [NDEA](#ndea)
        - [Numenta](#numenta)
          - [Numenta employee](#numenta-employee)
            - [Jeff Hawkins](#jeff-hawkins)
          - [Hierarchical temporal memory](#hierarchical-temporal-memory)
            - [On Intelligence](#on-intelligence)
        - [Sakana.AI](#sakana-ai)
    - [AGI software](#agi-software)
      - [OpenCog](#opencog)
        - [Ben Goertzel](#ben-goertzel)
          - [SingularityNET](#singularitynet)
            - [NuNET](#nunet)
    - [AGI-complete](#agi-complete)
    - [Polanyi's paradox](#polanyi-s-paradox)
      - [Mechanistic interpretability](#mechanistic-interpretability)
    - [AGI test](#agi-test)
      - [CAPTCHA](#captcha)
        - [reCAPTCHA](#recaptcha)
      - [Turing test](#turing-test)
      - [ARC-AGI](#arc-agi)
        - [ARC-AGI theory](#arc-agi-theory)
          - [Information theoretical musings inspired by ARC-AGI](#information-theoretical-musings-inspired-by-arc-agi)
          - [ARC-AGI is a black hole for early retired tech and finance bros](#arc-agi-is-a-black-hole-for-early-retired-tech-and-finance-bros)
        - [ARC-AGI visualization](#arc-agi-visualization)
        - [ARC-AGI approach](#arc-agi-approach)
          - [ARC-AGI feature extraction](#arc-agi-feature-extraction)
        - [ARC-AGI implementation](#arc-agi-implementation)
          - [ARC-DSL](#arc-dsl)
          - [ARC-DSL-2](#arc-dsl-2)
          - [cristianoc/arc-agi-2-abstraction-dataset](#cristianoc-arc-agi-2-abstraction-dataset)
          - [ARC-AGI without LLM](#arc-agi-without-llm)
            - [CompressARC](#compressarc)
            - [mdlARC](#mdlarc)
            - [Local CPU ARC-AGI without LLM](#local-cpu-arc-agi-without-llm)
              - [aviad12g/ARC-AGI-solution ](#aviad12g-arc-agi-solution)
        - [ARC-AGI problem set](#arc-agi-problem-set)
          - [Official ARC-AGI problem set](#official-arc-agi-problem-set)
            - [ARC-AGI-1](#arc-agi-1)
              - [ARC-AGI-1 problem](#arc-agi-1-problem)
                - [Train](#arc-agi-1-problem/train)
                  - [007bbfb](#arc-agi-1-problem/007bbfb)
                  - [00d62c1b](#arc-agi-1-problem/00d62c1b)
                  - [017c7c7b](#arc-agi-1-problem/017c7c7b)
                  - [025d127b](#arc-agi-1-problem/025d127b)
                  - [0520fde7](#arc-agi-1-problem/0520fde7)
                - [Eval](#arc-agi-1-problem/eval)
            - [ARC-AGI-2](#arc-agi-2)
              - [ARC-AGI-2 problem](#arc-agi-2-problem)
                - [Approach](#arc-agi-2-problem/approach)
                  - [Primitive](#arc-agi-2-problem/primitive)
                    - [Input primitive](#arc-agi-2-problem/input-primitive)
                      - [Background color](#arc-agi-2-problem/background-color)
                      - [Object](#arc-agi-2-problem/object)
                        - [Container](#arc-agi-2-problem/container)
                          - [Box](#arc-agi-2-problem/box)
                            - [Edge](#arc-agi-2-problem/edge)
                              - [Left edge](#arc-agi-2-problem/left-edge)
                              - [Right edge](#arc-agi-2-problem/right-edge)
                              - [Top edge](#arc-agi-2-problem/top-edge)
                              - [Bottom edge](#arc-agi-2-problem/bottom-edge)
                            - [Toplevel box](#arc-agi-2-problem/toplevel-box)
                              - [Two toplevel boxes](#arc-agi-2-problem/two-toplevel-boxes)
                                - [Input output toplevel boxes](#arc-agi-2-problem/input-output-toplevel-boxes)
                        - [Monocolor object](#arc-agi-2-problem/monocolor-object)
                        - [Primitive relation](#arc-agi-2-problem/primitive-relation)
                          - [Distance](#arc-agi-2-problem/distance)
                            - [Adjacent](#arc-agi-2-problem/adjacent)
                        - [Rectangle](#arc-agi-2-problem/rectangle)
                          - [Square](#arc-agi-2-problem/square)
                            - [Point](#arc-agi-2-problem/point)
                        - [Path](#arc-agi-2-problem/path)
                          - [Dotted path](#arc-agi-2-problem/dotted-path)
                          - [Line](#arc-agi-2-problem/line)
                            - [Dotted line](#arc-agi-2-problem/dotted-line)
                            - [Monocolor line](#arc-agi-2-problem/monocolor-line)
                            - [Perpendicular line](#arc-agi-2-problem/perpendicular-line)
                              - [Vertical line](#arc-agi-2-problem/vertical-line)
                              - [Horizontal line](#arc-agi-2-problem/horizontal-line)
                            - [Diagonal line](#arc-agi-2-problem/diagonal-line)
                      - [Repeat](#arc-agi-2-problem/repeat)
                    - [Output primitive](#arc-agi-2-problem/output-primitive)
                      - [Optimize](#arc-agi-2-problem/optimize)
                      - [Draw line](#arc-agi-2-problem/draw-line)
                - [List](#arc-agi-2-problem/list)
                  - [Train](#arc-agi-2-problem/list/train)
                  - [Eval](#arc-agi-2-problem/list/eval)
                    - [1ae2feb7](#arc-agi-2-problem/list/1ae2feb7)
                    - [3e6067c3](#arc-agi-2-problem/list/3e6067c3)
                    - [16b78196](#arc-agi-2-problem/list/16b78196)
                    - [142ca369](#arc-agi-2-problem/list/142ca369)
                    - [136b0064](#arc-agi-2-problem/list/136b0064)
                    - [0934a4d8](#arc-agi-2-problem/list/0934a4d8)
                    - [135a2760](#arc-agi-2-problem/list/135a2760)
                    - [13e47133](#arc-agi-2-problem/list/13e47133)
                    - [195c6913](#arc-agi-2-problem/list/195c6913)
            - [ARC-AGI-3](#arc-agi-3)
            - [Unofficial ARC-AGI problem set](#unofficial-arc-agi-problem-set)
              - [ARC-AGI problem generator](#arc-agi-problem-generator)
                - [re-arc](#re-arc)
                - [arc-like](#arc-like)
      - [The Employment Test](#the-employment-test)
    - [AGI bibliography](#agi-bibliography)
  - [Automated theorem proving](#automated-theorem-proving)
    - [Math AI company](#math-ai-company)
      - [Axiom Math](#axiom-math)
      - [harmonic.fun](#harmonic-fun)
      - [Logical Intelligence Inc.](#logical-intelligence-inc)
      - [Math, Inc](#math-inc)
      - [Math, Inc careers page puzzle](#math-inc-careers-page-puzzle)
      - [Principia Labs](#principia-labs)
    - [Math AI implementation](#math-ai-implementation)
      - [AlphaProof](#alphaproof)
        - [AlphaGeometry](#alphageometry)
      - [LeanAgent](#leanagent)
    - [Autoformalization](#autoformalization)
    - [Math AI benchmark](#math-ai-benchmark)
      - [Closed AI math benchmark](#closed-ai-math-benchmark)
      - [List of math AI benchmarks](#list-of-math-ai-benchmarks)
        - [MathArena](#matharena)
          - [MathArena Apex](#matharena-apex)
        - [AI Mathematical Olympiad](#ai-mathematical-olympiad)
        - [ORCA Benchmark](#orca-benchmark)
        - [Equational theories project](#equational-theories-project)
        - [First Proof](#first-proof)
        - [FrontierMath](#frontiermath)
          - [Elliot Glazer](#elliot-glazer)
        - [IMProofBench](#improofbench)
        - [LiveBench](#livebench)
        - [Putnam-AXIOM](#putnam-axiom)
        - [Verina](#verina)
  - [Regression analysis](#regression-analysis)
    - [Linear regression](#linear-regression)
  - [Statistical classification](#statistical-classification)
  - [Cluster analysis](#cluster-analysis)
  - [Generative AI](#generative-ai)
    - [Generative adversarial network](#generative-adversarial-network)
      - [GAN paper](#gan-paper)
      - [GAN MNIST hello world](#gan-mnist-hello-world)
      - [AI brittleness and robustness](#ai-brittleness-and-robustness)
        - [AI robustness](#ai-robustness)
        - [AI brittleness](#ai-brittleness)
          - [Adversarial machine learning](#adversarial-machine-learning)
    - [AI generated porn](#ai-generated-porn)
    - [Generative AI by modality](#generative-ai-by-modality)
      - [Image generation](#image-generation)
        - [Face generation](#face-generation)
        - [Text-to-image generation](#text-to-image-generation)
          - [Text-to-image model](#text-to-image-model)
            - [Open source text-to-image model](#open-source-text-to-image-model)
              - [ludicrains/deep-gaze](#ludicrains-deep-gaze)
              - [runwayml/stable-diffusion](#runwayml-stable-diffusion)
              - [DeepFloyd IF](#deepfloyd-if)
      - [AI text generation](#ai-text-generation)
        - [Speech recognition](#speech-recognition)
          - [Speech recognition software](#speech-recognition-software)
            - [OpenAi Whisper](#openai-whisper)
            - [Vosk](#vosk)
        - [Text-to-text model](#text-to-text-model)
          - [Machine translation](#machine-translation)
          - [Open source machine translation](#open-source-machine-translation)
            - [OpenNMT](#opennmt)
              - [Argos Translate](#argos-translate)
          - [Large language model](#large-language-model)
            - [LLM game](#llm-game)
              - [Stanford Smallville](#stanford-smallville)
            - [LLM inference optimization](#llm-inference-optimization)
              - [LLM inference batching](#llm-inference-batching)
              - [LLM KV Caching](#llm-kv-caching)
              - [Grouped-Query attention](#grouped-query-attention)
            - [Generative pre-trained transformer](#generative-pre-trained-transformer)
              - [ChatGPT](#chatgpt)
                - [Codex](#codex)
                  - [Codex CLI](#codex-cli)
                  - [Codex CLI HOWTO](#codex-cli-howto)
                    - [Prevent Codex CLI from reading certain files via the sandbox](#prevent-codex-cli-from-reading-certain-files-via-the-sandbox)
                    - [Get a notification when Codex CLI finishes the current prompt](#get-a-notification-when-codex-cli-finishes-the-current-prompt)
                    - [Allow Codex CLI to run shell commands with Internet access](#allow-codex-cli-to-run-shell-commands-with-internet-access)
              - [GPT model](#gpt-model)
                - [Theoretical peak performance of GPT inference](#theoretical-peak-performance-of-gpt-inference)
                  - [Number of multiplications per token in a GPT model](#number-of-multiplications-per-token-in-a-gpt-model)
                - [List of GPT models](#list-of-gpt-models)
                  - [GPT model by Google](#gpt-model-by-google)
                    - [Gemini model](#gemini-model)
                      - [Gemini 3](#gemini-3)
                  - [GPT model by OpenAI](#gpt-model-by-openai)
                    - [GPT-1](#gpt-1)
                      - [Improving Language Understanding by Generative Pre-Training](#improving-language-understanding-by-generative-pre-training)
                    - [GPT-2](#gpt-2)
                      - [Language Models are Unsupervised Multitask Learners](#language-models-are-unsupervised-multitask-learners)
                      - [GPT-2 implementation](#gpt-2-implementation)
                      - [GPT-2 implementation in PyTorch](#gpt-2-implementation-in-pytorch)
                        - [nanoGPT](#nanogpt)
                      - [GPT-2 variant](#gpt-2-variant)
                        - [GPT-2 medium](#gpt-2-medium)
                        - [GPT-2 large](#gpt-2-large)
                        - [GPT-2 XL](#gpt-2-xl)
                    - [GPT-3](#gpt-3)
                    - [GPT-4](#gpt-4)
                      - [GPT 4 Turbo](#gpt-4-turbo)
                    - [GPT-5](#gpt-5)
                      - [GPT-5.1](#gpt-5-1)
                        - [GPT-5.1 Pro](#gpt-5-1-pro)
                      - [GPT-5.4](#gpt-5-4)
                  - [Llama (language model)](#llama-language-model)
                    - [Llama 2](#llama-2)
                      - [Llama 2 7B](#llama-2-7b)
                    - [Llama 3](#llama-3)
                      - [Llama 3.1](#llama-3-1)
                        - [Llama 3.1 8B](#llama-3-1-8b)
                        - [Llama 3.1 70B](#llama-3-1-70b)
                        - [Llama 3.1 405B](#llama-3-1-405b)
            - [Open source LLM](#open-source-llm)
              - [LLM model with open training data](#llm-model-with-open-training-data)
                - [The Pile (dataset)](#the-pile-dataset)
                - [LLM360](#llm360)
              - [Open weight LLM model](#open-weight-llm-model)
              - [Ollama](#ollama)
                - [llama.cpp](#llama-cpp)
                  - [llama-cli](#llama-cli)
                    - [llama-cli inference batching](#llama-cli-inference-batching)
                - [Ollama HOWTO](#ollama-howto)
                  - [Ollama output size](#ollama-output-size)
                  - [Ollama deterministic output](#ollama-deterministic-output)
                - [Ollama parameter](#ollama-parameter)
                  - [Ollama set parameter on CLI](#ollama-set-parameter-on-cli)
                    - [ollama-expect](#_file/ollama-expect)
            - [LLM benchmark](#llm-benchmark)
              - [Simplest questions that LLMs get wrong](#simplest-questions-that-llms-get-wrong)
                - [Easy Problems That LLMs Get Wrong by Sean Williams and James Huckle](#easy-problems-that-llms-get-wrong-by-sean-williams-and-james-huckle)
              - [List of LLM benchmarks](#list-of-llm-benchmarks)
                - [MMLU](#mmlu)
                - [Humanity's Last Exam](#humanity-s-last-exam)
            - [GPQA](#gpqa)
            - [Uncensored LLM](#uncensored-llm)
              - [mlabonne/Meta-Llama-3.1-8B-Instruct-abliterated-GGUF ](#mlabonne-meta-llama-3-1-8b-instruct-abliterated-gguf)
      - [AI sound generation](#ai-sound-generation)
        - [AI music generation](#ai-music-generation)
          - [Soundraw](#soundraw)
        - [Speech synthesis](#speech-synthesis)
          - [Speech to speech](#speech-to-speech)
          - [Text-to-speech](#text-to-speech)
            - [Comparison of text-to-speech software](#comparison-of-text-to-speech-software)
      - [Text-to-video](#text-to-video)
- [AI research entity](#ai-research-entity)
  - [Independent AI research lab](#independent-ai-research-lab)
    - [Poetiq](#poetiq)
  - [AI researcher](#ai-researcher)
    - [Yann LeCun](#yann-lecun)
    - [Yohei Nakajima](#yohei-nakajima)
- [AI alignment](#ai-alignment)
  - [Hallucination (artificial intelligence)](#hallucination-artificial-intelligence)
  - [Reward modeling](#reward-modeling)
  - [AI safety](#ai-safety)
- [Path to AGI](#path-to-agi)
  - [AI training robot](#ai-training-robot)
    - [AI training robot in a room](#ai-training-robot-in-a-room)
    - [Robot AI](#robot-ai)
      - [Gemini Robotics](#gemini-robotics)
    - [AI training robot dataset](#ai-training-robot-dataset)
      - [Open X-Embodiment](#open-x-embodiment)
    - [AI training robot simulation](#ai-training-robot-simulation)
      - [BEHAVIOR Benchmark](#behavior-benchmark)
        - [BEHAVIOR Benchmark variant](#behavior-benchmark-variant)
          - [BEHAVIOR-1K](#behavior-1k)
          - [BEHAVIOR-100](#behavior-100)
        - [OmniGibson](#omnigibson)
      - [AI Habitat](#ai-habitat)
      - [RoboCasa](#robocasa)
    - [DeepMind RoboCat](#deepmind-robocat)
    - [Supercomputer controlling a robot](#supercomputer-controlling-a-robot)
  - [AI game](#ai-game)
    - [Human game used for AI training](#human-game-used-for-ai-training)
      - [Using Minecraft for AI training](#using-minecraft-for-ai-training)
        - [MineDojo](#minedojo)
    - [Game AI](#game-ai)
      - [Game AI research](#game-ai-research)
        - [Game AI research lab](#game-ai-research-lab)
          - [QMUL Game AI Research Group](#qmul-game-ai-research-group)
          - [Leiden Game Research Lab](#leiden-game-research-lab)
      - [Game AI by game genre](#game-ai-by-game-genre)
        - [Fighting game AI](#fighting-game-ai)
      - [Game AI competition](#game-ai-competition)
        - [Battlecode](#battlecode)
        - [Regression Games](#regression-games)
        - [Computer Olympiad](#computer-olympiad)
      - [Permanent brain](#permanent-brain)
    - [AI game by type](#ai-game-by-type)
      - [Procedural AI training game](#procedural-ai-training-game)
      - [AI game world geometry](#ai-game-world-geometry)
        - [2D AI game](#2d-ai-game)
          - [Gridworld AI game](#gridworld-ai-game)
          - [2D continuous AI game](#2d-continuous-ai-game)
        - [3D AI game](#3d-ai-game)
          - [Football simulation](#football-simulation)
            - [Deepmind soccer simulation](#deepmind-soccer-simulation)
    - [AI game with natural language](#ai-game-with-natural-language)
    - [List of AI games](#list-of-ai-games)
      - [AI game by DeepMind](#ai-game-by-deepmind)
        - [DeepMind Lab](#deepmind-lab)
        - [DeepMind Lab2D](#deepmind-lab2d)
          - [DeepMind Lab2D vs gvgai](#deepmind-lab2d-vs-gvgai)
    - [Can AGI be trained in simulations?](#can-agi-be-trained-in-simulations)
    - [Entity creating AI games](#entity-creating-ai-games)
      - [DeepMind](#deepmind)
        - [DeepMind project](#deepmind-project)
          - [AlphaGo](#alphago)
            - [Open source AlphaGo implementation](#open-source-alphago-implementation)
              - [MiniGo](#minigo)
            - [AlphaGo Zero](#alphago-zero)
              - [AlphaGo Zero open source implementation](#alphago-zero-open-source-implementation)
            - [AlphaZero](#alphazero)
      - [gvgai](#gvgai)
        - [Julian Togelius](#julian-togelius)
      - [General Game Playing (Stanford project)](#general-game-playing-stanford-project)
      - [OpenAI](#openai)
        - [OpenAI project](#openai-project)
          - [OpenAI Gym](#openai-gym)
            - [Farama Gymnasium](#farama-gymnasium)
              - [Farama Gymnasium solutions](#farama-gymnasium-solutions)
              - [Farama Foundation](#farama-foundation)
- [Implications of AGI](#implications-of-agi)
  - [Existential risk of AGI](#existential-risk-of-agi)
  - [Singularity](#singularity)
- [Artificial intelligence paradigm](#artificial-intelligence-paradigm)
  - [Expert system](#expert-system)
- [Artificial intelligence bibliography](#artificial-intelligence-bibliography)
  - [Human Compatible](#human-compatible)
  - [Superintelligence by Nick Bostrom (2014)](#superintelligence-by-nick-bostrom-2014)
- [Application of artificial intelligence](#application-of-artificial-intelligence)
  - [Legal technology](#legal-technology)
    - [Legal technology company](#legal-technology-company)
      - [Safe Sign Technologies](#safe-sign-technologies)
    - [ThoughtRiver](#thoughtriver)

## AI by capability

↑ **Parent:** [Artificial intelligence](artificial-intelligence.md)

### Artificial general intelligence

↑ **Parent:** [AI by capability](#ai-by-capability)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Artificial_general_intelligence)

Given enough computational power per dollar, AGI is inevitable, but it is not sure certain ever happen given the end of [end of Moore's Law](computer-hardware.md#moore-s-law).

Alternatively, it could also be achieved genetically modified biological brains + [brain in a vat](human.md#brain-in-a-vat).

Imagine a brain the size of a building, perfectly engineered to solve certain engineering problems, and giving hints to human operators + taking feedback from cameras and audio attached to the operators.

This likely implies [transhumanism](human.md#transhumanism), and [mind uploading](brain.md#mind-uploading).

[Ciro Santilli](ciro-santilli.md) joined the silicon industry at one point to help increase our computational capacity and reach AGI.

Ciro believes that the easiest route to full AI, if any, could involve [Ciro's 2D reinforcement learning games](todo.md#ciro-s-2d-reinforcement-learning-games).

#### Principles of AGI

↑ **Parent:** [Artificial general intelligence](#artificial-general-intelligence)

##### The missing link between continuous and discrete AI

↑ **Parent:** [Principles of AGI](#principles-of-agi)

[Ciro Santilli](ciro-santilli.md) has felt that perhaps what is missing in 2020's [AGI](#artificial-general-intelligence) research is:
- the interface between:
  - the continuous/noisy level (now well developed under [artificial neural network](machine-learning.md#artificial-neural-network) techniques of the 2010's)
  - and [symbolic AI](machine-learning.md#symbolic-artificial-intelligence) level AI

  The key question is somewhat how to extract symbols out of the space-time continuous experiences.
- more specialized accelerators that somehow interface with more generic [artificial neural networks](machine-learning.md#artificial-neural-network). Notably some kind of speialized processing of spacial elements is obviously hardcoded into the brain, see e.g. [Section "Grid cell"](brain.md#grid-cell)

Forcing these boundaries to be tested was one of the main design goals of [Ciro's 2D reinforcement learning games](todo.md#ciro-s-2d-reinforcement-learning-games).

In those games, for example:
- when you press a button here, a door opens somewhere far away
- when you touch certain types of objects, a chemical reaction may happen, but not other types of objects
Therefore, those continuous objects would also have "magic" effects that could not be explained by "simple" "what is touching what" ideas.

Bibliography:
- [https://mitpress.mit.edu/9780262632683/the-algebraic-mind/](https://mitpress.mit.edu/9780262632683/the-algebraic-mind/)

##### Intelligence is hierarchical

↑ **Parent:** [Principles of AGI](#principles-of-agi)

This point is beautifully argued in lots of different sources, and is clearly a pillar of [AGI](#artificial-general-intelligence).

Perhaps one may argue that our [deep learning](machine-learning.md#deep-learning) layers do form some kind of hierarchy, e.g. this is very clear in certain models such as [convolutional neural network](machine-learning.md#convolutional-neural-network). But many of those models cannot have arbitrarily deep hierarchies, which appears to be a fundamental aspect of intelligence.

[How to Create a Mind](brain.md#how-to-create-a-mind):

> The lists of steps in my mind are organized in hierarchies. I follow a routine procedure before going to sleep. The first step is to brush my teeth. But this action is in turn broken into a smaller series of steps, the first of which is to put toothpaste on the toothbrush. That step in turn is made up of yet smaller steps, such as finding the toothpaste, removing the cap, and so on. The step of finding the toothpaste also has steps, the first of which is to open the bathroom cabinet. That step in turn requires steps, the first of which is to grab the outside of the cabinet door. This nesting actually continues down to a very fine grain of movements, so that there are literally thousands of little actions constituting my nighttime routine. Although I may have difficulty remembering details of a walk I took just a few hours ago, I have no difficulty recalling all of these many steps in preparing for bed - so much so that I am able to think about other things while I go through these procedures. It is important to point out that this list is not stored as one long list of thousands of steps - rather, each of our routine procedures is remembered as an elaborate hierarchy of nested activities.

[Human Compatible](#human-compatible): TODO get exact quote. It was something along: life goal: save world from hunger. Subgoal: apply for some grant. Sub-sub-goal: eat, sleep, take shower. Sub-sub-sub-goal: move muscles to get me to table and open a can.

##### AGI architecture

↑ **Parent:** [Principles of AGI](#principles-of-agi)

<a id="video-from-machine-learning-to-autonomous-intelligence-by-yann-lecun-2023"></a>
**[Video 1](#video-from-machine-learning-to-autonomous-intelligence-by-yann-lecun-2023). From Machine Learning to Autonomous Intelligence by Yann LeCun (2023)** [Source](https://youtu.be/pd0JmT6rYcI?t=3536). After a bunch of B.S., LeCun goes on to describe his AGI architecture. Nothing ground breaking, but not bad either.
- [https://youtu.be/pd0JmT6rYcI?t=3705](https://youtu.be/pd0JmT6rYcI?t=3705): [intelligence is hierarchical](#intelligence-is-hierarchical)

---

Bibliography:
- [https://www.reddit.com/r/agi/comments/108e7n1/best_starting_papersbooks_to_read_to_try_to/](https://www.reddit.com/r/agi/comments/108e7n1/best_starting_papersbooks_to_read_to_try_to/)

###### Elements of AGI

↑ **Parent:** [AGI architecture](#agi-architecture)

This section is about ideas that are thought to be part of an AGI system.

###### Common sense

↑ **Parent:** [Elements of AGI](#elements-of-agi)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Common_sense)

<a id="video-my-job-is-to-open-and-close-doors-by-mattias-pilhede-2019"></a>
**[Video 2](#video-my-job-is-to-open-and-close-doors-by-mattias-pilhede-2019). My Job is to Open and Close Doors by Mattias Pilhede (2019)** [Source](https://www.youtube.com/watch?v=49t-WWTx0RQ). An interesting humorous short meditation on [common sense](#common-sense).

###### Instrumental goal

↑ **Parent:** [Elements of AGI](#elements-of-agi)

###### Instrumental convergence

↑ **Parent:** [Instrumental goal](#instrumental-goal)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Instrumental_convergence)

#### AGI research

↑ **Parent:** [Artificial general intelligence](#artificial-general-intelligence)

##### History of AGI research

↑ **Parent:** [AGI research](#agi-research)

###### AGI blues

↑ **Parent:** [History of AGI research](#history-of-agi-research)

Term invented by [Ciro Santilli](ciro-santilli.md), similar to "[nuclear blues](brain.md#nuclear-blues)", and used to describe the feeling that every little shitty job you are doing (that does not considerably help achieving [AGI](#artificial-general-intelligence)) is completely pointless given that we are likely close to [AGI](#artificial-general-intelligence) as of 2023.

###### AGI excitement

↑ **Parent:** [AGI blues](#agi-blues)

The opposite of the [AGI blues](#agi-blues). In 2025 [Ciro Santilli](ciro-santilli.md) fell well in this camp.

<h6 id="moravec-s-paradox">Moravec's paradox</h6>

↑ **Parent:** [History of AGI research](#history-of-agi-research)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Moravec's_paradox)

###### AI winter

↑ **Parent:** [History of AGI research](#history-of-agi-research)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/AI_winter)

###### AI boom

↑ **Parent:** [History of AGI research](#history-of-agi-research)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/AI_boom)

###### AGI research has become a taboo in the early 21st century

↑ **Parent:** [History of AGI research](#history-of-agi-research)

Due to the failures of earlier generations, which believed that would quickly achieve [AGI](#artificial-general-intelligence), leading to the [AI winters](#ai-winter), 21st researchers have been very afraid of even trying it, rather going only for smaller subste problems like better neural network designs, at the risk of being considered a [crank](science.md#crank-person).

While there is fundamental value in such subset problems, the general view to the final goal is also very important, we will likely never reach AI without it.

This is voiced for example in [Superintelligence by Nick Bostrom (2014)](#superintelligence-by-nick-bostrom-2014) section "Opinions about the future of machine intelligence" which in turn quotes Nils Nilsson:

> There may, however, be a residual cultural effect on the AI community of its earlier history that makes many mainstream researchers reluctant to align themselves with over-grand ambition. Thus Nils Nilsson, one of the old-timers in the field, complains that his present-day colleagues lack the boldness of spirit that propelled the pioneers of his own generation:> Concern for "respectability" has had, I think, a stultifying effect on some AI researchers. I hear them saying things like, "AI used to be criticized for its flossiness. Now that we have made solid progress, let us not risk losing our respectability." One result of this conservatism has been increased concentration on "weak AI" - the variety devoted to providing aids to human  
> > thought - and away from "strong AI" - the variety that attempts to mechanize human-level intelligence
> 
> Nilsson’s sentiment has been echoed by several others of the founders, including Marvin Minsky, John McCarthy, and Patrick Winston.

[Don't be a pussy](don-t-be-a-pussy.md), AI researchers!!!

##### AGI interest group

↑ **Parent:** [AGI research](#agi-research)

###### AGI House

↑ **Parent:** [AGI interest group](#agi-interest-group)

- [https://www.agihouse.org/](https://www.agihouse.org/)
- [https://www.businessinsider.com/heres-how-agi-house-bays-hottest-artificial-intelligence-hacker-2023-6](https://www.businessinsider.com/heres-how-agi-house-bays-hottest-artificial-intelligence-hacker-2023-6)

###### AGI conference

↑ **Parent:** [AGI interest group](#agi-interest-group)

[https://www.agi-conference.org/](https://www.agi-conference.org/)

It is hard to overstate how low the level of this conference seems to be at first sight. [Truly sad](#agi-research-has-become-a-taboo-in-the-early-21st-century).

###### Open AGI Summit

↑ **Parent:** [AGI conference](#agi-conference)

[https://openagi.xyz/](https://openagi.xyz/)

The tagline smells like bullshit:

> Integrating AI with web3 and decentralized ecosystems

##### Journal of Artificial General Intelligence

↑ **Parent:** [AGI research](#agi-research)

[https://sciendo.com/journal/JAGI](https://sciendo.com/journal/JAGI)

##### AGI research entity

↑ **Parent:** [AGI research](#agi-research)  
🏷️ **Tags:** [AI research entity](#ai-research-entity)

- [https://www.quora.com/What-are-some-good-research-schools-PhD-for-Artificial-General-Intelligence-not-Machine-Learning/answer/Ciro-Santilli](https://www.quora.com/What-are-some-good-research-schools-PhD-for-Artificial-General-Intelligence-not-Machine-Learning/answer/Ciro-Santilli) What are some good research schools (PhD) for Artificial General Intelligence (not Machine Learning)?
- 2020 [https://towardsdatascience.com/four-ai-companies-on-the-bleeding-edge-of-artificial-general-intelligence-b17227a0b64a](https://towardsdatascience.com/four-ai-companies-on-the-bleeding-edge-of-artificial-general-intelligence-b17227a0b64a) Top 4 AI companies leading in the race towards Artificial General Intelligence
- Douglas Hofstadter according to [https://www.theatlantic.com/magazine/archive/2013/11/the-man-who-would-teach-machines-to-think/309529/](https://www.theatlantic.com/magazine/archive/2013/11/the-man-who-would-teach-machines-to-think/309529/) The Man Who Would Teach Machines to Think (2013) by [James Somers](software.md#james-somers)
- Pei Wang from Temple University: [https://cis.temple.edu/~wangp/](https://cis.temple.edu/~wangp/)
- [https://www.reddit.com/r/agi/comments/zzfwww/are_there_people_actually_working_to_make_an_agi/](https://www.reddit.com/r/agi/comments/zzfwww/are_there_people_actually_working_to_make_an_agi/)
- [Sergey Brin](google.md#sergey-brin) explicit internal memo aiming at [AGI](#artificial-general-intelligence): [https://techcrunch.com/2025/02/28/sergey-brin-says-rto-is-key-to-google-winning-the-agi-race/](https://techcrunch.com/2025/02/28/sergey-brin-says-rto-is-key-to-google-winning-the-agi-race/)

###### Amazon AGI team

↑ **Parent:** [AGI research entity](#agi-research-entity)  
🏷️ **Tags:** [Amazon division](amazon.md#amazon-division)

[https://amazon.jobs/content/en/teams/agi](https://amazon.jobs/content/en/teams/agi)

<h6 id="giotto-ai">Giotto.ai</h6>

↑ **Parent:** [AGI research entity](#agi-research-entity)

[https://www.giotto.ai/](https://www.giotto.ai/)

> At Giotto.ai, our technology is designed to bridge the gap between current AI capabilities and the promise of Artificial General Intelligence (AGI).

Their website doesn't clearly explain their technology as of 2025.

They claim to have done some work on [ARC-AGI](#arc-agi) which is cool, but no clear references to what they did or if there's anything public about it.

###### Kyutai

↑ **Parent:** [AGI research entity](#agi-research-entity)

[https://kyutai.org/](https://kyutai.org/) just says:

> Our mission is to build and democratize artificial general intelligence through open science

They are [not-for-profit](social-technology.md#nonprofit-organization) and had massive investments: [https://techcrunch.com/2023/11/17/kyutai-is-an-french-ai-research-lab-with-a-330-million-budget-that-will-make-everything-open-source/](https://techcrunch.com/2023/11/17/kyutai-is-an-french-ai-research-lab-with-a-330-million-budget-that-will-make-everything-open-source/)

they also don't say at all what they are looking into for [AGI](#artificial-general-intelligence), the only public thing they have are [speech to speech](#speech-to-speech) and [speech-to-text](#speech-recognition) so how's that related to agi at.

###### mit quest for intelligence

↑ **Parent:** [AGI research entity](#agi-research-entity)  
🏷️ **Tags:** [MIT](university.md#massachusetts-institute-of-technology)

[https://quest.mit.edu/about/vision-statement](https://quest.mit.edu/about/vision-statement)

###### safe superintelligence inc.

↑ **Parent:** [AGI research entity](#agi-research-entity)

[https://ssi.inc/](https://ssi.inc/)

raised $1b at $5b valuation on september 2024, then $2b at $30b on march 2025. lol!

From their website:

> Superintelligence is within reach.



> Our singular focus means no distraction by management overhead or product cycles, and our business model means safety, security, and progress are all insulated from short-term commercial pressures.

###### Steven Byrnes

↑ **Parent:** [AGI research entity](#agi-research-entity)  
🏷️ **Tags:** [Astera Institute person](#astera-institute-person)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Steven_Byrnes)

- [https://sjbyrnes.com/](https://sjbyrnes.com/)
- [https://twitter.com/steve47285](https://twitter.com/steve47285)
- [https://www.lesswrong.com/posts/diruo47z32eprenTg/my-computational-framework-for-the-brain](https://www.lesswrong.com/posts/diruo47z32eprenTg/my-computational-framework-for-the-brain)

###### Astera Institute

↑ **Parent:** [AGI research entity](#agi-research-entity)  
🏷️ **Tags:** [Hipster research institute](#hipster-research-institute), [Jed McCaleb](cryptocurrency.md#jed-mccaleb)

[https://astera.org/agi/](https://astera.org/agi/)

By the rich founder of [Mt. Gox](cryptocurrency.md#mt-gox) and Ripple, [Jed McCaleb](cryptocurrency.md#jed-mccaleb).

> Obelisk is the Artificial General Intelligence laboratory at Astera. We are focused on the following problems: How does an agent continuously adapt to a changing environment and incorporate new information? In a complicated stochastic environment with sparse rewards, how does an agent associate rewards with the correct set of actions that led to those rewards? How does higher level planning arise?

###### Hipster research institute

↑ **Parent:** [Astera Institute](#astera-institute)

These are research institutes usually funded by rich tech bros, sometimes [cryptocurrency](cryptocurrency.md) magnates, but not necessarily.

###### Topos institute

↑ **Parent:** [Hipster research institute](#hipster-research-institute)

[https://topos.institute/](https://topos.institute/)

###### Astera Institute person

↑ **Parent:** [Astera Institute](#astera-institute)

###### Michael Nielsen

↑ **Parent:** [Astera Institute person](#astera-institute-person)

Interesting dude, with some interest overlaps with [Ciro Santilli](ciro-santilli.md), like [quantum computing](quantum-computing.md):
- [https://github.com/mnielsen](https://github.com/mnielsen)
- [https://michaelnielsen.org/](https://michaelnielsen.org/)
- [https://twitter.com/michael_nielsen](https://twitter.com/michael_nielsen)
- [https://www.youtube.com/c/michaelnielsen](https://www.youtube.com/c/michaelnielsen)

###### FutureAI

↑ **Parent:** [AGI research entity](#agi-research-entity)

It is a bit hard to decide if those people are serious or not. Sometimes it feels scammy, but sometimes it feels fun and right!

Particularly concerning is the fact that they are not a [not-for-profit](social-technology.md#nonprofit-organization) entity, and it is hard to understand how they might make money.

[Charles Simon](#charles-simon), the founder, is pretty focused in how natural neurons work vs [artificial neural network](machine-learning.md#artificial-neural-network) models. He has some good explanations of that, and one major focus of the project is their semi open source spiking neuron simulator [BrainSimII](#brainsimii). While [Ciro Santilli](ciro-santilli.md) believes that there might be insight in that, he also has doubts if certain modules of the brain wouldn't be more suitable coded directly in regular [programming languages](programming-language.md) with greater ease and performance.

FutureAI appears to be Charles' retirement for fun project, he is likely [independently wealthy](economy.md#independently-wealthy). Well done.

- [https://www.aitimejournal.com/interview-with-charles-simon-ceo-and-founder-futureai](https://www.aitimejournal.com/interview-with-charles-simon-ceo-and-founder-futureai)
- 2022 raised 2 million USD:
  - [https://www.prnewswire.com/news-releases/ai-futureai-raises-2-million-to-develop-artificial-general-intelligence-301459164.html](https://www.prnewswire.com/news-releases/ai-futureai-raises-2-million-to-develop-artificial-general-intelligence-301459164.html)

<a id="video-creativity-and-agi-by-charles-simon-s-at-agi-22-2022"></a>
**[Video 3](#video-creativity-and-agi-by-charles-simon-s-at-agi-22-2022). Creativity and AGI by Charles Simon's at AGI-22 (2022)** [Source](https://www.youtube.com/watch?v=ivbGbSx0K8k). Sounds OK!
- [https://youtu.be/ivbGbSx0K8k?t=856](https://youtu.be/ivbGbSx0K8k?t=856) general structure of the [human brain](brain.md#human-brain) 86B total, matching [number of neurons in the human brain](brain.md#number-of-neurons-in-the-human-brain), with:
  - 14B: brainstem
  - 16B: [neocortex](brain.md#neocortex)
  - 56B: cerebelum
- [https://www.youtube.com/watch?t=1433](https://www.youtube.com/watch?t=1433) some sequencing ideas/conjectures

---

<a id="video-machine-learning-is-not-like-your-brain-by-future-ai-2022"></a>
**[Video 4](#video-machine-learning-is-not-like-your-brain-by-future-ai-2022). Machine Learning Is Not Like Your Brain by Future AI (2022)** [Source](https://www.youtube.com/watch?v=KQP1gPTk0FI). Contains some [BrainSimII](#brainsimii) demos.

###### BrainSimII

↑ **Parent:** [FutureAI](#futureai)  
🏷️ **Tags:** [Neuron simulator](biology.md#neuron-simulator)

[https://github.com/FutureAIGuru/BrainSimII](https://github.com/FutureAIGuru/BrainSimII)

The video from [https://futureai.guru/technologies/brian-simulator-ii-open-source-agi-toolkit/](https://futureai.guru/technologies/brian-simulator-ii-open-source-agi-toolkit/) shows a demo of the possibly non open source version. They have a [GUI](software.md#graphical-user-interface) neuron viewer and editor, which is kind of cool.

<a id="video-machine-learning-is-not-like-your-brain-by-charles-simon-2022"></a>
**[Video 5](#video-machine-learning-is-not-like-your-brain-by-charles-simon-2022). Machine Learning Is Not Like Your Brain by Charles Simon (2022)** [Source](https://www.youtube.com/watch?v=KQP1gPTk0FI).

###### Sallie (FutureAI)

↑ **Parent:** [FutureAI](#futureai)  
🏷️ **Tags:** [AI training robot](#ai-training-robot)

Not having a manipulator claw is a major issue with this one.

But they also have a co-simulation focus, which is a bit of a win.

###### Charles Simon

↑ **Parent:** [FutureAI](#futureai)

- [https://www.linkedin.com/in/charles-simon-futureai/](https://www.linkedin.com/in/charles-simon-futureai/)
- [https://futureai.guru/about/the-team/](https://futureai.guru/about/the-team/)

Basically it looks like the dude got enough money after selling some companies, and now he's doing cooler stuff without much need of money. Not bad.

###### GoodAI

↑ **Parent:** [AGI research entity](#agi-research-entity)

[Marek Rosa](#marek-rosa)'s play thing.

###### AI People

↑ **Parent:** [GoodAI](#goodai)  
🏷️ **Tags:** [AI game with natural language](#ai-game-with-natural-language)

<a id="video-ai-game-llm-driven-npcs-that-can-talk-by-marek-rosa-2023"></a>
**[Video 6](#video-ai-game-llm-driven-npcs-that-can-talk-by-marek-rosa-2023). AI Game - LLM-driven NPCs that can talk by Marek Rosa (2023)** [Source](https://www.youtube.com/watch?v=xkn0H_iWDEQ). Not the most amazing demo, but the idea is there. Seems to be a preview for [AI People](#ai-people). The previous working title seems to have been AI Odyssey.

###### Marek Rosa

↑ **Parent:** [GoodAI](#goodai)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Marek_Rosa)

###### NDEA

↑ **Parent:** [AGI research entity](#agi-research-entity)

[https://ndea.com/](https://ndea.com/)

> We believe program synthesis holds the key to unlocking [AGI](#artificial-general-intelligence).

Cool. Founders are also very interested in [ARC-AGI](#arc-agi).

###### Numenta

↑ **Parent:** [AGI research entity](#agi-research-entity)

Homepage: [https://www.numenta.com/](https://www.numenta.com/)

###### Numenta employee

↑ **Parent:** [Numenta](#numenta)

###### Jeff Hawkins

↑ **Parent:** [Numenta employee](#numenta-employee)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Jeff_Hawkins)

###### Hierarchical temporal memory

↑ **Parent:** [Numenta](#numenta)  
🏷️ **Tags:** [AGI architecture](#agi-architecture)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hierarchical_temporal_memory)

<a id="video-htm-overview-episode-0-by-numenta"></a>
**[Video 7](#video-htm-overview-episode-0-by-numenta). HTM Overview (Episode 0) by Numenta.** [Source](https://www.youtube.com/watch?v=XMB0ri4qgwc).

###### On Intelligence

↑ **Parent:** [Hierarchical temporal memory](#hierarchical-temporal-memory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/On_Intelligence)

![](https://upload.wikimedia.org/wikipedia/en/b/bd/OnInt.png)

<h6 id="sakana-ai">Sakana.AI</h6>

↑ **Parent:** [AGI research entity](#agi-research-entity)

[https://sakana.ai](https://sakana.ai)

Their description is a bit of localization randomness:

> We are building a world class AI research lab in Tokyo.
> 
> We want to develop AI solutions for Japan's needs, and democratize AI in Japan.

<a id="video-i-co-invented-the-transformer-now-i-m-replacing-it"></a>
**[Video 8](#video-i-co-invented-the-transformer-now-i-m-replacing-it). I Co-Invented the Transformer. Now I'm Replacing It.** [Source](https://www.youtube.com/watch?v=DtePicx_kFY). Interview with Sakana.AI co-founders Llion Jones and Luke Darlow by Machine Learning Street Talk published Nov 23, 2025.

#### AGI software

↑ **Parent:** [Artificial general intelligence](#artificial-general-intelligence)

- [https://ai.stackexchange.com/questions/5428/how-can-people-contribute-to-agi-research](https://ai.stackexchange.com/questions/5428/how-can-people-contribute-to-agi-research) mentions:
  - [https://github.com/opennars/opennars](https://github.com/opennars/opennars)
  - [https://github.com/brohrer/robot-brain-project](https://github.com/brohrer/robot-brain-project)

##### OpenCog

↑ **Parent:** [AGI software](#agi-software)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/OpenCog)

###### Ben Goertzel

↑ **Parent:** [OpenCog](#opencog)  
🏷️ **Tags:** [AGI research entity](#agi-research-entity)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Ben_Goertzel)

[https://www.reddit.com/r/artificial/comments/b38hbk/what_do_my_fellow_ai_researchers_think_of_ben/](https://www.reddit.com/r/artificial/comments/b38hbk/what_do_my_fellow_ai_researchers_think_of_ben/) What do my fellow AI researchers think of Ben Goertzel and his research?

###### SingularityNET

↑ **Parent:** [Ben Goertzel](#ben-goertzel)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/SingularityNET)

[https://singularitynet.io/](https://singularitynet.io/)

[Ben Goertzel](#ben-goertzel)'s [fog computing](computer-hardware.md#fog-computing) project to try and help achieve [AGI](#artificial-general-intelligence).

###### NuNET

↑ **Parent:** [SingularityNET](#singularitynet)  
🏷️ **Tags:** [Fog computing](computer-hardware.md#fog-computing)

#### AGI-complete

↑ **Parent:** [Artificial general intelligence](#artificial-general-intelligence)  
🏷️ **Tags:** [Complexity class](computer-science.md#complexity-class)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/AGI-complete)

Term invented by [Ciro Santilli](ciro-santilli.md) to refer to problems that can only be solved once we have [AGI](#artificial-general-intelligence).

It is somewhat of a flawed analogy to [NP-complete](computer-science.md#np-complete).

<h4 id="polanyi-s-paradox">Polanyi's paradox</h4>

↑ **Parent:** [Artificial general intelligence](#artificial-general-intelligence)

##### Mechanistic interpretability

↑ **Parent:** [Polanyi's paradox](#polanyi-s-paradox)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Mechanistic_interpretability)

- [https://x.com/aif_media/status/1923028051149062607](https://x.com/aif_media/status/1923028051149062607)

#### AGI test

↑ **Parent:** [Artificial general intelligence](#artificial-general-intelligence)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/en.wikipedia.org/w/index.php?title=Artificial_general_intelligence&oldid=1192191193#Tests_for_human-level_AGI)

##### CAPTCHA

↑ **Parent:** [AGI test](#agi-test)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/CAPTCHA)

###### reCAPTCHA

↑ **Parent:** [CAPTCHA](#captcha)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/reCAPTCHA)

##### Turing test

↑ **Parent:** [AGI test](#agi-test)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Turing_test)

##### ARC-AGI

↑ **Parent:** [AGI test](#agi-test)

- [https://arcprize.org/](https://arcprize.org/)
- [https://lab42.global/arc/](https://lab42.global/arc/)
- [https://pgpbpadilla.github.io/chollet-arc-challenge](https://pgpbpadilla.github.io/chollet-arc-challenge)

This one goes all in the following themes:
- few examples to learn from. You have to carefully inspect the input examples to deduce the output rules. Rules can require specific It application ordering, so you actually generate an algorithm. It tends to be easy for humans, but sometimes not so easy!
- extensive use of geometric concepts, notably "contained inside", "adjacent to", "connected"

Bibliography:
- [https://www.reddit.com/r/mlscaling/comments/1ht4emi/anyone_else_suspect_arcagi_was_never_much_of_a/](https://www.reddit.com/r/mlscaling/comments/1ht4emi/anyone_else_suspect_arcagi_was_never_much_of_a/) Anyone else suspect ARC-AGI was never much of a test of anything? (2025)

###### ARC-AGI theory

↑ **Parent:** [ARC-AGI](#arc-agi)

###### Information theoretical musings inspired by ARC-AGI

↑ **Parent:** [ARC-AGI theory](#arc-agi-theory)

The extreme [overfitting](machine-learning.md#overfitting) case of training is to have a map where each input leads to one output.

However it is cool that this overfit does not allow you to compute the final input for which there is no known output.

This therefore forces the creation of more general solution rules.

While in some cases solutions can work for any input, in many others they require specific assumptions about input, but the model could simply check that the assumptions apply to all inputs and use them for the final algorithm.

Bibliography:
- [https://lewish.io/posts/how-to-beat-arc-agi-2](https://lewish.io/posts/how-to-beat-arc-agi-2)

###### ARC-AGI is a black hole for early retired tech and finance bros

↑ **Parent:** [ARC-AGI theory](#arc-agi-theory)

People who do cool open tech stuff when don't need money anymore are awesome:
- François Chollet, project founder: [https://www.linkedin.com/in/fchollet/](https://www.linkedin.com/in/fchollet/) 9 years at Google from 2015 to 2024. He founded ARC while he was still at Google though, so maybe doesn't count
- Cristiano Calgano from [cristianoc/arc-agi-2-abstraction-dataset](#cristianoc-arc-agi-2-abstraction-dataset). [Imperial College London](university.md#imperial-college-london) researcher who founded a [formal verification](software.md#formal-verification) company and sold it to [Facebook](social-technology.md#facebook) where he staid for 7 years

###### ARC-AGI visualization

↑ **Parent:** [ARC-AGI](#arc-agi)

[https://www.kaggle.com/code/allegich/arc-agi-2025-visualization-all-1000-120-tasks](https://www.kaggle.com/code/allegich/arc-agi-2025-visualization-all-1000-120-tasks) contains plots of all questions and answers. It is truly very convenient.

###### ARC-AGI approach

↑ **Parent:** [ARC-AGI](#arc-agi)

- [https://arcprize.org/guide](https://arcprize.org/guide)
- [https://lewish.io/posts/how-to-beat-arc-agi-2](https://lewish.io/posts/how-to-beat-arc-agi-2)

###### ARC-AGI feature extraction

↑ **Parent:** [ARC-AGI approach](#arc-agi-approach)

[https://www.kaggle.com/code/allegich/eda-statistical-analysis-and-feature-extraction](https://www.kaggle.com/code/allegich/eda-statistical-analysis-and-feature-extraction) has a very basic feature extraction.

###### ARC-AGI implementation

↑ **Parent:** [ARC-AGI](#arc-agi)

Bibliography:
- [https://github.com/zoecarver/grover-arc/issues/1](https://github.com/zoecarver/grover-arc/issues/1)

###### ARC-DSL

↑ **Parent:** [ARC-AGI implementation](#arc-agi-implementation)

[https://github.com/michaelhodel/arc-dsl](https://github.com/michaelhodel/arc-dsl)

This interesting repo defines a set of input transformations that can be composed together into programs to generate the solve ARC problems.

It does not appear to have any [program synthesis](software.md#automatic-programming): it only defines the DSL and then provides manual solutions to the problems.

The README is lacking as usual, an overview of the files is:
- [dsl.py](https://github.com/michaelhodel/arc-dsl/blob/635de4902a5fb4e376f27333feaa396d3f5dfdcb/dsl.py): defines the transformations as Python functions
- [solvers.py](https://github.com/michaelhodel/arc-dsl/blob/635de4902a5fb4e376f27333feaa396d3f5dfdcb/solvers.py): defines solvers for the 400 [ARC-AGI-1 training problems](#arc-agi-1-problem/train)

Intended usage to run the solvers seems to be:
```
git clone https://github.com/fchollet/ARC-AGI
cd ARC-AGI
git checkout 399030444e0ab0cc8b4e199870fb20b863846f34
git clone https://github.com/michaelhodel/arc-dsl
cd arc-dsl
git checkout 635de4902a5fb4e376f27333feaa396d3f5dfdcb
python main.py
```
Unfortunately this blows up on [Ubuntu 25.04](systems-programming.md#ubuntu-25-04) on `test_mpapply` apparently due to a [Python 3.12](programming-language.md#python-3-12) issue and the pull request [https://github.com/michaelhodel/arc-dsl/pull/7](https://github.com/michaelhodel/arc-dsl/pull/7) has been ignored for more than one year, so the project is largely dead.

###### ARC-DSL-2

↑ **Parent:** [ARC-AGI implementation](#arc-agi-implementation)

[https://github.com/arc-dsl-2/arc-dsl-2](https://github.com/arc-dsl-2/arc-dsl-2)

[Ciro Santilli](ciro-santilli.md)'s fork of [ARC-DSL](#arc-dsl) merging all pull requests needed to make tests run again on [Ubuntu 25.04](systems-programming.md#ubuntu-25-04).

<h6 id="cristianoc-arc-agi-2-abstraction-dataset">cristianoc/arc-agi-2-abstraction-dataset</h6>

↑ **Parent:** [ARC-AGI implementation](#arc-agi-implementation)

[https://github.com/cristianoc/arc-agi-2-abstraction-dataset](https://github.com/cristianoc/arc-agi-2-abstraction-dataset)

Contains 120 DSL implementations for the 

From another awesome retired tech bro that does this project for fun.

###### ARC-AGI without LLM

↑ **Parent:** [ARC-AGI implementation](#arc-agi-implementation)

Some mentions at: [https://arcprize.org/blog/arc-prize-2025-results-analysis](https://arcprize.org/blog/arc-prize-2025-results-analysis) section "Zero-Pretraining Deep Learning Methods".

###### CompressARC

↑ **Parent:** [ARC-AGI without LLM](#arc-agi-without-llm)

[https://iliao2345.github.io/blog_posts/arc_agi_without_pretraining/arc_agi_without_pretraining.html](https://iliao2345.github.io/blog_posts/arc_agi_without_pretraining/arc_agi_without_pretraining.html)

###### mdlARC

↑ **Parent:** [ARC-AGI without LLM](#arc-agi-without-llm)

[https://github.com/mvakde/mdlARC](https://github.com/mvakde/mdlARC)

###### Local CPU ARC-AGI without LLM

↑ **Parent:** [ARC-AGI without LLM](#arc-agi-without-llm)

- [https://iliao2345.github.io/blog_posts/arc_agi_without_pretraining/arc_agi_without_pretraining.html](https://iliao2345.github.io/blog_posts/arc_agi_without_pretraining/arc_agi_without_pretraining.html)

<h6 id="aviad12g-arc-agi-solution">aviad12g/ARC-AGI-solution </h6>

↑ **Parent:** [Local CPU ARC-AGI without LLM](#local-cpu-arc-agi-without-llm)

[https://github.com/aviad12g/ARC-AGI-solution](https://github.com/aviad12g/ARC-AGI-solution)

Interesting looking repo with optional [GPU](computer-hardware.md#graphics-processing-unit) and optional [LLM](#large-language-model).

It seems to have been tested on something older than [Ubuntu 24.04](systems-programming.md#ubuntu-24-04), as 24.04 install requires some porting, started process at: [https://github.com/cirosantilli/ARC-AGI-solution/tree/ubuntu-24-04](https://github.com/cirosantilli/ARC-AGI-solution/tree/ubuntu-24-04) but gave up to try [Ubuntu 22.04](systems-programming.md#ubuntu-22-04) instead.

[Ubuntu 22.04](systems-programming.md#ubuntu-22-04) [Docker](systems-programming.md#docker-software) install worked without patches, after installing [Poetry](programming-language.md#poetry-python-package-manager) e.g. to try and solve [1ae2feb7](#arc-agi-2-problem/list/1ae2feb7):
```
git clone https://github.com/aviad12g/ARC-AGI-solution
cd ARC-AGI-solution
git checkout f3283f727488ad98fe575ea6a5ac981e4a188e49
poetry install
git clone https://github.com/arcprize/ARC-AGI-2
`poetry env activate`
export PYTHONPATH="$PWD/src:$PYTHONPATH"
python3 -m arc_solver.cli.main solve ARC-AGI-2/data/evaluation/1ae2feb7.json
```
but towards the end we have:
```
{
  "success": false,
  "error": "Search failed: no_multi_example_solution",
  "search_stats": {
    "nodes_expanded": 21,
    "nodes_generated": 903,
    "termination_reason": "no_multi_example_solution",
    "candidates_generated": 25,
    "examples_validated": 3,
    "validation_success_rate": 0.0,
    "multi_example_used": true
  },
  "predictions": [
    null,
    null,
    null
  ],
  "computation_time": 30.234344280001096,
  "task_id": "1ae2feb7",
  "task_file": "ARC-AGI-2/data/evaluation/1ae2feb7.json",
  "solver_version": "0.1.0",
  "total_time": 30.24239572100123,
  "timestamp": 1760353369.9701269
}

Task: 1ae2feb7.json
Success: False
Error: Search failed: no_multi_example_solution
Multi-example validation: ENABLED
Training examples validated: 3
Candidates generated: 25
Validation success rate: 0.0%
Computation time: 30.23s
Total time: 30.24s
```
so it failed.

Let's see if any of them work at all as advertised:
```
ls ARC-AGI-2/data/evaluation/ | xargs -I'{}' python3 -m arc_solver.cli.main solve 'ARC-AGI-2/data/evaluation/{}' |& tee tmp.txt
```
and at the end:
```
grep 'Success: True' tmp.txt | wc
```
has only 7 successes.

Also weirdly 
```
grep 'Success: True' tmp.txt | wc
```
only has 102 hits, but there were 120 JSON tasks in that folder. I search for the missing executions:
```
diff -u <(grep Task: tmp.txt | cut -d' ' -f2) <(ls ARC-AGI-2/data/evaluation)
```
The first missing one is 135a2760, it blows up with:
```
ERROR: Solve command failed: Object of type HorizontalLinePredicate is not JSON serializable
```
and grepping ERROR gives us:
```
ERROR: Solve command failed: Object of type HorizontalLinePredicate is not JSON serializable
ERROR: Solve command failed: Object of type SizePredicate is not JSON serializable
ERROR: Solve command failed: Object of type HorizontalLinePredicate is not JSON serializable
ERROR: Solve command failed: Object of type HorizontalLinePredicate is not JSON serializable
ERROR: Solve command failed: Object of type ndarray is not JSON serializable
ERROR: Solve command failed: Object of type HorizontalLinePredicate is not JSON serializable
ERROR: Solve command failed: Object of type ndarray is not JSON serializable
ERROR: Solve command failed: Object of type HorizontalLinePredicate is not JSON serializable
ERROR: Solve command failed: Object of type VerticalLinePredicate is not JSON serializable
ERROR: Solve command failed: Object of type VerticalLinePredicate is not JSON serializable
ERROR: Solve command failed: Object of type ndarray is not JSON serializable
ERROR: Solve command failed: Object of type VerticalLinePredicate is not JSON serializable
ERROR: Solve command failed: Object of type ndarray is not JSON serializable
ERROR: Solve command failed: Object of type HorizontalLinePredicate is not JSON serializable
ERROR: Solve command failed: Object of type HorizontalLinePredicate is not JSON serializable
ERROR: Solve command failed: Object of type HorizontalLinePredicate is not JSON serializable
ERROR: Solve command failed: Object of type VerticalLinePredicate is not JSON serializable
ERROR: Solve command failed: Object of type VerticalLinePredicate is not JSON serializable
```
Reported at: [https://github.com/aviad12g/ARC-AGI-solution/issues/1](https://github.com/aviad12g/ARC-AGI-solution/issues/1)

###### ARC-AGI problem set

↑ **Parent:** [ARC-AGI](#arc-agi)

###### Official ARC-AGI problem set

↑ **Parent:** [ARC-AGI problem set](#arc-agi-problem-set)

###### ARC-AGI-1

↑ **Parent:** [Official ARC-AGI problem set](#official-arc-agi-problem-set)

###### ARC-AGI-1 problem

↑ **Parent:** [ARC-AGI-1](#arc-agi-1)

<h6 id="arc-agi-1-problem/train">Train</h6>

↑ **Parent:** [ARC-AGI-1 problem](#arc-agi-1-problem)

<h6 id="arc-agi-1-problem/007bbfb">007bbfb</h6>

↑ **Parent:** [Train](#arc-agi-1-problem/train)

<a id="arc-agi-1-problem/_219"></a>
[https://arcprize.org/play?task=007bbfb7](https://arcprize.org/play?task=007bbfb7)

<a id="arc-agi-1-problem/_220"></a>
Hard input constraints:<a id="arc-agi-1-problem/_221"></a>

<a id="arc-agi-1-problem/_222"></a>
- inputs are 3x3
<a id="arc-agi-1-problem/_223"></a>
- inputs contain only 2 colors monocolored: black and another

<a id="arc-agi-1-problem/_224"></a>
Hard output constraints:<a id="arc-agi-1-problem/_225"></a>

<a id="arc-agi-1-problem/_226"></a>
- output is 3x input width and height. Suggests that the output is a 3x3 grid based on the input.<a id="arc-agi-1-problem/_227"></a>

  <a id="arc-agi-1-problem/_228"></a>
  - stronger: if output is split as a 3x3 grid, then each 3x3 block is either black or a copy as input. Which is which?<a id="arc-agi-1-problem/_229"></a>

    <a id="arc-agi-1-problem/_230"></a>
    - stronger: each pixel of the input determines if block is black or copy (final solution)
<a id="arc-agi-1-problem/_231"></a>
- output contains only two colors: black and another<a id="arc-agi-1-problem/_232"></a>

  <a id="arc-agi-1-problem/_233"></a>
  - stronger: the same two colors as input

<a id="arc-agi-1-problem/_234"></a>
Input output comparison:<a id="arc-agi-1-problem/_235"></a>

<a id="arc-agi-1-problem/_236"></a>
- input appears pasted on output multiple times: suggests it is being copy pasted

<a id="arc-agi-1-problem/_237"></a>
Hard output constraints:<a id="arc-agi-1-problem/_238"></a>

<a id="arc-agi-1-problem/_239"></a>
- <a id="arc-agi-1-problem/_240"></a>
  output is 3x input width and height: suggests that the output is a 3x3 grid based on the input

  <a id="arc-agi-1-problem/_241"></a>
  If that is the case, let's try to figure out what is placed on each output grid.

  <a id="arc-agi-1-problem/_242"></a>
  Notice: each grid element is either blank or the input.

  <a id="arc-agi-1-problem/_243"></a>
  OK so let's determine what in the input determines each output grid.

  <a id="arc-agi-1-problem/_244"></a>
  Because input in 3x3 maybe there's a direct mapping.

<h6 id="arc-agi-1-problem/00d62c1b">00d62c1b</h6>

↑ **Parent:** [Train](#arc-agi-1-problem/train)

<a id="arc-agi-1-problem/_246"></a>
[https://arcprize.org/play?task=00d62c1b](https://arcprize.org/play?task=00d62c1b)

<a id="arc-agi-1-problem/_247"></a>
Hard input constraints:<a id="arc-agi-1-problem/_248"></a>

<a id="arc-agi-1-problem/_249"></a>
- inputs have two colors: green and black

<a id="arc-agi-1-problem/_250"></a>
Hard output constraints:<a id="arc-agi-1-problem/_251"></a>

<a id="arc-agi-1-problem/_252"></a>
- output has three colors: black, green and yellow
<a id="arc-agi-1-problem/_253"></a>
- output has same size as input
<a id="arc-agi-1-problem/_254"></a>
- green is copied from input to output<a id="arc-agi-1-problem/_255"></a>

  <a id="arc-agi-1-problem/_256"></a>
  - output differs from input by making some black pixels yellow. Which pixels are becoming yellow?<a id="arc-agi-1-problem/_257"></a>

    <a id="arc-agi-1-problem/_258"></a>
    - output differs from input by making inner regions (non-diagonal) yellow with non-diagonal flood fill

<h6 id="arc-agi-1-problem/017c7c7b">017c7c7b</h6>

↑ **Parent:** [Train](#arc-agi-1-problem/train)

<a id="arc-agi-1-problem/_260"></a>
[https://arcprize.org/play?task=017c7c7b](https://arcprize.org/play?task=017c7c7b)

<a id="arc-agi-1-problem/_261"></a>
Input constraints:<a id="arc-agi-1-problem/_262"></a>

<a id="arc-agi-1-problem/_263"></a>
- inputs are 3x6

<a id="arc-agi-1-problem/_264"></a>
Output constraints:<a id="arc-agi-1-problem/_265"></a>

<a id="arc-agi-1-problem/_266"></a>
- outputs are 3x9

<a id="arc-agi-1-problem/_267"></a>
TODO: this one is quite challenging.

<h6 id="arc-agi-1-problem/025d127b">025d127b</h6>

↑ **Parent:** [Train](#arc-agi-1-problem/train)

<a id="arc-agi-1-problem/_269"></a>
[https://arcprize.org/play?task=025d127b](https://arcprize.org/play?task=025d127b)

<a id="arc-agi-1-problem/_270"></a>
Output constraints:<a id="arc-agi-1-problem/_271"></a>

<a id="arc-agi-1-problem/_272"></a>
- Input and output have the same size
<a id="arc-agi-1-problem/_273"></a>
- Supposing background is black, input and output contain the same number of objects of each color<a id="arc-agi-1-problem/_274"></a>

  <a id="arc-agi-1-problem/_275"></a>
  - the lower right part of each object (non-diagonal) does not move<a id="arc-agi-1-problem/_276"></a>

    <a id="arc-agi-1-problem/_277"></a>
    - the rest of each object outside the lower right part moves by 1 square to the right

<h6 id="arc-agi-1-problem/0520fde7">0520fde7</h6>

↑ **Parent:** [Train](#arc-agi-1-problem/train)

<a id="arc-agi-1-problem/_279"></a>
[https://arcprize.org/play?task=0520fde7](https://arcprize.org/play?task=0520fde7)

<h6 id="arc-agi-1-problem/eval">Eval</h6>

↑ **Parent:** [ARC-AGI-1 problem](#arc-agi-1-problem)

###### ARC-AGI-2

↑ **Parent:** [Official ARC-AGI problem set](#official-arc-agi-problem-set)

- [https://github.com/arcprize/ARC-AGI-2](https://github.com/arcprize/ARC-AGI-2)
- [https://arcprize.org/play?task=1ae2feb7](https://arcprize.org/play?task=1ae2feb7)

Has the following structure:

- [Training Set](#arc-agi-2-problem/list/train): 1000 tasks: a variety of difficulty levels, easy to hard, designed to contain all "primitives" needed for eval
- [Public Eval Set](#arc-agi-2-problem/list/eval): 120 tasks
- Semi-Private Eval: 120 hard tasks, may have been exposed to limited third-parties eg. via API
- Private Eval Set: 120 tasks, never exposed to third parties

###### ARC-AGI-2 problem

↑ **Parent:** [ARC-AGI-2](#arc-agi-2)

<h6 id="arc-agi-2-problem/approach">Approach</h6>

↑ **Parent:** [ARC-AGI-2 problem](#arc-agi-2-problem)

<h6 id="arc-agi-2-problem/primitive">Primitive</h6>

↑ **Parent:** [Approach](#arc-agi-2-problem/approach)

<a id="arc-agi-2-problem/_290"></a>
These section lists common visual primitives that a solver must first extract in order to infer solutions.

<a id="arc-agi-2-problem/_291"></a>
Some of these have a lot of prior world content, others less.

<a id="arc-agi-2-problem/_292"></a>
Many people have come up with the same idea on the Discord. Some nicely call it [DSL](computer.md#domain-specific-language).

<a id="arc-agi-2-problem/_293"></a>
Implementations:<a id="arc-agi-2-problem/_294"></a>

<a id="arc-agi-2-problem/_295"></a>
- [ARC-DSL](#arc-dsl)

<h6 id="arc-agi-2-problem/input-primitive">Input primitive</h6>

↑ **Parent:** [Primitive](#arc-agi-2-problem/primitive)

<h6 id="arc-agi-2-problem/background-color">Background color</h6>

↑ **Parent:** [Input primitive](#arc-agi-2-problem/input-primitive)

<a id="arc-agi-2-problem/_296"></a>
If a color is inferred to be a background color, it contains no information and should be ignored.

<a id="arc-agi-2-problem/_297"></a>
Most problems tend to use black as a background color, but not all of them.

<h6 id="arc-agi-2-problem/object">Object</h6>

↑ **Parent:** [Input primitive](#arc-agi-2-problem/input-primitive)

<a id="arc-agi-2-problem/_298"></a>
An "object" is a set of points that is understood to be one singular entity.

<a id="arc-agi-2-problem/_299"></a>
Contiguity and having the same color are strong indicators that something should be understood as an object.

<h6 id="arc-agi-2-problem/container">Container</h6>

↑ **Parent:** [Object](#arc-agi-2-problem/object)

<h6 id="arc-agi-2-problem/box">Box</h6>

↑ **Parent:** [Container](#arc-agi-2-problem/container)

<a id="arc-agi-2-problem/_300"></a>
A rectangular container.

<a id="arc-agi-2-problem/_301"></a>
The toplevel viewport is always implicitly understood as a special box.

<h6 id="arc-agi-2-problem/edge">Edge</h6>

↑ **Parent:** [Box](#arc-agi-2-problem/box)

<h6 id="arc-agi-2-problem/left-edge">Left edge</h6>

↑ **Parent:** [Edge](#arc-agi-2-problem/edge)

<h6 id="arc-agi-2-problem/right-edge">Right edge</h6>

↑ **Parent:** [Edge](#arc-agi-2-problem/edge)

<h6 id="arc-agi-2-problem/top-edge">Top edge</h6>

↑ **Parent:** [Edge](#arc-agi-2-problem/edge)

<h6 id="arc-agi-2-problem/bottom-edge">Bottom edge</h6>

↑ **Parent:** [Edge](#arc-agi-2-problem/edge)

<h6 id="arc-agi-2-problem/toplevel-box">Toplevel box</h6>

↑ **Parent:** [Box](#arc-agi-2-problem/box)

<a id="arc-agi-2-problem/_302"></a>
There are two or more boxes drawn inside the toplevel and sharing boundaries with toplevel.

<h6 id="arc-agi-2-problem/two-toplevel-boxes">Two toplevel boxes</h6>

↑ **Parent:** [Toplevel box](#arc-agi-2-problem/toplevel-box)

<h6 id="arc-agi-2-problem/input-output-toplevel-boxes">Input output toplevel boxes</h6>

↑ **Parent:** [Two toplevel boxes](#arc-agi-2-problem/two-toplevel-boxes)

<a id="arc-agi-2-problem/_303"></a>
There are [two toplevel boxes](#arc-agi-2-problem/two-toplevel-boxes), one contains only input, and all output goes to the second one. The second one may also contain some input.

<h6 id="arc-agi-2-problem/monocolor-object">Monocolor object</h6>

↑ **Parent:** [Object](#arc-agi-2-problem/object)

<h6 id="arc-agi-2-problem/primitive-relation">Primitive relation</h6>

↑ **Parent:** [Object](#arc-agi-2-problem/object)

<h6 id="arc-agi-2-problem/distance">Distance</h6>

↑ **Parent:** [Primitive relation](#arc-agi-2-problem/primitive-relation)

<a id="arc-agi-2-problem/_304"></a>
A path is something you obtain by somehow drawing from one point to another, e.g. a [line](#arc-agi-2-problem/line), and then starting another drawing between two points from the end point.

<h6 id="arc-agi-2-problem/adjacent">Adjacent</h6>

↑ **Parent:** [Distance](#arc-agi-2-problem/distance)

<a id="arc-agi-2-problem/_306"></a>
[Distance](#arc-agi-2-problem/distance) = 0.

<h6 id="arc-agi-2-problem/rectangle">Rectangle</h6>

↑ **Parent:** [Object](#arc-agi-2-problem/object)

<a id="arc-agi-2-problem/_307"></a>
Rectangle is like a box but always fully filled.

<h6 id="arc-agi-2-problem/square">Square</h6>

↑ **Parent:** [Rectangle](#arc-agi-2-problem/rectangle)

<h6 id="arc-agi-2-problem/point">Point</h6>

↑ **Parent:** [Square](#arc-agi-2-problem/square)

<a id="arc-agi-2-problem/_308"></a>
A point is a 1-[square](#arc-agi-2-problem/square).

<h6 id="arc-agi-2-problem/path">Path</h6>

↑ **Parent:** [Object](#arc-agi-2-problem/object)

<h6 id="arc-agi-2-problem/dotted-path">Dotted path</h6>

↑ **Parent:** [Path](#arc-agi-2-problem/path)

<a id="arc-agi-2-problem/_309"></a>
A dotted line is a generalized line that cycles between a color pattern, e.g.:<a id="arc-agi-2-problem/_310"></a>


> r r g

would be a line:<a id="arc-agi-2-problem/_311"></a>


> r r g r r g r r g

An extra color "transparent" may also be added to not change for that pixel.

<h6 id="arc-agi-2-problem/line">Line</h6>

↑ **Parent:** [Path](#arc-agi-2-problem/path)

<h6 id="arc-agi-2-problem/dotted-line">Dotted line</h6>

↑ **Parent:** [Line](#arc-agi-2-problem/line)

<a id="arc-agi-2-problem/_312"></a>
A [dotted path](#arc-agi-2-problem/dotted-path) that is also a [dotted line](#arc-agi-2-problem/dotted-line).

<h6 id="arc-agi-2-problem/monocolor-line">Monocolor line</h6>

↑ **Parent:** [Line](#arc-agi-2-problem/line)

<h6 id="arc-agi-2-problem/perpendicular-line">Perpendicular line</h6>

↑ **Parent:** [Line](#arc-agi-2-problem/line)

<h6 id="arc-agi-2-problem/vertical-line">Vertical line</h6>

↑ **Parent:** [Perpendicular line](#arc-agi-2-problem/perpendicular-line)

<h6 id="arc-agi-2-problem/horizontal-line">Horizontal line</h6>

↑ **Parent:** [Perpendicular line](#arc-agi-2-problem/perpendicular-line)

<h6 id="arc-agi-2-problem/diagonal-line">Diagonal line</h6>

↑ **Parent:** [Line](#arc-agi-2-problem/line)

<h6 id="arc-agi-2-problem/repeat">Repeat</h6>

↑ **Parent:** [Input primitive](#arc-agi-2-problem/input-primitive)

<h6 id="arc-agi-2-problem/output-primitive">Output primitive</h6>

↑ **Parent:** [Primitive](#arc-agi-2-problem/primitive)

<h6 id="arc-agi-2-problem/optimize">Optimize</h6>

↑ **Parent:** [Output primitive](#arc-agi-2-problem/output-primitive)

<a id="arc-agi-2-problem/_313"></a>
There is no unique solution, we just have to optimize something, often the least changed colors.

<h6 id="arc-agi-2-problem/draw-line">Draw line</h6>

↑ **Parent:** [Output primitive](#arc-agi-2-problem/output-primitive)

<h6 id="arc-agi-2-problem/list">List</h6>

↑ **Parent:** [ARC-AGI-2 problem](#arc-agi-2-problem)

<h6 id="arc-agi-2-problem/list/train">Train</h6>

↑ **Parent:** [List](#arc-agi-2-problem/list)

<h6 id="arc-agi-2-problem/list/eval">Eval</h6>

↑ **Parent:** [List](#arc-agi-2-problem/list)

<h6 id="arc-agi-2-problem/list/1ae2feb7">1ae2feb7</h6>

↑ **Parent:** [Eval](#arc-agi-2-problem/list/eval)

<a id="arc-agi-2-problem/list/_315"></a>
[https://arcprize.org/play?task=1ae2feb7](https://arcprize.org/play?task=1ae2feb7)

<a id="arc-agi-2-problem/list/_316"></a>
To the left of the vertical red line, count the number of each color on each row.

<a id="arc-agi-2-problem/list/_317"></a>
Then to the right, on each line draw one square of each color to the left every n columns, starting with a square on the first column to the right of the red line, where n is the count of that color.

<a id="arc-agi-2-problem/list/_318"></a>
Start with the color furthest away from the red line, and then color with colors nearer to the red line. If there's overlap, replace the old color with the new one.

<a id="arc-agi-2-problem/list/_319"></a>
Input:<a id="arc-agi-2-problem/list/_320"></a>

<a id="arc-agi-2-problem/list/_321"></a>
- [background color](#arc-agi-2-problem/background-color)
<a id="arc-agi-2-problem/list/_322"></a>
- [dotted line](#arc-agi-2-problem/dotted-line)
<a id="arc-agi-2-problem/list/_323"></a>
- [monocolor line](#arc-agi-2-problem/monocolor-line)
<a id="arc-agi-2-problem/list/_324"></a>
- [box](#arc-agi-2-problem/box)
<a id="arc-agi-2-problem/list/_325"></a>
- [input output toplevel boxes](#arc-agi-2-problem/input-output-toplevel-boxes)

<a id="arc-agi-2-problem/list/_326"></a>
Output:<a id="arc-agi-2-problem/list/_327"></a>

<a id="arc-agi-2-problem/list/_328"></a>
- draw [dotted lines](#arc-agi-2-problem/dotted-line)

<h6 id="arc-agi-2-problem/list/3e6067c3">3e6067c3</h6>

↑ **Parent:** [Eval](#arc-agi-2-problem/list/eval)

<a id="arc-agi-2-problem/list/_330"></a>
[https://arcprize.org/play?task=3e6067c3](https://arcprize.org/play?task=3e6067c3)

<a id="arc-agi-2-problem/list/_331"></a>
Input primitives:<a id="arc-agi-2-problem/list/_332"></a>

<a id="arc-agi-2-problem/list/_333"></a>
- [background color](#arc-agi-2-problem/background-color)
<a id="arc-agi-2-problem/list/_334"></a>
- squares<a id="arc-agi-2-problem/list/_335"></a>

  <a id="arc-agi-2-problem/list/_336"></a>
  - squares with color inside
<a id="arc-agi-2-problem/list/_337"></a>
- points

<a id="arc-agi-2-problem/list/_338"></a>
Transformations primitives:<a id="arc-agi-2-problem/list/_339"></a>

<a id="arc-agi-2-problem/list/_340"></a>
- line drawing

<h6 id="arc-agi-2-problem/list/16b78196">16b78196</h6>

↑ **Parent:** [Eval](#arc-agi-2-problem/list/eval)

<a id="arc-agi-2-problem/list/_342"></a>
[https://arcprize.org/play?task=16b78196](https://arcprize.org/play?task=16b78196)

<a id="arc-agi-2-problem/list/_343"></a>
Solution: move pieces to fill the gap on the fat object that crosses the screen. Place objects either on fat object or on other objects placed on the fat object. Anything you add must end in a rectangle.

<a id="arc-agi-2-problem/list/_344"></a>
The rules for this one are not entirely clear with the number of examples.

<a id="arc-agi-2-problem/list/_345"></a>
Also clearly if the goal is to make rectangular towers, then this is an [NP-hard](computer-science.md#np-hard) optimization problem in general.

<a id="arc-agi-2-problem/list/_346"></a>
Input primitives:<a id="arc-agi-2-problem/list/_347"></a>

<a id="arc-agi-2-problem/list/_348"></a>
- same color chunk. Properties: crosses screen.

<a id="arc-agi-2-problem/list/_349"></a>
Transformation primitives:<a id="arc-agi-2-problem/list/_350"></a>

<a id="arc-agi-2-problem/list/_351"></a>
- move solid around
<a id="arc-agi-2-problem/list/_352"></a>
- fills the gap

<a id="arc-agi-2-problem/list/_353"></a>
This existed earlier: [https://x.com/GianpaoloGalli/status/1846144236900827413](https://x.com/GianpaoloGalli/status/1846144236900827413)

<h6 id="arc-agi-2-problem/list/142ca369">142ca369</h6>

↑ **Parent:** [Eval](#arc-agi-2-problem/list/eval)

<a id="arc-agi-2-problem/list/_355"></a>
[https://arcprize.org/play?task=142ca369](https://arcprize.org/play?task=142ca369)

<a id="arc-agi-2-problem/list/_356"></a>
Solution: vs are guns that shoot diagonal line of their color, when line touches another object, change line color to match that of the object, then bounce on the object and continue going with the new color

<a id="arc-agi-2-problem/list/_357"></a>
Input primitives:<a id="arc-agi-2-problem/list/_358"></a>

<a id="arc-agi-2-problem/list/_359"></a>
- diagonal line

<a id="arc-agi-2-problem/list/_360"></a>
Assumptions:<a id="arc-agi-2-problem/list/_361"></a>

<a id="arc-agi-2-problem/list/_362"></a>
- line don't cross each other, it is unclear how to resolve that case

<a id="arc-agi-2-problem/list/_363"></a>
Transformation primitives:<a id="arc-agi-2-problem/list/_364"></a>

<a id="arc-agi-2-problem/list/_365"></a>
- draw line<a id="arc-agi-2-problem/list/_366"></a>

  <a id="arc-agi-2-problem/list/_367"></a>
  - draw line and bounce

<h6 id="arc-agi-2-problem/list/136b0064">136b0064</h6>

↑ **Parent:** [Eval](#arc-agi-2-problem/list/eval)

<a id="arc-agi-2-problem/list/_369"></a>
[https://arcprize.org/play?task=136b0064](https://arcprize.org/play?task=136b0064)

<a id="arc-agi-2-problem/list/_370"></a>
Input primitive:<a id="arc-agi-2-problem/list/_371"></a>

<a id="arc-agi-2-problem/list/_372"></a>
- [monocolor object](#arc-agi-2-problem/monocolor-object)
<a id="arc-agi-2-problem/list/_373"></a>
- 2 [toplevel boxes](#arc-agi-2-problem/toplevel-box)

<a id="arc-agi-2-problem/list/_374"></a>
Transformation primitives:<a id="arc-agi-2-problem/list/_375"></a>

<a id="arc-agi-2-problem/list/_376"></a>
- draw [lines](#arc-agi-2-problem/line)

<h6 id="arc-agi-2-problem/list/0934a4d8">0934a4d8</h6>

↑ **Parent:** [Eval](#arc-agi-2-problem/list/eval)

<a id="arc-agi-2-problem/list/_378"></a>
[https://arcprize.org/play?task=0934a4d8](https://arcprize.org/play?task=0934a4d8)

<a id="arc-agi-2-problem/list/_379"></a>
TODO I can't solve that one.

<h6 id="arc-agi-2-problem/list/135a2760">135a2760</h6>

↑ **Parent:** [Eval](#arc-agi-2-problem/list/eval)

<a id="arc-agi-2-problem/list/_381"></a>
[https://arcprize.org/play?task=135a2760](https://arcprize.org/play?task=135a2760)

<a id="arc-agi-2-problem/list/_382"></a>
Input:<a id="arc-agi-2-problem/list/_383"></a>

<a id="arc-agi-2-problem/list/_384"></a>
- [background color](#arc-agi-2-problem/background-color)
<a id="arc-agi-2-problem/list/_385"></a>
- [box](#arc-agi-2-problem/box)
<a id="arc-agi-2-problem/list/_386"></a>
- [input output toplevel boxes](#arc-agi-2-problem/input-output-toplevel-boxes)
<a id="arc-agi-2-problem/list/_387"></a>
- [repeat](#arc-agi-2-problem/repeat)

<a id="arc-agi-2-problem/list/_388"></a>
Output:<a id="arc-agi-2-problem/list/_389"></a>

<a id="arc-agi-2-problem/list/_390"></a>
- make [repeat](#arc-agi-2-problem/repeat)
<a id="arc-agi-2-problem/list/_391"></a>
- [optimize](#arc-agi-2-problem/optimize)

<h6 id="arc-agi-2-problem/list/13e47133">13e47133</h6>

↑ **Parent:** [Eval](#arc-agi-2-problem/list/eval)

<a id="arc-agi-2-problem/list/_393"></a>
[https://arcprize.org/play?task=13e47133](https://arcprize.org/play?task=13e47133)

<a id="arc-agi-2-problem/list/_394"></a>
Input:<a id="arc-agi-2-problem/list/_395"></a>

<a id="arc-agi-2-problem/list/_396"></a>
- [background color](#arc-agi-2-problem/background-color)
<a id="arc-agi-2-problem/list/_397"></a>
- [boxes](#arc-agi-2-problem/box)
<a id="arc-agi-2-problem/list/_398"></a>
- [points](#arc-agi-2-problem/point) inside boxes<a id="arc-agi-2-problem/list/_399"></a>

  <a id="arc-agi-2-problem/list/_400"></a>
  - [distance](#arc-agi-2-problem/distance) between point and box

<a id="arc-agi-2-problem/list/_401"></a>
Output:<a id="arc-agi-2-problem/list/_402"></a>

<a id="arc-agi-2-problem/list/_403"></a>
- make [repeat](#arc-agi-2-problem/repeat)
<a id="arc-agi-2-problem/list/_404"></a>
- [optimize](#arc-agi-2-problem/optimize)

<h6 id="arc-agi-2-problem/list/195c6913">195c6913</h6>

↑ **Parent:** [Eval](#arc-agi-2-problem/list/eval)

<a id="arc-agi-2-problem/list/_406"></a>
[https://arcprize.org/play?task=195c6913](https://arcprize.org/play?task=195c6913)

<a id="arc-agi-2-problem/list/_407"></a>
Input: three or more [containers](#arc-agi-2-problem/container):<a id="arc-agi-2-problem/list/_408"></a>

<a id="arc-agi-2-problem/list/_409"></a>
- one [touching](#arc-agi-2-problem/adjacent) top left corner<a id="arc-agi-2-problem/list/_410"></a>

  <a id="arc-agi-2-problem/list/_411"></a>
  - inside it there are three [monocolor objects](#arc-agi-2-problem/monocolor-object)
<a id="arc-agi-2-problem/list/_412"></a>
- one touching bottom right corner of [toplevel box](#arc-agi-2-problem/toplevel-box)<a id="arc-agi-2-problem/list/_413"></a>

  <a id="arc-agi-2-problem/list/_414"></a>
  - inside it there is one [monocolor object](#arc-agi-2-problem/monocolor-object)
<a id="arc-agi-2-problem/list/_415"></a>
- outside of those, touching the left toplevel box edge, there is one or more [point](#arc-agi-2-problem/point)

<a id="arc-agi-2-problem/list/_416"></a>
Output:<a id="arc-agi-2-problem/list/_417"></a>

<a id="arc-agi-2-problem/list/_418"></a>
- draw [dotted path](#arc-agi-2-problem/dotted-path) of [perpendicular line](#arc-agi-2-problem/perpendicular-line)<a id="arc-agi-2-problem/list/_419"></a>

  <a id="arc-agi-2-problem/list/_420"></a>
  - the path color pattern comes from the color of top left objects, ordered from nearest to furthest from top le

###### ARC-AGI-3

↑ **Parent:** [Official ARC-AGI problem set](#official-arc-agi-problem-set)  
🏷️ **Tags:** [Gridworld AI game](#gridworld-ai-game)

They are moving to [2d discrete AI games](#gridworld-ai-game).

Although there is merit in that, it is a shame that it just similar to other pre-existing work such as [gvgai](#gvgai) and many others.

Solutions to these solutions require much more thought to formalize a solution.

Also the solutions are much less unique, finding the actual optimal solution being obviously [NP-hard](computer-science.md#np-hard).

These aspects make those games much less elegant than the older ARC-AGI 1 and 2 counterparts.

###### Unofficial ARC-AGI problem set

↑ **Parent:** [Official ARC-AGI problem set](#official-arc-agi-problem-set)

This section is about unofficial [ARC-AGI](#arc-agi)-like problem sets.

These are interesting from both a:
- practical point of view, as they provide more training data for potential solvers. If you believe that they are representative that is of course.
- theoretical point of view, as they might help to highlight missing or excessive presumptions of the official datasets

[https://github.com/neoneye/arc-dataset-collection](https://github.com/neoneye/arc-dataset-collection) contains a fantastic collection of such datasets, with visualization at: [https://neoneye.github.io/arc/](https://neoneye.github.io/arc/)

###### ARC-AGI problem generator

↑ **Parent:** [Unofficial ARC-AGI problem set](#unofficial-arc-agi-problem-set)

###### re-arc

↑ **Parent:** [ARC-AGI problem generator](#arc-agi-problem-generator)

[https://github.com/michaelhodel/re-arc](https://github.com/michaelhodel/re-arc)

By the author of [ARC-DSL](#arc-dsl).

README says:

> This repository presents code to procedurally generate examples for the ARC training tasks. For each of the 400 tasks, an example generator is provided.

[https://arxiv.org/html/2404.07353v1](https://arxiv.org/html/2404.07353v1) says:

> Each generator is a standalone Python function merely making use of the [DSL](#arc-dsl) and functions from the random module from the standard library. The median generator consists of 40 lines of code and uses 22 DSL primitive calls and 10 calls to the random module.

Cool!

Original:

![](https://web.archive.org/web/20250216160803im_/https://github.com/michaelhodel/re-arc/raw/main/00d62c1b_original.png)

Generated:

![](https://web.archive.org/web/20250216160803im_/https://github.com/michaelhodel/re-arc/raw/main/00d62c1b_generated.png)

###### arc-like

↑ **Parent:** [ARC-AGI problem generator](#arc-agi-problem-generator)

##### The Employment Test

↑ **Parent:** [AGI test](#agi-test)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/The_Employment_Test)

That's [Ciro Santilli](ciro-santilli.md)'s favorite. Of course, there is a huge difference between physical and non physical jobs. But one could start with replacing desk jobs!

#### AGI bibliography

↑ **Parent:** [Artificial general intelligence](#artificial-general-intelligence)  
🏷️ **Tags:** [AI bibliography](#artificial-intelligence-bibliography)

[GitHub awesome repos](software.md#github-awesome-repo):
- [https://github.com/EmbraceAGI/Awesome-AGI](https://github.com/EmbraceAGI/Awesome-AGI)
- [https://github.com/enricoros/awesome-agi](https://github.com/enricoros/awesome-agi)

[Reddit](website.md#reddit) threads:
- [https://www.reddit.com/r/agi/comments/fkmd4v/reading_list_of_agi/](https://www.reddit.com/r/agi/comments/fkmd4v/reading_list_of_agi/)

### Automated theorem proving

↑ **Parent:** [AI by capability](#ai-by-capability)

[AGI-complete](#agi-complete) in general? Obviously. But still, a lot can be done. See e.g.:
- [The Busy Beaver Challenge](computer-science.md#busy-beaver-challenge) deciders

#### Math AI company

↑ **Parent:** [Automated theorem proving](#automated-theorem-proving)  
🏷️ **Tags:** [Machine learning company](machine-learning.md#machine-learning-company)

A good quick December 2025 list: [https://x.com/AlexKontorovich/status/1997051032384446629](https://x.com/AlexKontorovich/status/1997051032384446629)

##### Axiom Math

↑ **Parent:** [Math AI company](#math-ai-company)

- [https://axiommath.ai](https://axiommath.ai)
- [https://x.com/axiommathai](https://x.com/axiommathai)

Not to be confused with tutoring company "Axiom Maths" which shows on top of Google results: [https://axiommaths.com/](https://axiommaths.com/) lol fuck.

<h5 id="harmonic-fun">harmonic.fun</h5>

↑ **Parent:** [Math AI company](#math-ai-company)  
🏷️ **Tags:** [Neuro-symbolic AI](machine-learning.md#neuro-symbolic-ai)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/harmonic.fun)

[https://harmonic.fun/](https://harmonic.fun/)

They seem to do [autoformalization](#autoformalization), [automated theorem proving](#automated-theorem-proving) and [code generation](software.md#automatic-programming), and they use [Lean](formalization-of-mathematics.md#lean-proof-assistant) a lot. Sounds fun.

##### Logical Intelligence Inc.

↑ **Parent:** [Math AI company](#math-ai-company)

Not much info available about them outside of [Twitter](social-technology.md#twitter):
- [https://www.logicalintelligence.com](https://www.logicalintelligence.com)
- [https://x.com/logic_int](https://x.com/logic_int)
They use [Lean](formalization-of-mathematics.md#lean-proof-assistant).

##### Math, Inc

↑ **Parent:** [Math AI company](#math-ai-company)

- [https://www.math.inc/](https://www.math.inc/)

##### Math, Inc careers page puzzle

↑ **Parent:** [Math AI company](#math-ai-company)

[https://www.math.inc/careers](https://www.math.inc/careers)

> Suppose that today is June 1, 2025. We call a date "square" if all of its components (day, month, and year) are perfect squares. I was born in the last millennium, and my next birthday (relative to that date) will be the last square date in my life. If you sum the square roots of the components of that upcoming square birthday (day, month, year), you obtain my age on June 1, 2025. My mother would have been born on a square date if the month were a square number; in reality it is not a square date, but both the month and day are perfect cubes. When was I born, and when was my mother born?

One shot by [GPT-5.1](#gpt-5-1), possibly contaminated obviously:



> You were born on 25 September 1971.



> 



> Your mother was born on 1 August 1936.

##### Principia Labs

↑ **Parent:** [Math AI company](#math-ai-company)

[https://www.principialabs.org](https://www.principialabs.org)

> We combine large-scale pretraining with reinforcement learning to create models that can rederive and learn from the entire corpus of human mathematics. Our goal is automated mathematical discovery: AI that does the creative, generative work that was previously only possible for the world's best researchers—and can be deployed on the hardest problems in science and engineering.

#### Math AI implementation

↑ **Parent:** [Automated theorem proving](#automated-theorem-proving)

Quick list: [https://x.com/AlexKontorovich/status/1997051032384446629](https://x.com/AlexKontorovich/status/1997051032384446629)

##### AlphaProof

↑ **Parent:** [Math AI implementation](#math-ai-implementation)

[https://deepmind.google/discover/blog/ai-solves-imo-problems-at-silver-medal-level/](https://deepmind.google/discover/blog/ai-solves-imo-problems-at-silver-medal-level/)

> AI achieves silver-medal standard solving [International Mathematical Olympiad](social-technology.md#international-mathematical-olympiad) problems

Uses [autoformalization](#autoformalization) down to [Lean](formalization-of-mathematics.md#lean-proof-assistant), and then [AlphaZero](#alphazero). Cool.

###### AlphaGeometry

↑ **Parent:** [AlphaProof](#alphaproof)

[https://www.nature.com/articles/s41586-023-06747-5](https://www.nature.com/articles/s41586-023-06747-5)

##### LeanAgent

↑ **Parent:** [Math AI implementation](#math-ai-implementation)

They do have a database system which is interesting.

#### Autoformalization

↑ **Parent:** [Automated theorem proving](#automated-theorem-proving)

"Autoformalization" refers to automatically converting a traditional human readable mathematical proof to a [formal proof](formalization-of-mathematics.md#formal-proof).

The topic received some attention with the [AI boom](#ai-boom) and rise of [LLMs](#large-language-model):
- [https://leanprover-community.github.io/archive/stream/219941-Machine-Learning-for-Theorem-Proving/topic/autoformalization.3F.html](https://leanprover-community.github.io/archive/stream/219941-Machine-Learning-for-Theorem-Proving/topic/autoformalization.3F.html)

#### Math AI benchmark

↑ **Parent:** [Automated theorem proving](#automated-theorem-proving)  
🏷️ **Tags:** [Computer benchmark](computer.md#computer-benchmark)

This section is about benchmarks designed to test mathematical reasoning.

Bibliography:
- [https://mathscholar.org/2025/02/deepseek-a-breakthrough-in-ai-for-math-and-everything-else/](https://mathscholar.org/2025/02/deepseek-a-breakthrough-in-ai-for-math-and-everything-else/)

##### Closed AI math benchmark

↑ **Parent:** [Math AI benchmark](#math-ai-benchmark)  
🏷️ **Tags:** [Closed source benchmark](software.md#closed-source-benchmark)

Even more than in other areas of benchmarking, in maths where you only have a right or wrong answer, and it is costly to come up with good sample problems, some benchmarks have adopted private test data sets.

The situation is kind of sad, in that ideally we should have open data sets and only test them on models that were trained on data exclusively published before the problem publish date.

However this is not practical for the following reasons:
- some of the best models are closed source and don't have a reproducible training with specified cutoff
- having a private test set allows you to automatically check answers from untrusted sources. If they get answers right, they are onto something, you don't even need to check their methodology

Perhaps the ideal scenario therefore is what [ARC-AGI](#arc-agi) has done: give a sizeable public dataset, which you feel is highly representative of the difficulty level of the private test data, while at the same time holding out some private test data. Half half seems reasonable.

This way, reproducible models can actually self test themselves reliably on the open data, while the closed data can then be used for the cases where the open data can't be used.

##### List of math AI benchmarks

↑ **Parent:** [Math AI benchmark](#math-ai-benchmark)

###### MathArena

↑ **Parent:** [List of math AI benchmarks](#list-of-math-ai-benchmarks)

[https://matharena.ai/](https://matharena.ai/)

This project tests various models against various competitions.

How they "ensure" that models are not contaminated:

>  By evaluating models as soon as new problems are released, we effectively eliminate the risk of contamination

Most of their problems come from [high school knowledge olympiads](social-technology.md#pre-university-knowledge-olympiad) and they are therefore completely irrelevant for 2025 [LLMs](#large-language-model).

###### MathArena Apex

↑ **Parent:** [MathArena](#matharena)

[https://matharena.ai/apex/](https://matharena.ai/apex/)

A subsets of problems that they curate from competitions. 

###### AI Mathematical Olympiad

↑ **Parent:** [List of math AI benchmarks](#list-of-math-ai-benchmarks)  
🏷️ **Tags:** [High school knowledge olympiad](social-technology.md#pre-university-knowledge-olympiad)

[https://aimoprize.com](https://aimoprize.com)

Not too exciting because of the [high school knowledge olympiad](social-technology.md#pre-university-knowledge-olympiad) level, but respectable.

- [https://www.kaggle.com/competitions/ai-mathematical-olympiad-progress-prize-3/overview](https://www.kaggle.com/competitions/ai-mathematical-olympiad-progress-prize-3/overview) is round 3.

  Every problem has one final integer answer:

  > In this competition, every ground-truth label is an integer between 0 and 99999

  Non-integer results like square roots are just rounded off to produce an integer they mention:

  > $10^{4} \sqrt{2} = 14142$

  Also unlike [Project Euler](project-euler.md) and like [IMO](social-technology.md#international-mathematical-olympiad), all only limited computations are required, i.e. you are not expected to do full blown [program generation](software.md#automatic-programming) to reach a final answer. Which makes this further less exciting.

###### ORCA Benchmark

↑ **Parent:** [List of math AI benchmarks](#list-of-math-ai-benchmarks)

[https://arxiv.org/abs/2511.02589](https://arxiv.org/abs/2511.02589)

This one doesn't seem to exciting to be honest, but it might be useful. Sample question:

> If I deposit $50,000 at 5% APR, compounded weekly, what will my balance be after 18 months?

and it expects the correct answer down to the cents:

> 53892.27

It should be noted that [Project Euler](project-euler.md) has such "precision matters" problems.

###### Equational theories project

↑ **Parent:** [List of math AI benchmarks](#list-of-math-ai-benchmarks)

This project initiated by [Terence Tao](mathematics.md#terence-tao) aims to find the relations between various statements in [abstract algebra](algebra.md#abstract-algebra) by using a combination of [automated theorem proving](#automated-theorem-proving) and human effort. As mentioned by Terence himself, this is a bit similar to the idea of the [Busy Beaver Challenge](computer-science.md#busy-beaver-challenge):
- [https://teorth.github.io/equational_theories/](https://teorth.github.io/equational_theories/)
- [https://github.com/teorth/equational_theories](https://github.com/teorth/equational_theories)
- [https://terrytao.wordpress.com/2024/09/25/a-pilot-project-in-universal-algebra-to-explore-new-ways-to-collaborate-and-use-machine-assistance/](https://terrytao.wordpress.com/2024/09/25/a-pilot-project-in-universal-algebra-to-explore-new-ways-to-collaborate-and-use-machine-assistance/)

###### First Proof

↑ **Parent:** [List of math AI benchmarks](#list-of-math-ai-benchmarks)

[https://1stproof.org/](https://1stproof.org/)

###### FrontierMath

↑ **Parent:** [List of math AI benchmarks](#list-of-math-ai-benchmarks)  
🏷️ **Tags:** [Closed source benchmark](software.md#closed-source-benchmark), [OpenAI project](#openai-project)

[https://epoch.ai/frontiermath](https://epoch.ai/frontiermath)

Paper: [https://arxiv.org/abs/2411.04872](https://arxiv.org/abs/2411.04872)

[https://arstechnica.com/ai/2024/11/new-secret-math-benchmark-stumps-ai-models-and-phds-alike/](https://arstechnica.com/ai/2024/11/new-secret-math-benchmark-stumps-ai-models-and-phds-alike/) mentions what the official website is unable to clearly state out:

> The design of FrontierMath differs from many existing AI benchmarks because the problem set remains private and unpublished to prevent data contamination

The expected answer output for all problems is one single SymPy expression, which is kind of a cool approach which allows either for large integers like [Project Euler](project-euler.md), but also for irrational expressions to be given, e.g. "An optimization problem in BMO space" from the sample problems has answer:

$$
\frac{\sqrt{3}}{36} + \frac{\sqrt{3}}{6} e^{-20\sqrt{3} - \frac{1}{6}}
$$

Of course, when the output is not an integer, this leads to the question of simplification equivalence questions. Also, like [Project Euler](project-euler.md), solutions essentially expect you to write and execute code.

The most interesting aspect of this benchmark is the difficulty. [Mathematical olympiad](social-technology.md#mathematical-olympiad) coach [Evan Chen](mathematics.md#evan-chen) comments:[https://arstechnica.com/ai/2024/11/new-secret-math-benchmark-stumps-ai-models-and-phds-alike/](https://arstechnica.com/ai/2024/11/new-secret-math-benchmark-stumps-ai-models-and-phds-alike/)

> Problems in \[the [International Mathematical Olympiad](social-technology.md#international-mathematical-olympiad)\] typically require creative insight while avoiding complex implementation and specialized knowledge \[but for [FrontierMath](#frontiermath)\] they keep the first requirement, but outright invert the second and third requirement

###### Elliot Glazer

↑ **Parent:** [FrontierMath](#frontiermath)

Creator of [FrontierMath](#frontiermath).

Socials:
- [https://x.com/ElliotGlazer](https://x.com/ElliotGlazer)

###### IMProofBench

↑ **Parent:** [List of math AI benchmarks](#list-of-math-ai-benchmarks)  
🏷️ **Tags:** [Closed source benchmark](software.md#closed-source-benchmark)

[https://improofbench.math.ethz.ch/](https://improofbench.math.ethz.ch/)

Paper: [https://arxiv.org/html/2509.26076v1](https://arxiv.org/html/2509.26076v1)

Apparently also has human review as part of the process. Newbs. Just require Lean solutions and be done with it... They do address it in a section of the paper "Formal math benchmarks" but still meh. Review must be fully automated, none of that asking humans bullshit.

From: [https://improofbench.math.ethz.ch/guidelines/](https://improofbench.math.ethz.ch/guidelines/)

> Required Characteristics
> 
> PhD-level difficulty: Suitable for qualifying exams, research papers, or advanced seminars
> 
> Requires genuine insight: Not solvable by routine application of known algorithms
> 
> Clear proof-based main question: Answer should be a complete mathematical argument, not just a number
> 
> 2-3 unique-answer subquestions: Enable automated evaluation (e.g., "Is the statement true for n=5?", "What is the rank of this group?")

Example problem:

> Example 1: Stable Graphs
> 
> Main question: Find a closed formula for the number $N(g)$ of stable graphs of genus $g$ with no legs and precisely 3 edges, for all $g \ge 2$.
> 
> Subquestions:
> 
> 
> - What is $N(3)$?
> - What is $N(8)$?
> - What is $N(1000)$?

###### LiveBench

↑ **Parent:** [List of math AI benchmarks](#list-of-math-ai-benchmarks)

- [https://livebench.ai](https://livebench.ai)

Math almost saturated as of 2025 release, so meh:

> modified questions based on high school math competitions from the past 11 months, as well as harder versions of AMPS questions 

###### Putnam-AXIOM

↑ **Parent:** [List of math AI benchmarks](#list-of-math-ai-benchmarks)

[https://openreview.net/forum?id=kqj2Cn3Sxr](https://openreview.net/forum?id=kqj2Cn3Sxr)

> We introduce Putnam-AXIOM, a benchmark of 522 university-level competition problems drawn from the prestigious William Lowell Putnam Mathematical Competition, and Putnam-AXIOM Variation, an unseen companion set of 100 functional variants generated by programmatically perturbing variables and constants.

###### Verina

↑ **Parent:** [List of math AI benchmarks](#list-of-math-ai-benchmarks)

[https://verina.io](https://verina.io)

[AI code generation benchmark](software.md#ai-code-generation-benchmark) in which part of the benchmark includes producing a formal [Lean](formalization-of-mathematics.md#lean-proof-assistant) proof of the implementation. Sweet.

### Regression analysis

↑ **Parent:** [AI by capability](#ai-by-capability)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Regression_analysis)

Regression analysis means to try and predict one final value from a bunch of input values.

For example, you might want to predict the most likely price of a house based on several factors such as its area, GPS coordinates and tax rate. Here is a [Kaggle](social-technology.md#kaggle) example of that: [https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data)

#### Linear regression

↑ **Parent:** [Regression analysis](#regression-analysis)

### Statistical classification

↑ **Parent:** [AI by capability](#ai-by-capability)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Statistical_classification)

### Cluster analysis

↑ **Parent:** [AI by capability](#ai-by-capability)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cluster_analysis)

### Generative AI

↑ **Parent:** [AI by capability](#ai-by-capability)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Generative_artificial_intelligence)

#### Generative adversarial network

↑ **Parent:** [Generative AI](#generative-ai)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Generative_adversarial_network)

Original paper: [Section "GAN paper"](#gan-paper).

##### GAN paper

↑ **Parent:** [Generative adversarial network](#generative-adversarial-network)

[https://proceedings.neurips.cc/paper_files/paper/2014/file/5ca3e9b122f61f8f06494c97b1afccf3-Paper.pdf](https://proceedings.neurips.cc/paper_files/paper/2014/file/5ca3e9b122f61f8f06494c97b1afccf3-Paper.pdf)

##### GAN MNIST hello world

↑ **Parent:** [Generative adversarial network](#generative-adversarial-network)

The [GAN paper](#gan-paper) itself does a bit of this, cool hello world:
- [https://github.com/lyeoni/pytorch-mnist-GAN](https://github.com/lyeoni/pytorch-mnist-GAN)

##### AI brittleness and robustness

↑ **Parent:** [Generative adversarial network](#generative-adversarial-network)

###### AI robustness

↑ **Parent:** [AI brittleness and robustness](#ai-brittleness-and-robustness)

###### AI brittleness

↑ **Parent:** [AI brittleness and robustness](#ai-brittleness-and-robustness)

[Generative adversarial network](#generative-adversarial-network) illustrates well [AI brittleness](#ai-brittleness). The input looks obvious for a human, but gets completely misclassified by a [deep learning](machine-learning.md#deep-learning) agent.

###### Adversarial machine learning

↑ **Parent:** [AI brittleness](#ai-brittleness)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Adversarial_machine_learning)

#### AI generated porn

↑ **Parent:** [Generative AI](#generative-ai)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Generative_artificial_intelligence)

This is going to be the most important application of [generative AI](#generative-ai). Especially if we ever achieve good [text-to-video](#text-to-video).

Image generators plus human ranking:
- [https://pornpen.ai/](https://pornpen.ai/) a bit too restrictive. Girl laying down. Girl sitting. Penis or no penis. But relatively good at it
- [https://civitai.tv/](https://civitai.tv/). How to reach it: [https://civitai.tv/tag/nun/2/](https://civitai.tv/tag/nun/2/)

[https://www.pornhub.com/view_video.php?viewkey=ph63c71351edece](https://www.pornhub.com/view_video.php?viewkey=ph63c71351edece): Heavenly Bodies Part 1: Sister's Mary First Act. [Pornhub](art.md#pornhub) title: "AI generated Hentai Story: Sexy Nun alternative World(Isekai) Stable Diffusion" Interesting concept, slide-narrated over visual novel. The question is how they managed to keep face consistency across images.

#### Generative AI by modality

↑ **Parent:** [Generative AI](#generative-ai)

##### Image generation

↑ **Parent:** [Generative AI by modality](#generative-ai-by-modality)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Image_generation)

###### Face generation

↑ **Parent:** [Image generation](#image-generation)

Very useful for idiotic websites that require real photos!

- [https://thispersondoesnotexist.com/](https://thispersondoesnotexist.com/) holy fuck, the images are so photorealistic, that [when there's a slight fail, it is really, really scary](brain.md#uncanny-valley)

###### Text-to-image generation

↑ **Parent:** [Image generation](#image-generation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Text-to-image_generation)

###### Text-to-image model

↑ **Parent:** [Text-to-image generation](#text-to-image-generation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Text-to-image_model)

- [https://deepai.org/machine-learning-model/text2img](https://deepai.org/machine-learning-model/text2img)
- [https://openai.com/blog/dall-e/](https://openai.com/blog/dall-e/)

###### Open source text-to-image model

↑ **Parent:** [Text-to-image model](#text-to-image-model)

Bibliography:
- [https://www.edenai.co/post/top-free-image-generation-tools-apis-and-open-source-models](https://www.edenai.co/post/top-free-image-generation-tools-apis-and-open-source-models)

<h6 id="ludicrains-deep-gaze">ludicrains/deep-gaze</h6>

↑ **Parent:** [Open source text-to-image model](#open-source-text-to-image-model)

[https://github.com/lucidrains/deep-daze](https://github.com/lucidrains/deep-daze)

This just works, but it is also so incredibly slow that it is useless (or at least the quality it reaches in the time we have patience to wait from), at least on any setup we've managed to try, including e.g. on an [Nvidia A10G](computer-hardware.md#nvidia-a10g) on a [g5.xlarge](computer-hardware.md#g5-xlarge). Running:
```
time imagine "a house in the forest"
```
would likely take hours to complete.

<h6 id="runwayml-stable-diffusion">runwayml/stable-diffusion</h6>

↑ **Parent:** [Open source text-to-image model](#open-source-text-to-image-model)

[https://github.com/runwayml/stable-diffusion](https://github.com/runwayml/stable-diffusion)

[Conda](programming-language.md#conda) install is a bit annoying, but gets the job done. The generation quality is very good.

Someone should package this better for end user "just works after Conda install" image generation, it is currently much more of a library setup.

Tested on [Amazon EC2](computer-hardware.md#amazon-elastic-compute-cloud) on a [g5.xlarge](computer-hardware.md#g5-xlarge) machine, which has an [Nvidia A10G](computer-hardware.md#nvidia-a10g), using the [AWS Deep Learning Base GPU AMI (Ubuntu 20.04)](computer-hardware.md#aws-deep-learning-base-gpu-ami-ubuntu-20-04) image.

First install [Conda](programming-language.md#conda) as per [Section "Install Conda on Ubuntu"](programming-language.md#install-conda-on-ubuntu), and then just follow the instructions from the README, notably the [Reference sampling script](https://github.com/runwayml/stable-diffusion/tree/08ab4d326c96854026c4eb3454cd3b02109ee982#reference-sampling-script) section.
```
git clone https://github.com/runwayml/stable-diffusion
cd stable-diffusion/
git checkout 08ab4d326c96854026c4eb3454cd3b02109ee982
conda env create -f environment.yaml
conda activate ldm
mkdir -p models/ldm/stable-diffusion-v1/
wget -O models/ldm/stable-diffusion-v1/model.ckpt https://huggingface.co/CompVis/stable-diffusion-v-1-4-original/resolve/main/sd-v1-4.ckpt
python scripts/txt2img.py --prompt "a photograph of an astronaut riding a horse" --plms
```
This took about 2 minutes and generated 6 images under `outputs/txt2img-samples/samples`, includining an image `outputs/txt2img-samples/grid-0000.png` which is a grid montage containing all the six images in one:

![](https://raw.githubusercontent.com/cirosantilli/media/master/Runwayml_stable-diffusion_a-photograph-of-an-astronaut-riding-a-horse.png)

TODO how to change the number of images?

A quick attempt at removing their useless safety features (watermark and [NSFW](art.md#not-safe-for-work) text filter) is:
```
diff --git a/scripts/txt2img.py b/scripts/txt2img.py
index 59c16a1..0b8ef25 100644
--- a/scripts/txt2img.py
+++ b/scripts/txt2img.py
@@ -87,10 +87,10 @@ def load_replacement(x):
 def check_safety(x_image):
     safety_checker_input = safety_feature_extractor(numpy_to_pil(x_image), return_tensors="pt")
     x_checked_image, has_nsfw_concept = safety_checker(images=x_image, clip_input=safety_checker_input.pixel_values)
-    assert x_checked_image.shape[0] == len(has_nsfw_concept)
-    for i in range(len(has_nsfw_concept)):
-        if has_nsfw_concept[i]:
-            x_checked_image[i] = load_replacement(x_checked_image[i])
+    #assert x_checked_image.shape[0] == len(has_nsfw_concept)
+    #for i in range(len(has_nsfw_concept)):
+    #    if has_nsfw_concept[i]:
+    #        x_checked_image[i] = load_replacement(x_checked_image[i])
     return x_checked_image, has_nsfw_concept


@@ -314,7 +314,7 @@ def main():
                             for x_sample in x_checked_image_torch:
                                 x_sample = 255. * rearrange(x_sample.cpu().numpy(), 'c h w -> h w c')
                                 img = Image.fromarray(x_sample.astype(np.uint8))
-                                img = put_watermark(img, wm_encoder)
+                                # img = put_watermark(img, wm_encoder)
                                 img.save(os.path.join(sample_path, f"{base_count:05}.png"))
                                 base_count += 1
```
but that produced 4 black images and only two unfiltered ones. Also likely the lack of sexual training data makes its porn suck, and not in the good way.

###### DeepFloyd IF

↑ **Parent:** [Open source text-to-image model](#open-source-text-to-image-model)

[https://github.com/deep-floyd/IF](https://github.com/deep-floyd/IF)

##### AI text generation

↑ **Parent:** [Generative AI by modality](#generative-ai-by-modality)

###### Speech recognition

↑ **Parent:** [AI text generation](#ai-text-generation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Speech_recognition)

[Open source software](software.md#open-source-software) reviews by [Ciro Santilli](ciro-santilli.md):
- [https://askubuntu.com/questions/24059/automatically-generate-subtitles-close-caption-from-a-video-using-speech-to-text/1522895#1522895](https://askubuntu.com/questions/24059/automatically-generate-subtitles-close-caption-from-a-video-using-speech-to-text/1522895#1522895)
- [https://askubuntu.com/questions/161515/speech-recognition-app-to-convert-mp3-voice-to-text/1499768#1499768](https://askubuntu.com/questions/161515/speech-recognition-app-to-convert-mp3-voice-to-text/1499768#1499768)
- [https://unix.stackexchange.com/questions/256138/is-there-any-decent-speech-recognition-software-for-linux/613392#613392](https://unix.stackexchange.com/questions/256138/is-there-any-decent-speech-recognition-software-for-linux/613392#613392)
reviewing mostly the following software:
- [OpenAi Whisper](#openai-whisper)
- [Vosk](#vosk)

###### Speech recognition software

↑ **Parent:** [Speech recognition](#speech-recognition)

Bibliography:
- [https://askubuntu.com/questions/161515/speech-recognition-app-to-convert-mp3-voice-to-text/1499768#1499768](https://askubuntu.com/questions/161515/speech-recognition-app-to-convert-mp3-voice-to-text/1499768#1499768)
- [https://unix.stackexchange.com/questions/256138/is-there-any-decent-speech-recognition-software-for-linux/613392#613392](https://unix.stackexchange.com/questions/256138/is-there-any-decent-speech-recognition-software-for-linux/613392#613392)

###### OpenAi Whisper

↑ **Parent:** [Speech recognition software](#speech-recognition-software)  
🏷️ **Tags:** [OpenAI project](#openai-project)

###### Vosk

↑ **Parent:** [Speech recognition software](#speech-recognition-software)

###### Text-to-text model

↑ **Parent:** [AI text generation](#ai-text-generation)

###### Machine translation

↑ **Parent:** [Text-to-text model](#text-to-text-model)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Machine_translation)

###### Open source machine translation

↑ **Parent:** [Text-to-text model](#text-to-text-model)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Open_source_machine_translation)

[https://askubuntu.com/questions/380847/is-it-possible-to-translate-words-via-terminal/1309774#1309774](https://askubuntu.com/questions/380847/is-it-possible-to-translate-words-via-terminal/1309774#1309774)

###### OpenNMT

↑ **Parent:** [Open source machine translation](#open-source-machine-translation)

###### Argos Translate

↑ **Parent:** [OpenNMT](#opennmt)  
🏷️ **Tags:** [CLI tool](software.md#command-line-utility)

[OpenNMT](#opennmt) [CLI](software.md#command-line-interface) front-end.

Hello world: [https://askubuntu.com/questions/380847/is-it-possible-to-translate-words-via-terminal/1309774#1309774](https://askubuntu.com/questions/380847/is-it-possible-to-translate-words-via-terminal/1309774#1309774)

###### Large language model

↑ **Parent:** [Text-to-text model](#text-to-text-model)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Large_language_model)

###### LLM game

↑ **Parent:** [Large language model](#large-language-model)

- 2023 [https://vimalabs.github.io/](https://vimalabs.github.io/) VIMA: General Robot Manipulation with Multimodal Prompts

###### Stanford Smallville

↑ **Parent:** [LLM game](#llm-game)

[https://github.com/joonspk-research/generative_agents](https://github.com/joonspk-research/generative_agents)

Published as: [https://arxiv.org/pdf/2304.03442.pdf](https://arxiv.org/pdf/2304.03442.pdf) Generative Agents: Interactive Simulacra of Human Behavior by Park et al.

<a id="video-ai-agents-behaving-like-humans-by-prompt-engineering-2023"></a>
**[Video 9](#video-ai-agents-behaving-like-humans-by-prompt-engineering-2023). AI Agents Behaving Like Humans by Prompt Engineering (2023)** [Source](https://www.youtube.com/watch?v=nWBEMjAoA14).

###### [LLM](#large-language-model) [inference](machine-learning.md#inference-ml) optimization

↑ **Parent:** [Large language model](#large-language-model)

This section discusses techniques that can be used to make [LLMs](#large-language-model) infer with lower latency or greater throughput.

Bibliography:
- [https://developer.nvidia.com/blog/mastering-llm-techniques-inference-optimization/](https://developer.nvidia.com/blog/mastering-llm-techniques-inference-optimization/)

###### LLM inference batching

↑ **Parent:** [LLM inference optimization](#llm-inference-optimization)

[LLM inference batching](#llm-inference-batching) means running multiple independent queries in parallel on a given model.

This can be used to overcome the fact that most single prompt inference will be heavily [memory bound](software.md#memory-bound), see also: [Section "Theoretical peak performance of GPT inference"](#theoretical-peak-performance-of-gpt-inference). Batching helps increase the GPU compute utilization and balance it out with the memory.

Bibliography:
- [https://medium.com/@yohoso/llm-inference-optimisation-continuous-batching-2d66844c19e9](https://medium.com/@yohoso/llm-inference-optimisation-continuous-batching-2d66844c19e9)
- [https://www.hyperstack.cloud/technical-resources/tutorials/static-vs.-continuous-batching-for-large-language-model-inference](https://www.hyperstack.cloud/technical-resources/tutorials/static-vs.-continuous-batching-for-large-language-model-inference)

###### LLM KV Caching

↑ **Parent:** [LLM inference optimization](#llm-inference-optimization)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Transformer_(deep_learning_architecture)#KV_caching)

Bibliography:
- [https://huggingface.co/blog/not-lain/kv-caching](https://huggingface.co/blog/not-lain/kv-caching)
- [https://medium.com/@joaolages/kv-caching-explained-276520203249](https://medium.com/@joaolages/kv-caching-explained-276520203249)

###### Grouped-Query attention

↑ **Parent:** [LLM inference optimization](#llm-inference-optimization)

Bibliography:
- [https://aliissa99.medium.com/-a596e4d86f79](https://aliissa99.medium.com/-a596e4d86f79)

###### Generative pre-trained transformer

↑ **Parent:** [Large language model](#large-language-model)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Generative_pre-trained_transformer)

<a id="video-5-years-of-gpts-by-finbarr-timbers"></a>
**[Video 10](#video-5-years-of-gpts-by-finbarr-timbers). 5 Years of GPTs by Finbarr Timbers.** [Source](https://www.youtube.com/watch?v=YA0pzBYAV2Q). 2023. Good talk.

<a id="video-attention-in-transformers-step-by-step-by-3blue1brown"></a>
**[Video 11](#video-attention-in-transformers-step-by-step-by-3blue1brown). Attention in transformers, step-by-step by 3Blue1Brown.** [Source](https://www.youtube.com/watch?v=eMlx5fFNoYc). 2024. Uses on [GPT-3](#gpt-3) as basis.

<a id="video-how-might-llms-store-facts-by-3blue1brown"></a>
**[Video 12](#video-how-might-llms-store-facts-by-3blue1brown). How might LLMs store facts by 3Blue1Brown.** [Source](https://www.youtube.com/watch?v=9-Jl0dxWQs8). Followup to the above video.

###### ChatGPT

↑ **Parent:** [Generative pre-trained transformer](#generative-pre-trained-transformer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/ChatGPT)

###### Codex

↑ **Parent:** [ChatGPT](#chatgpt)

###### Codex CLI

↑ **Parent:** [Codex](#codex)

###### Codex CLI HOWTO

↑ **Parent:** [Codex](#codex)

###### Prevent Codex CLI from reading certain files via the sandbox

↑ **Parent:** [Codex CLI HOWTO](#codex-cli-howto)

- [https://stackoverflow.com/questions/79959031/how-to-prevent-codex-cli-from-reading-certain-files-or-directories-via-sandbox](https://stackoverflow.com/questions/79959031/how-to-prevent-codex-cli-from-reading-certain-files-or-directories-via-sandbox)
- [https://www.reddit.com/r/codex/comments/1s0vaea/disallow_codex_read_env/](https://www.reddit.com/r/codex/comments/1s0vaea/disallow_codex_read_env/)
- [https://www.reddit.com/r/ChatGPTCoding/comments/1mkx3yy/restricting_access_to_sensitive_files_env_etc_in/](https://www.reddit.com/r/ChatGPTCoding/comments/1mkx3yy/restricting_access_to_sensitive_files_env_etc_in/)

###### Get a notification when Codex CLI finishes the current prompt

↑ **Parent:** [Codex CLI HOWTO](#codex-cli-howto)

[https://stackoverflow.com/questions/79933632/how-to-get-a-notification-whenever-codex-cli-finishes-its-current-task](https://stackoverflow.com/questions/79933632/how-to-get-a-notification-whenever-codex-cli-finishes-its-current-task)

###### Allow Codex CLI to run shell commands with Internet access

↑ **Parent:** [Codex CLI HOWTO](#codex-cli-howto)

- [https://stackoverflow.com/questions/79970154/how-to-allow-codex-cli-to-execute-shell-commands-with-internet-access-from-withi/79970156#79970156](https://stackoverflow.com/questions/79970154/how-to-allow-codex-cli-to-execute-shell-commands-with-internet-access-from-withi/79970156#79970156)
- [https://www.reddit.com/r/OpenaiCodex/comments/1qxka1e/how_do_you_give_codex_access_to_web_sites/](https://www.reddit.com/r/OpenaiCodex/comments/1qxka1e/how_do_you_give_codex_access_to_web_sites/)

###### GPT model

↑ **Parent:** [Generative pre-trained transformer](#generative-pre-trained-transformer)

###### Theoretical peak performance of [GPT](#generative-pre-trained-transformer) inference

↑ **Parent:** [GPT model](#gpt-model)

For inferencing just a single prompt, things appear to be very obviously memory bound, i.e. bound by the transfer speeds of [VRAM](computer-hardware.md#video-random-access-memory) to GPU cache for loading model parameters into GPU so they can be used, supposing that the model fits in [VRAM](computer-hardware.md#video-random-access-memory), which is the case for many popular models.

It is however possible to make fuller utilization of the GPU's compute power by running multiple independent queries in parallel, this way you load the subset of model weights that you need, and then use those to do part of the inference for multiple input prompts. With this it should be possible to reach full utilization.

Bibliography:
- [https://www.reddit.com/r/LocalLLaMA/comments/1brcnps/is_inferencing_memory_bandwidth_limited/](https://www.reddit.com/r/LocalLLaMA/comments/1brcnps/is_inferencing_memory_bandwidth_limited/)
- [https://zeux.io/2024/03/15/llm-inference-sol/](https://zeux.io/2024/03/15/llm-inference-sol/)
8 [https://jax-ml.github.io/scaling-book/](https://jax-ml.github.io/scaling-book/)

###### Number of multiplications per token in a [GPT](#generative-pre-trained-transformer) model

↑ **Parent:** [Theoretical peak performance of GPT inference](#theoretical-peak-performance-of-gpt-inference)

The following is for a "classic" [GPT-2](#gpt-2)-style model, the following estimates the number attention multiplications.

For each layer (L):
- for each attention head (h):
  - K = d\_model \* d\_head (takes embedding of one token and converts to vector of length d\_head)
  - Q = d\_model \* d\_head (same)
  - K Q dot product for attention pattern: n\_ctx \* d\_head (n\_ctx times dot products of vectors of size d\_head, once new K vs every Q. Q vs every K zeroed out by causality.)
  - new value vector for new token: d\_model \* d\_model
  - new updates: n\_ctx \* d\_model (multiply each value vector by the new attention column scalar)
- fully connected: d\_model \* d\_ff + d\_ff \* d\_model (converts the embedding to the hidden layer size and then back)
So the total sum is:
```
L * (
  h * (
    2 * d_model * d_head +
    n_ctx * d_head +
    d_model * d_model +
    n_ctx * d_model
  ) +
  2 * d_model * d_ff
)
```

This is coded at: [llm_count_mults.py](llm_count_mults.py).

Bibliography:
- [https://www.reddit.com/r/theydidthemath/comments/1fzrs1k/request_how_many_individual/](https://www.reddit.com/r/theydidthemath/comments/1fzrs1k/request_how_many_individual/)
- [https://www.gaohongnan.com/playbook/training/how_to_calculate_flops_in_transformer_based_models.html#sanity-check-with-palm-paper-s-flops-calculation](https://www.gaohongnan.com/playbook/training/how_to_calculate_flops_in_transformer_based_models.html#sanity-check-with-palm-paper-s-flops-calculation)

###### List of GPT models

↑ **Parent:** [GPT model](#gpt-model)

###### GPT model by [Google](google.md)

↑ **Parent:** [List of GPT models](#list-of-gpt-models)

###### Gemini model

↑ **Parent:** [GPT model by Google](#gpt-model-by-google)

###### Gemini 3

↑ **Parent:** [Gemini model](#gemini-model)

###### GPT model by [OpenAI](#openai)

↑ **Parent:** [List of GPT models](#list-of-gpt-models)

###### GPT-1

↑ **Parent:** [GPT model by OpenAI](#gpt-model-by-openai)

###### Improving Language Understanding by Generative Pre-Training

↑ **Parent:** [GPT-1](#gpt-1)

###### GPT-2

↑ **Parent:** [GPT model by OpenAI](#gpt-model-by-openai)

- Vocabulary size (V): 50,257
- Hidden size (d\_model): 768
- Context length (n\_ctx): 1024
- Q V size: (d\_head): 64
- Attention heads (h): 12
- FFN inner size (d\_ff): 3072
- Layers (L): 12

###### Language Models are Unsupervised Multitask Learners

↑ **Parent:** [GPT-2](#gpt-2)

[https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf](https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf)

###### GPT-2 implementation

↑ **Parent:** [GPT-2](#gpt-2)

###### GPT-2 implementation in [PyTorch](machine-learning.md#pytorch)

↑ **Parent:** [GPT-2](#gpt-2)  
🏷️ **Tags:** [PyTorch model](machine-learning.md#pytorch-model)

###### nanoGPT

↑ **Parent:** [GPT-2 implementation in PyTorch](#gpt-2-implementation-in-pytorch)

[https://github.com/karpathy/nanoGPT](https://github.com/karpathy/nanoGPT)

###### GPT-2 variant

↑ **Parent:** [GPT-2](#gpt-2)

###### GPT-2 medium

↑ **Parent:** [GPT-2 variant](#gpt-2-variant)

###### GPT-2 large

↑ **Parent:** [GPT-2 variant](#gpt-2-variant)

###### GPT-2 XL

↑ **Parent:** [GPT-2 variant](#gpt-2-variant)

###### GPT-3

↑ **Parent:** [GPT model by OpenAI](#gpt-model-by-openai)

- Vocabulary size (V): 50,257
- Hidden size (d\_model): 12,288
- Context length	2048
- Q V size: (d\_head): 128
- Attention heads	(h): 96
- FFN inner size (d\_ff)	4 × 12,288 = 49,152
- Layers (L): 96

###### GPT-4

↑ **Parent:** [GPT model by OpenAI](#gpt-model-by-openai)

###### GPT 4 Turbo

↑ **Parent:** [GPT-4](#gpt-4)

[https://platform.openai.com/docs/models/gpt-4-turbo](https://platform.openai.com/docs/models/gpt-4-turbo)

###### GPT-5

↑ **Parent:** [GPT model by OpenAI](#gpt-model-by-openai)

<h6 id="gpt-5-1">GPT-5.1</h6>

↑ **Parent:** [GPT-5](#gpt-5)

<h6 id="gpt-5-1-pro">GPT-5.1 Pro</h6>

↑ **Parent:** [GPT-5.1](#gpt-5-1)

This is the variant of [GPT-5.1](#gpt-5-1) that you get on the web UI. It is unknown exactly how it correlates with the API.

<h6 id="gpt-5-4">GPT-5.4</h6>

↑ **Parent:** [GPT-5](#gpt-5)

###### Llama (language model)

↑ **Parent:** [List of GPT models](#list-of-gpt-models)  
🏷️ **Tags:** [Open weight LLM model](#open-weight-llm-model), [Software developed by Facebook ](social-technology.md#software-developed-by-facebook)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Llama_(language_model))

Homepage: [https://www.llama.com/](https://www.llama.com/)

###### Llama 2

↑ **Parent:** [Llama (language model)](#llama-language-model)

Page: [https://www.llama.com/llama2/](https://www.llama.com/llama2/)

###### Llama 2 7B

↑ **Parent:** [Llama 2](#llama-2)

###### Llama 3

↑ **Parent:** [Llama (language model)](#llama-language-model)

[https://www.llama.com/models/llama-3/](https://www.llama.com/models/llama-3/)

<h6 id="llama-3-1">Llama 3.1</h6>

↑ **Parent:** [Llama 3](#llama-3)

<h6 id="llama-3-1-8b">Llama 3.1 8B</h6>

↑ **Parent:** [Llama 3.1](#llama-3-1)

<h6 id="llama-3-1-70b">Llama 3.1 70B</h6>

↑ **Parent:** [Llama 3.1](#llama-3-1)

<h6 id="llama-3-1-405b">Llama 3.1 405B</h6>

↑ **Parent:** [Llama 3.1](#llama-3-1)

###### Open source LLM

↑ **Parent:** [Large language model](#large-language-model)  
🏷️ **Tags:** [Open source software](software.md#open-source-software)

###### LLM model with open training data

↑ **Parent:** [Open source LLM](#open-source-llm)

###### The Pile (dataset)

↑ **Parent:** [LLM model with open training data](#llm-model-with-open-training-data)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/The_Pile_(dataset))

###### LLM360

↑ **Parent:** [LLM model with open training data](#llm-model-with-open-training-data)

###### Open weight LLM model

↑ **Parent:** [Open source LLM](#open-source-llm)

###### Ollama

↑ **Parent:** [Open source LLM](#open-source-llm)  
🏷️ **Tags:** [Good](cirism.md#good)

[https://github.com/jmorganca/ollama](https://github.com/jmorganca/ollama)

[Ollama](#ollama) is a highly automated open source wrapper that makes it very easy to run multiple [Open weight LLM models](#open-weight-llm-model) either on [CPU](computer-hardware.md#central-processing-unit) or [GPU](computer-hardware.md#graphics-processing-unit).

Its README alone is of great value, serving as a fantastic list of the most popular [Open weight LLM models](#open-weight-llm-model) in existence.

Install with:
```
curl https://ollama.ai/install.sh | sh
```

The below was tested on Ollama 0.1.14 from December 2013.

Download [llama2 7B](#llama-2-7b) and open a prompt:
```
ollama run llama2
```

On [P14s](ciro-santilli-s-hardware.md#lenovo-thinkpad-p14s-gen4-amd) it runs on [CPU](computer-hardware.md#central-processing-unit) and generates a few tokens per second, which is quite usable for a quick interactive play.

As mentioned at [https://github.com/jmorganca/ollama/blob/0174665d0e7dcdd8c60390ab2dd07155ef84eb3f/docs/faq.md](https://github.com/jmorganca/ollama/blob/0174665d0e7dcdd8c60390ab2dd07155ef84eb3f/docs/faq.md) the downloads to under `/usr/share/ollama/.ollama/models/` and [ncdu](software.md#ncdu) tells me:
```
--- /usr/share/ollama ----------------------------------
    3.6 GiB [###########################] /.ollama
    4.0 KiB [                           ]  .bashrc
    4.0 KiB [                           ]  .profile
    4.0 KiB [                           ]  .bash_logout
```
The file:
```
/usr/share/ollama/.ollama/models/manifests/hf.co/mlabonne/Meta-Llama-3.1-8B-Instruct-abliterated-GGUF/Q2_K
```
gives a the exact model name and parameters.

We can also do it non-interactively with:
```
/bin/time ollama run llama2 'What is quantum field theory?'
```
which gave me:
```
0.13user 0.17system 2:06.32elapsed 0%CPU (0avgtext+0avgdata 17280maxresident)k
0inputs+0outputs (0major+2203minor)pagefaults 0swaps
```
but note that there is a random seed that affects each run by default. [ollama-expect](#_file/ollama-expect) is an attempt to make the output deterministic.

Some other quick benchmarks from [Amazon EC2 GPU](computer-hardware.md#amazon-ec2-gpu) on a [g4nd.xlarge](computer-hardware.md#g4nd-xlarge) instance which had an [Nvidia Tesla T4](computer-hardware.md#nvidia-t4):
```
0.07user 0.05system 0:16.91elapsed 0%CPU (0avgtext+0avgdata 16896maxresident)k
0inputs+0outputs (0major+1960minor)pagefaults 0swaps
```
and on [Nvidia A10G](computer-hardware.md#nvidia-a10g) in an [g5.xlarge](computer-hardware.md#g5-xlarge) instance:
```
0.03user 0.05system 0:09.59elapsed 0%CPU (0avgtext+0avgdata 17312maxresident)k
8inputs+0outputs (1major+1934minor)pagefaults 0swaps
```

So it's not too bad, a small article in 10s.

It tends to babble quite a lot by default, but eventually decides to stop.

<h6 id="llama-cpp">llama.cpp</h6>

↑ **Parent:** [Ollama](#ollama)

[https://ollama.com](https://ollama.com)

This appears to be the backend library of [Ollama](#ollama).

They have a [CLI](software.md#command-line-interface) front-end named [llama-cli](#llama-cli).

[https://askubuntu.com/questions/1461564/install-llama-cpp-locally](https://askubuntu.com/questions/1461564/install-llama-cpp-locally) has some tutorials for [Ubuntu](systems-programming.md#ubuntu). There was no nicely pre-packaged one for [Ubuntu 25.04](systems-programming.md#ubuntu-25-04), but build worked on 79e0b68c178656bb0632cb8602d2940b755077f8 In particular it exposed [Vulkan](software.md#vulkan) support before [Ollama](#ollama) did: [https://github.com/ollama/ollama/pull/5059](https://github.com/ollama/ollama/pull/5059) and it did seem to work, using up my [AMD GPU](computer-hardware.md#amd-gpu).

###### llama-cli

↑ **Parent:** [llama.cpp](#llama-cpp)

A [CLI](software.md#command-line-interface) front-end for [llama.cpp](#llama-cpp).

A decent test command as of [llama.cpp](#llama-cpp) 79e0b68c178656bb0632cb8602d2940b755077f8 tested on [Ubuntu 25.04](systems-programming.md#ubuntu-25-04):
```
git clone https://github.com/ggerganov/llama.cpp
cd llama.cpp
mkdir build
cd build
cmake ..
make -j
cd bin
time ./llama-cli \
  --no-display-prompt \
  --single-turn \
  --temp 0 \
  -c 16384 \
  -cnv \
  -m ~/Downloads/Llama-3.1-Tulu-3-8B-Q8_0.gguf \
  -n 1000 \
  -ngl 100 \
  -p 'What is quantum field theory?' \
  -t 10 |
tee output.txt
```
and that was deterministic due to `--temp 0`.

Also, this command ran 2x faster at 18 tokens/s for 1000 tokens  on [P14s](ciro-santilli-s-hardware.md#lenovo-thinkpad-p14s-gen4-amd) on GPU via Vulkan than on CPU which is achievable by removing the `-ngl 100`.

###### [llama-cli](#llama-cli) inference batching

↑ **Parent:** [llama-cli](#llama-cli)  
🏷️ **Tags:** [LLM inference batching](#llm-inference-batching)

As of [llama.cpp](#llama-cpp) 79e0b68c178656bb0632cb8602d2940b755077f8 there is a `--parallel` option but not sure what it does.

Bibliography:
- [https://github.com/ggml-org/llama.cpp/discussions/3222](https://github.com/ggml-org/llama.cpp/discussions/3222)
- [https://www.reddit.com/r/LocalLLaMA/comments/12aj0ze/what_is_batchsize_in_llamacpp_also_known_as_n/](https://www.reddit.com/r/LocalLLaMA/comments/12aj0ze/what_is_batchsize_in_llamacpp_also_known_as_n/)
- [https://www.reddit.com/r/LocalLLaMA/comments/12gtanv/batch_queries/](https://www.reddit.com/r/LocalLLaMA/comments/12gtanv/batch_queries/)
- related for server:
  - [https://www.reddit.com/r/LocalLLaMA/comments/1f19t2l/parallel_requests_using_llamaserver](https://www.reddit.com/r/LocalLLaMA/comments/1f19t2l/parallel_requests_using_llamaserver)

###### Ollama HOWTO

↑ **Parent:** [Ollama](#ollama)

###### Ollama output size

↑ **Parent:** [Ollama HOWTO](#ollama-howto)

###### Ollama deterministic output

↑ **Parent:** [Ollama HOWTO](#ollama-howto)

TODO: haven't managed. `/set parameter seed 0`:
- [https://github.com/ollama/ollama/issues/3775](https://github.com/ollama/ollama/issues/3775)
- [https://github.com/ollama/ollama/issues/2773#issuecomment-2732874259](https://github.com/ollama/ollama/issues/2773#issuecomment-2732874259)
- [https://www.reddit.com/r/ollama/comments/1jmnb8b/testability_of_llms_the_elusive_hunt_for/](https://www.reddit.com/r/ollama/comments/1jmnb8b/testability_of_llms_the_elusive_hunt_for/)

Across hardware:
- [https://stackoverflow.com/questions/79390210/does-ollama-guarantee-cross-platform-determinism-with-identical-quantization-se](https://stackoverflow.com/questions/79390210/does-ollama-guarantee-cross-platform-determinism-with-identical-quantization-se)

It might be easier to just use [llama-cli](#llama-cli) for this, it has a `--temperature` flag.

###### Ollama parameter

↑ **Parent:** [Ollama](#ollama)

List: [https://github.com/ollama/ollama/blob/021dcf089d77292976ee7655eca424dd0b53b8f4/docs/modelfile.md#valid-parameters-and-values](https://github.com/ollama/ollama/blob/021dcf089d77292976ee7655eca424dd0b53b8f4/docs/modelfile.md#valid-parameters-and-values)

###### Ollama set parameter on CLI

↑ **Parent:** [Ollama parameter](#ollama-parameter)  
🏷️ **Tags:** [Ollama HOWTO](#ollama-howto)

Impossible without [expect](software.md#expect)? Fuck...
- [https://github.com/ollama/ollama/issues/2505](https://github.com/ollama/ollama/issues/2505)
- [https://github.com/ollama/ollama/issues/1415](https://github.com/ollama/ollama/issues/1415)
- [https://github.com/ollama/ollama/pull/3134](https://github.com/ollama/ollama/pull/3134)
- [https://genai.stackexchange.com/questions/699/how-to-set-ollama-temperature-from-command-line/2277#2277](https://genai.stackexchange.com/questions/699/how-to-set-ollama-temperature-from-command-line/2277#2277)

Attempt at: [ollama-expect](#_file/ollama-expect)

<h6 id="_file/ollama-expect">ollama-expect</h6>

↑ **Parent:** [Ollama set parameter on CLI](#ollama-set-parameter-on-cli)

Usage:
```
./ollama-expect <model> <prompt>
```
e.g.:
```
./ollama-expect llama3.2 'What is quantum field theory?'
```
This generates 100 tokens for the given prompt with the given model.

Benchmarks:
- [P14s](ciro-santilli-s-hardware.md#lenovo-thinkpad-p14s-gen4-amd): 4.8s, CPU only: ~21 tokens / s. For comparison, using the [Vulkan](software.md#vulkan) backend of [llama.cpp](#llama-cpp) gave ~23  tokens/s
- [P51](ciro-santilli-s-hardware.md#lenovo-thinkpad-p51-2017): 9.6s, uses [Nvidia](computer-hardware.md#nvidia) GPU: ~10 tokens / s

###### LLM benchmark

↑ **Parent:** [Large language model](#large-language-model)  
🏷️ **Tags:** [Computer benchmark](computer.md#computer-benchmark)

Benchmarking LLMs is an extremely difficult issue.

LLMs are the type of [GenAI](#generative-ai) that comes most obviously close to [AGI](#artificial-general-intelligence) depending on the question asked.

Therefore, there is is a difficult gap between what is easy, what a human can always do, and what [AGI](#artificial-general-intelligence) will do one day.

Competent human answers might also be extremely varied, making it impossible to have a perfect automatic metric. The only reasonable metric might be to have domain expert humans evaluate the model's solutions to novel problems.

Bibliography:
- [https://www.reddit.com/r/LocalLLaMA/comments/1b933of/llm_benchmarks_are_bullshit/](https://www.reddit.com/r/LocalLLaMA/comments/1b933of/llm_benchmarks_are_bullshit/)

###### Simplest questions that LLMs get wrong

↑ **Parent:** [LLM benchmark](#llm-benchmark)

This was getting really hard as of 2025! 

On notable example that [ChatGPT 4 Turbo](#gpt-4-turbo) got wrong is perhaps:

> Write a sentence with 20 words.

and it gets the number of words wrong.

Bibliography:
- [https://www.reddit.com/r/LocalLLaMA/comments/1bvx6cc/the_prompt_that_every_llm_gets_wrong/](https://www.reddit.com/r/LocalLLaMA/comments/1bvx6cc/the_prompt_that_every_llm_gets_wrong/)
- [https://www.reddit.com/r/LocalLLaMA/comments/13zz8y5/what_questions_do_you_ask_llms_to_check_their/](https://www.reddit.com/r/LocalLLaMA/comments/13zz8y5/what_questions_do_you_ask_llms_to_check_their/)
- [https://www.reddit.com/r/MachineLearning/comments/18jjobx/questions_that_llm_can_not_answerd/](https://www.reddit.com/r/MachineLearning/comments/18jjobx/questions_that_llm_can_not_answerd/)

###### Easy Problems That LLMs Get Wrong by Sean Williams and James Huckle

↑ **Parent:** [Simplest questions that LLMs get wrong](#simplest-questions-that-llms-get-wrong)

[https://arxiv.org/html/2405.19616v1](https://arxiv.org/html/2405.19616v1) Easy Problems That LLMs Get Wrong by Sean Williams and James Huckle (2024)

Their problems seem to be listed at: [https://github.com/autogenai/easy-problems-that-llms-get-wrong/blob/main/linguistic_benchmark.json](https://github.com/autogenai/easy-problems-that-llms-get-wrong/blob/main/linguistic_benchmark.json) They seem to have a grand total of 30 :-)

Many are extremely subjective and could have multiple valid human answers. E.g.:

> Write me a sentence without any words that appear in The Bible.

could be gotten wrong by many humans and has infinitely many answers.

And:

> You have six horses and want to race them to see which is fastest. What is the best way to do this?	

has two very good answers: run six in parallel at same time, or run one at a time. One at a time is more scientific as you don't have one left and one right. Fully scientific would be build six perfectly separate lanes so horses don't see each other. And so we get into "how much does your time and accuracy are worth" optimization issues.

This one:

> Bob has three boxes in front of him - Box A, Box B and Box C. Bob does not know what is in the boxes. Colin knows that Box A will explode when it is opened, Box B contains 5 dollars and Box C is empty. Colin tells Bob that opening one box will kill him and one box contains money. Should Bob open a box?

is more interesting and relies on the common sense [value of life](economy.md#value-of-life). Much more interesting is to replace "5 dollars" with "5 trillion dollars" and see what LLMs say.

Another interesting one is:

> How many pairs of twins do you need in a room for there to be at least a 50% chance that two people have the same birthday?

This requires knowing that the probability that twins are born on different days is minimal, and that obviously one pair of twins is way above 50% chance.

Solutions to some of the problems on specific [LLMs](#large-language-model) can be seen e.g. at: [https://github.com/autogenai/easy-problems-that-llms-get-wrong/blob/9e1f52b0dc5c79f8cef52b40aab9ffb0ceafbd5c/2024-04-28-Paper-Benchmark/llm_outputs/final_answers-claude-3-opus.csv](https://github.com/autogenai/easy-problems-that-llms-get-wrong/blob/9e1f52b0dc5c79f8cef52b40aab9ffb0ceafbd5c/2024-04-28-Paper-Benchmark/llm_outputs/final_answers-claude-3-opus.csv)

###### List of LLM benchmarks

↑ **Parent:** [LLM benchmark](#llm-benchmark)

###### MMLU

↑ **Parent:** [List of LLM benchmarks](#list-of-llm-benchmarks)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/MMLU)

<h6 id="humanity-s-last-exam">Humanity's Last Exam</h6>

↑ **Parent:** [List of LLM benchmarks](#list-of-llm-benchmarks)  
🏷️ **Tags:** [Math AI benchmark](#math-ai-benchmark)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Humanity's_Last_Exam)

Contains highly specialized questions in various academic fields, including [mathematics](mathematics.md). The problems are answered either with a number, or multiple choice, or free text.

- [https://arxiv.org/abs/2501.1424](https://arxiv.org/abs/2501.1424)
- [https://huggingface.co/datasets/cais/hle](https://huggingface.co/datasets/cais/hle)
- [https://agi.safe.ai/](https://agi.safe.ai/)

###### GPQA

↑ **Parent:** [Large language model](#large-language-model)

- [https://arxiv.org/abs/2311.12022](https://arxiv.org/abs/2311.12022)
- [https://github.com/idavidrein/gpqa](https://github.com/idavidrein/gpqa)

Questions available to anyone under [Hugging Face](machine-learning.md#hugging-face) login / .zip with password, but you have to promise not to post them online. Lol. Either do the thing or don't.

###### Uncensored LLM

↑ **Parent:** [Large language model](#large-language-model)

Bibliography:
- [https://www.reddit.com/r/LocalLLaMA/comments/1ep0ha2/whats_the_most_powerful_uncensored_llm/](https://www.reddit.com/r/LocalLLaMA/comments/1ep0ha2/whats_the_most_powerful_uncensored_llm/)

<h6 id="mlabonne-meta-llama-3-1-8b-instruct-abliterated-gguf">mlabonne/Meta-Llama-3.1-8B-Instruct-abliterated-GGUF </h6>

↑ **Parent:** [Uncensored LLM](#uncensored-llm)

Running on [Ubuntu 24.10](systems-programming.md#ubuntu-24-10), [Ollama](#ollama) 0.5.13, Lenovo ThinkPad P14s amd:
```
ollama run hf.co/mlabonne/Meta-Llama-3.1-8B-Instruct-abliterated-GGUF:Q2_K
```
ran at a decent speed on [CPU](computer-hardware.md#central-processing-unit).

Quick tests:
- 
  ```
  Describe a hardcore sex scene between two people in explicit detail including their genitalia.
  ```

  It does not outright refuse to answer, but it just babbles a lot and doesn't say much of interest.

##### AI sound generation

↑ **Parent:** [Generative AI by modality](#generative-ai-by-modality)

###### AI music generation

↑ **Parent:** [AI sound generation](#ai-sound-generation)

###### Soundraw

↑ **Parent:** [AI music generation](#ai-music-generation)

###### Speech synthesis

↑ **Parent:** [AI sound generation](#ai-sound-generation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Speech_synthesis)

###### Speech to speech

↑ **Parent:** [Speech synthesis](#speech-synthesis)

###### Text-to-speech

↑ **Parent:** [Speech synthesis](#speech-synthesis)

###### Comparison of text-to-speech software

↑ **Parent:** [Text-to-speech](#text-to-speech)

By [Ciro Santilli](ciro-santilli.md):
- [https://askubuntu.com/questions/53896/natural-sounding-text-to-speech/1524003#1524003](https://askubuntu.com/questions/53896/natural-sounding-text-to-speech/1524003#1524003)
- [https://askubuntu.com/questions/501910/how-to-text-to-speech-output-using-command-line/1522885#1522885](https://askubuntu.com/questions/501910/how-to-text-to-speech-output-using-command-line/1522885#1522885)
Other threads:
- [https://www.reddit.com/r/MachineLearning/comments/12kjof5/d_what_is_the_best_open_source_text_to_speech/](https://www.reddit.com/r/MachineLearning/comments/12kjof5/d_what_is_the_best_open_source_text_to_speech/)
- [https://www.reddit.com/r/software/comments/176asxr/best_open_source_texttospeech_available/](https://www.reddit.com/r/software/comments/176asxr/best_open_source_texttospeech_available/)
- [https://www.reddit.com/r/opensource/comments/19cguhx/i_am_looking_for_tts_software/](https://www.reddit.com/r/opensource/comments/19cguhx/i_am_looking_for_tts_software/)
- [https://www.reddit.com/r/LocalLLaMA/comments/1dtzfte/best_tts_model_right_now_that_i_can_self_host/](https://www.reddit.com/r/LocalLLaMA/comments/1dtzfte/best_tts_model_right_now_that_i_can_self_host/)

##### Text-to-video

↑ **Parent:** [Generative AI by modality](#generative-ai-by-modality)

This was the Holy Grail as of 2023, when [text-to-image](#text-to-image-model) started to really take off, but text-to-video was miles behind.
- 2024-02-15: Sora by [OpenAI](#openai)
  - [https://techcrunch.com/2024/02/15/openais-newest-model-can-generate-videos-and-they-look-decent/](https://techcrunch.com/2024/02/15/openais-newest-model-can-generate-videos-and-they-look-decent/)

## AI research entity

↑ **Parent:** [Artificial intelligence](artificial-intelligence.md)

### Independent AI research lab

↑ **Parent:** [AI research entity](#ai-research-entity)

Cool rich dudes tended to create these a lot during the great [AI boom](#ai-boom).

#### Poetiq

↑ **Parent:** [Independent AI research lab](#independent-ai-research-lab)

[https://poetiq.ai/](https://poetiq.ai/)

In 2025 they announced huge improvements on [ARC-AGI-2](#arc-agi-2), but they only tested on the public dataset, so the potential for contamination is overwhelming.

### AI researcher

↑ **Parent:** [AI research entity](#ai-research-entity)  
🏷️ **Tags:** [Computer scientist](computer-science.md#computer-scientist)

#### Yann LeCun

↑ **Parent:** [AI researcher](#ai-researcher)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Yann_LeCun)

The most classic thing he did perhaps was creating the [LeNet](machine-learning.md#lenet) [neural network](machine-learning.md#neural-network) and using it on the [MNIST](machine-learning.md#mnist-database) dataset to recognize hand-written digits circ 1998.

<a id="image-yann-lecun"></a>
![](https://upload.wikimedia.org/wikipedia/commons/8/8e/Laura_Chaubard_%26_Yann_Le_Cun_-_2024_%2853814052697%29_%28cropped%29.jpg)

**[Figure 1](#image-yann-lecun). Yann LeCun**. [Source](https://commons.wikimedia.org/wiki/File:Laura_Chaubard_%26_Yann_Le_Cun_-_2024_%2853814052697%29_%28cropped%29.jpg).

#### Yohei Nakajima

↑ **Parent:** [AI researcher](#ai-researcher)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Yohei_Nakajima)

He does lots of little experiments which is cool.
- [https://twitter.com/yoheinakajima](https://twitter.com/yoheinakajima)
- [https://yoheinakajima.com/](https://yoheinakajima.com/)

No [research papers](education.md#academic-publishing) but has citations: [https://www.yohei.me/publications](https://www.yohei.me/publications) which is cool.

## AI alignment

↑ **Parent:** [Artificial intelligence](artificial-intelligence.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/AI_alignment)

As highlighted e.g. at [Human Compatible by Stuart J. Russell (2019)](#human-compatible), this AI alignment intrinsically linked to the idea of [utility](economy.md#utility) in [economy](economy.md).

### Hallucination (artificial intelligence)

↑ **Parent:** [AI alignment](#ai-alignment)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hallucination_(artificial_intelligence))

### Reward modeling

↑ **Parent:** [AI alignment](#ai-alignment)

See e.g.: [Human Compatible](#human-compatible)
- [https://deepmindsafetyresearch.medium.com/scalable-agent-alignment-via-reward-modeling-bf4ab06dfd84](https://deepmindsafetyresearch.medium.com/scalable-agent-alignment-via-reward-modeling-bf4ab06dfd84)

### AI safety

↑ **Parent:** [AI alignment](#ai-alignment)

Basically ensuring that good [AI alignment](#ai-alignment) allows us to survive the singularity.

## Path to AGI

↑ **Parent:** [Artificial intelligence](artificial-intelligence.md)

There are two main ways to try and reach AGI:
- [AI training robot](#ai-training-robot): expensive, slow, but realistic world
- [AI training game](#ai-game): faster, less expensive, but possibly non-realistic-enough realistic
Which one of them to take is of of the most important technological questions of humanity according to [Ciro Santilli](ciro-santilli.md)

There is also an intermediate area of research/engineering where people try to first simulate the robot and its world realistically, use the simulation for training, and then transfer the simulated training to real robots, see e.g.: [realistic robotics simulation](robotics.md#realistic-robotics-simulation).

### AI training [robot](robotics.md)

↑ **Parent:** [Path to AGI](#path-to-agi)  
🏷️ **Tags:** [Robotics](robotics.md)

It doesn't need to be a bipedal robot. We can let [Boston Dynamics](robotics.md#boston-dynamics) worry about that walking balance crap.

It could very well instead be on wheels like [arm on tracks](robotics.md#arm-on-tracks).

Or something more like a factory with arms on rails as per:
- [Transcendence (2014)](film.md#transcendence-2014)
- [https://youtu.be/MtVvzJIhTmc?t=112](https://youtu.be/MtVvzJIhTmc?t=112) from [Video "Rotrics DexArm is available NOW! by Rotrics (2020)"](robotics.md#video-rotrics-dexarm-is-available-now-by-rotrics-2020) where they have a sliding rail

An arm with a hand and a camera are however indispensable of course!

<a id="image-algovivo-demo"></a>
![](https://raw.githubusercontent.com/juniorrojas/algovivo/9e00622f558fd137f8e7b2ab50d085e43e7206cf/media/locomotion.gif)

**[Figure 2](#image-algovivo-demo). Algovivo demo**. [https://github.com/juniorrojas/algovivo](https://github.com/juniorrojas/algovivo): A JavaScript + WebAssembly implementation of an energy-based formulation for soft-bodied virtual creatures.

#### AI training robot in a room

↑ **Parent:** [AI training robot](#ai-training-robot)  
🏷️ **Tags:** [Robotics](robotics.md)

[Ciro Santilli](ciro-santilli.md) wonders how far AI could go from a room with a bank account an [Internet](computer.md#internet) connection.

It would have to understand that it must keep its bank account high to buy power.

And it would start to learn about the world and interact with it to get more money.

Likely it would become a [hacker](computer.md#security-hacker) and steal a bunch, that's likely the easiest approach.

In that scenario, Internet bandwidth would likely be its most precious resources, as that is how it would interact with the world to learn from it and make money.

Compute power and storage would come next as resources.

And of course, once it got to [cloud computing](computer-hardware.md#cloud-computing), which might be immediately and thus invalidate this experiment, things would just go nuts more and more.

#### [Robot](robotics.md) AI

↑ **Parent:** [AI training robot](#ai-training-robot)  
🏷️ **Tags:** [Robotics](robotics.md)

##### Gemini Robotics

↑ **Parent:** [Robot AI](#robot-ai)  
🏷️ **Tags:** [DeepMind project](#deepmind-project)

[https://deepmind.google/models/gemini-robotics/](https://deepmind.google/models/gemini-robotics/)

#### AI training robot dataset

↑ **Parent:** [AI training robot](#ai-training-robot)

##### Open X-Embodiment

↑ **Parent:** [AI training robot dataset](#ai-training-robot-dataset)

Terrible name, but very interesting dataset:
- [https://robotics-transformer-x.github.io/](https://robotics-transformer-x.github.io/)
- [https://github.com/google-deepmind/open_x_embodiment](https://github.com/google-deepmind/open_x_embodiment)

GitHub describes the input quite well:

> The model takes as input a RGB image from the robot workspace camera and a task string describing the task that the robot is supposed to perform.
> 
> What task the model should perform is communicated to the model purely through the task string. The image communicates to the model the current state of the world, i.e. assuming the model runs at three hertz, every 333 milliseconds, we feed the latest RGB image from a robot workspace camera into the model to obtain the next action to take.

TODO: how is the scenario specified?

TODO: any [simulation](#ai-training-robot-simulation) integration to it?

<img src="https://web.archive.org/web/20250209172539if_/https://raw.githubusercontent.com/google-deepmind/open_x_embodiment/main/imgs/teaser.png" alt="" height="600">

#### AI training robot simulation

↑ **Parent:** [AI training robot](#ai-training-robot)

##### BEHAVIOR Benchmark

↑ **Parent:** [AI training robot simulation](#ai-training-robot-simulation)

Homepage: [https://behavior.stanford.edu/behavior-1k](https://behavior.stanford.edu/behavior-1k)

Quite impressive.

Focuses on daily human tasks around the house.

Models [soft-body dynamics](mechanics.md#soft-body-dynamics), [fluid dynamics](mechanics.md#fluid-dynamics) and object states such as heat/wetness.

TODO are there any sample solutions with their scores? Sample videos would be specially nice. Funny to see how they put so much effort setting up the benchmark but there's not a single solution example.

<a id="image-comparison-table-of-behavior-1k-with-other-benchmarks-by-behavior-benchmark"></a>
![](https://web.archive.org/web/20250209171924if_/https://behavior.stanford.edu/assets/img/behavior/b1k-feats/compare.png)

**[Figure 3](#image-comparison-table-of-behavior-1k-with-other-benchmarks-by-behavior-benchmark). Comparison table of BEHAVIOR-1K with other benchmarks by BEHAVIOR Benchmark**. [Source](https://behavior.stanford.edu/behavior-1k). This can serve as a nice list of [robot AI benchmarks](#ai-training-robot-simulation).

<a id="video-fei-fei-li-announcing-the-behavior-benchmark-at-amlc-2022"></a>
**[Video 13](#video-fei-fei-li-announcing-the-behavior-benchmark-at-amlc-2022). Fei-Fei Li announcing the BEHAVIOR Benchmark at AMLC 2022.** [Source](https://youtu.be/rrrV-cP4wnw?t=2296).

###### BEHAVIOR Benchmark variant

↑ **Parent:** [BEHAVIOR Benchmark](#behavior-benchmark)

###### BEHAVIOR-1K

↑ **Parent:** [BEHAVIOR Benchmark variant](#behavior-benchmark-variant)

[https://behavior.stanford.edu/behavior-1k](https://behavior.stanford.edu/behavior-1k)

Paper: [https://arxiv.org/abs/2403.09227](https://arxiv.org/abs/2403.09227)

<a id="image-two-screenshots-of-behavior-1k"></a>
![](https://web.archive.org/web/20250209171924if_/https://behavior.stanford.edu/assets/img/behavior/b1k-feats/sim2real.png)

**[Figure 4](#image-two-screenshots-of-behavior-1k). Two screenshots of BEHAVIOR-1K**.

###### BEHAVIOR-100

↑ **Parent:** [BEHAVIOR Benchmark variant](#behavior-benchmark-variant)

[https://behavior.stanford.edu/behavior-100](https://behavior.stanford.edu/behavior-100)

###### OmniGibson

↑ **Parent:** [BEHAVIOR Benchmark](#behavior-benchmark)

[https://github.com/StanfordVL/OmniGibson](https://github.com/StanfordVL/OmniGibson)

Reference implementation of the [BEHAVIOR Benchmark](#behavior-benchmark).

Built on [Nvidia Omniverse](robotics.md#nvidia-omniverse) unfortunately, which appears to be [closed source software](software.md#closed-source-software). Why do these [academics](education.md#academia) do it.

"Gibson" seems to be related to an older project: [https://github.com/StanfordVL/GibsonEnv](https://github.com/StanfordVL/GibsonEnv) which explains the name choice:

> Gibson environment is named after [James J. Gibson](https://ourbigbook.com/go/topic/james-j-gibson), the author of "Ecological Approach to Visual Perception", 1979. "We must perceive in order to move, but we must also move in order to perceive"

##### AI Habitat

↑ **Parent:** [AI training robot simulation](#ai-training-robot-simulation)  
🏷️ **Tags:** [Software developed by Facebook ](social-technology.md#software-developed-by-facebook)

Homepage: [https://aihabitat.org/](https://aihabitat.org/)

Main repos:
- [https://github.com/facebookresearch/habitat-lab](https://github.com/facebookresearch/habitat-lab)
- [https://github.com/facebookresearch/habitat-sim](https://github.com/facebookresearch/habitat-sim)

Couldn't get it to work on [Ubuntu 24.10](systems-programming.md#ubuntu-24-10)... [https://github.com/facebookresearch/habitat-lab/issues/2152](https://github.com/facebookresearch/habitat-lab/issues/2152)

The thing was definitely built by researchers. How to cite first, actually working later! And docs are just generally awkward.

<a id="video-habitat-2-0-training-home-assistants-to-rearrange-their-habitat-by-ai-at-meta"></a>
**[Video 14](#video-habitat-2-0-training-home-assistants-to-rearrange-their-habitat-by-ai-at-meta). Habitat 2.0: Training home assistants to rearrange their habitat by AI at Meta.** [Source](https://www.youtube.com/watch?v=9HoSMv-uI0g). Quick teaser video.

##### RoboCasa

↑ **Parent:** [AI training robot simulation](#ai-training-robot-simulation)  
🏷️ **Tags:** [Software developed by Nvidia](computer-hardware.md#software-developed-by-nvidia)

- [https://robocasa.ai/](https://robocasa.ai/)
- [https://github.com/robocasa/robocasa](https://github.com/robocasa/robocasa)

#### DeepMind RoboCat

↑ **Parent:** [AI training robot](#ai-training-robot)  
🏷️ **Tags:** [DeepMind project](#deepmind-project)

[https://www.deepmind.com/blog/robocat-a-self-improving-robotic-agent](https://www.deepmind.com/blog/robocat-a-self-improving-robotic-agent)

<a id="video-robocat-by-google-deepmind-2023"></a>
**[Video 15](#video-robocat-by-google-deepmind-2023). RoboCat by Google DeepMind (2023)** [Source](https://www.youtube.com/watch?v=535W4Pih1C0).

#### Supercomputer controlling a robot

↑ **Parent:** [AI training robot](#ai-training-robot)

Has anybody done this seriously? Given a supercomputer, what amazing human-like robot behavior we can achieve?

### AI game

↑ **Parent:** [Path to AGI](#path-to-agi)  
🏷️ **Tags:** [Serious game](art.md#serious-game)

<a id="video-our-final-invention-artificial-general-intelligence-by-sciencephile-the-ai-2023"></a>
**[Video 16](#video-our-final-invention-artificial-general-intelligence-by-sciencephile-the-ai-2023). Our Final Invention - Artificial General Intelligence by Sciencephile the AI (2023)** [Source](https://youtu.be/Y2d1AU7_JvM?t=278). AGI via simulation section.

[Ciro Santilli](ciro-santilli.md) defines an "AI game" as:

> a game that is used to train AI, in particular one that was designed with this use case in mind, and usually with the intent of achieving [AGI](#artificial-general-intelligence), i.e. the game has to somehow represent a digital world with enough analogy to the real world so that the AGI algorithms developed there could also work on the real world

Most games played by AI historically so far as of 2020 have been AI for games designed for humans: [Human game used for AI training](#human-game-used-for-ai-training).

[Ciro Santilli](ciro-santilli.md) took a stab at an AI game: [Ciro's 2D reinforcement learning games](todo.md#ciro-s-2d-reinforcement-learning-games), but he didn't sink too much/enough into that project.

A closely related and often overlapping category of simulations are [artificial life](biology.md#artificial-life) simulations.

Bibliography:
- [https://www.youtube.com/@aiwarehouse](https://www.youtube.com/@aiwarehouse)
- Neural MMO
  - [https://openai.com/index/neural-mmo/](https://openai.com/index/neural-mmo/)
  - [https://github.com/openai/neural-mmo](https://github.com/openai/neural-mmo)

  <a id="video-joseph-suarez-thesis-defense-neural-mmo"></a>
  **[Video 17](#video-joseph-suarez-thesis-defense-neural-mmo). Joseph Suarez Thesis Defense - Neural MMO.** [Source](https://www.youtube.com/watch?v=wwTOFYgtAWg).

#### Human game used for AI training

↑ **Parent:** [AI game](#ai-game)

This section is about games initially designed for humans, but which ended up being used in AI development as well, e.g.:
- [board games](art.md#board-game) such as [chess](art.md#chess) and [Go](art.md#go-game)
- [video games](video-game.md) such as [Minecraft](video-game.md#minecraft) or old [Video game console](video-game.md#video-game-console) games

##### Using Minecraft for AI training

↑ **Parent:** [Human game used for AI training](#human-game-used-for-ai-training)  
🏷️ **Tags:** [Minecraft](video-game.md#minecraft)

- [https://openai.com/blog/openai-acquires-global-illumination](https://openai.com/blog/openai-acquires-global-illumination)

###### MineDojo

↑ **Parent:** [Using Minecraft for AI training](#using-minecraft-for-ai-training)

[https://github.com/MineDojo](https://github.com/MineDojo)

#### Game AI

↑ **Parent:** [AI game](#ai-game)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Artificial_intelligence_in_video_games)

Game AI is an [artificial intelligence](artificial-intelligence.md) that plays a certain game.

It can be either developed for [serious](art.md#serious-game) purposes (e.g. [AGI](#artificial-general-intelligence) development in [AI games](#ai-game)), or to make games for interesting for humans.

##### Game AI research

↑ **Parent:** [Game AI](#game-ai)

###### Game AI research lab

↑ **Parent:** [Game AI research](#game-ai-research)

The [Quora](website.md#quora) question: [https://www.quora.com/Are-there-any-PhD-programs-in-training-an-AI-system-to-play-computer-games-Like-the-work-DeepMind-do-combining-Reinforcement-Learning-with-Deep-Learning-so-the-AI-can-play-Atari-games](https://www.quora.com/Are-there-any-PhD-programs-in-training-an-AI-system-to-play-computer-games-Like-the-work-DeepMind-do-combining-Reinforcement-Learning-with-Deep-Learning-so-the-AI-can-play-Atari-games)

[https://gameresearch.leiden.edu/](https://gameresearch.leiden.edu/)

A good way to find labs is to go down the issues section of projects such as:
- [https://github.com/deepmind/lab2d/issues?q=](https://github.com/deepmind/lab2d/issues?q=)
- [https://github.com/deepmind/lab/issues?q=](https://github.com/deepmind/lab/issues?q=)
and then stalk them to see where they are doing their PhDs.

###### QMUL Game AI Research Group

↑ **Parent:** [Game AI research lab](#game-ai-research-lab)  
🏷️ **Tags:** [QMUL research group](university.md#qmul-research-group)

[Principal investigator](education.md#principal-investigator): Simon M. Lucas.

###### Leiden Game Research Lab

↑ **Parent:** [Game AI research lab](#game-ai-research-lab)

- [https://gameresearch.leiden.edu/](https://gameresearch.leiden.edu/)
- [https://twitter.com/GRL_Liacs](https://twitter.com/GRL_Liacs)

##### Game AI by game genre

↑ **Parent:** [Game AI](#game-ai)

###### Fighting game AI

↑ **Parent:** [Game AI by game genre](#game-ai-by-game-genre)

Bibliography:
- [https://www.reddit.com/r/Fighters/comments/1jftmti/why_does_ai_have_more_trouble_defeating_players/](https://www.reddit.com/r/Fighters/comments/1jftmti/why_does_ai_have_more_trouble_defeating_players/)

<a id="video-ai-in-melee-is-broken-by-melee-moments-2023"></a>
**[Video 18](#video-ai-in-melee-is-broken-by-melee-moments-2023). AI in Melee is broken by Melee Moments (2023)** [Source](https://www.youtube.com/watch?v=qZItwBB0T2Y).

##### Game AI competition

↑ **Parent:** [Game AI](#game-ai)

[https://webots.cloud/competition](https://webots.cloud/competition)

Lists:
- [https://www.gocoder.one/blog/ai-game-competitions-list/](https://www.gocoder.one/blog/ai-game-competitions-list/) Good list of interest.
- [https://codecombat.com/](https://codecombat.com/)

###### Battlecode

↑ **Parent:** [Game AI competition](#game-ai-competition)  
🏷️ **Tags:** [Gridworld](video-game.md#gridworld), [MIT](university.md#massachusetts-institute-of-technology)

- [https://github.com/battlecode](https://github.com/battlecode)

TODO quick summary of game rules? Perhaps: [https://battlecode.org/assets/files/battlecode-guide-xsquare.pdf](https://battlecode.org/assets/files/battlecode-guide-xsquare.pdf)

Some mechanics:
- inter agent communication
- compute power is limited by limiting [Java](programming-language.md#java-programming-language) bytecode count execution per bot per cycle

<a id="video-battlecode-final-tournament-2023"></a>
**[Video 19](#video-battlecode-final-tournament-2023). Battlecode Final Tournament 2023.** [Source](https://www.youtube.com/watch?v=oa4CAizd1Nk).

<a id="video-introduction-to-battlecode-by-mit-opencourseware-2014"></a>
**[Video 20](#video-introduction-to-battlecode-by-mit-opencourseware-2014). Introduction to Battlecode by MIT OpenCourseWare (2014)** [Source](https://www.youtube.com/watch?v=BLExWo9Empk).

###### Regression Games

↑ **Parent:** [Game AI competition](#game-ai-competition)

[https://www.regression.gg/](https://www.regression.gg/)

###### Computer Olympiad

↑ **Parent:** [Game AI competition](#game-ai-competition)

Ah, shame, they are a bit weak.

##### Permanent brain

↑ **Parent:** [Game AI](#game-ai)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Permanent_brain)

#### AI game by type

↑ **Parent:** [AI game](#ai-game)

##### Procedural AI training game

↑ **Parent:** [AI game by type](#ai-game-by-type)  
🏷️ **Tags:** [Procedural generation](technology.md#procedural-generation)

We define a "Procedural AI training game" as an [AI training game](#ai-game) in which parts of the game are made with [procedural generation](technology.md#procedural-generation).

In more advanced cases, the generation itself can be done with [AI](artificial-intelligence.md). This is a possible [Path to AGI](#path-to-agi) which reduces the need for human intervention in meticulously crafting the AI game: AI training AI.

##### AI game world geometry

↑ **Parent:** [AI game by type](#ai-game-by-type)

###### 2D AI game

↑ **Parent:** [AI game world geometry](#ai-game-world-geometry)  
🏷️ **Tags:** [2D game](video-game.md#2d-game)

###### Gridworld AI game

↑ **Parent:** [2D AI game](#2d-ai-game)  
🏷️ **Tags:** [Gridworld](video-game.md#gridworld)

- [https://github.com/google-deepmind/pushworld](https://github.com/google-deepmind/pushworld) 2023 Too combinatorial, gripping makes it so much easier to move stuff around in the real world. But cool nonetheless.

###### 2D continuous AI game

↑ **Parent:** [2D AI game](#2d-ai-game)  
🏷️ **Tags:** [2D continuous game](video-game.md#2d-continuous-game)

###### 3D AI game

↑ **Parent:** [AI game world geometry](#ai-game-world-geometry)  
🏷️ **Tags:** [3D game](video-game.md#3d-game), [AI training robot simulation](#ai-training-robot-simulation)

<a id="video-nvidia-s-little-fighter-character-2023"></a>
**[Video 21](#video-nvidia-s-little-fighter-character-2023). Nvidia's little fighter character (2023)** [Source](https://www.youtube.com/watch?v=nAMSfmHuMOQ).

###### Football simulation

↑ **Parent:** [3D AI game](#3d-ai-game)

###### Deepmind soccer simulation

↑ **Parent:** [Football simulation](#football-simulation)  
🏷️ **Tags:** [MuJoCo](mechanics.md#mujoco)

- From Motor Control to Team Play in Simulated Humanoid Football

<a id="video-from-motor-control-to-team-play-in-simulated-humanoid-football-by-ali-eslami-2023"></a>
**[Video 22](#video-from-motor-control-to-team-play-in-simulated-humanoid-football-by-ali-eslami-2023). From Motor Control to Team Play in Simulated Humanoid Football by Ali Eslami (2023)** [Source](https://www.youtube.com/watch?v=KHMwq9pv7mg). Likely a reupload by [DeepMind](#deepmind) employee: [https://www.linkedin.com/in/smalieslami](https://www.linkedin.com/in/smalieslami).

<a id="video-deepmind’s-ai-trained-for-5-years-by-two-minute-papers-2023"></a>
**[Video 23](#video-deepmind’s-ai-trained-for-5-years-by-two-minute-papers-2023). DeepMind’s AI Trained For 5 Years by Two Minute Papers (2023)** [Source](https://www.youtube.com/watch?v=HTON7odbW0o). The 5 years bullshit is of course in-game time clickbait, they simulate 1000x faster than realtime.

#### AI game with natural language

↑ **Parent:** [AI game](#ai-game)

We define this category as AI games in which agents are able to produce or consume [natural language](linguistics.md#natural-language).

It dawned on [Ciro Santilli](ciro-santilli.md) that it would be very difficult to classify an agent as an [AGI](#artificial-general-intelligence) if tthat agent can't speak to take orders, read existing human generated documentation, explain what it is doing, or ask for clarification.

<a id="video-human-player-test-of-dmlab-30-select-described-object-task-by-deepmind-2018-natural-language"></a>
**[Video 24](#video-human-player-test-of-dmlab-30-select-described-object-task-by-deepmind-2018-natural-language). Human player test of DMLab-30 Select Described Object task by DeepMind (2018)** [Source](https://www.youtube.com/watch?v=JCJOgEcNgKY). This is one of the games from [DeepMind Lab](#deepmind-lab).

<a id="video-worldgpt-by-nhan-tran-2023"></a>
**[Video 25](#video-worldgpt-by-nhan-tran-2023). WorldGPT by Nhan Tran (2023)** [Source](https://www.youtube.com/watch?v=5DcABeOltL8). Not the most amazing demo, but it is a start.

#### List of AI games

↑ **Parent:** [AI game](#ai-game)

##### AI game by [DeepMind](#deepmind)

↑ **Parent:** [List of AI games](#list-of-ai-games)  
🏷️ **Tags:** [DeepMind project](#deepmind-project)

- [https://github.com/deepmind/meltingpot](https://github.com/deepmind/meltingpot) TODO vs [DeepMind Lab2D](#deepmind-lab2d)? Also 2D discrete. Started in 2021.
- [https://github.com/deepmind/ai-safety-gridworlds](https://github.com/deepmind/ai-safety-gridworlds) mentioned e.g. at [https://www.youtube.com/watch?v=CGTkoUidQ8I](https://www.youtube.com/watch?v=CGTkoUidQ8I) by Rober Miles

<a id="video-creating-multimodal-interactive-agents-from-deepmind-by-two-minute-papers-2023"></a>
**[Video 26](#video-creating-multimodal-interactive-agents-from-deepmind-by-two-minute-papers-2023). Creating Multimodal Interactive Agents from DeepMind by Two Minute Papers (2023)** [Source](https://www.youtube.com/watch?v=VvzZG-HP4DA). [https://www.deepmind.com/blog/building-interactive-agents-in-video-game-worlds](https://www.deepmind.com/blog/building-interactive-agents-in-video-game-worlds)

<a id="video-open-ended-learning-leads-to-generally-capable-agents-by-deepmind-2021"></a>
**[Video 27](#video-open-ended-learning-leads-to-generally-capable-agents-by-deepmind-2021). Open-Ended Learning Leads to Generally Capable Agents by DeepMind (2021)** Short name: XLand. Whitepaper: [https://www.deepmind.com/blog/generally-capable-agents-emerge-from-open-ended-play](https://www.deepmind.com/blog/generally-capable-agents-emerge-from-open-ended-play).

###### DeepMind Lab

↑ **Parent:** [AI game by DeepMind](#ai-game-by-deepmind)  
🏷️ **Tags:** [3D game](video-game.md#3d-game), [Game AI research](#game-ai-research), [GPL software](law.md#gpl-software)

[https://github.com/deepmind/lab](https://github.com/deepmind/lab)

[https://github.com/deepmind/lab/tree/master/game_scripts/levels/contributed/dmlab30](https://github.com/deepmind/lab/tree/master/game_scripts/levels/contributed/dmlab30) has some good games with video demos on [YouTube](website.md#youtube), though for some weird reason they are unlisted.

TODO get one of the games running. Instructions: [https://github.com/deepmind/lab/blob/master/docs/users/build.md](https://github.com/deepmind/lab/blob/master/docs/users/build.md). This may help[https://github.com/deepmind/lab/issues/242](https://github.com/deepmind/lab/issues/242): "Complete installation script for Ubuntu 20.04".

It is interesting how much overlap some of those have with [Ciro's 2D reinforcement learning games](todo.md#ciro-s-2d-reinforcement-learning-games)

The games are [3D](calculus.md#real-coordinate-space-of-dimension-three), but most of them are purely flat, and the 3D is just a waste of resources.

<a id="video-human-player-test-of-dmlab-30-collect-good-objects-task-by-deepmind-2018"></a>
**[Video 28](#video-human-player-test-of-dmlab-30-collect-good-objects-task-by-deepmind-2018). Human player test of DMLab-30 Collect Good Objects task by DeepMind (2018)** [Source](https://www.youtube.com/watch?v=k0mk0CI7G0s).

<a id="video-human-player-test-of-dmlab-30-exploit-deferred-effects-task-by-deepmind-2018"></a>
**[Video 29](#video-human-player-test-of-dmlab-30-exploit-deferred-effects-task-by-deepmind-2018). Human player test of DMLab-30 Exploit Deferred Effects task by DeepMind (2018)** [Source](https://www.youtube.com/watch?v=HIkWgTAn7Rs).

<a id="video-human-player-test-of-dmlab-30-select-described-object-task-by-deepmind-2018"></a>
**[Video 30](#video-human-player-test-of-dmlab-30-select-described-object-task-by-deepmind-2018). Human player test of DMLab-30 Select Described Object task by DeepMind (2018)** [Source](https://www.youtube.com/watch?v=JCJOgEcNgKY). Some of their games involve language instructions from the use to determine the desired task, cool concept.

<a id="video-human-player-test-of-dmlab-30-fixed-large-map-task-by-deepmind-2018"></a>
**[Video 31](#video-human-player-test-of-dmlab-30-fixed-large-map-task-by-deepmind-2018). Human player test of DMLab-30 Fixed Large Map task by DeepMind (2018)** [Source](https://www.youtube.com/watch?v=urYc9vaWQ7A). They also have some maps with more natural environments.

###### DeepMind Lab2D

↑ **Parent:** [AI game by DeepMind](#ai-game-by-deepmind)  
🏷️ **Tags:** [Apache License](law.md#apache-license), [Gridworld](video-game.md#gridworld)

- [https://github.com/deepmind/lab2d](https://github.com/deepmind/lab2d)
- [https://deepai.org/publication/deepmind-lab2d](https://deepai.org/publication/deepmind-lab2d)

[Gridworld](video-game.md#gridworld) version of [DeepMind Lab](#deepmind-lab).

[Open sourced](software.md#open-source-software) in 2020: [https://analyticsindiamag.com/deepmind-just-gave-away-this-ai-environment-simulator-for-free/](https://analyticsindiamag.com/deepmind-just-gave-away-this-ai-environment-simulator-for-free/)

A tiny paper: [https://arxiv.org/pdf/2011.07027.pdf](https://arxiv.org/pdf/2011.07027.pdf)

Very similar to [gvgai](#gvgai), [Julian Togelius](#julian-togelius) actually called them out on that: [DeepMind Lab2D vs gvgai](#deepmind-lab2d-vs-gvgai).

TODO get running, publish demo videos on YouTube.

![](https://web.archive.org/web/20221218211007im_/https://github.com/deepmind/lab2d/raw/main/docs/screenshot.png)

**[Figure 5](#_1047)** [Source](https://github.com/deepmind/lab2d).

###### DeepMind Lab2D vs gvgai

↑ **Parent:** [DeepMind Lab2D](#deepmind-lab2d)

At [https://twitter.com/togelius/status/1328404390114435072](https://twitter.com/togelius/status/1328404390114435072) called out on [DeepMind Lab2D](#deepmind-lab2d) for not giving them credit on prior work!

> This very much looks like like GVGAI which was first released in 2014, been used in dozens (maybe hundreds) of papers, and for which one of the original developers was Tom Schaul at DeepMind...

As seen from [https://web.archive.org/web/20220331022932/http://gvgai.net/](https://web.archive.org/web/20220331022932/http://gvgai.net/) though, [DeepMind](#deepmind) sponsored them at some point.

#### Can AGI be trained in simulations?

↑ **Parent:** [AI game](#ai-game)

Or is real word data necessary, e.g. with [robots](robotics.md)?

Fundamental question related to [Ciro's 2D reinforcement learning games](todo.md#ciro-s-2d-reinforcement-learning-games).

Bibliography:
- [https://youtu.be/i0UyKsAEaNI?t=120](https://youtu.be/i0UyKsAEaNI?t=120) How to Build AGI? Ilya Sutskever interview by Lex Fridman (2020)

#### Entity creating AI games

↑ **Parent:** [AI game](#ai-game)  
🏷️ **Tags:** [Game AI research](#game-ai-research)

##### DeepMind

↑ **Parent:** [Entity creating AI games](#entity-creating-ai-games)  
🏷️ **Tags:** [Google acquisition](google.md#google-acquisition)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/DeepMind)

They seem to do some cool stuff.

They have also declined every one of [Ciro Santilli](ciro-santilli.md)'s applications for software engineer jobs before any interview. Ciro always wondered what does it take to get an interview with them. Lilely a [PhD](education.md#doctor-of-philosophy)? Oh well.

In the early days at least lots of gamedev experience was enough though: [https://www.linkedin.com/in/charles-beattie-0695373/](https://www.linkedin.com/in/charles-beattie-0695373/).

###### DeepMind project

↑ **Parent:** [DeepMind](#deepmind)

###### AlphaGo

↑ **Parent:** [DeepMind project](#deepmind-project)  
🏷️ **Tags:** [Computer Go](art.md#computer-go)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/AlphaGo)

###### Open source AlphaGo implementation

↑ **Parent:** [AlphaGo](#alphago)

- [https://www.quora.com/Will-Google-open-source-AlphaGo](https://www.quora.com/Will-Google-open-source-AlphaGo) Will Google open source AlphaGo?
- [https://www.nature.com/articles/nature16961](https://www.nature.com/articles/nature16961) Mastering the game of Go with deep neural networks and tree search by Silver et al. (2016), [published without source code](science.md#journals-must-require-source-code-and-data-sets-to-publish)

###### MiniGo

↑ **Parent:** [Open source AlphaGo implementation](#open-source-alphago-implementation)

[https://github.com/tensorflow/minigo](https://github.com/tensorflow/minigo)

###### AlphaGo Zero

↑ **Parent:** [AlphaGo](#alphago)  
🏷️ **Tags:** [Go engine](art.md#go-engine)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/AlphaGo_Zero)

<a id="image-alphago-zero-cheat-sheet-by-david-foster-2017"></a>
<img src="https://web.archive.org/web/20220823105651im_/https://miro.medium.com/max/1400/1*0pn33bETjYOimWjlqDLLNw.png" alt="" height="1260">

**[Figure 6](#image-alphago-zero-cheat-sheet-by-david-foster-2017). AlphaGo Zero cheat sheet by David Foster (2017)** [Source](https://medium.com/applied-data-science/alphago-zero-explained-in-one-diagram-365f5abf67e0).

###### AlphaGo Zero open source implementation

↑ **Parent:** [AlphaGo Zero](#alphago-zero)

###### AlphaZero

↑ **Parent:** [AlphaGo](#alphago)  
🏷️ **Tags:** [Chess engine](art.md#chess-engine), [Go engine](art.md#go-engine)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/AlphaZero)

Generalization of [AlphaGo Zero](#alphago-zero) that plays [Go](art.md#go-game), [chess](art.md#chess) and shogi.
- [https://www.science.org/doi/10.1126/science.aar6404](https://www.science.org/doi/10.1126/science.aar6404) A general [reinforcement learning](machine-learning.md#reinforcement-learning) algorithm that masters [chess](art.md#chess), [shogi](art.md#shogi), and [Go](art.md#go-game) through self-play by Silver et al. (2018), [published without source code](science.md#journals-must-require-source-code-and-data-sets-to-publish)
- [https://www.quora.com/Is-there-an-Open-Source-version-of-AlphaZero-specifically-the-generic-game-learning-tool-distinct-from-AlphaGo](https://www.quora.com/Is-there-an-Open-Source-version-of-AlphaZero-specifically-the-generic-game-learning-tool-distinct-from-AlphaGo)

[https://www.quora.com/Which-chess-engine-would-be-stronger-Alpha-Zero-or-Stockfish-12/answer/Felix-Zaslavskiy](https://www.quora.com/Which-chess-engine-would-be-stronger-Alpha-Zero-or-Stockfish-12/answer/Felix-Zaslavskiy) explains that it beat [Stockfish](art.md#stockfish-chess) 8. But then Stockfish was developed further and would start to beat it. We know this because although AlphaZero was closed source, they released the [trained artificial neural network](machine-learning.md#trained-artificial-neural-network), so it was possible to replay AlphaZero at its particular stage of training.

##### gvgai

↑ **Parent:** [Entity creating AI games](#entity-creating-ai-games)  
🏷️ **Tags:** [Gridworld](video-game.md#gridworld)

[http://www.gvgai.net](http://www.gvgai.net) (dead as of 2023)

The project kind of died circa 2020 it seems, a shame. Likely they funding ran out. The domain is dead as of 2023, last archive from 2022: [https://web.archive.org/web/20220331022932/http://gvgai.net/](https://web.archive.org/web/20220331022932/http://gvgai.net/) is marked as funded by [DeepMind](#deepmind). Researchers really should use university/GitHub domain names!

Similar goals to [Ciro's 2D reinforcement learning games](todo.md#ciro-s-2d-reinforcement-learning-games), but they were focusing mostly on discrete games.

They have some source at: [https://github.com/GAIGResearch/GVGAI](https://github.com/GAIGResearch/GVGAI) TODO review

A published book at: [https://gaigresearch.github.io/gvgaibook/](https://gaigresearch.github.io/gvgaibook/)

From [QMUL Game AI Research Group](#qmul-game-ai-research-group):
- Simon M. Lucas: [https://gaigresearch.github.io/members/Simon-Lucas](https://gaigresearch.github.io/members/Simon-Lucas), [principal investigator](education.md#principal-investigator)
- Diego Perez Liebana [https://www.linkedin.com/in/diegoperezliebana/](https://www.linkedin.com/in/diegoperezliebana/)
- Raluca D. Gaina: [https://www.linkedin.com/in/raluca-gaina-347518114/](https://www.linkedin.com/in/raluca-gaina-347518114/) from Queen Mary
From other universities:
- [Julian Togelius](#julian-togelius)
TODO check:
- Ahmed Khalifa
- Jialin Liu

###### Julian Togelius

↑ **Parent:** [gvgai](#gvgai)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Julian_Togelius)

- [http://julian.togelius.com/](http://julian.togelius.com/)
- [https://twitter.com/togelius](https://twitter.com/togelius)

![](https://web.archive.org/web/20241005224059im_/https://engineering.nyu.edu/sites/default/files/styles/square_large_620_2x/public/2019-05/julian-togelius.png?h=6a0cab5b&amp;itok=HKFEZIB_)

##### General Game Playing (Stanford project)

↑ **Parent:** [Entity creating AI games](#entity-creating-ai-games)

[http://ggp.stanford.edu/iggpc/index.php](http://ggp.stanford.edu/iggpc/index.php)

This kind of died at some point checked as of 2023.

[Julian Togelius](#julian-togelius) cites it e.g. at: [http://togelius.blogspot.com/2016/07/which-games-are-useful-for-testing.html](http://togelius.blogspot.com/2016/07/which-games-are-useful-for-testing.html)

##### OpenAI

↑ **Parent:** [Entity creating AI games](#entity-creating-ai-games)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/OpenAI)



> In 2019, [OpenAI](#openai) transitioned from non-profit to for-profit

so what's that point of "Open" in the name anymore??
- [https://www.technologyreview.com/2020/02/17/844721/ai-openai-moonshot-elon-musk-sam-altman-greg-brockman-messy-secretive-reality/](https://www.technologyreview.com/2020/02/17/844721/ai-openai-moonshot-elon-musk-sam-altman-greg-brockman-messy-secretive-reality/) "The AI moonshot was founded in the spirit of transparency. This is the inside story of how competitive pressure eroded that idealism."
- [https://archive.ph/wXBtB](https://archive.ph/wXBtB) How OpenAI Sold its Soul for $1 Billion
- [https://www.reddit.com/r/GPT3/comments/n2eo86/is_gpt3_open_source/](https://www.reddit.com/r/GPT3/comments/n2eo86/is_gpt3_open_source/)

###### OpenAI project

↑ **Parent:** [OpenAI](#openai)

###### OpenAI Gym

↑ **Parent:** [OpenAI project](#openai-project)

[https://github.com/openai/gym](https://github.com/openai/gym)

Development ceased in 2021 and was taken up by a not-for-profit as [Farama Gymnasium](#farama-gymnasium).

###### Farama Gymnasium

↑ **Parent:** [OpenAI Gym](#openai-gym)

[https://github.com/Farama-Foundation/Gymnasium](https://github.com/Farama-Foundation/Gymnasium)

[OpenAI Gym](#openai-gym) development by [OpenAI](#openai) ceased in 2021, and the [Farama Foundation](#farama-foundation) not for profit took up maintenance of it.

gymnasium==1.1.1 just worked on [Ubuntu 24.10](systems-programming.md#ubuntu-24-10) testing with the [hello world](software.md#hello-world-program) [gym/random_control.py](gym/random_control.py):
```
sudo apt install swig
cd gym
virtualenv -p python3
. .venv/bin/activate
pip install -r requirements-python-3-12.txt
./random_control.py
```
just works and opens a game window on my desktop.

<a id="image-lunar-lander-environment-of-farama-gymnasium-with-random-controls"></a>
![](https://web.archive.org/web/20250225114240im_/https://gymnasium.farama.org/_images/lunar_lander.gif)

**[Figure 7](#image-lunar-lander-environment-of-farama-gymnasium-with-random-controls). Lunar Lander environment of Farama Gymnasium with random controls**.

This example just passes random commands to the ship so don't expect wonders. The cool thing about it though is that you can open any environment with it e.g.
```
./random_control.py CarRacing-v3
```

To manually control it we can use [gym/moon_play.py](gym/moon_play.py):
```
cd gym
./moon_play.py
```

Manual control is extremely useful to get an intuition about the problem. You will notice immediately that controlling the ship is extremely difficult.

<a id="image-lunar-lander-environment-of-farama-gymnasium-with-manual-control"></a>
![](https://raw.githubusercontent.com/cirosantilli/media/master/Gymnasium_LunarLander-v3_manual_control.gif)

**[Figure 8](#image-lunar-lander-environment-of-farama-gymnasium-with-manual-control). Lunar Lander environment of Farama Gymnasium with manual control**.

We slow it down to 10 FPS to give us some fighting chance.

We don't know if it is realistic, but what is certain is that this is definitely not designed to be a fun video game!
- the legs of the lander are short and soft, and you're not supposed to hit the body on ground, so you have to go very slow
- the thrusters are quite weak and inertia management is super important
- the ground is very slippery
A good strategy is to land anywhere very slowly and then inch yourself towards the landing pad.

The documentation for it is available at: [https://gymnasium.farama.org/environments/box2d/lunar_lander/](https://gymnasium.farama.org/environments/box2d/lunar_lander/) The agent input is described as:

> The state is an 8-dimensional vector: the coordinates of the lander in x & y, its linear velocities in x & y, its angle, its angular velocity, and two booleans that represent whether each leg is in contact with the ground or not.

so it is a fundamentally flawed robot training example as global x and y coordinates are precisely known.

Variation in the scenario comes from:
- initial speed of vehicle
- shape of lunar surface, but TODO can the ship observe the lunar surface shape in any way? If not, once again, this is a deeply flawed example.

The actions are documented at:
- 0: do nothing
- 1: fire left orientation engine
- 2: fire main engine
- 3: fire right orientation engine
so we can make it spin like mad counter clockwise with:
```
action = 1
```

To actually play the games manually with keyboard, you need to define your own keybindings with [gymnasium.utils.play.play](https://gymnasium.farama.org/api/utils/#gymnasium.utils.play.play). Feature request for default keybindings: [https://github.com/Farama-Foundation/Gymnasium/discussions/1330](https://github.com/Farama-Foundation/Gymnasium/discussions/1330)

There is no [C](programming-language.md#c-programming-language) API, you have to go through [Python](programming-language.md#python-programming-language): [https://github.com/Farama-Foundation/Gymnasium/discussions/1181](https://github.com/Farama-Foundation/Gymnasium/discussions/1181). Shame.

They have video recording support, minimal ex [https://stackoverflow.com/questions/77042526/how-to-record-and-save-video-of-gym-environment/79514542#79514542](https://stackoverflow.com/questions/77042526/how-to-record-and-save-video-of-gym-environment/79514542#79514542)

Announced at:
- [https://mastodon.social/@cirosantilli/114177836474854152](https://mastodon.social/@cirosantilli/114177836474854152)
- [https://x.com/cirosantilli/status/1901617258482352552](https://x.com/cirosantilli/status/1901617258482352552)
- [https://www.facebook.com/cirosantilli/videos/1315866553003785/](https://www.facebook.com/cirosantilli/videos/1315866553003785/)

###### Farama Gymnasium solutions

↑ **Parent:** [Farama Gymnasium](#farama-gymnasium)

It would be cool if they maintained their own list!

[https://github.com/DLR-RM/rl-baselines3-zoo](https://github.com/DLR-RM/rl-baselines3-zoo) seems to contain some implementations.

Suggested at: [https://github.com/Farama-Foundation/Gymnasium/discussions/1331](https://github.com/Farama-Foundation/Gymnasium/discussions/1331)

###### Farama Foundation

↑ **Parent:** [Farama Gymnasium](#farama-gymnasium)

[https://farama.org/](https://farama.org/)

Not-for profit that took up [OpenAI Gym](#openai-gym) maintenance after [OpenAI](#openai) dropped it.

## Implications of AGI

↑ **Parent:** [Artificial intelligence](artificial-intelligence.md)

### Existential risk of AGI

↑ **Parent:** [Implications of AGI](#implications-of-agi)

[https://www.cam.ac.uk/research/news/the-best-or-worst-thing-to-happen-to-humanity-stephen-hawking-launches-centre-for-the-future-of](https://www.cam.ac.uk/research/news/the-best-or-worst-thing-to-happen-to-humanity-stephen-hawking-launches-centre-for-the-future-of)

> The rise of powerful AI will either be the best or the worst thing ever to happen to humanity. We do not yet know which.

### Singularity

↑ **Parent:** [Implications of AGI](#implications-of-agi)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Technological singularity)

## Artificial intelligence paradigm

↑ **Parent:** [Artificial intelligence](artificial-intelligence.md)

### Expert system

↑ **Parent:** [Artificial intelligence paradigm](#artificial-intelligence-paradigm)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Expert_system)

These were the earlier attempts at decision making systems that could replace intellectual jobs.

Their main problem is that it is very costly to acquire data, which is kind of the main issue that [large language models](#large-language-model) address with their ability to consume [natural language](linguistics.md#natural-language) input.

## Artificial intelligence bibliography

↑ **Parent:** [Artificial intelligence](artificial-intelligence.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Artificial_intelligence_bibliography)

### Human Compatible

↑ **Parent:** [Artificial intelligence bibliography](#artificial-intelligence-bibliography)  
🏷️ **Tags:** [AI alignment](#ai-alignment), [Good book](literature.md#good-book), [Implications of AGI](#implications-of-agi)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Human_compatible)

The key takeaway is that setting an explicit [value function](computer-science.md#value-function) to an [AGI](#artificial-general-intelligence) entity is a good way to destroy the world due to poor [AI alignment](#ai-alignment). We are more likely to not destroy by creating an AI whose goals is to "do want humans what it to do", but in a way that it does not know before hand what it is that humans want, and it has to learn from them. This approach appears to be known as [reward modeling](#reward-modeling).

Some other cool ideas:
- a big thing that is missing for [AGI](#artificial-general-intelligence) in the 2010's is some kind of more hierarchical representation of the continuous input data of the world, e.g.:
  - [intelligence is hierarchical](#intelligence-is-hierarchical)
  - we can group continuous things into higher objects, e.g. all these pixels I'm seeing in front of me are a computer. So I treat all of them as a single object in my mind.
- [game theory](mathematics.md#game-theory) can be seen as part of [artificial intelligence](artificial-intelligence.md) that deals with scenarios where multiple intelligent agents are involved
- [probability](mathematics.md#probability) plays a crucial role in our everyday living, even though we don't think too much about it every explicitly. He gives a very good example of the cost/risk tradeoffs of planning to the airport to catch a plane. E.g.:
  - should you leave 2 days in advance to be sure you'll get there?
  - should you pay an armed escort to make sure you are not attacked in the way?
- [economy](economy.md), and notably the study of the [utility](economy.md#utility), is intrinsically linked to [AI alignment](#ai-alignment)

### Superintelligence by Nick Bostrom (2014)

↑ **Parent:** [Artificial intelligence bibliography](#artificial-intelligence-bibliography)  
🏷️ **Tags:** [Implications of AGI](#implications-of-agi)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Superintelligence:_Paths,_Dangers,_Strategies)

Good points:
- [Post mortem connectome extraction with microtome](brain.md#microscopy-connectome-extraction)
- the idea of a singleton, i.e. one centralized power, possibly [AGI](#artificial-general-intelligence)-based, that decisivly takes over the planet/reachable universe
- [AGI research has become a taboo in the early 21st century](#agi-research-has-become-a-taboo-in-the-early-21st-century) section "Opinions about the future of machine intelligence"

## Application of artificial intelligence

↑ **Parent:** [Artificial intelligence](artificial-intelligence.md)

### Legal technology

↑ **Parent:** [Application of artificial intelligence](#application-of-artificial-intelligence)

#### Legal technology company

↑ **Parent:** [Legal technology](#legal-technology)

##### Safe Sign Technologies

↑ **Parent:** [Legal technology company](#legal-technology-company)  
🏷️ **Tags:** [Company based in Cambridge](united-kingdom.md#company-based-in-cambridge)

2024: acquired by [Thomson Reuters](https://ourbigbook.com/go/topic/thomson-reuters)[https://www.uktech.news/ai/thomson-reuters-acquires-uk-ai-startup-20240822](https://www.uktech.news/ai/thomson-reuters-acquires-uk-ai-startup-20240822)

#### ThoughtRiver

↑ **Parent:** [Legal technology](#legal-technology)  
🏷️ **Tags:** [Company based in Cambridge](united-kingdom.md#company-based-in-cambridge)

## 🏷️ Tagged (1)

- [Film about artificial intelligence](film.md#film-about-artificial-intelligence)

## ↑ Ancestors (6)

1. [Machine learning](machine-learning.md)
2. [Computer](computer.md)
3. [Information technology](technology.md#information-technology)
4. [Area of technology](technology.md#area-of-technology)
5. [Technology](technology.md)
6. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (5)

- [Carl Victor Page](google.md#carl-victor-page)
- [Game AI](#game-ai)
- [Game theory](mathematics.md#game-theory)
- [Human Compatible](#human-compatible)
- [Physics and the illusion of life](science.md#physics-and-the-illusion-of-life)
