---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: ab1a8f9b91f8a47f5c6b97b537489c65a53e146e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359424"
---
# <span data-ttu-id="5dfbd-101">Get-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="5dfbd-101">Get-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="5dfbd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5dfbd-102">SYNOPSIS</span></span>
<span data-ttu-id="5dfbd-103">Pobiera ustawienia inspekcji obszaru roboczego analizy usługi Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="5dfbd-103">Gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="5dfbd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5dfbd-104">SYNTAX</span></span>

### <span data-ttu-id="5dfbd-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5dfbd-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5dfbd-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5dfbd-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5dfbd-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5dfbd-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5dfbd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5dfbd-108">DESCRIPTION</span></span>
<span data-ttu-id="5dfbd-109">Polecenie cmdlet **Get-AzSynapseSqlAuditSetting** pobiera ustawienia inspekcji obszaru roboczego funkcji Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5dfbd-109">The **Get-AzSynapseSqlAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="5dfbd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5dfbd-110">EXAMPLES</span></span>

### <span data-ttu-id="5dfbd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5dfbd-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="5dfbd-112">Pobiera ustawienia inspekcji obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="5dfbd-112">Gets the auditing settings of a workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="5dfbd-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5dfbd-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAuditSetting
```

<span data-ttu-id="5dfbd-114">Pobiera ustawienia inspekcji obszaru roboczego o nazwie ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="5dfbd-114">Gets the auditing settings of a workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="5dfbd-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5dfbd-115">PARAMETERS</span></span>

### <span data-ttu-id="5dfbd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dfbd-116">-DefaultProfile</span></span>
<span data-ttu-id="5dfbd-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5dfbd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dfbd-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5dfbd-118">-InputObject</span></span>
<span data-ttu-id="5dfbd-119">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="5dfbd-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5dfbd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dfbd-120">-ResourceGroupName</span></span>
<span data-ttu-id="5dfbd-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5dfbd-121">Resource group name.</span></span>

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

### <span data-ttu-id="5dfbd-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5dfbd-122">-ResourceId</span></span>
<span data-ttu-id="5dfbd-123">Identyfikator zasobu obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="5dfbd-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="5dfbd-124">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="5dfbd-124">-WorkspaceName</span></span>
<span data-ttu-id="5dfbd-125">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="5dfbd-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5dfbd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dfbd-126">CommonParameters</span></span>
<span data-ttu-id="5dfbd-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dfbd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dfbd-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5dfbd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dfbd-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5dfbd-129">INPUTS</span></span>

### <span data-ttu-id="5dfbd-130">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5dfbd-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5dfbd-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5dfbd-131">OUTPUTS</span></span>

### <span data-ttu-id="5dfbd-132">Microsoft. Azure. Commands. Synapse. models. WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="5dfbd-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="5dfbd-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5dfbd-133">NOTES</span></span>

## <span data-ttu-id="5dfbd-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5dfbd-134">RELATED LINKS</span></span>
