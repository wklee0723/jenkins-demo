
pipeline {
    // GitHub Actions의 `runs-on: ubuntu-latest / windows-latest` 와 유사
    // → 이 파이프라인을 실행할 Jenkins 실행 노드(에이전트)를 지정
    // `any` = Jenkins가 사용 가능한 아무 노드에서나 실행
    agent any

    // GitHub Actions의 `on: push:` 와 같은 역할
    // → GitHub에 push 이벤트가 발생하면 이 파이프라인을 자동 실행
    triggers {
        githubPush()
    }

    stages {
        // GitHub Actions의 `jobs:` 또는 `steps:` 중
        // "의미 있는 작업 단위"에 해당.
        // CI 과정의 큰 단계라고 보면 됨
        stage('Run CI Script') {

            steps {
                // GitHub Actions의 `run:` 과 동일한 개념
                // → 실제로 실행될 커맨드
                bat 'main.bat'

                // 만약 GitHub Actions였다면 아래와 비슷함
                // run: main.bat
            }
        }
    }
}
