
# multi_tool_agent

This project was created based on ADK Quickstart.
It is a Python package that implements an agent (`Agent`) that provides the current time and weather information for a specific city.

## Reference Documents

- ADK Quickstart: https://google.github.io/adk-docs/get-started/quickstart/

## Key Features

- **Weather Information Query**: Returns the current weather information for a city when its name is entered. (Currently supports only “New York”)
- **Current Time Query**: Returns the current time for a city when its name is entered. (Currently supports only “New York”)

## Technologies Used

- Python 3
- [google.adk.agents](https://github.com/google/adk) library
- Standard library(`datetime`, `zoneinfo`)

## Security and Precautions
- Sensitive configuration values should be managed via environment variables and not hardcoded in the code.
- Always exercise caution when handling user input.

## Example

```sh
python3 -m venv .venv


source .venv/bin/activate


pip install google-adk


adk run multi_tool_agent


Log setup complete: /var/folders/q0/s21_cs310_51tn_md1slhfbm0000gn/T/agents_log/agent.20250626_172207.log
To access latest log: tail -F /var/folders/q0/s21_cs310_51tn_md1slhfbm0000gn/T/agents_log/agent.latest.log
/Users/scone-dsrv/develop/github/sconeman/adk-quickstart/.venv/lib/python3.13/site-packages/google/adk/cli/cli.py:134: UserWarning: [EXPERIMENTAL] InMemoryCredentialService: This feature is experimental and may change or be removed in future versions without notice. It may introduce breaking changes at any time.
  credential_service = InMemoryCredentialService()
/Users/scone-dsrv/develop/github/sconeman/adk-quickstart/.venv/lib/python3.13/site-packages/google/adk/auth/credential_service/in_memory_credential_service.py:33: UserWarning: [EXPERIMENTAL] BaseCredentialService: This feature is experimental and may change or be removed in future versions without notice. It may introduce breaking changes at any time.
  super().__init__()
Running agent weather_time_agent, type exit to exit.
[user]: hello!
[weather_time_agent]: Hello! How can I help you today?

[user]: what's the whether like today?
[weather_time_agent]: Could you please tell me which city you're interested in?

[user]: new york
[weather_time_agent]: The weather in New York is sunny with a temperature of 25 degrees Celsius (77 degrees Fahrenheit).

[user]: What is the weather in Paris?
[weather_time_agent]: I am sorry, weather information for Paris is not available.

[user]: What is the time in Paris?
[weather_time_agent]: I am sorry, I don't have timezone information for Paris.

[user]: new york의 날씨는 어때?
[weather_time_agent]: 현재 New York의 날씨는 맑고, 온도는 25도 Celsius (77도 Fahrenheit)입니다.

[user]: ^D
Aborted


deactivate
```