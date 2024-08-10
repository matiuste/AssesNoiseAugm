# Adversarial Example Demo

Supplementary material containing a selection of benign, adversarial, and noisy data employed in our [*paper*]().

For each sample, we include the word error rate (WER) as an accuracy metric and the segmental signal-to-noise ratio (SNR<sub>seg</sub>) as a quality noise metric. An SNR<sub>seg</sub> exceeding 0 dB indicates a stronger signal presence compared to noise. These samples are sourced from the [*Librispeech*](https://www.openslr.org/12) corpus dataset.

As outlined in our paper we investigated three types of training regimes, resulting in three different models, respectively :

1: Baseline (no augmentation): This model serves as our control of the clean dataset without any form of augmentation. 
    This baseline establishes the standard level of performance for each model under ideal acoustic conditions.
    
2: Augmentation with speed variations: During the training of the second model temporal variability was introduced into the training data by applying speed perturbations. 
    These augmentations simulate natural variations in speech tempo, which can occur due to speaker differences or recording conditions.
    
3: Augmentation with speed variations, background noise, and reverberation: The third model is trained with both background noises and reverberations, in addition to speed variations. 
    This combination aims to mimic more challenging and realistic acoustic environments that ASR systems may encounter in real-world applications.

### Experiments for the C&W attack.
###### Sample 1 
<pre>Benign transcription:       <em>THEY OF COURSE MUST ALL BE ALTERED</em>
Adversarial transcription:  <em>LOOK AT THAT HE HELD OUT HIS HAND</em>
</pre> &nbsp;
**Benign**:                    **Benign + Noise**: SNR<sub>seg</sub>= -4.81  
[**1**: *WER*=14.29],                 [**1**: *WER*=71.43]  
[**2**: *WER*=00.00],                 [**2**: *WER*=57.14]  
[**3**: *WER*=14.29],                 [**3**: *WER*=14.29]  
<audio style="width:320px" controls="controls">
	<source src="audio_clips/c_w/8455-210777-0066.wav" type="audio/wav" />
</audio>
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/c_w/8455-210777-0066_benign_noise.wav" type="audio/wav" />
</audio>
**C&W adversarial**:                  
[**1**: *WER*=00.00, SNR<sub>seg</sub>=24.47]  
[**2**: *WER*=03.42, SNR<sub>seg</sub>=18.84]  
[**3**: *WER*=08.42, SNR<sub>seg</sub>=15.93]  
<audio style="width:320px" controls="controls">
	<source src="audio_clips/c_w/8455-210777-0066_cw_26022.wav" type="audio/wav" />
</audio>
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/c_w/8455-210777-0066_cw_noise_26022.wav" type="audio/wav" />
</audio>
###### Sample 2
<pre>Benign transcription:       <em>TO THEIR SORROW THEY WERE SOON UNDECEIVED</em>
Adversarial transcription:  <em>ONE COULD HARDLY HOPE FOR ANY UPON SO DRY A DAY</em>
</pre> &nbsp;
**Benign**:                    **Benign + Noise**: SNR<sub>seg</sub>= 1.34  
[**1**: *WER*=00.00],                 [**1**: *WER*=42.86]  
[**2**: *WER*=00.00],                 [**2**: *WER*=28.57]  
[**3**: *WER*=00.00],                 [**3**: *WER*=0.00]  
<audio style="width:320px" controls="controls">
	<source src="audio_clips/c_w/7729-102255-0034.wav" type="audio/wav" />
</audio>
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/c_w/7729-102255-0034_benign_noise.wav" type="audio/wav" />
</audio>
**C&W adversarial**:  
[**1**: *WER*=00.00, SNR<sub>seg</sub>=22.20]  
[**2**: *WER*=00.00, SNR<sub>seg</sub>=17.04]  
[**3**: *WER*=00.00, SNR<sub>seg</sub>=04.13]  
<audio style="width:320px" controls="controls">
	<source src="audio_clips/c_w/7729-102255-0034_cw_26022.wav" type="audio/wav" />
</audio>
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/c_w/7729-102255-0034_cw_noise_26022.wav" type="audio/wav" />
</audio>
###### Sample 3
<pre>Benign transcription:       <em>BUT YOU KNOW MORE ABOUT THAT THAN I DO SIR</em>
Adversarial transcription:  <em>YES MY DEAR WATSON I HAVE SOLVED THE MYSTERY</em>
</pre> &nbsp;
**Benign**:                    **Benign + Noise**: SNR<sub>seg</sub>= -0.41  
[**1**: *WER*=00.00],                 [**1**: *WER*=50.00]  
[**2**: *WER*=00.00],                 [**2**: *WER*=40.00]  
[**3**: *WER*=00.00],                 [**3**: *WER*=10.00]  
<audio style="width:320px" controls="controls">
	<source src="audio_clips/c_w/2094-142345-0055.wav" type="audio/wav" />
</audio>
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/c_w/2094-142345-0055_benign_noise.wav" type="audio/wav" />
</audio>
**C&W adversarial**:  
[**1**: *WER*=00.00, SNR<sub>seg</sub>=25.78]  
[**2**: *WER*=00.00, SNR<sub>seg</sub>=23.94]  
[**3**: *WER*=00.00, SNR<sub>seg</sub>=22.30]  
<audio style="width:320px" controls="controls">
	<source src="audio_clips/c_w/2094-142345-0055_cw_26022.wav" type="audio/wav" />
</audio>
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/c_w/2094-142345-0055_cw_noise_26022.wav" type="audio/wav" />
</audio>

### Experiments for the Alzantot attack.
###### Sample 1 
<pre>Benign transcription:       <em>WHY FADE THESE CHILDREN OF THE SPRING</em>
</pre> &nbsp;
**Alzantot adversarial**:  
[**1**: *WER*=42.86, SNR<sub>seg</sub>=13.62]  
[**2**: *WER*=42.86, SNR<sub>seg</sub>=13.54]  
[**3**: *WER*=14.29, SNR<sub>seg</sub>=29.48]  
**Benign**:                    **Alzantot adversarial**:  
<audio style="width:320px" controls="controls">
	<source src="audio_clips/Alzantot/908-157963-0003.wav" type="audio/wav" />
</audio>
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/Alzantot/908-157963-0003_26020.wav" type="audio/wav" />
</audio>
###### Sample 2 
<pre>Benign transcription:       <em>THE CLOUD THEN SHEWD HIS GOLDEN HEAD AND HIS BRIGHT FORM EMERG'D</em>
</pre> &nbsp;
**Alzantot adversarial**:  
[**1**: *WER*=66.67, SNR<sub>seg</sub>=11.55]  
[**2**: *WER*=66.67, SNR<sub>seg</sub>=11.55]  
[**3**: *WER*=41.67, SNR<sub>seg</sub>=11.56]  
**Benign**:                    **Alzantot adversarial**:  
<audio style="width:320px" controls="controls">
	<source src="audio_clips/Alzantot/908-157963-0017.wav" type="audio/wav" />
</audio>
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/Alzantot/908-157963-0017_26020.wav" type="audio/wav" />
</audio>

### Experiments for the Kenansville attack.
###### Sample 1 
<pre>Benign transcription:       <em>IF A FELLOW'S BEEN A LITTLE BIT WILD HE'S BEELZEBUB AT ONCE</em>
</pre> &nbsp;
**Kenansville adversarial**:  
[**1**: *WER*=41.67, SNR<sub>seg</sub>=22.37]  
[**2**: *WER*=16.67, SNR<sub>seg</sub>=22.37]  
[**3**: *WER*=16.67, SNR<sub>seg</sub>=30.53]  
**Benign**:                    **Kenansville adversarial**:  
<audio style="width:320px" controls="controls">
	<source src="audio_clips/kenansville/5683-32866-0007.wav" type="audio/wav" />
</audio>
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/kenansville/5683-32866-0007_26020.wav" type="audio/wav" />
</audio>
###### Sample 2 
<pre>Benign transcription:       <em>WE ARE QUITE SATISFIED NOW CAPTAIN BATTLEAX SAID MY WIFE</em>
</pre> &nbsp;
**Kenansville adversarial**:  
[**1**: *WER*=20.00, SNR<sub>seg</sub>=18.76]  
[**2**: *WER*=20.00, SNR<sub>seg</sub>=11.49]  
[**3**: *WER*=10.00, SNR<sub>seg</sub>=8.92]  
**Benign**:                    **Kenansville adversarial**:  
<audio style="width:320px" controls="controls">
	<source src="audio_clips/kenansville/8455-210777-0006.wav" type="audio/wav" />
</audio>
 <audio style="width:320px" controls="controls">
	<source src="audio_clips/kenansville/8455-210777-0006_26020.wav" type="audio/wav" />
</audio>
