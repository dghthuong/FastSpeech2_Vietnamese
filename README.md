1. Update preprocessed_path in config/preprocess.yaml point to folder preprocessed_data in TextAudioAlignment project

2. python train.py -p config/preprocess.yaml -m config/model.yaml -t config/train.yaml

or download pretrained: https://drive.google.com/file/d/1_VXA6yaPuw9W0p2uQ4ZAem73gB8vcY4l/view?usp=sharing
store in folder: ./output/ckpt/100000.pth.tar

3. python synthesize.py --text "Xin chào các bạn" --restore_step 100000 --mode single -p config/preprocess.yaml -m config/model.yaml -t config/train.yaml --ref_voice ./audio_samples/sontung.wav --ref_lib_config ../../SpeakerEmbedding/config/speaker_encoder.yaml 
