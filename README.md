<img width="1100" height="1361" alt="image" src="https://github.com/user-attachments/assets/7b5cb4a1-2944-4789-a7c3-32effebabde1" />




### LLM | Types of AI Agents

✅ Simple Reflex Agents: These follow condition–action rules. For example, if the temperature is high, turn on the fan. No memory, no thinking, just instant reaction. They are fast and simple.

✅ Model-based Reflex Agents: These maintain an internal understanding of their environment. They are not just reacting to immediate inputs, they have a model that helps them make sense of what is happening beyond what they can see right now.

✅ Goal-based Agents: Here, the focus shifts to goals. Decisions are made based on whether an action brings the agent closer to its objective.

✅ Utility-based Agents: These go a step further by weighing different outcomes. They choose the action that offers the best overall result, balancing trade-offs along the way.

✅ Learning Agents: These are the most advanced. They improve continuously, using feedback to adapt and perform better over time.


#### Key Features
```
✅ Coordinator,processes manage data availability on the cluster.
✅ Overlord,processes control the assignment of data ingestion workloads.
✅ Broker,processes handle queries from external clients.
✅ Router,processes are optional; they route requests to Brokers, Coordinators, and Overlords.
✅ Historical,processes store queryable data.
✅ MiddleManager,Processes ingest data.
```

#### Prerequisites
The deployment process is fully automated using AWS CDK and SeedFarmer.

- AWS Account with appropriate permissions
- AWS CLI configured with credentials
- Node.js 18+ and npm
- Python 3.8+
- AWS CDK CLI version compatible with aws-cdk-lib 2.206.0 or later
  ```bash
  # Install or update the CDK CLI globally
  npm install -g aws-cdk@latest
  
  # Verify the installed version
  cdk --version
  ```


🚀 Deployment 
```
git clone https://github.com/crypterio-app/aws-genai-llm-chatbot.git
cd aws-genai-llm-chatbot
npm ci && npm run build
npm run test && pip install -r pytest_requirements.txt && pytest tests
npm run config

npm run cdk bootstrap aws://{targetAccountId}/{targetRegion}
npm run cdk deploy
```


