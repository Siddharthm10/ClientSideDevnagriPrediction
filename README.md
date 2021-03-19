## Client Side Devnagri Prediction
### Reason
Imagine you created a model which does some great stuff and helps people. You put this model on a web, and daily usage is around 1000 queries, not a lot. The simple server can handle it, but one day this model was discovered by the public, and you started receiving 100k queries daily, the same server would probably die. So now you can either scale server and add more and more memory, or you can try rewriting prediction to the client side. In case you choose the second option here is a tutorial for you.

### Components
#### Backend: Flask (I know that TFJS supports node now but for the sake of suitable preprocessing it's in python)
#### Preprocessing: cv2, numpy, any python library you want
#### Frontend: tensorflowjs (I have a script in head from cdn, made for python developers in order not to download a module)

##### Model
Model is custom designed and is present in `Model.ipynb`. 
Test accuracy = 92%

##### Usage
Simply run `app.py`, open link in browser<br>
Upload files and press predict, if you select around 100-300 files, you can observe how browser instantly eats your CPU. :)

### TODOS:
- [ ] Add a new Inference method and redirect to respective pages(1. Using images, 2. Drawing on Canvas)
- [ ] Add a canvas.
- [ ] Add features so that user can draw on the canvas.
- [ ] Run the inference on predict button click.

### Enjoy!
