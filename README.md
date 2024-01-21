# ai_assistant

## Notes


1. Create conda envs for both unix and windows.
a) create environemnt.yml file with a seperate pip requirements.txt file and python version specified
b) use pip to install all of the packages
c) freeze packages versioning
d) zip the envs and verify if it works on both unix and windows
2. Read more about `Visual Question Answering (VQA)`
3. The third step (using GPT4 vision) can be extended to use multiple layers e.g:
a) Preprocessing of images (remove the noise like snow/rain/birds from the pictures recently taken)
b) Initial verification of a turbine component -> e.g. comparing to the origin image created at the start of a lifetime.
c) Multiple agents each specialised for detecting a different issue like corossion, distortion, holes.
