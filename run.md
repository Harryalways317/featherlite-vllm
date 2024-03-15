docker build -t featherlite-vllm .


docker run --gpus all -p 8000:8000 --ipc=host featherlite-vllm --model HuggingFaceH4/zephyr-7b-beta --dtype "auto" --tensor-parallel-size 1 --max-model-len 16830
