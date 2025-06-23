# resumo-criação-aruze

 Passos para criar uma VM Windows no Azure
- Acesse o portal do Azure com sua conta (ou crie uma gratuita se ainda não tiver).
- Pesquise por "Máquinas Virtuais", vá até a seção de serviços e clique em Criar > Máquina virtual do Azure.
- Configure os detalhes da VM:
- Nome: myVM
- Imagem: Windows Server 2022 Datacenter (x64 Gen 2)
- Usuário e senha do administrador
- Regiões e tamanhos podem ser mantidos como padrão
- Habilite as portas de entrada para acesso remoto e web:
- Selecione RDP (3389) e HTTP (80)
- Clique em Examinar + criar, revise os dados e depois selecione Criar.
- Após a implantação, clique em Ir para o recurso.

🔌 Conectando-se à VM via RDP
- Na página da VM, clique em Conectar > RDP, baixe o arquivo .rdp e abra-o.
- Use as credenciais criadas para acessar o sistema.
- Ignore o aviso de certificado se aparecer.

🌐 Instalar o servidor IIS
Na sessão da VM (via RDP), abra o PowerShell e rode:
Install-WindowsFeature -name Web-Server -IncludeManagementTools


Depois, acesse o IP público da VM no navegador para ver a página padrão do IIS.

🧹 Limpando os recursos
- Se não precisar mais da VM, vá até o Grupo de Recursos e selecione Excluir grupo de recursos.
⏲️ Ativar desligamento automático (opcional)
- Dentro da VM, vá em Operações > Desligamento automático, ative e defina o horário.


Etapas para configurar uma instância de banco de dados no Azure


- Acesse o Portal do Azure
Vá para portal.azure.com e faça login com sua conta.
- Crie um novo recurso de banco de dados
Pesquise por "SQL Database" e clique em + Criar.
- Configure os detalhes básicos
- Assinatura e grupo de recursos (crie um novo ou use um existente)
- Nome do banco de dados (ex: meuBancoSQL)
- Servidor lógico: crie um novo servidor com nome, login e senha de administrador
- Localização: escolha a região mais próxima de seus usuários
- Configurações adicionais
- Camada de desempenho: escolha entre opções como Basic, Standard ou Premium
- Backup, segurança e rede: configure conforme suas necessidades (por exemplo, permitir acesso público ou restringir por IP)
- Revisar e criar
Revise todas as configurações e clique em Criar. O Azure provisionará a instância em poucos minutos.

🔐 Acesso e gerenciamento
- Após a criação, você pode acessar o banco de dados via Azure Data Studio, SQL Server Management Studio (SSMS) ou diretamente pelo portal.
- Use o nome do servidor, login e senha definidos para se conectar.

Se quiser, posso te mostrar como fazer isso com PostgreSQL, MySQL ou até Cosmos DB também. Quer explorar alguma dessas opções?

