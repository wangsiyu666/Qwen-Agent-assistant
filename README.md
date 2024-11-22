# Qwen-Agent-assistant
使用这个框架是因为在使用LangChain接入Qwen时对Fn的命中不高，固借鉴了官方的代码，感觉效果很好，列出此Demo。
本项目使用Xinference启动的Qwen2.5-instruct以保证兼容OpenAI API，如何使用Xinference请自行百度，或者使用其他工具Vllm，Ollama启动
# 为什么使用Assistant？
一般建议先试试function call；不满足需求就再看看react；依然不满足需求就可以类似 qwen_agent/llm/function_calling.py
那样实现自己的function call（对一般用户来说难度较大），或参考 FnCallAgent、Assistant、ReActChat 这些agent类实现自己的agent（相对容易）。
# 如何(register)添加自己的模型或者工具
tools： 本项目简单注册了一个OpenWeather的工具(免费) 可在官网申请
注册模型：请参看llm/custom_xinference_qwen2_5.py里的逻辑
注册函数：请参看tools/OpenWeather.py里的逻辑
## 欢迎大家一起讨论LangChain, Qwen, Agent, RAG, Xinference, multimodal~~
