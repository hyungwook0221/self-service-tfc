
## 변수선언
![img](https://raw.githubusercontent.com/hyungwook0221/img/main/uPic/54iGQi.jpg)

```javascript
var orgToken = "값 입력";
var userToken = "값 입력";

// varset 값은 Global Vars 생성 후 URL에서 획득
var tfVarSet = "varset-GYigSzGs925Y3eS9";
```

## createWorkspaceData

![img](https://raw.githubusercontent.com/hyungwook0221/img/main/uPic/gJXkJA.jpg)

```json
  var createWorkspaceData = { 
    'data':
    { 
      'attributes': {
        "name": rangeArray[0][4],
        "description": "Created via Google Forms",
        "vcs-repo": {
          "identifier": "hyungwook0221/self-service-tfc",
          "oauth-token-id": "ot-BaLqh4H6A8nnzHJ4",
          "branch": "main",
          "tags-regex": null
        },
        "execution-mode": "remote",
        "auto-apply": true,
        "drift-detection": true,
        "speculative-enabled": false,
        "pull-request-outputs-enabled": false,
        "working-directory": "",
        "terraform-version": null,
        "allow-destroy-plan": true,
        "auto-destroy-at": null,
        "file-triggers-enabled": false,
        "trigger-prefixes": [],
        "trigger-patterns": [],
        "structured-run-output-enabled": true,
        "tag-names": ["gForms"]
      },
      'type': "workspaces" 
    }
  };
```


## emailNotificationData
- user-id 획득방법
> 참고 :   
https://developer.hashicorp.com/terraform/cloud-docs/api-docs#inclusion-of-related-resources

```bash
 $ curl \
  --header "Authorization: Bearer $TOKEN" \
  --header "Content-Type: application/vnd.api+json" \
  --request GET \
  https://app.terraform.io/api/v2/teams/team-Q6KGzRJvzvKW3Z1g\?include\=users | jq .data.relationships
```

- json 데이터 결과
```json
{
  "organization": {
    "data": {
      "id": "hyungwook",
      "type": "organizations"
    }
  },
  "users": {
    "data": [
      {
        "id": "user-2FB1FXN7NpK7cvce",
        "type": "users"
      },
      {
        "id": "user-Q6g847ovPx7q48Py",
        "type": "users"
      },
      {
        "id": "user-2rMYvq9amdbdmjJS",
        "type": "users"
      }
    ]
  },
  "organization-memberships": {
    "data": [
      {
        "id": "ou-F1d4Ktr697prAtVV",
        "type": "organization-memberships"
      },
      {
        "id": "ou-9QK28DTDryphXX1K",
        "type": "organization-memberships"
      },
      {
        "id": "ou-4PuPWZv2ooG4vbyn",
        "type": "organization-memberships"
      }
    ]
  },
  "authentication-token": {
    "meta": {}
  }
}
```

- user name 획득
```bash
 curl \
  --header "Authorization: Bearer $TOKEN" \
  --header "Content-Type: application/vnd.api+json" \
  --request GET \
  https://app.terraform.io/api/v2/users/user-2rMYvq9amdbdmjJS | jq .
```

```json
{
  "data": {
    "id": "user-2rMYvq9amdbdmjJS",
    "type": "users",
    "attributes": {
      "username": "hyungwook",
      "is-service-account": false,
      "avatar-url": "https://www.gravatar.com/avatar/c720274d0e787af6dd8605ef77c952a5?s=100&d=mm",
      "permissions": {
        "can-create-organizations": false,
        "can-view-settings": false,
        "can-change-email": false,
        "can-change-username": true,
        "can-manage-user-tokens": false,
        "can-view2fa-settings": false,
        "can-manage-hcp-account": false
      }
    },
    "relationships": {
      "authentication-tokens": {
        "links": {
          "related": "/api/v2/users/user-2rMYvq9amdbdmjJS/authentication-tokens"
        }
      },
      "github-app-oauth-tokens": {
        "links": {
          "related": "/api/v2/users/user-2rMYvq9amdbdmjJS/github-app-oauth-tokens"
        }
      }
    },
    "links": {
      "self": "/api/v2/users/user-2rMYvq9amdbdmjJS"
    }
  }
}
```




## 완료화면

![img](https://raw.githubusercontent.com/hyungwook0221/img/main/uPic/0uvKbW.jpg)

![img](https://raw.githubusercontent.com/hyungwook0221/img/main/uPic/vHJIIQ.jpg)

![img](https://raw.githubusercontent.com/hyungwook0221/img/main/uPic/BUcHeR.jpg)


## 삭제화면

![img](https://raw.githubusercontent.com/hyungwook0221/img/main/uPic/690Ohj.jpg)

![img](https://raw.githubusercontent.com/hyungwook0221/img/main/uPic/q4D20c.jpg)
