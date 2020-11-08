---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 8ce5369605f419821994c771dc9200e138e5ad7a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052310"
---
# <span data-ttu-id="6b689-101">Get-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="6b689-101">Get-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="6b689-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6b689-102">SYNOPSIS</span></span>
<span data-ttu-id="6b689-103">Pobiera grupę kolekcji reguł zasad zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="6b689-103">Gets a Azure Firewall Policy Rule Collection Group</span></span>

## <span data-ttu-id="6b689-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6b689-104">SYNTAX</span></span>

### <span data-ttu-id="6b689-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6b689-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b689-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b689-106">GetByInputObjectParameterSet</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -Name <String> -AzureFirewallPolicy <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b689-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b689-107">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b689-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6b689-108">DESCRIPTION</span></span>
<span data-ttu-id="6b689-109">Polecenie cmdlet **Get-AzFirewallPolicyRuleCollectionGroup** pobiera RuleCollectionGroup wymienione na podstawie zasad zapory</span><span class="sxs-lookup"><span data-stu-id="6b689-109">The **Get-AzFirewallPolicyRuleCollectionGroup** cmdlet gets the RuleCollectionGroup mentioned from a Firewall Policy</span></span>

## <span data-ttu-id="6b689-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6b689-110">EXAMPLES</span></span>

### <span data-ttu-id="6b689-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6b689-111">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicyRuleCollectionGroup -Name rg1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="6b689-112">W tym przykładzie otrzymano zestaw kolekcji reguł w $fp zasad zapory</span><span class="sxs-lookup"><span data-stu-id="6b689-112">This example get the rule collectionGroup in the firewall policy $fp</span></span>

## <span data-ttu-id="6b689-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b689-113">PARAMETERS</span></span>

### <span data-ttu-id="6b689-114">-AzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="6b689-114">-AzureFirewallPolicy</span></span>
<span data-ttu-id="6b689-115">Zasady zapory.</span><span class="sxs-lookup"><span data-stu-id="6b689-115">Firewall Policy.</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b689-116">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="6b689-116">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="6b689-117">Nazwa zasad zapory</span><span class="sxs-lookup"><span data-stu-id="6b689-117">The Firewall policy name</span></span>

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

### <span data-ttu-id="6b689-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b689-118">-DefaultProfile</span></span>
<span data-ttu-id="6b689-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6b689-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b689-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6b689-120">-Name</span></span>
<span data-ttu-id="6b689-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="6b689-121">The resource name.</span></span>

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

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b689-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b689-122">-ResourceGroupName</span></span>
<span data-ttu-id="6b689-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6b689-123">The resource group name.</span></span>

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

### <span data-ttu-id="6b689-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b689-124">-ResourceId</span></span>
<span data-ttu-id="6b689-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="6b689-125">The resource Id.</span></span>

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

### <span data-ttu-id="6b689-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b689-126">CommonParameters</span></span>
<span data-ttu-id="6b689-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b689-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b689-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b689-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b689-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b689-129">INPUTS</span></span>

### <span data-ttu-id="6b689-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6b689-130">System.String</span></span>

### <span data-ttu-id="6b689-131">Microsoft. Azure. Commands. Network. models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="6b689-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="6b689-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6b689-132">OUTPUTS</span></span>

### <span data-ttu-id="6b689-133">Microsoft. Azure. Commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="6b689-133">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="6b689-134">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. models. PSAzureFirewall, Microsoft. Azure. PowerShell. PowerShell</span><span class="sxs-lookup"><span data-stu-id="6b689-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6b689-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6b689-135">NOTES</span></span>

## <span data-ttu-id="6b689-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b689-136">RELATED LINKS</span></span>
