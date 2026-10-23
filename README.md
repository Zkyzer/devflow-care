# Devflow Care

Manutenção para Windows com a identidade da Devflow. Versão **beta 1.10.0-beta.1**, para testes com amigos.

## Baixar

- **[Instalador para Windows 64 bits](https://github.com/Zkyzer/devflow-care/releases/download/v1.10.0-beta.1/Devflow-Care-1.10.0-beta.1-win-x64.msi)** — instale para sua conta e abra pelo menu Iniciar.
- [Versão portátil](https://github.com/Zkyzer/devflow-care/releases/download/v1.10.0-beta.1/Devflow-Care-1.10.0-beta.1-win-x64.zip) — extraia o ZIP inteiro e abra `DevflowCare.exe`.
- [Todas as versões e notas](https://github.com/Zkyzer/devflow-care/releases).
- [Versão atual em destaque](https://github.com/Zkyzer/devflow-care/releases/latest).

Requer Windows 10 ou 11 x64, .NET Framework 4.8 e Windows PowerShell 5.1. O instalador verifica Windows e .NET; não baixa dependências automaticamente.

## O que faz

- Limpeza de Temp do Windows, Temp do usuário, Recentes e Prefetch, com tarefas selecionáveis.
- Opção de preservar temporários recentes por 7, 14 ou 30 dias, ou **Não preservar**. Arquivos em uso ou sem permissão são ignorados.
- Análise antes da limpeza, prévia por categoria, relatórios e histórico local.
- Perfis **Recomendado** (temporários com mais de 7 dias e Limpeza de Disco) e **Personalizado**, com tarefas e prazo salvos. Alternar perfis preserva suas escolhas, inclusive ao reabrir o Care.
- Analisador de armazenamento: distribuição por pasta, os 100 maiores arquivos, busca e navegação até as pastas. Leitura manual com cancelamento, sem apagar ou mover arquivos. Totais usam os tamanhos lógicos lidos; itens sem acesso, links e conteúdo de nuvem indisponível são ignorados. Resultados ficam apenas em memória.
- Limpeza de Disco e otimização da unidade do Windows conforme o tipo de mídia.
- **Armazenamento → Revisar resíduos:** consulta possíveis resíduos nas pastas AppData da conta, com motivos e comparação com inventários locais anteriores. As indicações exigem revisão e não garantem exclusão segura. Permite preservar uma pasta ou enviá-la à Lixeira, uma por vez, após conferir o caminho e confirmar. O Care refaz as verificações de aplicativos, identidade, alterações e bloqueios antes do envio. A ação fica fora da limpeza de um clique, não oferece exclusão permanente nem esvazia a Lixeira. A primeira leitura ainda não conhece desinstalações anteriores.
- Diagnóstico de CPU, RAM e atividade dos discos.
- Alívio manual de RAM para aplicativos elegíveis da conta atual, sem fechá-los. O efeito é temporário e pode causar lentidão ao recarregar dados; não garante aumento da RAM disponível.

O envio de resíduos exige sessão sem administrador, subpasta direta de AppData padrão dentro do perfil atual, unidade local NTFS e até 5.000 itens na verificação. Se um vínculo atual, alteração, item protegido, arquivo bloqueado ou inventário incompleto for detectado, o envio é recusado. Nenhuma heurística comprova ausência de dados importantes: revise o conteúdo antes de confirmar. Use **Ver Lixeira** para consultar ou restaurar pelo Windows; o espaço continua ocupado até esvaziá-la.

Abrir o Care não inicia uma limpeza. Use **Analisar arquivos** para conferir a prévia e **Iniciar manutenção** para executar. A manutenção pede a autorização de administrador do Windows; uma autorização com outra conta é recusada.

Em **Sobre o Care**, use **Verificar atualizações**. No canal beta, o aplicativo consulta as versões públicas apenas quando você clica. Havendo uma versão nova, oferece baixar e abrir o instalador após conferir tamanho e SHA-256. Betas podem estar sem assinatura digital, com aviso na interface; versões estáveis exigem assinatura válida. A instalação mantém preferências e histórico. Na versão portátil, o MSI instala a nova cópia no menu Iniciar; substitua ou remova seu atalho antigo manualmente.

## Privacidade e suporte

Sem conta no aplicativo, anúncios ou telemetria. Preferências e relatórios ficam em `%LOCALAPPDATA%\DevflowCare`. A revisão de resíduos também guarda ali um inventário local de aplicativos e as pastas preservadas; esses dados não são incluídos no diagnóstico de suporte. Relatórios completos podem conter caminhos locais: revise-os antes de compartilhar. **Exportar diagnóstico**, em Sobre o Care, gera um resumo sem nomes, caminhos, listas de processos ou mensagens brutas. Nada é enviado automaticamente.

Encontrou um problema? [Abra um relato](https://github.com/Zkyzer/devflow-care/issues/new?template=problema.yml), descrevendo a ação, o resultado esperado e o que aconteceu. Anexe o diagnóstico somente depois de revisá-lo.

Esta beta ainda não possui assinatura digital do editor. O Windows pode exibir aviso de editor desconhecido ou de reputação. Não desative suas proteções. Os hashes SHA-256 permitem conferir a integridade dos downloads; não equivalem a uma assinatura digital.

Para remover a cópia instalada, use **Configurações → Aplicativos → Devflow Care → Desinstalar**. Preferências e histórico são preservados; remova-os separadamente apenas se desejar.

Este repositório hospeda os downloads, instruções e relatos de problemas. O código-fonte é mantido separadamente. A limpeza não garante ganhos de desempenho ou FPS. Prefetch é recriado pelo Windows e sua exclusão não garante melhora de velocidade.
