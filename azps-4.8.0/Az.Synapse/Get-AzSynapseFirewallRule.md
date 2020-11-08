---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
ms.openlocfilehash: 22a7bb4c135a4424aa27a76f9e13ba14f21ca572
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94061952"
---
# <span data-ttu-id="05cd7-101">Get-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="05cd7-101">Get-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="05cd7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="05cd7-102">SYNOPSIS</span></span>
<span data-ttu-id="05cd7-103">Pobiera regułę zapory Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="05cd7-103">Gets a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="05cd7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="05cd7-104">SYNTAX</span></span>

### <span data-ttu-id="05cd7-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="05cd7-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05cd7-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05cd7-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseFirewallRule -WorkSpaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05cd7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="05cd7-107">DESCRIPTION</span></span>
<span data-ttu-id="05cd7-108">Polecenie cmdlet **Get-AzSynapseFirewallRule** pobiera regułę zapory Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="05cd7-108">The **Get-AzSynapseFirewallRule** cmdlet gets a Azure Synapse Analytics Firewall Rule.</span></span>
<span data-ttu-id="05cd7-109">Jeśli nie określisz nazwy reguły, to polecenie cmdlet będzie pobierać wszystkie reguły.</span><span class="sxs-lookup"><span data-stu-id="05cd7-109">If you do not specify a rule name, this cmdlet gets all rules.</span></span>

## <span data-ttu-id="05cd7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="05cd7-110">EXAMPLES</span></span>

### <span data-ttu-id="05cd7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="05cd7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="05cd7-112">To polecenie pobiera wszystkie reguły zapory w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="05cd7-112">This command gets all firewall rules under a workspace.</span></span>

### <span data-ttu-id="05cd7-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="05cd7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="05cd7-114">To polecenie pobiera regułę zapory w obszarze roboczym ContosoWorkspace z nazwą ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="05cd7-114">This command gets the firewall rule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="05cd7-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="05cd7-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseFirewallRule
```

<span data-ttu-id="05cd7-116">To polecenie pobiera wszystkie reguły zapory w obszarze roboczym za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="05cd7-116">This command gets all firewall rules under a workspace through pipeline.</span></span>

## <span data-ttu-id="05cd7-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="05cd7-117">PARAMETERS</span></span>

### <span data-ttu-id="05cd7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05cd7-118">-DefaultProfile</span></span>
<span data-ttu-id="05cd7-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="05cd7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05cd7-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="05cd7-120">-Name</span></span>
<span data-ttu-id="05cd7-121">Nazwa reguły firerwall dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="05cd7-121">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="05cd7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05cd7-122">-ResourceGroupName</span></span>
<span data-ttu-id="05cd7-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="05cd7-123">Resource group name.</span></span>

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

### <span data-ttu-id="05cd7-124">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="05cd7-124">-WorkspaceName</span></span>
<span data-ttu-id="05cd7-125">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="05cd7-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="05cd7-126">-WorkSpaceobject</span><span class="sxs-lookup"><span data-stu-id="05cd7-126">-WorkSpaceObject</span></span>
<span data-ttu-id="05cd7-127">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="05cd7-127">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="05cd7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05cd7-128">CommonParameters</span></span>
<span data-ttu-id="05cd7-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05cd7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05cd7-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05cd7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05cd7-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05cd7-131">INPUTS</span></span>

### <span data-ttu-id="05cd7-132">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="05cd7-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="05cd7-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="05cd7-133">OUTPUTS</span></span>

### <span data-ttu-id="05cd7-134">Microsoft. Azure. Commands. Synapse. models. PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="05cd7-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="05cd7-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="05cd7-135">NOTES</span></span>

## <span data-ttu-id="05cd7-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05cd7-136">RELATED LINKS</span></span>
