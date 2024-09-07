I successfully deployed the application using Argo CD by carefully following a structured approach to manage and apply Kubernetes configurations. First, I cloned the repository containing the necessary YAML files for the deployment and service configurations. The repository included deployment manifests for both the frontend and backend applications. I then applied these configurations to my Kubernetes cluster using kubectl apply, which created the necessary resources in the cluster.

Next, I focused on setting up the Argo CD application to manage these deployments. I created an Argo CD Application resource by defining a YAML file with the correct specifications. During this process, I encountered an issue related to an unrecognized field in the Application resource. Specifically, the target field was incorrectly used in the spec.source section, which led to a decoding error. To resolve this, I corrected the field name to targetRevision, aligning it with Argo CD’s requirements.

After making the necessary adjustments, I applied the Argo CD configuration using kubectl apply -f application.yaml. This step successfully registered the application with Argo CD, enabling it to track and manage the specified Kubernetes manifests from the Git repository. The deployment process was seamless, and the application was effectively synchronized with the specified repository, ensuring that the application’s state was accurately reflected in the Kubernetes cluster.

Through this process, I achieved a successful deployment using Argo CD, leveraging its capabilities for GitOps-based continuous deployment and ensuring smooth operation and management of the application within the Kubernetes environment.

Repo for my deployed app : https://github.com/ramzibouzaiene/EmployeeManagement-SpringBoot-VueJS

![myapp-argo-application-Application-Details-Tree-Argo-CD](https://github.com/user-attachments/assets/54533314-0e56-4684-a627-47b76fd671c1)
