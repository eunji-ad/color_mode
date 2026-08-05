<div align="center">
  <h1>MICHELAN GOLF Clone Project</h1>
  <p><strong>미켈란사이트의 후기 게시판, 공지사항 클론</strong></p>
  <p>실제 서비스의 UI/UX를 구현하고, 컴포넌트 기반 개발과 Mock API를 활용한 CRUD 기능을 경험하기 위해 제작한 프로젝트입니다.</p>
</div>

---

## Features
<details>
  <ul>
    <li>Notice : 공지사항 목록 / 상세 조회</li>
  <li>Review : 리뷰 CRUD
  <li>Image Upload : 리뷰 이미지 업로드
  <li>Rating : 별점 등록
  <li>Password : 비밀번호 팝업으로 검증 후 수정/삭제
  <li>Pagination : 목록 카드 리스트 페이지네이션
  <li>Responsive : 반응형 레이아웃
  <li>Mock API : MSW 기반 API Mocking
  <li>Input : React Hook Form 기반 입력 상태 관리
  </ul>
</details>


--- 

## Tech Stack 
<details> 
  <ul>
    <li>Framework: Next.js  <img src="https://img.shields.io/badge/Next.js-16-000000?style=flat-square&logo=next.js"/></li>
    <li>Library: React  <img src="https://img.shields.io/badge/React-19-61DAFB?style=flat-square&logo=react"/></li>
    <li>Language: TypeScript  <img src="https://img.shields.io/badge/TypeScript-5-3178C6?style=flat-square&logo=typescript&logoColor=white"/></li> 
    <li>Styling: Tailwind CSS <img src="https://img.shields.io/badge/TailwindCSS-4-06B6D4?style=flat-square&logo=tailwindcss"/></li> 
    <li>State/Form Management: React Hook Form  <img src="https://img.shields.io/badge/ReactHookForm-7-EC5990?style=flat-square&logo=reacthookform"/></li> 
    <li>Validation: Zod  <img src="https://img.shields.io/badge/Zod-4-3E67B1?style=flat-square"/></li> 
    <li>Architecture: Feature-Sliced Design (FSD)  <img src="https://img.shields.io/badge/Architecture-FSD-6C63FF?style=flat-square"/></li> 
    <li>Mock API: MSW  <img src="https://img.shields.io/badge/MSW-2-FF6A33?style=flat-square"/></li> 
    <li>Date Utility: date-fns  <img src="https://img.shields.io/badge/date--fns-770C56?style=flat-square&logo=date-fns&logoColor=white"/></li>  
  </ul> 
</details> 

---


<details>
<summary><strong>프로젝트 구조</strong></summary>

```
src/
├── app/                   # Next.js App Router (globals.css, layout, loading, not-found, error, pages)
│   ├── (List)/            # 페이지 목록
│   │   ├── notice/          > 공통 layout사용
│   │   ├── review/          > Route Group 관리
│   │   └── layout           
│   ├── example/           # 컴포넌트 확인 (예제 페이지)
│   ├── notice/            # 공지사항 상세 페이지
│   └── review/            # 후기 게시판 상세 페이지, 등록 페이지
│       ├── view/[id]        > Dynamic Segment 사용
│       └── write/[[...id]]  > Optional Catch-all Segment 사용 (id존재: 수정하기/ id미존재: 등록하기)    
│
├── features/              # 사용자 기능 UI 조합
├── public/                # 공통 소스들(파일, 폰트, 이미지)
├── schema/                # 후기 등록 Input 입력 값 검증 규칙 정의
├── shared/
│   └── ui/
│       ├── atoms/         # 기본 컴포넌트 (Text, Checkbox 등)
│       ├── config/        # 공통으로 사용하는 상수
│       └── molecules/     # atoms 조합
├── src/
│   ├── mocks/             # MSW 핸들러 + 테스트 데이터
│   └── types/             # 공통 타입 및 인터페이스 관리
└── widgets/               # 페이지 단위 UI 조합

```

</details>

---

## Component

재사용 가능한 공통 컴포넌트를 제작했습니다.

- Button
- BreadCrumb
- CheckBox
- Icon
- Input
- ImageUpload
- Logo
- Pagination
- Popup
- PostMenu
- Rating
- Textarea
- ToolTip

---

## Getting Started

```bash
git clone <repository>

pnpm install

pnpm run dev

```
