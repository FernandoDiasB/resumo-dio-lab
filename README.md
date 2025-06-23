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
