```

pods :
    
    
    
    
     alias k=kubectl
   39  k get pods -A -o wide
   40  clear
   41  exit
   42  clear
   43  k get pods
   44  alias k=kubectl
   45  k get pods
   46  docker ps
   47  clear
   48  k get pods -A
   49  k get pods -A -o wide
   50  k run myapp --image httpd 
   51  k get pods
   52  clear
   53  k get pods -A
   54  k get pods -o wide
   55  clear
   56  k get pods -A 
   57  k get pods -A -o wide
   58  k create ns raman
   59  k egt pods -A
   60  k gEt pods -A
   61  k get pods -A
   62  k run ramanapp --image httpd -n raman
   63  clear
   64  k get pods -A
   65  clear
   66  k get pods -A -o wide
   67  k get pods -n raman
   68  clear
   69  k get pods -A
   70  k delete pod ramanapp -n raman
   71  k get pods -A
   72  k api-resources
   73  clear
   74  k get pods -A
   75  ls
   76  k run ramanapp --image httpd 
   77  k delete pod ramanapp
   78  ls
   79  k run ramanapp --image httpd -n raman
   80  k get pods -A
   81  LS
   82  ls
   83  vi pod.yml
   84  k create -f pod.yml
   85  k get pods -A
   86  k get pods -A -o wide
   87  k delete -f pod.yml
   88  cat pod.yml 
   89  ls
   90  vi pod.yml 
   91  k create -f pod.yml
   92  k get pods -A
   93  k get pods -A -O WIDE
   94  k get pods -A -o wide
   95  k delete pods --all -n raman
   
   
   
   
   
   root@master:~# cat pod.yml 
apiVersion: v1
kind: Pod
metadata:
  name: ramanapp2
  namespace: raman
spec:
  containers:
  - name: httpd
    image: httpd
    ports:
    - containerPort: 80
    
    
    ====================================
    
    




alias k=kubectl
  667  k get po -A 
  668  clear
  669  k get po -n raman
  670  k create deployment dep1 --image httpd --replicas 5 
  671  k delete deploy --all 
  672  k create deployment dep1 --image httpd --replicas 5 -n raman
  673  k get po -n raman
  674  clear
  675  k get all -n raman
  676  k describe pod dep1-7fd854dc89-45g9g
  677  k describe pod dep1-7fd854dc89-45g9g -n raman
  678  clear
  679  k get deploy -n raman
  680  k get rs -n raman
  681  k get po -n raman
  682  k get po -n raman -o wide
  683  kubectl delete pod dep1-7fd854dc89-45g9g -n raman
  684  k get po -n raman -o wide
  685  clear
  686  k delete deploy --all -n raman
  687  k get pods -A
  688  CLEAR
  689  clear
  690  k describe pod anoop-app -n anoop
  691  clear
  692  ls
  693  vi pod.yml 
  694  vi pod.yaml
  695  mkdir raman
  696  ls
  697  cat pod.yml
  698  k describe pod anoop-app -n anoop
  699  clear
  700  k get po --selector run=anoop-app
  701  k get po --selector run=anoop-app -A
  702  cat pod.yml
  703  cd raman
  704  vi pod.yml
  705  k create -f pod.yml 
  706  k get pods -A
  707  k get po --selector tier=frontend -A
  708  k describe pod ramanapp -n raman
  709  k get po --selector tier=front-end -A
  710  clear
  711  k describe po -A | grep -i label
  712  clear
  713  k get po -A
  
  
  

  
  
  
  root@master:~/raman# cat pod.yml 
apiVersion: v1
kind: Pod
metadata:
  name: ramanapp
  namespace: raman
  labels:
    tier: front-end
spec:
  containers:
  - name: httpd
    image: httpd
    ports:
    - containerPort: 80
    
    
    
    =============================
    
    
    
    
    
    cat pod.yml 
  717  clear
  718  kubectl get pods --show-labels
  719  kubectl get pods --show-labels -A
  720  clear
  721  k get po -A
  722  CLEAR
  723  clear
  724  k get po A
  725  k get po -A
  726  CLEAR
  727  clearclear
  728  clear
  729  k get po -A | wc -l
  730  k get deploy -A
  731  k get po
  732  k get deploy -n raman
  733  k scale deploy dep000 -n abhishek --replicas 0
  734  k get deploy -A
  735  k get pods
  736  k get pods -n raman
  737  k label pod ramanapp env=stage
  738  k label pod ramanapp env=stage -n raman
  739  k describe pod | grep -i label -n raman
  740  k describe pod -n raman | grep -i label
  741  clear
  742  ls
  743  vi deploy.yaml
  744  k get deploy
  745  k get deploy -n raman
  746  ls
  747  k create -f deploy.yaml 
  748  k get deploy -n raman
  749  ls
  750  vi deploy.yaml 
  751  k appply -f deploy.yaml 
  752  k apply -f deploy.yaml 
  753  k get deploy -n raman
  754  k get deploy 
  755  k delete deploy --all 
  756  clear
  757  k get deploy -n raman
  758  k get rs
  759  k get rs -n raman
  760  k get po -n raman
  761  k describe po raman-deployment-86dcfdf4c6-5mdfx -n raman | grep -i label
  762  k describe rs raman-deployment-86dcfdf4c6-5mdfx -n raman | grep -i selector
  763  k describe rs  -n raman | grep -i selector
  764  k describe rs  -n raman | grep -i label
  765  k describe deploy  -n raman | grep -i label
  766  k describe deploy  -n raman | grep -i selector
  767  vi deploy.yaml 
  768  k apply -f deploy.yaml 
  769  k get deploy -n raman
  770  k describe po  -n raman | grep -i label
  771  k get rs
  772  k get rs -n raman
  773  k get pods -n raman --show-labels
  774  ls
  775  k get po -n raman
  776  vi deploy.yaml 
  777  k apply -f deploy.yaml 
  778  k get po -n raman
  779  k get pods -n raman --show-labels
  780  k delete deploy --all -n raman
  781  k delete deploy --all 
  
  
  
  
  
  
  root@master:~/raman# cat deploy.yaml 
apiVersion: apps/v1
kind: Deployment
metadata:
  name: raman-deployment2
  namespace: raman
  labels:
    app: nginx2
spec:
  replicas: 5
  selector:
    matchLabels:
      app: nginx
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: httpd
        image: httpd
        ports:
        - containerPort: 80
        
        
        
        
        =============================================================================
        
        
        
        
        
        cat deploy.yaml 
  784  clear
  785  k get deploy -n raman
  786  ls
  787  k get po -A 
  788  k get po -A -o wided
  789  k get po -A -o wide
  790  clear
  791  k get po -n raman
  792  k delete po -n raman
  793  k delete po --all -n raman
  794  k run ramanapp --image httpd -n raman
  795  k get all -n raman
  796  k get po -o wide
  797  k get po -o wide -n raman
  798  curl 192.168.190.105
  799  curl 192.168.190.105:80
  800  k expose pod ramanapp --type NodePort --port 80 --target-port 80 -n raman
  801  k get all -n raman
  802  k describe svc ramanapp -n raman
  803  k get po -n raman --show-labels
  804  k get po -o wide -n raman
  805  clear
  806  k get pod
  807  k get po -n raman
  808  k delete po --all -n raman
  809  k delete svc --all -n raman
  810  clear
  811  k create deploy ramandep --image nginx --replicas 5
  812  k get po
  813  k get po -o wide
  814  k expose deploy ramandep --type NodePort --port 80 --target-port 80 
  815  k get svc
  816  k describe svc 
  817  k get po --show-labels
  818  k get po -o wide
  819  k get ep
  820  clear
  821  k expose deploy ramandep --type LoadBalancer  --target-port 80 
  822  k expose deploy ramandep --type LoadBalancer  --port 80 --target-port 80 
  823  k get svc 
  824  k delete svc ramandep
  825  k expose deploy ramandep --type LoadBalancer  --port 80 --target-port 80 
  826  k get svc
  827  clear
  828  ls
  
  
  
  
  
  ===================================================================================
        
        ```
