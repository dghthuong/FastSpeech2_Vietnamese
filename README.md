1. Update preprocessed_path in config/preprocess.yaml point to folder preprocessed_data in TextAudioAlignment project

2. python train.py -p config/preprocess.yaml -m config/model.yaml -t config/train.yaml

3. python synthesize.py --text "Xin chào các bạn" --restore_step 17000 --mode single -p config/preprocess.yaml -m config/model.yaml -t config/train.yaml --ref_voice ./audio_samples/sontung.wav --ref_lib_config ../../SpeakerEmbedding/config/speaker_encoder.yaml 
