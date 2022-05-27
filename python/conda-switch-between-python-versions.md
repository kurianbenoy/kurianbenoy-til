# conda switch between python versions

![](<../.gitbook/assets/image (17).png>)

What is `rdkit` and `nb_conda_kernels`? I see you are switching to a virtual environment with different python version. Was it the trick to change kernels you mentioned during walk-thrus session?

**Radek's explaination:**

Yup, that’s it. Essentially, how to have one conda env but multiple python versions. You can have one nb running python 3.5, and another python 3.7. Very rarely is this useful, but in the scenario where you want to run some old python code, there is a solution without having to set up a new environment.

(also, if you have two envs and want to work on the code at the same time or execute files in succession – for instance to process some data in one notebook and continue in the other --, it gets painful… this is just a cleaner way to achieve it, though it is a super rare case that this might be needed)

`rdkit` is just some random repo I wanted to use for a Kaggle competition, not sure I will use it ever again in my life**.**

In fact, this is such a niche case I don’t even think it is worth covering this in the walk-thrus, but probably good to know this solution exists if you ever encounter a situation where it might be helpful (googling for this is not that easy).



Bookmark for conversation:



{% embed url="https://forums.fast.ai/t/official-course-walk-thrus/96617/18?u=kurianbenoy" %}
