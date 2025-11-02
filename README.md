<div align="center">

<img src="static/image/logo_compressed.png" alt="Weibo Public Opinion Analysis System Logo" width="100%">

<a href="https://trendshift.io/repositories/15286" target="_blank"><img src="https://trendshift.io/api/badge/repositories/15286" alt="666ghj%2FBettaFish | Trendshift" style="width: 250px; height: 55px;" width="250" height="55"/></a>

<a href="https://leaflow.net/" target="_blank"><img src="static/image/Leaflow_logo.png" alt="666ghj%2FWeibo_PublicOpinion_AnalysisSystem | Leaflow" style="width: 150px;" width="150"/></a>

[![GitHub Stars](https://img.shields.io/github/stars/666ghj/Weibo_PublicOpinion_AnalysisSystem?style=flat-square)](https://github.com/666ghj/Weibo_PublicOpinion_AnalysisSystem/stargazers)
[![GitHub Watchers](https://img.shields.io/github/watchers/666ghj/Weibo_PublicOpinion_AnalysisSystem?style=flat-square)](https://github.com/666ghj/Weibo_PublicOpinion_AnalysisSystem/watchers)
[![GitHub Forks](https://img.shields.io/github/forks/666ghj/Weibo_PublicOpinion_AnalysisSystem?style=flat-square)](https://github.com/666ghj/Weibo_PublicOpinion_AnalysisSystem/network)
[![GitHub Issues](https://img.shields.io/github/issues/666ghj/Weibo_PublicOpinion_AnalysisSystem?style=flat-square)](https://github.com/666ghj/Weibo_PublicOpinion_AnalysisSystem/issues)
[![GitHub Pull Requests](https://img.shields.io/github/issues-pr/666ghj/Weibo_PublicOpinion_AnalysisSystem?style=flat-square)](https://github.com/666ghj/Weibo_PublicOpinion_AnalysisSystem/pulls)

[![GitHub License](https://img.shields.io/github/license/666ghj/Weibo_PublicOpinion_AnalysisSystem?style=flat-square)](https://github.com/666ghj/Weibo_PublicOpinion_AnalysisSystem/blob/main/LICENSE)
[![Version](https://img.shields.io/badge/version-v1.0.0-green.svg?style=flat-square)](https://github.com/666ghj/Weibo_PublicOpinion_AnalysisSystem)
[![Docker](https://img.shields.io/badge/Docker-Build-2496ED?style=flat-square&logo=docker&logoColor=white)](https://hub.docker.com/)


[English](./README-EN.md) | [中文文档](./README.md)

</div>

> [!IMPORTANT]
> **One-click online deployment experience** will be available on Monday (11.3), stay tuned!

## ⚡ Project Overview

"**WeiYu (MicroOpinion)**" is an innovative multi-agent public opinion analysis system built from scratch, helping users break through information echo chambers, restore the true picture of public opinion, predict future trends, and assist in decision-making. Users simply need to submit analysis requirements like a chat conversation, and the intelligent agents automatically analyze 30+ mainstream domestic and international social media platforms and millions of public comments.

> "WeiYu" (微舆) is a homophone of "WeiYu" (微鱼, meaning "small fish"). BettaFish is a small but very aggressive and beautiful fish, symbolizing "small but powerful, fearless of challenges"

View the system-generated research report using "Wuhan University public opinion" as an example: [Wuhan University Brand Reputation In-depth Analysis Report](./final_reports/final_report__20250827_131630.html)

Not only reflected in report quality, compared to similar products, we have 🚀 six major advantages:

1. **AI-Driven Full-Domain Monitoring**: AI crawler clusters operate 24/7 non-stop, comprehensively covering 10+ key domestic and international social media platforms including Weibo, Xiaohongshu, Douyin, Kuaishou, etc. Not only capturing trending content in real-time, but also drilling down to massive user comments, allowing you to hear the most authentic and widespread public voice.

2. **Composite Analysis Engine Beyond LLM**: We not only rely on 5 types of professionally designed Agents but also integrate fine-tuned models, statistical models, and other middleware. Through multi-model collaboration, we ensure depth, accuracy, and multi-dimensional perspectives in analysis results.

3. **Powerful Multimodal Capabilities**: Breaking through text and image limitations, capable of deep analysis of short video content from Douyin and Kuaishou, and precise extraction of structured multimodal information cards such as weather, calendar, and stock data from modern search engines, giving you comprehensive control of public opinion dynamics.

4. **Agent "Forum" Collaboration Mechanism**: Endowing different Agents with unique toolsets and thinking patterns, introducing a debate moderator model, and conducting chain-of-thought collision and debate through a "forum" mechanism. This not only avoids the thinking limitations of a single model and homogenization caused by communication but also generates higher-quality collective intelligence and decision support.

5. **Seamless Integration of Public and Private Domain Data**: The platform not only analyzes public opinion but also provides highly secure interfaces supporting seamless integration of your internal business database with public opinion data. Breaking down data silos to provide powerful analytical capabilities of "external trends + internal insights" for vertical businesses.

6. **Lightweight and Highly Extensible Framework**: Based on pure Python modular design, achieving lightweight, one-click deployment. Clear code structure allows developers to easily integrate custom models and business logic, enabling rapid expansion and deep customization of the platform.

**Starting with public opinion, but not limited to public opinion**. The goal of "WeiYu" is to become a simple and universal data analysis engine driving all business scenarios.

> For example, you only need to simply modify the API parameters and prompts in the Agent toolset to transform it into a financial market analysis system
>
> Here's a fairly active project discussion thread on Linux.do: https://linux.do/t/topic/1009280

<div align="center">
<img src="static/image/system_schematic.png" alt="banner" width="800">

Say goodbye to traditional data dashboards. In "WeiYu", everything starts with a simple question. You only need to submit your analysis requirements like a conversation.
</div>

## 🏗️ System Architecture

### Overall Architecture Diagram

**Insight Agent** Private Database Mining: AI agent for deep analysis of private public opinion databases

**Media Agent** Multimodal Content Analysis: AI agent with powerful multimodal capabilities

**Query Agent** Precise Information Search: AI agent with domestic and international web search capabilities

**Report Agent** Intelligent Report Generation: Multi-round report generation AI agent with built-in templates

<div align="center">
<img src="static/image/framework.png" alt="banner" width="800">
</div>

### Complete Analysis Workflow

| Step | Phase Name | Main Operations | Participating Components | Loop Characteristics |
|------|----------|----------|----------|----------|
| 1 | User Query | Flask main app receives query | Flask main app | - |
| 2 | Parallel Startup | Three Agents start simultaneously | Query Agent, Media Agent, Insight Agent | - |
| 3 | Preliminary Analysis | Each Agent uses dedicated tools for overview search | Each Agent + dedicated toolset | - |
| 4 | Strategy Formulation | Develop segmented research strategy based on preliminary results | Internal decision module of each Agent | - |
| 5-N | **Loop Phase** | **Forum Collaboration + Deep Research** | **ForumEngine + All Agents** | **Multiple Rounds** |
| 5.1 | Deep Research | Each Agent conducts specialized search guided by forum moderator | Each Agent + reflection mechanism + forum guidance | Each round |
| 5.2 | Forum Collaboration | ForumEngine monitors Agent speeches and generates moderator summary | ForumEngine + LLM moderator | Each round |
| 5.3 | Communication Integration | Each Agent adjusts research direction based on discussion | Each Agent + forum_reader tool | Each round |
| N+1 | Result Integration | Report Agent collects all analysis results and forum content | Report Agent | - |
| N+2 | Report Generation | Dynamically selects templates and styles, generates final report in multiple rounds | Report Agent + template engine | - |

### Project Code Structure Tree

```
Weibo_PublicOpinion_AnalysisSystem/
├── QueryEngine/                   # Domestic and international news breadth search Agent
│   ├── agent.py                   # Agent main logic
│   ├── llms/                      # LLM interface wrapper
│   ├── nodes/                     # Processing nodes
│   ├── tools/                     # Search tools
│   ├── utils/                     # Utility functions
│   └── ...                        # Other modules
├── MediaEngine/                   # Powerful multimodal understanding Agent
│   ├── agent.py                   # Agent main logic
│   ├── nodes/                     # Processing nodes
│   ├── llms/                      # LLM interface
│   ├── tools/                     # Search tools
│   ├── utils/                     # Utility functions
│   └── ...                        # Other modules
├── InsightEngine/                 # Private database mining Agent
│   ├── agent.py                   # Agent main logic
│   ├── llms/                      # LLM interface wrapper
│   │   └── base.py                # Unified OpenAI compatible client
│   ├── nodes/                     # Processing nodes
│   │   ├── base_node.py           # Base node class
│   │   ├── formatting_node.py     # Formatting node
│   │   ├── report_structure_node.py # Report structure node
│   │   ├── search_node.py         # Search node
│   │   └── summary_node.py        # Summary node
│   ├── tools/                     # Database query and analysis tools
│   │   ├── keyword_optimizer.py   # Qwen keyword optimization middleware
│   │   ├── search.py              # Database operation toolset
│   │   └── sentiment_analyzer.py  # Sentiment analysis integration tool
│   ├── state/                     # State management
│   │   ├── __init__.py
│   │   └── state.py               # Agent state definition
│   ├── prompts/                   # Prompt templates
│   │   ├── __init__.py
│   │   └── prompts.py             # Various prompts
│   └── utils/                     # Utility functions
│       ├── __init__.py
│       ├── config.py              # Configuration management
│       └── text_processing.py     # Text processing tools
├── ReportEngine/                  # Multi-round report generation Agent
│   ├── agent.py                   # Agent main logic
│   ├── llms/                      # LLM interface
│   ├── nodes/                     # Report generation nodes
│   │   ├── template_selection.py  # Template selection node
│   │   └── html_generation.py     # HTML generation node
│   ├── report_template/           # Report template library
│   │   ├── 社会公共热点事件分析.md
│   │   ├── 商业品牌舆情监测.md
│   │   └── ...                    # More templates
│   └── flask_interface.py         # Flask API interface
├── ForumEngine/                   # Simple Forum Engine implementation
│   ├── monitor.py                 # Log monitoring and forum management
│   └── llm_host.py                # Forum moderator LLM module
├── MindSpider/                    # Weibo crawler system
│   ├── main.py                    # Crawler main program
│   ├── config.py                  # Crawler configuration file
│   ├── BroadTopicExtraction/      # Topic extraction module
│   │   ├── database_manager.py    # Database manager
│   │   ├── get_today_news.py      # Today's news acquisition
│   │   ├── main.py                # Topic extraction main program
│   │   └── topic_extractor.py     # Topic extractor
│   ├── DeepSentimentCrawling/     # Deep sentiment crawling
│   │   ├── keyword_manager.py     # Keyword manager
│   │   ├── main.py                # Deep crawling main program
│   │   ├── MediaCrawler/          # Media crawler core
│   │   └── platform_crawler.py    # Platform crawler management
│   └── schema/                    # Database structure
│       ├── db_manager.py          # Database manager
│       ├── init_database.py       # Database initialization
│       └── mindspider_tables.sql  # Database table structure
├── SentimentAnalysisModel/        # Sentiment analysis model collection
│   ├── WeiboSentiment_Finetuned/  # Fine-tuned BERT/GPT-2 models
│   ├── WeiboMultilingualSentiment/# Multilingual sentiment analysis (recommended)
│   ├── WeiboSentiment_SmallQwen/  # Small parameter Qwen3 fine-tuning
│   └── WeiboSentiment_MachineLearning/ # Traditional machine learning methods
├── SingleEngineApp/               # Streamlit applications for individual Agents
│   ├── query_engine_streamlit_app.py
│   ├── media_engine_streamlit_app.py
│   └── insight_engine_streamlit_app.py
├── templates/                     # Flask templates
│   └── index.html                 # Main interface frontend
├── static/                        # Static resources
├── logs/                          # Runtime logs directory
├── final_reports/                 # Final generated HTML report files
├── utils/                         # Common utility functions
│   ├── forum_reader.py            # Inter-Agent forum communication
│   └── retry_helper.py            # Network request retry mechanism tool
├── app.py                         # Flask main application entry
├── config.py                      # Global configuration file
└── requirements.txt               # Python dependency list
```

## 🚀 Quick Start

> If you're learning how to build an Agent system for the first time, you can start with a very simple demo: [Deep Search Agent Demo](https://github.com/666ghj/DeepSearchAgent-Demo)

### Environment Requirements

- **Operating System**: Windows, Linux, MacOS
- **Python Version**: 3.9+
- **Conda**: Anaconda or Miniconda
- **Database**: MySQL (optional cloud database service available)
- **Memory**: 2GB+ recommended

### 1. Create Conda Environment

```bash
# Create conda environment
conda create -n your_conda_name python=3.11
conda activate your_conda_name
```

### 2. Install Dependencies

```bash
# Install basic dependencies
pip install -r requirements.txt
# If you don't want to use local sentiment analysis models (very low computing requirements, CPU version installed by default), you can comment out the "Machine Learning" section in this file before executing the command
```

### 3. Install Playwright Browser Driver

```bash
# Install browser driver (for crawler functionality)
playwright install chromium
```

### 4. Configure System

#### 4.1 Configure API Keys

Edit the `config.py` file and fill in your API keys (you can also choose your own models and search proxies, see details in the config file):

```python
# MySQL database configuration
DB_HOST = "localhost"
DB_PORT = 3306
DB_USER = "your_username"
DB_PASSWORD = "your_password"
DB_NAME = "your_db_name"
DB_CHARSET = "utf8mb4"

# LLM configuration
# You can change the API used by each LLM section, as long as it's compatible with OpenAI request format

# Insight Agent
INSIGHT_ENGINE_API_KEY = "your_api_key"
INSIGHT_ENGINE_BASE_URL = "https://api.moonshot.cn/v1"
INSIGHT_ENGINE_MODEL_NAME = "kimi-k2-0711-preview"
# Media Agent
...
```

#### 4.2 Database Initialization

**Option 1: Use Local Database**

> The MindSpider crawler system and public opinion system are independent of each other, so you need to configure `MindSpider\config.py` separately

```bash
# Local MySQL database initialization
cd MindSpider
python schema/init_database.py
```

**Option 2: Use Cloud Database Service (Recommended)**

We provide convenient cloud database service, including 100,000+ daily real public opinion data, currently **free to apply**!

- Real public opinion data, updated in real-time
- Multi-dimensional tag classification
- High-availability cloud service
- Professional technical support

**Contact us to apply for free cloud database access: 📧 670939375@qq.com**

> For data compliance review and service upgrade, the cloud database will suspend accepting new applications from October 1, 2025

### 5. Start System

#### 5.1 Complete System Startup (Recommended)

```bash
# In the project root directory, activate conda environment
conda activate your_conda_name

# Start the main application
python app.py
```

> Note 1: After a run terminates, the streamlit app may end abnormally and still occupy the port. In this case, search for the process occupying the port and kill it.

> Note 2: Data crawling requires separate operations, see section 5.3 for guidance

> Note 3: If page display issues occur during remote server deployment, see [PR#45](https://github.com/666ghj/BettaFish/pull/45)

Visit http://localhost:5000 to use the complete system

#### 5.2 Start Individual Agent Separately

```bash
# Start QueryEngine
streamlit run SingleEngineApp/query_engine_streamlit_app.py --server.port 8503

# Start MediaEngine  
streamlit run SingleEngineApp/media_engine_streamlit_app.py --server.port 8502

# Start InsightEngine
streamlit run SingleEngineApp/insight_engine_streamlit_app.py --server.port 8501
```

#### 5.3 Crawler System Standalone Use

This section has detailed configuration documentation: [MindSpider Usage Instructions](./MindSpider/README.md)

<div align="center">
<img src="MindSpider\img\example.png" alt="banner" width="600">

MindSpider Running Example
</div>

```bash
# Enter crawler directory
cd MindSpider

# Project initialization
python main.py --setup

# Run complete crawler workflow
python main.py --complete --date 2024-01-20

# Run topic extraction only
python main.py --broad-topic --date 2024-01-20

# Run deep crawling only
python main.py --deep-sentiment --platforms xhs dy wb
```

## ⚙️ Advanced Configuration

### Modify Key Parameters

#### Agent Configuration Parameters

Each Agent has a dedicated configuration file that can be adjusted according to needs. Here are some examples:

```python
# QueryEngine/utils/config.py
class Config:
    max_reflections = 2           # Number of reflection rounds
    max_search_results = 15       # Maximum search results
    max_content_length = 8000     # Maximum content length
    
# MediaEngine/utils/config.py  
class Config:
    comprehensive_search_limit = 10  # Comprehensive search limit
    web_search_limit = 15           # Web search limit
    
# InsightEngine/utils/config.py
class Config:
    default_search_topic_globally_limit = 200    # Global search limit
    default_get_comments_limit = 500             # Comment retrieval limit
    max_search_results_for_llm = 50              # Maximum results for LLM
```

#### Sentiment Analysis Model Configuration

```python
# InsightEngine/tools/sentiment_analyzer.py
SENTIMENT_CONFIG = {
    'model_type': 'multilingual',     # Options: 'bert', 'multilingual', 'qwen', etc.
    'confidence_threshold': 0.8,      # Confidence threshold
    'batch_size': 32,                 # Batch size
    'max_sequence_length': 512,       # Maximum sequence length
}
```

### Integrate Different LLM Models

Supports any LLM provider with OpenAI call format. Simply fill in the corresponding KEY, BASE_URL, and MODEL_NAME in /config.py.

> What is OpenAI call format? Here's a simple example:
>```python
>from openai import OpenAI
>
>client = OpenAI(api_key="your_api_key", 
>                base_url="https://api.siliconflow.cn/v1")
>
>response = client.chat.completions.create(
>    model="Qwen/Qwen2.5-72B-Instruct",
>    messages=[
>        {'role': 'user', 
>         'content': "What new opportunities will reasoning models bring to the market"}
>    ],
>)
>
>complete_response = response.choices[0].message.content
>print(complete_response)
>```

### Change Sentiment Analysis Model

The system integrates multiple sentiment analysis methods, which can be selected according to needs:

#### 1. Multilingual Sentiment Analysis

```bash
cd SentimentAnalysisModel/WeiboMultilingualSentiment
python predict.py --text "This product is amazing!" --lang "en"
```

#### 2. Small Parameter Qwen3 Fine-tuning

```bash
cd SentimentAnalysisModel/WeiboSentiment_SmallQwen
python predict_universal.py --text "这次活动办得很成功"
```

#### 3. BERT-based Fine-tuned Model

```bash
# Use BERT Chinese model
cd SentimentAnalysisModel/WeiboSentiment_Finetuned/BertChinese-Lora
python predict.py --text "这个产品真的很不错"
```

#### 4. GPT-2 LoRA Fine-tuned Model

```bash
cd SentimentAnalysisModel/WeiboSentiment_Finetuned/GPT2-Lora
python predict.py --text "今天心情不太好"
```

#### 5. Traditional Machine Learning Methods

```bash
cd SentimentAnalysisModel/WeiboSentiment_MachineLearning
python predict.py --model_type "svm" --text "服务态度需要改进"
```

### Integrate Custom Business Database

#### 1. Modify Database Connection Configuration

```python
# Add your business database configuration in config.py
BUSINESS_DB_HOST = "your_business_db_host"
BUSINESS_DB_PORT = 3306
BUSINESS_DB_USER = "your_business_user"
BUSINESS_DB_PASSWORD = "your_business_password"
BUSINESS_DB_NAME = "your_business_database"
```

#### 2. Create Custom Data Access Tool

```python
# InsightEngine/tools/custom_db_tool.py
class CustomBusinessDBTool:
    """Custom business database query tool"""
    
    def __init__(self):
        self.connection_config = {
            'host': config.BUSINESS_DB_HOST,
            'port': config.BUSINESS_DB_PORT,
            'user': config.BUSINESS_DB_USER,
            'password': config.BUSINESS_DB_PASSWORD,
            'database': config.BUSINESS_DB_NAME,
        }
    
    def search_business_data(self, query: str, table: str):
        """Query business data"""
        # Implement your business logic
        pass
    
    def get_customer_feedback(self, product_id: str):
        """Get customer feedback data"""
        # Implement customer feedback query logic
        pass
```

#### 3. Integrate into InsightEngine

```python
# Integrate custom tool in InsightEngine/agent.py
from .tools.custom_db_tool import CustomBusinessDBTool

class DeepSearchAgent:
    def __init__(self, config=None):
        # ... other initialization code
        self.custom_db_tool = CustomBusinessDBTool()
    
    def execute_custom_search(self, query: str):
        """Execute custom business data search"""
        return self.custom_db_tool.search_business_data(query, "your_table")
```

### Custom Report Templates

#### 1. Upload in Web Interface

The system supports uploading custom template files (.md or .txt format), which can be selected when generating reports.

#### 2. Create Template File

Create a new template in the `ReportEngine/report_template/` directory. Our Agent will automatically select the most appropriate template.

## 🤝 Contribution Guidelines

We welcome all forms of contributions!

### How to Contribute

1. **Fork the project** to your GitHub account
2. **Create Feature branch**: `git checkout -b feature/AmazingFeature`
3. **Commit changes**: `git commit -m 'Add some AmazingFeature'`
4. **Push to branch**: `git push origin feature/AmazingFeature`
5. **Open Pull Request**

### Development Standards

- Code follows PEP8 standards
- Commit messages use clear Chinese and English descriptions
- New features need to include corresponding test cases
- Update relevant documentation

## 🦖 Next Development Plan

Currently, the system has only completed the first two steps of the "three axes": input requirements -> detailed analysis. It still lacks the prediction step. Directly handing it to LLM is not convincing.

<div align="center">
<img src="static/image/banner_compressed.png" alt="banner" width="800">
</div>

Currently, after a long period of crawling and collection, we have accumulated a large amount of data on how topic popularity changes over time, explosive points, and other trend data across the web. We already have the conditions to develop prediction models. Our team will apply time series models, graph neural networks, multimodal fusion, and other predictive model technical reserves here to achieve truly data-driven public opinion prediction functionality.

## ⚠️ Disclaimer

**Important Reminder: This project is for learning, academic research, and educational purposes only**

1. **Compliance Statement**:
   - All code, tools, and functions in this project are for learning, academic research, and educational purposes only
   - It is strictly prohibited to use this project for any commercial purposes or profit-making activities
   - It is strictly prohibited to use this project for any illegal, non-compliant, or rights-infringing behaviors

2. **Crawler Function Disclaimer**:
   - The crawler function in the project is for technical learning and research purposes only
   - Users must comply with the target website's robots.txt protocol and terms of use
   - Users must comply with relevant laws and regulations and not conduct malicious crawling or data abuse
   - Any legal consequences arising from the use of crawler functions shall be borne by the user

3. **Data Use Disclaimer**:
   - The data analysis functions involved in the project are for academic research only
   - It is strictly prohibited to use analysis results for commercial decisions or profit purposes
   - Users should ensure the legality and compliance of the analyzed data

4. **Technical Disclaimer**:
   - This project is provided "as is" without any express or implied warranties
   - The author is not responsible for any direct or indirect losses caused by using this project
   - Users should evaluate the applicability and risks of the project themselves

5. **Liability Limitation**:
   - Users should fully understand relevant laws and regulations before using this project
   - Users should ensure that their use behavior complies with local laws and regulations
   - Any consequences arising from the use of this project in violation of laws and regulations shall be borne by the user

**Please read and understand the above disclaimer carefully before using this project. Using this project indicates that you have agreed to and accepted all the above terms.**

## 📄 License

This project is licensed under the [GPL-2.0 License](LICENSE). For detailed information, please refer to the LICENSE file.

## 🎉 Support and Contact

### Get Help

- **Project Homepage**: [GitHub Repository](https://github.com/666ghj/Weibo_PublicOpinion_AnalysisSystem)
- **Issue Feedback**: [Issues Page](https://github.com/666ghj/Weibo_PublicOpinion_AnalysisSystem/issues)
- **Feature Suggestions**: [Discussions Page](https://github.com/666ghj/Weibo_PublicOpinion_AnalysisSystem/discussions)

### Contact Information

- 📧 **Email**: 670939375@qq.com

### Business Cooperation

- **Enterprise Custom Development**
- **Big Data Services**
- **Academic Cooperation**
- **Technical Training**

## 👥 Contributors

Thanks to these excellent contributors:

[![Contributors](https://contrib.rocks/image?repo=666ghj/Weibo_PublicOpinion_AnalysisSystem)](https://github.com/666ghj/Weibo_PublicOpinion_AnalysisSystem/graphs/contributors)

## 📈 Project Statistics

<a href="https://www.star-history.com/#666ghj/BettaFish&type=date&legend=top-left">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=666ghj/BettaFish&type=date&theme=dark&legend=top-left" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=666ghj/BettaFish&type=date&legend=top-left" />
   <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=666ghj/BettaFish&type=date&legend=top-left" />
 </picture>
</a>

![Alt](https://repobeats.axiom.co/api/embed/e04e3eea4674edc39c148a7845c8d09c1b7b1922.svg "Repobeats analytics image")
