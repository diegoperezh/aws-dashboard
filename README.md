# Git Sync

https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/git-sync.html


1. Create CloudFormation Stack
    > Sync from Git
        1. Set a stack name
        2. Configurar un nuevo role o reutilizar un iam role existente, si se utiliza uno creado por otro stack se debe editar y agregar el nuevo stack como Resource autorizado.
        3. Una nueva conexion se debe establecer con el repositorio de Git (Git sync supports GitHub, GitHub Enterprise, GitLab, and Bitbucket repositories). Se puede instalar un nuevo conectar cuando se crea un nuevo proyecto de CloudFormation.