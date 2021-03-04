---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyfilterrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
ms.openlocfilehash: 3bdd96bfe85d6b78476e16a49b2700131ae5aca9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962705"
---
# <span data-ttu-id="ee84c-101">New-AzFirewallPolicyFilterRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ee84c-101">New-AzFirewallPolicyFilterRuleCollection</span></span>

## <span data-ttu-id="ee84c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee84c-102">SYNOPSIS</span></span>
<span data-ttu-id="ee84c-103">Tworzenie nowej kolekcji reguł filtru zasad zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ee84c-103">Create a new Azure Firewall Policy Filter Rule Collection</span></span>

## <span data-ttu-id="ee84c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ee84c-104">SYNTAX</span></span>

```
New-AzFirewallPolicyFilterRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallPolicyRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee84c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ee84c-105">DESCRIPTION</span></span>
<span data-ttu-id="ee84c-106">Polecenie **cmdlet New-AzFirewallPolicyFilterRuleCollection** tworzy kolekcję reguł filtru dla zasad zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ee84c-106">The **New-AzFirewallPolicyFilterRuleCollection** cmdlet creates a Filter rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="ee84c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ee84c-107">EXAMPLES</span></span>

### <span data-ttu-id="ee84c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ee84c-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyFilterRuleCollection -Name FR1 -Priority 400 -Rule $appRule1 ,$appRule2 -ActionType "Allow"
```

<span data-ttu-id="ee84c-109">W tym przykładzie jest tworzyna reguła filtru z 2 warunkami reguły</span><span class="sxs-lookup"><span data-stu-id="ee84c-109">This example creates a Filter rule with 2 rule conditions</span></span>

## <span data-ttu-id="ee84c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee84c-110">PARAMETERS</span></span>

### <span data-ttu-id="ee84c-111">- ActionType</span><span class="sxs-lookup"><span data-stu-id="ee84c-111">-ActionType</span></span>
<span data-ttu-id="ee84c-112">Akcja zbioru reguł</span><span class="sxs-lookup"><span data-stu-id="ee84c-112">The action of the rule collection</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee84c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee84c-113">-DefaultProfile</span></span>
<span data-ttu-id="ee84c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ee84c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee84c-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ee84c-115">-Name</span></span>
<span data-ttu-id="ee84c-116">Nazwa zbioru reguł aplikacji</span><span class="sxs-lookup"><span data-stu-id="ee84c-116">The name of the Application Rule Collection</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee84c-117">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="ee84c-117">-Priority</span></span>
<span data-ttu-id="ee84c-118">Priorytet zbioru reguł</span><span class="sxs-lookup"><span data-stu-id="ee84c-118">The priority of the rule collection</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee84c-119">— reguła</span><span class="sxs-lookup"><span data-stu-id="ee84c-119">-Rule</span></span>
<span data-ttu-id="ee84c-120">Lista reguł aplikacji</span><span class="sxs-lookup"><span data-stu-id="ee84c-120">The list of application rules</span></span>

```yaml
Type: PSAzureFirewallPolicyRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee84c-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ee84c-121">-Confirm</span></span>
<span data-ttu-id="ee84c-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ee84c-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee84c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee84c-123">-WhatIf</span></span>
<span data-ttu-id="ee84c-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee84c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee84c-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ee84c-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee84c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee84c-126">CommonParameters</span></span>
<span data-ttu-id="ee84c-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee84c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee84c-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee84c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee84c-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee84c-129">INPUTS</span></span>

### <span data-ttu-id="ee84c-130">Brak</span><span class="sxs-lookup"><span data-stu-id="ee84c-130">None</span></span>

## <span data-ttu-id="ee84c-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee84c-131">OUTPUTS</span></span>

### <span data-ttu-id="ee84c-132">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="ee84c-132">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="ee84c-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ee84c-133">NOTES</span></span>

## <span data-ttu-id="ee84c-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee84c-134">RELATED LINKS</span></span>
