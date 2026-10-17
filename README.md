# prompt_generator.py
import json

def generate_video_prompts(story_text):
    """
    [MVP Version]
    這個模組未來會串接 OpenAI API，
    自動將使用者的短故事拆解成給 Sora 或 Runway 的分鏡提示詞。
    """
    print(f"🎬 正在分析故事內容: '{story_text}'...\n")
    
    # 這裡先使用預設的結構做示範 (Mock data)
    scenes = [
        {"scene": 1, "prompt": "Wide shot, cinematic lighting, establishing the main character in a futuristic cyber city."},
        {"scene": 2, "prompt": "Close-up, the character looking surprised, glowing neon lights reflecting in their eyes."},
        {"scene": 3, "prompt": "Action shot, character running through a rainy alleyway, 8k resolution, photorealistic."}
    ]
    
    print("✅ 成功生成 AI 影片分鏡提示詞 (Prompts):")
    for s in scenes:
        print(f"👉 分鏡 {s['scene']}: {s['prompt']}")
        
    return scenes

if __name__ == "__main__":
    # 測試執行
    sample_story = "一個穿著太空衣的女孩在賽博龐克城市裡奔跑。"
    generate_video_prompts(sample_story)
