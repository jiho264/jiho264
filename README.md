#### LEE, JIHO
#### M.S. Student
#### Department of Embedded Systems Engineering, Incheon National University, South Korea
#### jiho264@inu.ac.kr  


import torch
import sys
import subprocess


print("")
print("- Ubuntu : ")
# Execute the command in a shell
subprocess.call("uname -a", shell=True)

print("")
print("- Python : ")
print("Python version :", sys.version)

print("")
print("- CUDA :")
subprocess.call("nvcc -V", shell=True)
print("cuda available on python: ", torch.cuda.is_available())
# print(torch.cuda.get_device_name(0))


print("")
print("- PyTorch : ")
print("torch version : ", torch.__version__)

print("")
print("- cuDNN :")
print("cudnn ver : ", torch.backends.cudnn.version())
print("cudnn enabled:", torch.backends.cudnn.enabled)

print("")
print("- NCCL version", torch.cuda.nccl.version())

print("")
# import tensorrt

# print("- TensorRT : ")
# subprocess.call("dpkg-query -W tensorrt", shell=True)
# print(tensorrt.__version__)
# print("")

# import torch_tensorrt

# print("- torch_tensorrt : ")
# print(torch_tensorrt.__version__)
