| Роль  | Права роли | Группы пользователей |
| --- | --- | --- |
| cluster-reader | Просмотр всех нересурсных объектов на уровне кластера: get, list, watch для: pods, services, deployments, statefulsets, configmaps, namespaces, nodes, events.Запрещено: secrets, clusterroles, roles, rolebindings. | Бизнес-аналитики, Менеджеры по продукту, Аудиторы (вне ИБ) |
| namespace-developer | Полный доступ к объектам в выделенных namespace-ах: get, list, watch, create, update, patch, delete для: pods, services, deployments, configmaps, ingresses. Запрещено: secrets (только через внешние vault), rbac-ресурсы, nodes, cluster-level объекты. | Функциональные команды разработки, DevOps-инженеры продуктовых команд |
| cluster-admin | Полный доступ ко всем ресурсам кластера, включая: * на все API-группы (apps, batch, networking.k8s.io, rbac.authorization.k8s.ioи т.д.). Включает управление nodes, storage, network policies, custom resource definitions. | Platform Team / SRE, Системные администраторы ЦОД |
| secrets-reader | Только просмотр секретов в выделенных namespace: get, list для secrets в определённых namespace (например, prod-*,finance). Не имеет доступак другим ресурсам без дополнительных ролей. | Специалист по ИБ, Ведущие инженеры (по запросу и с одобрением) |


