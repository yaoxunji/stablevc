# stablevc

StableVC: Flexible Stylistic Voice Conversion in Latent Space Driven by Natural Language Prompts

Zero-shot voice conversion (VC) aims to transfer the timbre from the source speaker to an arbitrary unseen speaker while preserving the original linguistic content. Despite recent advancements in zero-shot VC using language model-based or diffusion-based approaches, several challenges remain: 1) current approaches primarily focus on adapting timbre from unseen speakers and are unable to transfer style and timbre to different unseen speakers independently; 2) these approaches often suffer from slower inference speeds due to the autoregressive modeling methods or the need for numerous sampling steps; 3) the quality and similarity of the converted samples are still not fully satisfactory.To address these challenges, we propose a Stable controllable zero-shot VC approach named StableVC, which aims to transfer timbre and style from source speech to different unseen target speakers. Specifically, we decompose speech into linguistic content, timbre, and style, and then employ a conditional flow matching module to reconstruct the high-quality mel-spectrogram based on these decomposed features. To effectively capture timbre and style in a zero-shot manner, we introduce a novel dual attention mechanism with an adaptive gate, rather than using conventional feature concatenation. With this non-autoregressive design, StableVC can efficiently capture the intricate timbre and style from different unseen speakers and generate high-quality speech significantly faster than real-time. Experiments demonstrate that our proposed StableVC outperforms state-of-the-art baseline systems in zero-shot VC and achieves flexible control over timbre and style from different unseen speakers. Moreover, StableVC offers approximately 25x and 1.65x faster sampling compared to autoregressive and diffusion-based baselines.