# Git Sync

https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/git-sync.html


1. Create CloudFormation Stack
    > Sync from Git
        1. Template is ready > Sync from Git
        2. Set a stack name
        3. Stack deployment file. Select: `I am providing my own file in my repository.`
            Si es la primera vez que configura el repo de git, elija `Link a Git repository` y de click en add a new connection, vincule el repo que quiere usar.
            si el repositorio ya existe y se vinculo previamentee elija `Choose a linked Git repository`. Luego elija el repositorioi y el branch.
        4. Deployment file path e sun archivo que define el template que se usara para el despliegue asi como los parametros y tags.

            ```bash
            template-file-path: ./template.yml

            parameters: 
                SNSEmailAddress: diegoperezh.sso@gmail.com
                OutpostsID: 0123acf0919c25aa123
                VirtualInterfaceGroupId: lgw-vif-grp-0a23ccd11d11aa123
                VirtualInterface1Id: lgw-vif-012341811821aa123
                VirtualInterface2Id: lgw-vif-012345601076aa123

            tags:
                cost-center: 'abc678'
                owner: 'diegoph'
            ```

        5. Configurar un nuevo role o reutilizar un iam role existente, si se utiliza uno creado por otro stack se debe editar y agregar el nuevo stack como Resource autorizado.



