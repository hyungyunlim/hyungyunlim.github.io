---
layout: post
title:  "블로그 다시 시작"
author: "junlim"
tags: wiki knowledgebase documentation archive
---

<figure>
  <img data-action="zoom" src='{{ "/images/notion-use-case-screenshot-wiki.gif" | relative_url }}' alt='notion'>
  <figcaption>노션을 통한 위키 구조 예시</figcaption>
</figure>

[노션(Notion)](https://www.notion.so/?r=c28c8f6d88af411986aa657212492b58)은 단순하게 얘기하면 고도화된 노트앱이라서 개인적으로 사용할 수도 있고, 팀/조직내의 문서 정리 및 위키로 활용 가능한 서비스다. 웹, 데스크탑, 모바일을 모두 지원한다. 아직까지 국내에서는 조직 및 팀내 사례보다는 얼리어답터분들이 개인적으로 사용하고 있는 경우가 더 흔한 것 같다.

- [디자이너, 첫 회사 생활로 배운 6가지 업무 습관](https://brunch.co.kr/@andsalt/17) - 디자이너분이 개인적인 업무일지로 활용하는 사례
- [요즘 뜨는 노트 앱 노션(Notion) 3시간 사용기 – 마이크로소프트웨어](https://www.imaso.co.kr/archives/3810) - 기자의 노트앱 체험기

조직 내 도입 사례는 많지 않은데 최근 [당근 마켓](https://www.daangn.com/)에서 조직 내 도입 과정을 상세히 [정리](https://medium.com/daangn/스타트업-더-좋은-문서도구가-필요해요-notion을-만나다-ff4f7e0414f)해 주셨다. 여전히 조직 내 도입 관련 포스팅은 별로 없는 것 같아서 정리해보기로 했다.

### 노션(Notion)
보통 신규 서비스를 사용할때는 어떤 철학으로 만들어졌는지, 어떤 팀이 만들고 있는지, 면밀히 살펴보는 편이다. 일단 노션의 웹사이트에 접속하면 아래와 같은 메인 화면이 제일 먼저 눈에 들어온다.

<figure>
  <img data-action="zoom" src='{{ "/images/notion-front-page-hero.png" | relative_url }}' alt='notion'>
  <figcaption>노션 웹사이트 메인 이미지</figcaption>
</figure>
일단 제일 먼저 눈에 들어오는 것은 “All-in-One Workspace”이라는 슬로건이다. 그 아래로는 일러스트로 표시된 각 기능을 상징하는 캐릭터들이 있다. 여담이지만 이런 일러스트레이트가 들어간 웹사이트가 자주 보이는데 최근에 디자인을 담당하는 회사 동료를 통해 일러스트풍의 웹사이트가 [글로벌 트렌드](https://webflow.com/blog/illustration-trends-in-web-design-for-2018)라는 것을 알게 되었다.  어쨌든 각각의 캐릭터들은 노션의 핵심 기능을 상징한다.

- Notes, Docs: 노트, 문서 정리
- Knowledge Base: 위키, 정보 포털
- Tasks, Project: 할일 관리 및 프로젝트 관리
- Spreadsheets, Database: 데이터베이스 기반의 관리 (엑셀 관련 기능)

좀더 내리다 보면 아래와 같은 이미지가 나온다. 한마디로 노션을 사용하면 여기에 명시된 서비스들을 대체할 수 있다는 것이다. 구글독(Google Doc), 지라(JIRA), 트렐로(Trello), 드롭박스 페이퍼(Dropbox Paper), 컨플루언스(Confluence) 등 문서 작성/관리 및 프로젝트 관리 분야의 내노라하는 솔루션들이다. 솔루션들의 가치가 각각 수천억에서 수조원에 이르기때문에 이 모든 툴을 대체한다고 명시하는 것 자체가 상당히 대담한 설명이라고 할 수 있다.
<figure>
  <img data-action="zoom" src='{{ "/images/notion_replace_tools.png" | relative_url }}' alt='notion'>
  <figcaption>노션을 통해 대체할 수 있다고 설명하는 일러스트</figcaption>
</figure>
그래서 더욱 호기심이 생겼던 것 같다. 회사의 [About 페이지](https://www.notion.so/about?r=c28c8f6d88af411986aa657212492b58)를 참고하면 설계 의도를 알 수 있다. 아직 국내에서는 다소 생소할 수 있지만 이미 글로벌하게는 클라우드기반의 파일관리, 협업 커뮤니케이션 및 메시징 서비스의 활용, 업무의 생산성을 높히기 위한 프로젝트 관리 관련 서비스들이 급속도로 확산되고 있다. 이 때문에 트렐로/슬랙과 같은 솔루션이 적게는 수천억 많게는 수조원의 가치를 인정받고 있다. ~~그래서 우리도 관련 분야의 서비스를 만들고 있다.~~ 하지만 좋은 점만 있는 것은 아니다. 개인별/팀별 사용하는 서비스가 달라지다보니 구성원들의 피로도도 올라가고, 자료를 찾기도 쉽지 않다. 노션은 이런점에 착안해서 여러 툴들의 기능들을 마치 레고 블록처럼 구성해서 편집할 수 있도록 했다.
<figure>
  <img data-action="zoom" src='{{ "/images/notion_lego_blocks.png" | relative_url }}' alt='notion'>
  <figcaption>노션의 레고 블록에 대한 콘셉</figcaption>
</figure>

<figure>
  <img data-action="zoom" src='{{ "/images/notion_lego_blocks.gif" | relative_url }}' alt='notion'>
  <figcaption>레고 블록처럼 화면을 에디팅할 수 있는 노션</figcaption>
</figure>

나중에 알게된 사실이지만 노션의 수장을 맡고 있는 이반 자오(Ivan Zhao)는 전 직장이 [잉클링(Inkling)](https://www.inkling.com)이다. 검색을 하다가 처음 알게되었는데 웹사이트를 보면 문서 작성 및 협업을 도와 주는 도구다. 물론 노션과는 많이 다르지만 아마 이곳에서의 경험이 노션에 크게 영향을 줬을 것 같다.

### 노션과 이미지블
[이미지블(IMGIBBLE)](https://www.imgibble.com/?utm_source=Blog&utm_medium=Jun&utm_campaign=Post)은 이미지/영상 등 콘텐츠 기반의 커뮤니케이션 솔루션을 개발하는 스타트업으로 현재 네 명의 구성원이 있다. 팀 내 메신저는 슬랙을 사용하고 있고, 구글 앱스(지메일, 구글드라이브, 구글독스)를 적극적으로 활용하고 있다. 트렐로를 통해서 일부 프로젝트를 관리했다. 예전부터 소위 '스마트워크’ 라고 하는 서비스들을 많이 사용해봤기때문에 내부에서 셋업된 방식에 어느정도의 자부심이 있었다.  그러던 와중에 누군가 페이스북에 노션을 소개하는 글을 보게 되었고, 호기심에 찾아보다가 다운로드 받아서 조금 써봤다.

첫 인상은 복잡한 느낌이었고 아직은 몇 명 안되는 조직이라서 거부감이 먼저 들었다. 하지만 사용을 해보면 해볼수록 깔끔하고, 잘만들었다는 생각이 들었고, 팀원들에게 먼저 간단히 소개를 했다. 당장은 도입하지 않더라도 잘 만든 서비스 같으니 만들고 있는 서비스에도 참고해보자는 의미였다. 역시 잘만든 서비스라 그런지 구성원 중 한명이 먼저 개인적으로 써보기 시작했다. 그와 동시에 회사에서도 여러가지 이벤트가 있었다. 초기 투자를 조금 받았고, 같이 일하는 사무실이 생겼고, 만들던 서비스에도 큰 변화가 있었다.

그 밖에 전직장에서의 [경험](https://hyungyunlim.github.io/2017-06-20/how-to-adopt-slack)이 바탕이 되었다. 전 직장에서 사내 메신저를 스카이프에서 슬랙으로 변경하는 역할을 맡아서 이를 주도적으로 진행했는데 이 과정에서 배운게 많았다. 우선 좋은 툴을 적절히 도입하면 내부의 조직 문화에까지 영향을 준다.  무엇보다 뼈저리게 느낀 점은 조직이 커지면 커질수록 새로운 서비스를 도입하게 어렵다는 점이다.

그래서 일단 회사의 어드민 정보가 정리되어 있는 포털과 같은 페이지를 만들어 보기로 했다.

#### 팀 포탈(Team Portal)
일단 각종 회사 관련 정보들을 취합할 곳이 필요했다. 이전에는 구글드라이브의 어드민(Admin)이라는 폴더에 각종 정보를 모아놓거나 스프레드시트로 정리를 했다. 해당 문서를 매번 찾아서 매번 업데이트를 하는 것도 일이지만 업데이트를 거듭하다보면 문서가 복잡해져서 가독성이 떨어졌다. 그래서 아래와 같이 정리 했다.
<figure>
  <img data-action="zoom" src='{{ "/images/notion_portal.png" | relative_url }}' alt='notion'>
  <figcaption>이미지블팀의 노션 메인 페이지</figcaption>
</figure>
가장 왼쪽에는 회사의 비전, 목표, 근무 규정 및 장소 등의 기본정보를 넣고, 가운데에서는 내부에서 돌아가는 주요 영역들의 프로젝트에 대한 링크, 가장 오른쪽에는 주변 맛집 및 카페를 정리하고 있다. 가장 하단에는 현재 입주해있는 창조경제혁신센터의 미팅룸 예약링크를 북마크로 넣어둬 언제든지 편하게 접근할 수 있도록 했다.

#### 서비스 스펙문서(Spec Documents)
이후 스펙 문서를 [노션](https://www.notion.so/?r=c28c8f6d88af411986aa657212492b58)으로 제일 먼저 옮겼다. 스펙문서는 보통 제품이나 서비스의 기능별 특징들을 상세하게 작성해놓은 문서를 의미하는데 테크기반의 서비스를 개발 및 운영하는 곳에서 가장 중요한 문서 중 하나다. 그동안 구글 문서에 스펙을 정리했다. 처음 한 문서에 통합적으로 정리하다가 길어지고 복잡해져 기능별로 문서를 나눠 정리 했다. 스펙문서를 자주 다뤄본 담당자는 알겠지만 지속적으로 문서가 업데이트 되지 않으면 결국 다시 써야한다. 이를 개선하려면 접근성이 좋고 언제든지 업데이트를 할 수 있어야 한다. 구글 문서가 기능상으로는 워드의 대체제로 여겨질만큼 기능이 많고, 교정 모드 등의 협업 기능도 있지만 가장 큰 약점은 구글드라이브 내에 존재 한다는 것. 무엇보다 구글드라이브는 태생이 정리가 쉽지 않다. 하지만 노션에서는 개별문서를 폴더 안에 정리해놓으면 아래와 같이 체계화된 간단한 위키를 만들 수 있다.
<figure>
  <img data-action="zoom" src='{{ "/images/notion_spec.png" | relative_url }}' alt='notion'>
  <figcaption>노션을 통한 내부 스펙 문서 관리</figcaption>
</figure>
보통 스펙문서에는 프로토타입이 포함되는 경우가 많기 때문에 노션으로 문서의 내용까지 완전히 갈아탄 것이아니라 문서 내부에 구글슬라이드나 프로토타입 관련 툴을 임베드(Embed)하는 방식으로 정리했다. 작은 변화지만 큰 차이가 있었다. 일단 찾기가 쉬워졌고, 변경이 쉽고, 업데이트(Update) 부분에 일목요연하게 변경된 내용이 기록되기때문에 훨씬 더 살아있는 문서에 가까워졌다.
<figure>
  <img data-action="zoom" src='{{ "/images/notion_update.png" | relative_url }}' alt='notion'>
  <figcaption>업데이트 이력을 통해 특정 페이지의 히스토리 확인가능</figcaption>
</figure>
#### 세일즈 및 각종 미팅 관리 (CRM)
<figure>
  <img data-action="zoom" src='{{ "/images/notion-use-case-screenshot-database.gif" | relative_url }}' alt='notion'>
  <figcaption>데이터베이스로 활용할 수 있는 노션</figcaption>
</figure>
개인적으로 회사의 가장 중요한 데이터 중 하나가 고객 관련 데이터다. 이전 직장에서는 세일즈와 관련 고객 데이터를 기록하기위해 상당 비용을 투자해 세일즈포스라는 솔루션을 내부적으로 사용했고, 시중에는 스트릭(Streak) 등 다양한 CRM 솔루션이 존재한다. 노션에서는 아래와 같이 스프레드시트에 데이터테이블이 연동된 [에어테이블(Airtable)](https://airtable.com/)과 비슷한 기능을 지원하는데 기본적인 CRM 솔루션으로 활용하기에 손색이 없다.
<figure>
  <img data-action="zoom" src='{{ "/images/notion_crm.png" | relative_url }}' alt='notion'>
  <figcaption>노션에서 사용가능한 스프레드시트</figcaption>
</figure>
해당 문서는 잠재적인 고객사들과 미팅내용을 정리한 문서다. 미팅에 관한 회사명, 카테고리 등의 개괄적인 내용은 스프레드시트 형태로 정리된 문서로 확인할 수 있고, 이렇게 입력된 한줄한줄은 하나의 데이터베이스로 팝업으로 열어서 미팅 내용을 정리하는 방식으로 기록하고 있다. 설명하면 복잡해 보이는데 막상 사용해보면 쉽게 익숙해진다.
<figure>
  <img data-action="zoom" src='{{ "/images/notion_crm_popup.png" | relative_url }}' alt='notion'>
  <figcaption>스프레드시트 형식의 데이터베이스 팝업</figcaption>
</figure>
이밖에 구성원들이 익숙해질수록 활용 방법은 다양해지고 있다. 개인적으로 사용할 수 있는 공간과 팀 공간(Workspace)이 나뉘어져 있어 개인적인 노트 및 업무관리 툴로 사용하기도 한다. 사용한 지 얼마되지 않았지만 벌써 업무용 필수 서비스로 자리 잡았다.

### 노션의 미래 (The Future of Notion)
앞서 언급 했지만 노션은 홈페이지에 구글독스, 지라, 트렐로, 드롭박스 페이퍼, 컨플루언스, 에어테이블의 솔루션을 하나로 통합할 수 있는 툴로 설명한다. 팀내 노션을 도입하고 내부에 있는 여러 문서들을 정리하면서 정말 그럴 수 있겠다는 생각이 들었다. 이제 더 이상 구글독스, 트렐로 등을 거의 사용하지 않는다. 아직 완성도 있는 제품들을 백프로 대체하기에는 부족한 부분들이 보이지만 여느 스타트업들처럼 빠르게 유저들이 원하는 바를 반영해서 서비스를 개선하고 있다.
<figure>
  <img data-action="zoom" src='{{ "/images/notion_slack.png" | relative_url }}' alt='notion'>
  <figcaption>노션 웹사이트에 있는 슬랙 관련 설명 문서</figcaption>
</figure>
노션은 슬랙의 빈자리를 채워준다. 우리 팀은 사내에서 슬랙을 메신저로 사용하는데 백번 공감한다. 슬랙은 일종의 사내 메신저로 많은 정보가 물처럼 흐른다. 하지만 문서들을 통합하는 위키로 사용하기에 적합하지 않다. 아이러니하게도 슬랙의 디자인팀이 노션을 사용한다고 웹사이트에 명시되어 있다. 점점 팀 내에서 [노션](https://www.notion.so/?r=c28c8f6d88af411986aa657212492b58)에 정리한 문서를 슬랙에 공유하는 사례가 빈번해졌고, 문서화가 필요한 부분은 노션을 통해서 작성한다. 이런 부분들 때문에 미래는 밝아보이고 점점 더 쓰는 곳이 급속히 늘어가리라 생각한다.

여담이지만 [이미지블(IMGIBBLE)](https://www.imgibble.com/?utm_source=Blog&utm_medium=Jun&utm_campaign=Post)도 한두달 내에 런칭을 앞두고 있는데 노션처럼 꾸준히 개발하고, 개선해서 널리 쓰일 수 있는 서비스가 되었으면 좋겠다.
