# cometrue.ai AI API

## Introduction
### API Integration
Cometrue.ai는 REST API를 통해 다양한 환경 및 프로그래밍 언어와 통합 될 수 있습니다. 다양한 프로그래밍 언어로 API래퍼를 제공하고 있습니다. 래퍼 및 사용가능한 코드 샘플에 대한 소개는 **API코드개요** 문서를 확인하세요
관련 문의는 `ask@comtrue.com`로 접수해주시면 순차적으로 답변을 드리겠습니다.

### API Overview
Cometrue.ai API를 사용하면 자신의 애플리케이션에서 얼굴인식, 신분증 OCR 등을 구현할 수 있습니다.

### Authentication
인증은 HTTP프로토콜을 기반으로 한 TLS 1.2이상에서 지원됩니다.

### URL
API 호출을 위한 URL은 다음과 같이 지원됩니다.
`https://api.cometrue.ai/<resource URI>`

### Data Request
POST 요청 데이터는 JSON(`application/json`) 형식으로 지정할 수 있습니다.
Cometrue.ai는 `api_key`를 제외한 데이터는 쿼리 매개변수로 전송할 수 없습니다.

### Data Response
요청에 대한 응답데이터는 JSON형식으로 전송되며 응답코드는 HTTP Status Code를 전달됩니다.

### HTTP Status Code
HTTP Status Code | HTTP | Description
---------|----------|---------
 200 | OK | 정상응답
 400 | Bad Request | 필수요청 변수가 누락되었거나, 변수 이름이 잘못되었을 경우
 401 | Unauthorized | 허가되자 않은 접근
 404 | Not Found | API 호출 URL이 잘못되었을 경우
 422 | Unprocessable Entity | API 구독이 취소되거나, 평가판이 종료되었을 경우
 429 | Too many Request |비정상적으로 호출을 많이 시도하였을 때
 500 | Internal Server Error | API 호출은 정상적으로 했지만 API 서버 오류로 인한 경우

