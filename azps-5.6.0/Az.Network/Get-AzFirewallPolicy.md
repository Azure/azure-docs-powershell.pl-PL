---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
ms.openlocfilehash: 056a70f6c085f3c0a936f9e144708c7258a3d5c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956929"
---
# <span data-ttu-id="8d335-101">Get-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="8d335-101">Get-AzFirewallPolicy</span></span>

## <span data-ttu-id="8d335-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d335-102">SYNOPSIS</span></span>
<span data-ttu-id="8d335-103">Otrzymuje zasady zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="8d335-103">Gets a Azure Firewall Policy</span></span>

## <span data-ttu-id="8d335-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8d335-104">SYNTAX</span></span>

### <span data-ttu-id="8d335-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="8d335-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8d335-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d335-106">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d335-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8d335-107">DESCRIPTION</span></span>
<span data-ttu-id="8d335-108">Polecenie **cmdlet Get-AzFirewallPolicy** pobiera jedną lub więcej zapór w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="8d335-108">The **Get-AzFirewallPolicy** cmdlet gets one or more Firewalls in a resource group</span></span>

## <span data-ttu-id="8d335-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8d335-109">EXAMPLES</span></span>

### <span data-ttu-id="8d335-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8d335-110">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicy -Name firwallPolicy -ResourceGroupName TestRg
```

<span data-ttu-id="8d335-111">W tym przykładzie zasady zapory o nazwie "firewallPolicy" w grupie zasobów "TestRg"</span><span class="sxs-lookup"><span data-stu-id="8d335-111">This example get a firewall policy named "firewallPolicy" in the resource group "TestRg"</span></span>

## <span data-ttu-id="8d335-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d335-112">PARAMETERS</span></span>

### <span data-ttu-id="8d335-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d335-113">-DefaultProfile</span></span>
<span data-ttu-id="8d335-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8d335-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d335-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8d335-115">-Name</span></span>
<span data-ttu-id="8d335-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="8d335-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d335-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d335-117">-ResourceGroupName</span></span>
<span data-ttu-id="8d335-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8d335-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d335-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d335-119">-ResourceId</span></span>
<span data-ttu-id="8d335-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="8d335-120">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d335-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d335-121">CommonParameters</span></span>
<span data-ttu-id="8d335-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d335-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d335-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d335-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d335-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d335-124">INPUTS</span></span>

### <span data-ttu-id="8d335-125">System.String</span><span class="sxs-lookup"><span data-stu-id="8d335-125">System.String</span></span>

## <span data-ttu-id="8d335-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d335-126">OUTPUTS</span></span>

### <span data-ttu-id="8d335-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="8d335-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="8d335-128">System.Collections.generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlet.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="8d335-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8d335-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8d335-129">NOTES</span></span>

## <span data-ttu-id="8d335-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d335-130">RELATED LINKS</span></span>
