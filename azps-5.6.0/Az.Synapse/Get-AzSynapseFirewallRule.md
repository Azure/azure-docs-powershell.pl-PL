---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
ms.openlocfilehash: 71622fbfa60a8961f10346aa9197b2c019f31bec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981825"
---
# <span data-ttu-id="9d9a0-101">Get-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9d9a0-101">Get-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="9d9a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d9a0-102">SYNOPSIS</span></span>
<span data-ttu-id="9d9a0-103">Pobiera regułę zapory analizy synapse.</span><span class="sxs-lookup"><span data-stu-id="9d9a0-103">Gets a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="9d9a0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9d9a0-104">SYNTAX</span></span>

### <span data-ttu-id="9d9a0-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="9d9a0-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d9a0-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d9a0-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseFirewallRule -WorkSpaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d9a0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="9d9a0-107">DESCRIPTION</span></span>
<span data-ttu-id="9d9a0-108">Polecenie **cmdlet Get-AzSynapseFirewallRule** pobiera regułę zapory analizy Synapse platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9d9a0-108">The **Get-AzSynapseFirewallRule** cmdlet gets a Azure Synapse Analytics Firewall Rule.</span></span>
<span data-ttu-id="9d9a0-109">Jeśli nie określisz nazwy reguły, to polecenie cmdlet pobiera wszystkie reguły.</span><span class="sxs-lookup"><span data-stu-id="9d9a0-109">If you do not specify a rule name, this cmdlet gets all rules.</span></span>

## <span data-ttu-id="9d9a0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9d9a0-110">EXAMPLES</span></span>

### <span data-ttu-id="9d9a0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9d9a0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="9d9a0-112">To polecenie pobiera wszystkie reguły zapory w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="9d9a0-112">This command gets all firewall rules under a workspace.</span></span>

### <span data-ttu-id="9d9a0-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9d9a0-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="9d9a0-114">To polecenie pobiera regułę zapory w obszarze roboczym ContosoWorkspace o nazwie ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="9d9a0-114">This command gets the firewall rule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="9d9a0-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="9d9a0-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseFirewallRule
```

<span data-ttu-id="9d9a0-116">To polecenie pobiera wszystkie reguły zapory w obszarze roboczym przez potok.</span><span class="sxs-lookup"><span data-stu-id="9d9a0-116">This command gets all firewall rules under a workspace through pipeline.</span></span>

## <span data-ttu-id="9d9a0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d9a0-117">PARAMETERS</span></span>

### <span data-ttu-id="9d9a0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d9a0-118">-DefaultProfile</span></span>
<span data-ttu-id="9d9a0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d9a0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d9a0-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9d9a0-120">-Name</span></span>
<span data-ttu-id="9d9a0-121">Nazwa reguły firerwall dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="9d9a0-121">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d9a0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d9a0-122">-ResourceGroupName</span></span>
<span data-ttu-id="9d9a0-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9d9a0-123">Resource group name.</span></span>

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

### <span data-ttu-id="9d9a0-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9d9a0-124">-WorkspaceName</span></span>
<span data-ttu-id="9d9a0-125">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="9d9a0-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9d9a0-126">- WorkSpaceObject</span><span class="sxs-lookup"><span data-stu-id="9d9a0-126">-WorkSpaceObject</span></span>
<span data-ttu-id="9d9a0-127">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="9d9a0-127">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d9a0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d9a0-128">CommonParameters</span></span>
<span data-ttu-id="9d9a0-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d9a0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d9a0-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d9a0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d9a0-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d9a0-131">INPUTS</span></span>

### <span data-ttu-id="9d9a0-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9d9a0-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="9d9a0-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d9a0-133">OUTPUTS</span></span>

### <span data-ttu-id="9d9a0-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9d9a0-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="9d9a0-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9d9a0-135">NOTES</span></span>

## <span data-ttu-id="9d9a0-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d9a0-136">RELATED LINKS</span></span>
