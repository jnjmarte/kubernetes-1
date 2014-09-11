ENV SSH_KEY
ENV IMAGE
ENV INTANCE_PREFIX
ENV MASTER_SIZE
ENV MASTER_NAME="${INSTANCE_PREFIX}-master"
ENV MINION_SIZE
ENV MINION_NAMES=($(eval echo ${INSTANCE_PREFIX}-minion-{1..${RAX_NUM_MINIONS}}))
ENV REGION
ENV PRIVATE_NETWORKING
ENV VIRT_IO
ENV IP6
ENV BACKUPS

Command kupe-up
+set -e
+
+source $(dirname $0)/../kube-env.sh
+source $(dirname $0)/../$KUBERNETES_PROVIDER/util.sh
+
+echo "Starting cluster using provider: $KUBERNETES_PROVIDER"
+
+verify-prereqs
+kube-up
+
+source $(dirname $0)/validate-cluster.sh
+
+echo "Done"

No download -> scp directo
Utils, que es la clave.