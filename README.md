### 🎯 Understanding Kernels in Support Vector Machines (SVM)
### 📌 Project Overview

This project demonstrates the intuition of kernels in SVMs by experimenting with datasets that are not linearly separable.
We explore how different kernels — linear, RBF (Radial Basis Function), and polynomial — transform data into higher dimensions, making classification possible.

### ⚙️ Tools & Libraries

NumPy

Pandas

Matplotlib & mpl_toolkits.mplot3d (for 3D visualization)

scikit-learn SVM

### 🔎 Steps & Observations

### 1. Dataset Creation

Created a circular dataset (two concentric classes).

<img width="559" height="413" alt="ker1" src="https://github.com/user-attachments/assets/69798fb4-031e-4f3b-97b5-09a63454f8fc" />


### 2. Linear Kernel (Baseline)

Applied SVC with linear kernel.

Accuracy: 0.65

Decision boundary image shows a straight line misclassifying many points.
<img width="585" height="455" alt="ker2" src="https://github.com/user-attachments/assets/2bc38435-495f-490f-93c7-1e3018476be5" />

➡️ Confirms that linear SVM is not suitable for circular patterns.

### 3. Radial Basis Function (RBF Kernel)

Defined a function to manually apply the RBF transformation.

Visualization (📸 attached) shows red points lifted in higher dimension.
<img width="409" height="397" alt="ker3" src="https://github.com/user-attachments/assets/af218307-447f-4812-a7cf-b4fd0f89969a" />

Trained SVC with kernel = RBF → Accuracy: 100% 🎉

Decision boundary plot shows perfect separation of classes.
<img width="585" height="455" alt="ker4" src="https://github.com/user-attachments/assets/d9606dee-1f62-4564-8947-8d20a60a6f78" />


### 4. Polynomial Kernel

Applied SVC with polynomial kernel (degree=2).

Accuracy: 100%
<img width="585" height="455" alt="ker5" src="https://github.com/user-attachments/assets/6ded91c3-9ce6-4f60-9c70-d12cc57009ab" />
Decision boundary image shows circular separation, correctly classifying all points.

Transformation visualization shows how polynomial kernel creates new feature space where separation is possible.
<img width="547" height="413" alt="ker6" src="https://github.com/user-attachments/assets/ce291496-0226-4ca4-aab7-2d93977b97ae" />



### 📊 Key Intuitions Learned

Linear kernel fails on non-linear datasets like circles.

RBF kernel maps data into a higher dimension where linear separation becomes possible.

Polynomial kernel creates polynomial feature combinations that also allow perfect separation.

Kernels = “shortcuts” to higher-dimensional transformations → they let SVM handle complex boundaries without explicitly computing new features.

✨ This project helped build intuition about why kernels are powerful and how they allow SVM to go beyond straight lines into flexible, non-linear decision boundaries.
