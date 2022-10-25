# 사전 세팅

## Homebrew 설치 및 사용법(mac OS)

### Homebrew 소개
- mac os 운영체제의 패키지 관리자
- 주로 CLI 도구나 시스템 패키지 설치에 사용

### Homebrew 기본 사용 방법
- 패키지 검색
```
brew search TEXT|/REGEX
```
- 패키지 상세 정보 확인
```
brew info [FORMULA|CASK...]
```
- 패키지 설치 
```
brew install FORMULA|CASK...
```
- 패키지 업그레이드
```
brew upgrade [FORMULA|CASK...]
```
- 패키지 삭제
```
brew uninstall FORMULA|CASK...
```
- Homebrew 업데이트 및 포뮬라 정보 갱신 (Homebrew 자신을 최신 버전으로 업데이트하고, Homebrew가 제공하는 최신 패키지 정보를 가져온다)
```
brew update
```
- Homebrew Cask
> Homebrew를 확장하여 GUI 어플리케이션 설치까지 지원
> 기존 Homebrew 명령어에 '--cask' 옵션 사용

