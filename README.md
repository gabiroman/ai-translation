# ai-translation
Translator web app with ai using traslator service of Azure.

## Demo
![Web capture_16-10-2023_114552_127 0 0 1](https://github.com/gabiroman/ai-translation/assets/45351498/ab97e02f-8cae-446f-8895-18701e42b1c1)
![Web capture_16-10-2023_11464_127 0 0 1](https://github.com/gabiroman/ai-translation/assets/45351498/0ae14d07-b7ab-46c0-be24-dfa21fe8a3a6)

## Prerequisites
Here's what you need to be able to run ai-translator:
- Azure account
- Python 3.6 o later

## Installation

### 1. Clone this repository
```shell
git clone https://github.com/gabiroman/ai-translation.git
cd ai-translation
```

### 2. Create and activate virtual enviroment
```shell
python3 -m venv venv
source ./venv/bin/activate
```

### 3. Install dependencies
```shell
pip install -r requirements.txt
```

### 4. Copy the example .env file
```shell
cp .env.example .env
```

### 5. Create Translator service
- Browse to the <a href="https://portal.azure.com/">Azure portal</a>
- Select **Create a resource**
- Search **Translator**
- Select **Create**
- Complete the Create Translator form with the following values:

| Variable | Value |
|---|---|
|Subscription|Your subscription|
|Resource group|Select Create new; Name: app-ai|
|Resource group region|Select a region near you|
|Resource region|Select the same region as above|
|Name|A unique value, such as ai-yourname|
|Pricing tier|Free F0|

- Select **Review + create**
- Select **Create**
- Select **Go to resource**
- Select Keys and Endpoint on the left side under **RESOURCE MANAGEMENT**

### 6. Configure the variables in `.env`
| Variable | Value |
|---|---|
| KEY | < Service's key > |
| ENDPOINT | < Service's endpoit > |
| LOCATION  | < Service's location > |

Your .env file should look like the following (with your values):
```shell
KEY=00d09299d68548d646c097488f7d9be9
ENDPOINT=https://api.cognitive.microsofttranslator.com/
LOCATION=westus2
```

### 7. Run the app
```shell
export FLASK_ENV=development
flask run
```

### 8. Open the app in your browser
Visit http://localhost:5000 in your browser.

