# AfetLLM: Domain-Specific Large Language Model for Disaster Management 

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/133ItwK44O0RjQETDDCjaxvy8W6JJksA4?usp=sharing)

AfetLLM is a Large Language Model (LLM) specifically fine-tuned to provide accurate and procedural responses (SOP) during earthquake and emergency disaster scenarios.

## Project Overview
This project fine-tunes the **Qwen2-1.5B-Instruct** base model using **QLoRA (4-bit)**. The model is specialized in disaster management terminology, search-and-rescue strategies, and emergency coordination protocols.

### Key Technical Details:
- **Base Model:** Qwen2-1.5B (Alibaba Research)
- **Method:** LoRA (Low-Rank Adaptation)
- **Quantization:** 4-bit NormalFloat (NF4)
- **Hardware:** Google Colab (NVIDIA Tesla T4 GPU)
- **Language:** Turkish (Target Domain)


## Repository Structure
- `Afet_LLM_Qwen2_QLoRA.ipynb`: Jupyter notebook containing the full training and evaluation pipeline.
- `afet_llm_final_dataset.jsonl`: Specialized dataset containing disaster scenarios and SOPs.
- `adapter_config.json` & `adapter_model.safetensors`: The trained LoRA weights (adapters).

## Sample Inference (Turkish)
Since the model is specialized for Turkish disaster response, here is a sample output:

**Instruction (Talimat):** İletişimin kesildiği bir ortamda yaralı tahliyesi nasıl planlanmalıdır?

**Input (Girdi):** GSM ve telsiz yok, artçı sarsıntılar devam ediyor.

**AfetLLM Output (Yanıt):** "Öncelikle fiziksel güvenlik alanı oluşturulmalı, artçı sarsıntı riskine karşı çevre emniyeti alınmalıdır. İletişim altyapısı çökmüşse, önceden belirlenen acil durum toplanma noktaları ve kurye usulü fiziksel haberleşme protokolü devreye alınarak yaralıların triyaj önceliğine göre tahliyesi planlanmalıdır."
