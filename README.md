# LRC-models

LRC 데스크톱 앱이 처음 실행될 때 내려받는 모델 파일 모음입니다. 파일은 [Releases](../../releases)에 있습니다.

## 포함 파일과 출처

| 파일 | 원본 | 라이선스 | 변경 내용 |
|---|---|---|---|
| `w2v2_large_960h.onnx` 및 `w2v2_large_960h__*.json` | [facebook/wav2vec2-large-960h](https://huggingface.co/facebook/wav2vec2-large-960h) | Apache-2.0 | PyTorch 가중치를 ONNX(fp32)로 형식 변환. 출력에 `last_hidden_state` 추가. 가중치 값은 변경하지 않음 |
| `w2v2_lv60_espeak.onnx` 및 `w2v2_lv60_espeak__*.json` | [facebook/wav2vec2-lv-60-espeak-cv-ft](https://huggingface.co/facebook/wav2vec2-lv-60-espeak-cv-ft) | Apache-2.0 | PyTorch 가중치를 ONNX(fp32)로 형식 변환. 가중치 값은 변경하지 않음 |
| `kokoro__misaki__us_gold.json`, `kokoro__misaki__us_silver.json` | [hexgrad/misaki](https://github.com/hexgrad/misaki) 0.9.4 | Apache-2.0 | 변경 없음 |

Kokoro 음성 모델(`model.onnx`, `voices/af_heart.bin`)은 이 저장소에 두지 않고, 앱이 [onnx-community/Kokoro-82M-v1.0-ONNX](https://huggingface.co/onnx-community/Kokoro-82M-v1.0-ONNX)(Apache-2.0)에서 고정된 리비전으로 직접 내려받습니다.

파일 이름의 `__`는 앱 안 폴더 경로의 `/`를 뜻합니다. 각 파일의 sha256은 Release 노트에 있습니다.

Apache License 2.0 전문: https://www.apache.org/licenses/LICENSE-2.0
