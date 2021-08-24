# martin-fowler-refactoring-2nd
Martin Fowler의 Refactoring 2판을 연습합니다.

## Yarn

이 프로젝트는 [Yarn](https://yarnpkg.com/en/docs/install) package manager에 의존하고 있습니다.

프로젝트를 세팅하기 이전에 Yarn을 설치해주세요

## JS 코드를 작성할수 있는 조건하에 전체가 아닌 일부의 코드를 테스트 할수있는 간단한 JS Project를 직접 세팅할수 있습니다.

프로젝트를 위한 여러분컴퓨터 아무곳에나 Root Directory를 생성하세요.

그리고 여러분의 프로젝트의 Root Directory에서 다음의 명령을 실행하세요.

``` sh
 yarn init
 yarn add --save-dev mocha chai babel-register babel-preset-es201
```

`package.json`을 열어서 `test script`를 아래와 같이 작성하세요
``` javascript
  "scripts": {
    "test": "mocha --watch --recursive --require babel-core/register"
  },
```  

Create a .babelrc file in the project directory:
Project directory `.babelrc`파일을 생성하시고 다음의 내용을 추가해주세요

```
{
  "presets": ["es2015"]
}
```


## Set up project: 

## Project 세팅

이 프로젝트는 [Yarn](https://yarnpkg.com/en/docs/install) package manager에 의존하고 있습니다.

Project의 Root Directory에서 다음의 명령어를 실행하세요

``` sh
 yarn
```

## 테스트 실행

Project의 Root Directory에서 다음의 명령어를 실행하세요

``` sh
  yarn test
```

## Setup JetBrain's WebStorm to run test:

Configuration 창에서 다음을 Node options에 추가해주세요

```
-r babel-register
````
![](webstorm-setup.png)
