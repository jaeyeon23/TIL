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

---

## WSL2 + Ubuntu LTS 구성 (Windows)

### WSL 소개
- Windows Subsystem for Linux의 약자로 윈도우에서 리눅스를 사용할 수 있도록 만들어주는 기술

### WSL 사용 설정 및 Ubuntu 설치
- DISM 명령어
- 윈도우 이미지와 관련된 조작을 위한 커맨드 명령어

> WSL 활성화
```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart

```
> 가상머신 플랫폼 활성화
```
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

- Microsoft Store에서 Ubuntu LTS 설치
> PowerShell에서 확인
```
wsl -l -v
```

### WSL2 사용 설정  
https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi
> 해당 파일 설치 후 아래 명령어를 통해 버전 변경
```
wsl --set-version Ubuntu-20.04 2
```
> wsl 기본 버전 2버전으로 변경
```
wsl --set-default-version 2
```
