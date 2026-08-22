# 국민체육센터팀 2026 위험성평가 사후교육

의왕도시공사 국민체육센터팀 2026년 위험성평가 사후교육 웹페이지. 단일 HTML 파일로 되어 있어 빌드 없이 정적으로 배포됩니다.

## 현재 상태: 미리보기 모드

이수 기록(이름/부서/서명)이 서버에 저장되지 않습니다. 실제 DB(Supabase) 연동을 활성화하려면 별도로 요청해주세요.

## 관리자 페이지

`/admin/`에서 7개 팀의 전체 이수확인서를 조회·검색·인쇄할 수 있습니다. 접근 시 비밀번호를 입력해야 하며, 기본값은 `admin/index.html` 상단의 `ADMIN_PASSWORD` 값입니다(필요 시 직접 수정). 목록에서 팀/이름/부서로 필터링한 뒤 "필터 결과 전체 인쇄" 또는 개별 행의 "인쇄" 버튼을 누르면 브라우저 인쇄 대화상자가 열리며, 여기서 PDF로 저장할 수 있습니다.

이 페이지는 DB에서 전체 이수 기록(서명 이미지 포함)을 읽어오므로, 링크를 팀 페이지에는 노출하지 않았습니다. URL과 비밀번호는 관리자만 공유해주세요.

## 배포 방법

### 1. GitHub 저장소 만들기

```bash
cd "C:\Users\user\Desktop\gukmin-safety-training-2026"
gh repo create gukmin-safety-training-2026 --private --source=. --remote=origin --push
```

`gh` CLI가 없다면 GitHub 웹사이트(https://github.com/new)에서 저장소를 만든 뒤:

```bash
git remote add origin https://github.com/<your-username>/gukmin-safety-training-2026.git
git branch -M main
git push -u origin main
```

### 2. Vercel에 배포하기

https://vercel.com/new 에서 방금 만든 GitHub 저장소를 Import 하면 별도 설정 없이 바로 배포됩니다 (정적 HTML이라 빌드 명령/출력 폴더 설정 불필요).

또는 Vercel CLI가 있다면:

```bash
vercel --prod
```
