---
tags: [main]
---

# Identification-Documentation

Cometrue.ai의 신분증 검출, 진위여부 API는 여러가지 정보를 리턴해줍니다. 예를 들면 신분증 이미지가 주민등록증인지 운전면허증인지, 신분증에 존재하는 텍스트와 위치를 파악하여 좌표를 `JSON` 형태로 돌려줍니다.

이 문서에서는 신분증 인식에 대한 API호출 및 속성에 대해 설명합니다. 문의사항이 있으면 `info@cometrue.ai`로 연락하십시오.


# API Reference
## 신분증 OCR
**Method**

POST

**Argument**

id_type은 jumin, driver 중 하나를 선택하고, image는 이미지를 base64로 인코딩하여 전달하면 됩니다.

**Example Request**
```json
//POST https://api.cometrue.ai/v1/idocr/text
{
    "id_type" : "jumin",
    "image" : "iVBORw0KGgoAAAANSUhEUgAACbEAAA2zCAYAAADce6KLAAAA...."
}
```

**Example Response**

```json
{
    "quadrilateral": true,
    "result": {
        "date": "20150107",
        "name": "홍길동",
        "number": "610220-1250511",
        "title": "주민등록증"
    }
}
```

**Example Error Response**

```json
{
    "message": "image cannot be read"
}
```