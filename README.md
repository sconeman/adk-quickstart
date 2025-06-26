
# multi_tool_agent

이 프로젝트는 ADK Quickstart에 따라 만들어졌습니다.
특정 도시의 현재 시간과 날씨 정보를 제공하는 에이전트(`Agent`)를 구현한 Python 패키지입니다.

## 참고 문서

- ADK Quickstart: https://google.github.io/adk-docs/get-started/quickstart/

## 주요 기능

- **날씨 정보 조회**: 도시 이름을 입력하면 해당 도시의 현재 날씨 정보를 반환합니다. (현재는 "New York"만 지원)
- **현재 시간 조회**: 도시 이름을 입력하면 해당 도시의 현재 시간을 반환합니다. (현재는 "New York"만 지원)

## 사용 기술

- Python 3
- [google.adk.agents](https://github.com/google/adk) 라이브러리
- 표준 라이브러리(`datetime`, `zoneinfo`)

## 보안 및 주의사항

- 민감한 설정 값은 환경 변수로 관리해야 하며, 코드에 직접 입력하지 않습니다.
- 사용자 입력을 처리할 때는 항상 보안에 유의해야 합니다.

## 예시

```sh
python3 -m venv .venv


source .venv/bin/activate


pip install google-adk


adk run multi_tool_agent


deactivate
```

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
```