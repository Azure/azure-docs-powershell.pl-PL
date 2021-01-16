---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: ab1a8f9b91f8a47f5c6b97b537489c65a53e146e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383896"
---
# <span data-ttu-id="84224-101">Get-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="84224-101">Get-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="84224-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84224-102">SYNOPSIS</span></span>
<span data-ttu-id="84224-103">Pobiera ustawienia inspekcji obszaru roboczego analizy usługi Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="84224-103">Gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="84224-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84224-104">SYNTAX</span></span>

### <span data-ttu-id="84224-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="84224-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84224-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84224-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84224-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="84224-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84224-108">Opis</span><span class="sxs-lookup"><span data-stu-id="84224-108">DESCRIPTION</span></span>
<span data-ttu-id="84224-109">Polecenie cmdlet **Get-AzSynapseSqlAuditSetting** pobiera ustawienia inspekcji obszaru roboczego funkcji Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="84224-109">The **Get-AzSynapseSqlAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="84224-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84224-110">EXAMPLES</span></span>

### <span data-ttu-id="84224-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="84224-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="84224-112">Pobiera ustawienia inspekcji obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="84224-112">Gets the auditing settings of a workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="84224-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="84224-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAuditSetting
```

<span data-ttu-id="84224-114">Pobiera ustawienia inspekcji obszaru roboczego o nazwie ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="84224-114">Gets the auditing settings of a workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="84224-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84224-115">PARAMETERS</span></span>

### <span data-ttu-id="84224-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84224-116">-DefaultProfile</span></span>
<span data-ttu-id="84224-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="84224-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84224-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="84224-118">-InputObject</span></span>
<span data-ttu-id="84224-119">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="84224-119">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84224-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84224-120">-ResourceGroupName</span></span>
<span data-ttu-id="84224-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="84224-121">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84224-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84224-122">-ResourceId</span></span>
<span data-ttu-id="84224-123">Identyfikator zasobu obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="84224-123">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84224-124">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="84224-124">-WorkspaceName</span></span>
<span data-ttu-id="84224-125">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="84224-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84224-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84224-126">CommonParameters</span></span>
<span data-ttu-id="84224-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84224-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84224-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84224-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84224-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84224-129">INPUTS</span></span>

### <span data-ttu-id="84224-130">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="84224-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="84224-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84224-131">OUTPUTS</span></span>

### <span data-ttu-id="84224-132">Microsoft. Azure. Commands. Synapse. models. WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="84224-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="84224-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84224-133">NOTES</span></span>

## <span data-ttu-id="84224-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84224-134">RELATED LINKS</span></span>
