## 公式ドキュメント

- Pod は、コンテナの管理やネットワーキングの目的でまとめられた、1 つ以上のコンテナのグループです。
- Deployment は Pod の状態を確認し、Pod のコンテナが停止した場合には再起動します。Deployment は Pod の作成やスケールを管理するために推奨される方法(手段)です。
- Service で Pod をインターネットに公開

  - kubectl get nodes

- マスターがクラスターを管理する
- ノードがアプリケーションを動かすワーカーとなる
  - kubectl get deployments
  - デプロイされているアプリケーションの一覧

## Deployment でアプリケーションをデプロイ

- kubectl get pods
- kubectl describe pods
- kubectl proxy
- kubectl logs \$POD_NAME
- kubectl exec \$POD_NAME
![image](https://user-images.githubusercontent.com/33531901/173571314-8c7fe7ce-ab0a-4910-8270-52af7719fbe1.png)


## アプリケーションを Service で公開

- kubectl get services
- kubectl describe deployment

<img width="579" alt="image" src="https://user-images.githubusercontent.com/33531901/173571331-5607cd86-1820-4edf-b590-2c1c752c25f9.png">


## ReplicaSet でサービスをスケーリング

- kubectl get rs

## ingress

- クラスター内の Service に対する外部からのアクセス(主に HTTP)を管理する API オブジェクトです。
- Ingress は負荷分散、SSL 終端、名前ベースの仮想ホスティングの機能を提供します。

## RoleBinding

- RoleBinding は、同じ Namespace 内の任意の Role を参照できます。

## Rollout(デプロイメントの実行)

- kubectl rollout status
