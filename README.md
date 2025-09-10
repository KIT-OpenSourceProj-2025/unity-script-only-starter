# Unity Script-Only Classroom Starter

이 리포지토리는 **Unity 프로젝트에서 C# 스크립트만 제출**하도록 설계된 템플릿입니다.
씬(.unity), 프리팹(.prefab), 이미지/오디오 등 대용량 에셋은 **커밋 금지**입니다.

## 제출 규칙 (필수)
- `Assets/Scripts/` 폴더에 있는 `*.cs`, `*.asmdef`, 그리고 해당 `.meta`만 커밋하세요.
- 대용량/바이너리 파일(이미지, 오디오, 프리팹, 씬 등) 금지.
- 패키지 재현성을 위해 `Packages/manifest.json`, `Packages/packages-lock.json`, `ProjectSettings/ProjectVersion.txt`는 포함됩니다.

## Unity 설정 권장
- **Edit → Project Settings → Editor**
  - Version Control: **Visible Meta Files**
  - Asset Serialization: **Force Text**

## 로컬 개발 흐름
```bash
git clone <repo-url>
# 작업 후
git add .
git commit -m "feat: add solution scripts"
git push
```

## GitHub Actions
이 리포지토리는 **대용량/금지 확장자**를 커밋하면 CI가 실패하도록 구성되어 있습니다.
자세한 정책은 `.github/workflows/block-binaries.yml`을 확인하세요.
