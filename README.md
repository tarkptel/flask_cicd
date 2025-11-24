<h1>🚀 Laptop Price Predictor – Kubernetes Deployment (Minikube)</h1>

<p>
This project demonstrates how to containerize a Machine Learning model and deploy it using 
<strong>Kubernetes</strong> on a local cluster through <strong>Minikube</strong>.  
The goal is to understand containerization, orchestration, and real-world deployment flow—similar 
to production systems like AWS EKS.
</p>

<hr/>

<h2>📌 Project Goal</h2>
<ul>
  <li>Build and containerize a machine learning model.</li>
  <li>Deploy it using <strong>Kubernetes</strong>.</li>
  <li>Learn how Kubernetes handles scaling, pods, services, and rollouts.</li>
  <li>Test the project locally using <strong>Minikube</strong>.</li>
  <li>Make the project ready for cloud platforms like AWS EKS, GCP GKE, Azure AKS.</li>
</ul>

<hr/>

<h2>🛠️ Technologies Used</h2>
<ul>
  <li>Python</li>
  <li>Machine Learning (Regression Model)</li>
  <li>Docker</li>
  <li>Kubernetes</li>
  <li>Minikube</li>
  <li>YAML</li>
  <li>Docker Hub</li>
</ul>

<hr/>

<h1>📂 Project Steps (Start → End)</h1>

<h2>1️⃣ Clone the Repository</h2>
<pre>
git clone &lt;your-repo-link&gt;
cd &lt;your-folder&gt;
</pre>

<h2>2️⃣ Build Docker Image</h2>
<pre>
docker build -t laptop-price-predictor .
</pre>

<h2>3️⃣ Tag Image for Docker Hub</h2>
<pre>
docker tag laptop-price-predictor your-dockerhub-username/laptop-price-predictor:latest
</pre>

<h2>4️⃣ Push Image to Docker Hub</h2>
<pre>
docker push your-dockerhub-username/laptop-price-predictor:latest
</pre>

<hr/>

<h1>☸️ Kubernetes Section</h1>

<h2>5️⃣ Start Minikube</h2>
<pre>
minikube start
</pre>

<h2>6️⃣ Apply Deployment</h2>
<pre>
kubectl apply -f deployment.yaml
</pre>

<h2>7️⃣ Apply Service</h2>
<pre>
kubectl apply -f service.yaml
</pre>

<h2>8️⃣ Check Pods</h2>
<pre>
kubectl get pods
</pre>

<h2>9️⃣ Check Deployment</h2>
<pre>
kubectl get deployment
</pre>

<h2>🔟 Check Service</h2>
<pre>
kubectl get svc
</pre>

<h2>🌐 Access the Application</h2>
<pre>
minikube service laptop-service
</pre>
<p>This will automatically open the app in the browser.</p>

<hr/>

<h1>🛠️ Useful Kubernetes Commands</h1>

<h3>Delete Deployment</h3>
<pre>
kubectl delete deployment laptop-deployment
</pre>

<h3>Delete Service</h3>
<pre>
kubectl delete svc laptop-service
</pre>

<h3>Restart Deployment</h3>
<pre>
kubectl rollout restart deployment laptop-deployment
</pre>

<h3>Describe Pod</h3>
<pre>
kubectl describe pod &lt;pod-name&gt;
</pre>

<h3>View Logs</h3>
<pre>
kubectl logs &lt;pod-name&gt;
</pre>

<hr/>

<h1>📦 Stopping Minikube</h1>
<pre>
minikube stop
</pre>

<h1>🧹 Delete Minikube Cluster (optional)</h1>
<pre>
minikube delete
</pre>

<hr/>

<h1>☁️ Deploying on AWS EKS</h1>
<p>
The same YAML files will work on AWS EKS.  
After creating a cluster, run:
</p>
<pre>
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
</pre>

<hr/>

<h1>⭐ Conclusion</h1>
<ul>
  <li>Dockerization</li>
  <li>Kubernetes basics</li>
  <li>Deploying ML model as a microservice</li>
  <li>Working with Minikube</li>
  <li>Scaling & managing applications</li>
  <li>Ready for deploying on cloud platforms</li>
</ul>

<p>Feel free to ask if you want badges, folder structure, or auto-generated YAML files!</p>
