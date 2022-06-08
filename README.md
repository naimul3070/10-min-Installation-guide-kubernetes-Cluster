## Welcome to DevOps Learn.

#Prerequisites

## linux (Ububuntu-20.04.3-live-server-amd64.iso LTS)
### For Download <a href="https://old-releases.ubuntu.com/releases/20.04.3/ubuntu-20.04-beta-live-server-amd64.iso" rel="nofollow" style="color:red;">CLICK HERE</a>

## For Master Node
#### FOR EASY Installation just Run the command

    git clone https://github.com/naimul3070/kubernetes.git&&cd kubernetes/&&chmod +x master.sh&&./master.sh
    
### Just Press Y when you IF see this

<img width="419" alt="image" src="https://user-images.githubusercontent.com/50922314/172578341-bbaed7ad-74c7-4b58-b17d-3b3987dbdb1c.png" class="center">

### There will be token like image JUST COPY THAT KEEP SOME WHERE FOR next use

<img width="671" alt="image" src="https://user-images.githubusercontent.com/50922314/172582907-59912f27-8e23-4850-b6e9-e6b3bf5ed151.png" class="center">

### for check run the command in master node for check the nodes status
    kubectl get node
    
# ==1st worker 

#### after installation there will be a token like 

# Example :  
kubeadm join 10.209.99.220:6443 --token yn0e71.7fy4apmhg060nuxp \
--discovery-token-ca-cert-hash sha256:b6445c3c7c29b96c042f00c98b544838d4954faccfa3001096281de340444357

### Just copy and run into worker node after make ready the worker node,
## For Worker Node 
### FOR EASY Installation JUST run the command in wokrer pc
    git clone https://github.com/naimul3070/kubernetes.git&&cd kubernetes/&&chmod +x worker.sh&&./worker.sh
    
### Just Press Y when you IF see this

<img width="419" alt="image" src="https://user-images.githubusercontent.com/50922314/172578341-bbaed7ad-74c7-4b58-b17d-3b3987dbdb1c.png" class="center">

### If this is the first worker node then just follow the instruton                            
# FOLLOW==1st worker

#### Check in master node by the command 
    kubectl get node
    
# for multiple worker node
## after imstallation worker node need to create new token in master node and copy the token then run it in worker node.

#### run the comedy for see token list in master node  
    kubeadm token list
#### for create new token 
    sudo kubeadm token create --print-join-command
#### now copy the token and run to the worker node, 

### for check run the command in master node for check the nodes status
    kubectl get node
# Troubleshooting

#### if the node status in showiing not-ready just enable the docker and turn of the the swap memory of all-nodes

    sudo systemctl enable docker.service
    sudo swapoff -a

# Happy kubernetes ---- enjoy---
