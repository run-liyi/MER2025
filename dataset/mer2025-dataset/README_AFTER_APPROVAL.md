# 📦 MER2025 Dataset Download Instructions

Congratulations!  
Your access request for the **MER2025 Dataset** has been approved.

You can download the dataset using the following methods:

---

## 1. Download via Hugging Face Hub (Recommended)

Use the Hugging Face CLI to download the dataset:

```bash
pip install huggingface_hub

huggingface-cli download \
  MERChallenge/MER2025 \
  --token hf_xxxxxxxxxxxxxxxxxxxxxxxxxxx \
  --repo-type dataset \
  --resume-download \
  --local-dir /your/local/path/
```

### 📝 Parameter Explanation:
- `token`: Your Hugging Face access token, required for accessing gated/private datasets.
- `repo-type dataset`: Specifies that you are downloading a dataset (not a model).
- `resume-download`: Enables resuming downloads if interrupted.
- `--local-dir`: Specifies the local directory to save the dataset.

🔗 Dataset URL: [https://huggingface.co/datasets/MERChallenge/MER2025](https://huggingface.co/datasets/MERChallenge/MER2025)

> If you encounter access issues, ensure that you are logged into your Hugging Face account and that your access request has been approved.

---

## 2. Download via Mirror Site (Optional)

If you experience network issues when accessing Hugging Face, you can use the official mirror:

```bash
export HF_ENDPOINT=https://hf-mirror.com

huggingface-cli download \
  MERChallenge/MER2025 \
  --token hf_xxxxxxxxxxxxxxxxxxxxxxxxxxx \
  --repo-type dataset \
  --resume-download \
  --local-dir /your/local/path/
```

After downloading, the `openface_face` folder will contain the following split archive files:

```
openface_face_split.z01   
openface_face_split.z02
... ...
openface_face_split.z09
openface_face_split.zip
```

To extract the contents, we recommend using **7-Zip**:

```bash
7z x openface_face_split.zip
```

The same procedure applies to the `video` folder if it also contains split archive files.

---

## 3. Download via Baidu Netdisk (Optional)

For users in regions with limited access to Hugging Face, we also provide an alternative download via **Baidu Netdisk**:

* **Baidu Netdisk Link**: [https://pan.baidu.com/s/1UiMkCWgFoqehZ4AgK8cHzg?pwd=zewf](https://pan.baidu.com/s/1UiMkCWgFoqehZ4AgK8cHzg?pwd=zewf)

> ⚠️ **Note:** The dataset content is identical between Hugging Face and Baidu Netdisk.

### ✅ Verify File Integrity with MD5

Since the files are large, we recommend verifying their integrity using MD5 checksums after downloading:

| File Name           | MD5 Checksum                       |
| ------------------- | ---------------------------------- |
| `openface_face.zip` | `eca0f3553aec879abc78094863f81d91` |
| `audio.zip`         | `282b1bf3df7abcb63da919edbcc1a37a` |
| `video.zip`         | `134b9f29895b223a5df2867dabb8efe2` |

### 🧪 How to Check MD5

* **On Windows:**

```cmd
certutil -hashfile openface_face.zip MD5
```

* **On Ubuntu / Linux:**

```bash
md5sum openface_face.zip
```

Repeat the command for `audio.zip` and `video.zip` to verify all files.


---

# 📋 Important Reminders

- Please comply with the [LICENSE](https://github.com/zeroQiaoba/MERTools/blob/master/MER2025/LICENSE) and the EULA terms at all times.
- Redistribution, modification, or public release of the dataset without permission is strictly prohibited.
- For any questions, please contact us:  
  📧 merchallenge.contact@gmail.com

---

# 📢 Thank You for Your Support!

We wish you great success in your research with the MER2025 Dataset!

---
