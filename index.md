# <center> Any-to-Many Voice Conversion with Location-Relative Sequence-to-Sequence Modeling</center>

<center> Songxiang Liu, Yuewen Cao, Disong Wang, Xixin Wu, Xunying Liu and Helen Meng</center>  


<center>Human-Computer Communications Laboratory (HCCL), The Chinese University of Hong Kong</center>  

## Abstract
This paper proposes an any-to-many location-relative, sequence-to-sequence (seq2seq) based, non-parallel voice conversion approach. 
In this approach, we combine a bottle-neck feature extractor (BNE) with a seq2seq based synthesis module. During the training stage, 
an encoder-decoder based hybrid connectionist-temporal-classification-attention (CTC-attention) phoneme recognizer is trained, 
whose encoder has a bottle-neck layer. A BNE is obtained from the phoneme recognizer and is utilized to extract speaker-independent, 
dense and rich linguistic representations from spectral features. Then a multi-speaker location-relative attention based seq2seq synthesis 
model is trained to reconstruct spectral features from the bottle-neck features, conditioning on speaker representations for speaker 
identity control in the generated speech. To mitigate the difficulties of using seq2seq based models to align long sequences, we down-sample 
the input spectral feature along the temporal dimension and equip the synthesis model with a discretized mixture of logistic (MoL) attention mechanism. 
Since the phoneme recognizer is trained with large speech recognition data corpus, the proposed approach can conduct any-to-many voice conversion.
Objective and subjective evaluations shows that the proposed any-to-many approach has superior voice conversion performance in terms of both 
naturalness and speaker similarity. Ablation studies are conducted to confirm the effectiveness of feature selection and model design strategies 
in the proposed approach. The proposed VC approach can readily be extended to support any-to-any VC (also known as one/few-shot VC), and achieve 
high performance according to objective and subjective evaluations.

Paper link: [arXiv](https://arxiv.org/abs/2009.02725)  
[Source Codes](https://github.com/liusongxiang/ppg-vc)  

## Any-to-Many VC Demo (10 utterances randomly chosen from the test set)
### Female (clb) to Male (bdl)

| **Source** | **Target** | **BNE-Seq2seqMoL (Proposed)** | **Seq2seqPR-DurIAN (Proposed)** | **PPG-VC** | **NonParaSeq2seq-VC** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| <audio src="wavs/recordings/clb/arctic_a0015.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0015.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/clb_to_bdl/clb_arctic_a0015_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_clb_to_bdl/clb_arctic_a0015_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/clb-to-bdl/clb_arctic_a0015_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/clb-to-bdl/clb_arctic_a0015_to_bdl.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0080.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0080.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/clb_to_bdl/clb_arctic_a0080_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_clb_to_bdl/clb_arctic_a0080_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/clb-to-bdl/clb_arctic_a0080_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/clb-to-bdl/clb_arctic_a0080_to_bdl.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0101.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0101.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/clb_to_bdl/clb_arctic_a0101_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_clb_to_bdl/clb_arctic_a0101_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/clb-to-bdl/clb_arctic_a0101_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/clb-to-bdl/clb_arctic_a0101_to_bdl.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0135.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0135.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/clb_to_bdl/clb_arctic_a0135_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_clb_to_bdl/clb_arctic_a0135_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/clb-to-bdl/clb_arctic_a0135_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/clb-to-bdl/clb_arctic_a0135_to_bdl.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0179.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0179.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/clb_to_bdl/clb_arctic_a0179_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_clb_to_bdl/clb_arctic_a0179_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/clb-to-bdl/clb_arctic_a0179_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/clb-to-bdl/clb_arctic_a0179_to_bdl.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0197.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0197.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/clb_to_bdl/clb_arctic_a0197_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_clb_to_bdl/clb_arctic_a0197_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/clb-to-bdl/clb_arctic_a0197_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/clb-to-bdl/clb_arctic_a0197_to_bdl.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0209.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0209.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/clb_to_bdl/clb_arctic_a0209_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_clb_to_bdl/clb_arctic_a0209_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/clb-to-bdl/clb_arctic_a0209_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/clb-to-bdl/clb_arctic_a0209_to_bdl.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0247.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0247.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/clb_to_bdl/clb_arctic_a0247_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_clb_to_bdl/clb_arctic_a0247_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/clb-to-bdl/clb_arctic_a0247_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/clb-to-bdl/clb_arctic_a0247_to_bdl.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0316.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0316.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/clb_to_bdl/clb_arctic_a0316_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_clb_to_bdl/clb_arctic_a0316_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/clb-to-bdl/clb_arctic_a0316_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/clb-to-bdl/clb_arctic_a0316_to_bdl.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0354.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0354.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/clb_to_bdl/clb_arctic_a0354_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_clb_to_bdl/clb_arctic_a0354_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/clb-to-bdl/clb_arctic_a0354_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/clb-to-bdl/clb_arctic_a0354_to_bdl.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |

### Female (clb) to Female (slt)

| **Source** | **Target** | **BNE-Seq2seqMoL (Proposed)** | **Seq2seqPR-DurIAN (Proposed)** | **PPG-VC** | **NonParaSeq2seq-VC** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| <audio src="wavs/recordings/clb/arctic_a0015.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0015.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/clb_to_slt/clb_arctic_a0015_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_clb_to_slt/clb_arctic_a0015_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/clb-to-slt/clb_arctic_a0015_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/clb-to-slt/clb_arctic_a0015_to_slt.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0080.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0080.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/clb_to_slt/clb_arctic_a0080_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_clb_to_slt/clb_arctic_a0080_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/clb-to-slt/clb_arctic_a0080_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/clb-to-slt/clb_arctic_a0080_to_slt.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0101.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0101.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/clb_to_slt/clb_arctic_a0101_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_clb_to_slt/clb_arctic_a0101_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/clb-to-slt/clb_arctic_a0101_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/clb-to-slt/clb_arctic_a0101_to_slt.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0135.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0135.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/clb_to_slt/clb_arctic_a0135_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_clb_to_slt/clb_arctic_a0135_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/clb-to-slt/clb_arctic_a0135_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/clb-to-slt/clb_arctic_a0135_to_slt.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0179.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0179.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/clb_to_slt/clb_arctic_a0179_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_clb_to_slt/clb_arctic_a0179_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/clb-to-slt/clb_arctic_a0179_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/clb-to-slt/clb_arctic_a0179_to_slt.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0197.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0197.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/clb_to_slt/clb_arctic_a0197_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_clb_to_slt/clb_arctic_a0197_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/clb-to-slt/clb_arctic_a0197_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/clb-to-slt/clb_arctic_a0197_to_slt.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0209.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0209.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/clb_to_slt/clb_arctic_a0209_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_clb_to_slt/clb_arctic_a0209_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/clb-to-slt/clb_arctic_a0209_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/clb-to-slt/clb_arctic_a0209_to_slt.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0247.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0247.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/clb_to_slt/clb_arctic_a0247_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_clb_to_slt/clb_arctic_a0247_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/clb-to-slt/clb_arctic_a0247_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/clb-to-slt/clb_arctic_a0247_to_slt.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0316.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0316.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/clb_to_slt/clb_arctic_a0316_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_clb_to_slt/clb_arctic_a0316_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/clb-to-slt/clb_arctic_a0316_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/clb-to-slt/clb_arctic_a0316_to_slt.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0354.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0354.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/clb_to_slt/clb_arctic_a0354_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_clb_to_slt/clb_arctic_a0354_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/clb-to-slt/clb_arctic_a0354_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/clb-to-slt/clb_arctic_a0354_to_slt.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |

### Male (rms) to Male (bdl)

| **Source** | **Target** | **BNE-Seq2seqMoL (Proposed)** | **Seq2seqPR-DurIAN (Proposed)** | **PPG-VC** | **NonParaSeq2seq-VC** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| <audio src="wavs/recordings/rms/arctic_a0015.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0015.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/rms_to_bdl/rms_arctic_a0015_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_rms_to_bdl/rms_arctic_a0015_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/rms-to-bdl/rms_arctic_a0015_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/rms_to_bdl/rms_arctic_a0015_to_bdl.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0080.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0080.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/rms_to_bdl/rms_arctic_a0080_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_rms_to_bdl/rms_arctic_a0080_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/rms-to-bdl/rms_arctic_a0080_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/rms-to-bdl/rms_arctic_a0080_to_bdl.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0101.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0101.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/rms_to_bdl/rms_arctic_a0101_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_rms_to_bdl/rms_arctic_a0101_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/rms-to-bdl/rms_arctic_a0101_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/rms-to-bdl/rms_arctic_a0101_to_bdl.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0135.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0135.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/rms_to_bdl/rms_arctic_a0135_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_rms_to_bdl/rms_arctic_a0135_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/rms-to-bdl/rms_arctic_a0135_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/rms-to-bdl/rms_arctic_a0135_to_bdl.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0179.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0179.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/rms_to_bdl/rms_arctic_a0179_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_rms_to_bdl/rms_arctic_a0179_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/rms-to-bdl/rms_arctic_a0179_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/rms-to-bdl/rms_arctic_a0179_to_bdl.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0197.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0197.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/rms_to_bdl/rms_arctic_a0197_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_rms_to_bdl/rms_arctic_a0197_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/rms-to-bdl/rms_arctic_a0197_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/rms-to-bdl/rms_arctic_a0197_to_bdl.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0209.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0209.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/rms_to_bdl/rms_arctic_a0209_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_rms_to_bdl/rms_arctic_a0209_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/rms-to-bdl/rms_arctic_a0209_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/rms-to-bdl/rms_arctic_a0209_to_bdl.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0247.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0247.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/rms_to_bdl/rms_arctic_a0247_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_rms_to_bdl/rms_arctic_a0247_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/rms-to-bdl/rms_arctic_a0247_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/rms-to-bdl/rms_arctic_a0247_to_bdl.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0316.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0316.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/rms_to_bdl/rms_arctic_a0316_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_rms_to_bdl/rms_arctic_a0316_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/rms-to-bdl/rms_arctic_a0316_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/rms-to-bdl/rms_arctic_a0316_to_bdl.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0354.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0354.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/rms_to_bdl/rms_arctic_a0354_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_rms_to_bdl/rms_arctic_a0354_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/rms-to-bdl/rms_arctic_a0354_to_bdl.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/rms-to-bdl/rms_arctic_a0354_to_bdl.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |

### Male (rms) to  Female (slt)

| **Source** | **Target** | **BNE-Seq2seqMoL (Proposed)** | **Seq2seqPR-DurIAN (Proposed)** | **PPG-VC** | **NonParaSeq2seq-VC** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| <audio src="wavs/recordings/rms/arctic_a0015.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0015.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/rms_to_slt/rms_arctic_a0015_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_rms_to_slt/rms_arctic_a0015_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/rms-to-slt/rms_arctic_a0015_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/rms-to-slt/rms_arctic_a0015_to_slt.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0080.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0080.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/rms_to_slt/rms_arctic_a0080_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_rms_to_slt/rms_arctic_a0080_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/rms-to-slt/rms_arctic_a0080_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/rms-to-slt/rms_arctic_a0080_to_slt.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0101.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0101.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/rms_to_slt/rms_arctic_a0101_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_rms_to_slt/rms_arctic_a0101_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/rms-to-slt/rms_arctic_a0101_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/rms-to-slt/rms_arctic_a0101_to_slt.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0135.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0135.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/rms_to_slt/rms_arctic_a0135_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_rms_to_slt/rms_arctic_a0135_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/rms-to-slt/rms_arctic_a0135_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/rms-to-slt/rms_arctic_a0135_to_slt.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0179.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0179.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/rms_to_slt/rms_arctic_a0179_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_rms_to_slt/rms_arctic_a0179_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/rms-to-slt/rms_arctic_a0179_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/rms-to-slt/rms_arctic_a0179_to_slt.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0197.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0197.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/rms_to_slt/rms_arctic_a0197_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_rms_to_slt/rms_arctic_a0197_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/rms-to-slt/rms_arctic_a0197_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/rms-to-slt/rms_arctic_a0197_to_slt.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0209.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0209.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/rms_to_slt/rms_arctic_a0209_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_rms_to_slt/rms_arctic_a0209_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/rms-to-slt/rms_arctic_a0209_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/rms-to-slt/rms_arctic_a0209_to_slt.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0247.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0247.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/rms_to_slt/rms_arctic_a0247_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_rms_to_slt/rms_arctic_a0247_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/rms-to-slt/rms_arctic_a0247_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/rms-to-slt/rms_arctic_a0247_to_slt.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0316.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0316.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/rms_to_slt/rms_arctic_a0316_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_rms_to_slt/rms_arctic_a0316_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/rms-to-slt/rms_arctic_a0316_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/rms-to-slt/rms_arctic_a0316_to_slt.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0354.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0354.wav" controls preload></audio> | <audio src="wavs/any-to-many/bne-seq2seqmol/rms_to_slt/rms_arctic_a0354_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/seq2seqPR-durian/wav_rms_to_slt/rms_arctic_a0354_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/ppg-vc/rms-to-slt/rms_arctic_a0354_to_slt.wav" controls preload></audio> | <audio src="wavs/any-to-many/non-para-seq2seq/rms-to-slt/rms_arctic_a0354_to_slt.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- |

## Any-to-Any VC (also known as one-shot/few-shot VC) of the BNE-Seq2seqMoL approach Demo (10 utterances randomly chosen from the test set)

### Female (clb) to  Male (bdl)

| **Source** | **Target** | **BNE-Seq2seqMoL (Proposed)** |
| :--- | :--- | :--- |
| <audio src="wavs/recordings/clb/arctic_a0015.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0015.wav" controls preload></audio> | <audio src="wavs/any-to-any/clb_to_bdl/clb_arctic_a0015_to_bdl.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0080.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0080.wav" controls preload></audio> | <audio src="wavs/any-to-any/clb_to_bdl/clb_arctic_a0080_to_bdl.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0101.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0101.wav" controls preload></audio> | <audio src="wavs/any-to-any/clb_to_bdl/clb_arctic_a0101_to_bdl.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0135.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0135.wav" controls preload></audio> | <audio src="wavs/any-to-any/clb_to_bdl/clb_arctic_a0135_to_bdl.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0179.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0179.wav" controls preload></audio> | <audio src="wavs/any-to-any/clb_to_bdl/clb_arctic_a0179_to_bdl.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0197.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0197.wav" controls preload></audio> | <audio src="wavs/any-to-any/clb_to_bdl/clb_arctic_a0197_to_bdl.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0209.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0209.wav" controls preload></audio> | <audio src="wavs/any-to-any/clb_to_bdl/clb_arctic_a0209_to_bdl.wav" controls preload></audio> | 
| --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0247.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0247.wav" controls preload></audio> | <audio src="wavs/any-to-any/clb_to_bdl/clb_arctic_a0247_to_bdl.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0316.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0316.wav" controls preload></audio> | <audio src="wavs/any-to-any/clb_to_bdl/clb_arctic_a0316_to_bdl.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0354.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0354.wav" controls preload></audio> | <audio src="wavs/any-to-any/clb_to_bdl/clb_arctic_a0354_to_bdl.wav" controls preload></audio> | 
| --- | --- | --- |

### Female (clb) to  Female (slt)

| **Source** | **Target** | **BNE-Seq2seqMoL (Proposed)** |
| :--- | :--- | :--- |
| <audio src="wavs/recordings/clb/arctic_a0015.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0015.wav" controls preload></audio> | <audio src="wavs/any-to-any/clb_to_slt/clb_arctic_a0015_to_slt.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0080.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0080.wav" controls preload></audio> | <audio src="wavs/any-to-any/clb_to_slt/clb_arctic_a0080_to_slt.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0101.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0101.wav" controls preload></audio> | <audio src="wavs/any-to-any/clb_to_slt/clb_arctic_a0101_to_slt.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0135.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0135.wav" controls preload></audio> | <audio src="wavs/any-to-any/clb_to_slt/clb_arctic_a0135_to_slt.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0179.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0179.wav" controls preload></audio> | <audio src="wavs/any-to-any/clb_to_slt/clb_arctic_a0179_to_slt.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0197.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0197.wav" controls preload></audio> | <audio src="wavs/any-to-any/clb_to_slt/clb_arctic_a0197_to_slt.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0209.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0209.wav" controls preload></audio> | <audio src="wavs/any-to-any/clb_to_slt/clb_arctic_a0209_to_slt.wav" controls preload></audio> | 
| --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0247.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0247.wav" controls preload></audio> | <audio src="wavs/any-to-any/clb_to_slt/clb_arctic_a0247_to_slt.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0316.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0316.wav" controls preload></audio> | <audio src="wavs/any-to-any/clb_to_slt/clb_arctic_a0316_to_slt.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/clb/arctic_a0354.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0354.wav" controls preload></audio> | <audio src="wavs/any-to-any/clb_to_slt/clb_arctic_a0354_to_slt.wav" controls preload></audio> | 
| --- | --- | --- |

### Male (rms) to  Male (bdl)

| **Source** | **Target** | **BNE-Seq2seqMoL (Proposed)** |
| :--- | :--- | :--- |
| <audio src="wavs/recordings/rms/arctic_a0015.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0015.wav" controls preload></audio> | <audio src="wavs/any-to-any/rms_to_bdl/rms_arctic_a0015_to_bdl.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0080.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0080.wav" controls preload></audio> | <audio src="wavs/any-to-any/rms_to_bdl/rms_arctic_a0080_to_bdl.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0101.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0101.wav" controls preload></audio> | <audio src="wavs/any-to-any/rms_to_bdl/rms_arctic_a0101_to_bdl.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0135.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0135.wav" controls preload></audio> | <audio src="wavs/any-to-any/rms_to_bdl/rms_arctic_a0135_to_bdl.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0179.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0179.wav" controls preload></audio> | <audio src="wavs/any-to-any/rms_to_bdl/rms_arctic_a0179_to_bdl.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0197.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0197.wav" controls preload></audio> | <audio src="wavs/any-to-any/rms_to_bdl/rms_arctic_a0197_to_bdl.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0209.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0209.wav" controls preload></audio> | <audio src="wavs/any-to-any/rms_to_bdl/rms_arctic_a0209_to_bdl.wav" controls preload></audio> | 
| --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0247.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0247.wav" controls preload></audio> | <audio src="wavs/any-to-any/rms_to_bdl/rms_arctic_a0247_to_bdl.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0316.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0316.wav" controls preload></audio> | <audio src="wavs/any-to-any/rms_to_bdl/rms_arctic_a0316_to_bdl.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0354.wav" controls preload></audio> | <audio src="wavs/recordings/bdl/arctic_a0354.wav" controls preload></audio> | <audio src="wavs/any-to-any/rms_to_bdl/rms_arctic_a0354_to_bdl.wav" controls preload></audio> | 
| --- | --- | --- |

### Male (rms) to  Female (slt)

| **Source** | **Target** | **BNE-Seq2seqMoL (Proposed)** |
| :--- | :--- | :--- |
| <audio src="wavs/recordings/rms/arctic_a0015.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0015.wav" controls preload></audio> | <audio src="wavs/any-to-any/rms_to_slt/rms_arctic_a0015_to_slt.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0080.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0080.wav" controls preload></audio> | <audio src="wavs/any-to-any/rms_to_slt/rms_arctic_a0080_to_slt.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0101.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0101.wav" controls preload></audio> | <audio src="wavs/any-to-any/rms_to_slt/rms_arctic_a0101_to_slt.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0135.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0135.wav" controls preload></audio> | <audio src="wavs/any-to-any/rms_to_slt/rms_arctic_a0135_to_slt.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0179.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0179.wav" controls preload></audio> | <audio src="wavs/any-to-any/rms_to_slt/rms_arctic_a0179_to_slt.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0197.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0197.wav" controls preload></audio> | <audio src="wavs/any-to-any/rms_to_slt/rms_arctic_a0197_to_slt.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0209.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0209.wav" controls preload></audio> | <audio src="wavs/any-to-any/rms_to_slt/rms_arctic_a0209_to_slt.wav" controls preload></audio> | 
| --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0247.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0247.wav" controls preload></audio> | <audio src="wavs/any-to-any/rms_to_slt/rms_arctic_a0247_to_slt.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0316.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0316.wav" controls preload></audio> | <audio src="wavs/any-to-any/rms_to_slt/rms_arctic_a0316_to_slt.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/recordings/rms/arctic_a0354.wav" controls preload></audio> | <audio src="wavs/recordings/slt/arctic_a0354.wav" controls preload></audio> | <audio src="wavs/any-to-any/rms_to_slt/rms_arctic_a0354_to_slt.wav" controls preload></audio> | 
| --- | --- | --- |

## Previous Demo Pages

Voice Conversion Across Arbitrary Speakers Based on a Single Target-Speaker Utterance [Demo page](https://vcdemo.github.io) [Paper](http://www1.se.cuhk.edu.hk/~hccl/publications/pub/sxliu.pdf)


Jointly Trained Conversion Model and WaveNet Vocoder for Non-Parallel Voice Conversion Using Mel-Spectrograms and Phonetic Posteriorgrams [Demo page](https://ooshaunoo.github.io/JntTrn-PPGMelsp-VC-samples/)  [Paper](http://www1.se.cuhk.edu.hk/~hccl/publications/pub/INTERSPEECH2019_SongxiangLiu_final.pdf)

End-to-End Accent Conversion Without Using Native Utterances [Demo page](https://liusongxiang.github.io/end2endAC/) [Paper](http://www1.se.cuhk.edu.hk/~hccl/publications/pub/ICASSP2020_e2eAC%20(1).pdf)

Transferring Source Style in Non-Parallel Voice Conversion [Demo Page](https://liusongxiang.github.io/StyleTransferVC/) [Paper](http://www1.se.cuhk.edu.hk/~hccl/publications/pub/INTERSPEECH_2020.pdf)
