# argocd-django-postgres-app-config

- To access to ArgoCD UI from the browser, enter the following command in the terminal :
"""bash
kubectl port-forward svc/argocd-server -n argocd 8080:443
"""

- To access to the diango application from the browser,
  - Migrate :
"""bash
kubectl exec -it <pod_name> -n django-postgres-app -- bin/bash
python manage.py migrate
""" 
  - Enter the following command in the terminal :
"""bash
kubectl port-forward svc/django-app-service -n django-postgres-app 8000:8000
"""
