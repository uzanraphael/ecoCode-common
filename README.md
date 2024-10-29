# Common doc / tools

This repository contains common parts like :

- documentation : please read MarkDown files (`*.md`) in `doc` directory
- tools : if needed, please read `README.md` files on each tool of `tool` directory


```mermaid
graph TD
    subgraph ecoCode-common[<a href='http://google.com'>ecoCode-common</a>]
        A1['1. ./check_requirements.sh']
    end

    subgraph ecoCode-python[<a href='http://google.com'>ecoCode-python</a>]
        B1['2. ./tool_build.sh']
    end

    subgraph ecoCode-common
        A2['3. ./tool_docker-init.sh']
    end

    subgraph ecoCode-common
        D['3. ./tool_docker-init.sh']
    end

    subgraph ecoCode-python-test-project[<a href='http://google.com'>ecoCode-python-test-project</a>]
        C1['5. ./tool_send_to_sonar.sh MY_SONAR_TOKEN']
    end

    A1 -->|If not OK| D[Info d'install dans le HOWTO]
    D-->|If OK| B1
    A1 -->|If OK| B1
    B1 --> A2
    A2 --> E['4. Configure SonarQube on local UI']
    E --> C1

```
