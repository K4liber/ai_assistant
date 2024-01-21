# AI assistant

## Notes

1. Create a FastAPI scheme.
2. Create `pytest` scheme.
3. Create conda envs for both unix and windows.
a) create environemnt.yml file with a seperate pip requirements.txt file and python version specified
b) use pip to install all of the packages
c) freeze packages versioning
d) zip the envs and verify if it works on both unix and windows
4. Create a GUI (make it simple, only html, css + JS, without any framework, `npm` can be heavy, we should
not focus on a GUI to much)
5. Read more about `Visual Question Answering (VQA)`

## Steps

Each step should have own branch.

0. Starting point
- requirements.txt
- environemnt.yml
- conda zips (should work just after unzipping, user do not need to do additional work) and conda env create instruction
- FastAPI scheme
- pytest scheme with a units test that need to pass after the first step is finished.
1. Function calling for creating a task
2. Function calling for a) creating a task b) domain question
- Maybe we should use RAG for the second task?
- We can create a server with `Qdrant` already filled with a data
a) Example of vector database using `Qdrant`: https://github.com/K4liber/ai_devs/blob/main/script/tasks/search.py
b) Database should contain a various content from the wind turbines domain
c) User ask a question -> we do a similarity search -> based on the result we ask LLM model
to answer the question
3. Using GPT4 vision to make a wind turbine inspection
- we can use multiple layers e.g:
a) Preprocessing of images (remove the noise like snow/rain/birds from the pictures recently taken)
b) Initial verification of a turbine component -> e.g. comparing to the origin image created at the start of a lifetime.
c) Multiple agents each specialised for detecting a different issue like corossion, distortion, holes.
