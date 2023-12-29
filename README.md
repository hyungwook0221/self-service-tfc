
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
