---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyfilterrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
ms.openlocfilehash: d5871a9e1a99a27cc0b2728ca3638a0548f42fc6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225375"
---
# <span data-ttu-id="5178e-101">New-AzFirewallPolicyFilterRuleCollection</span><span class="sxs-lookup"><span data-stu-id="5178e-101">New-AzFirewallPolicyFilterRuleCollection</span></span>

## <span data-ttu-id="5178e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5178e-102">SYNOPSIS</span></span>
<span data-ttu-id="5178e-103">Tworzenie nowej kolekcji reguł filtrowania zasad zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="5178e-103">Create a new Azure Firewall Policy Filter Rule Collection</span></span>

## <span data-ttu-id="5178e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5178e-104">SYNTAX</span></span>

```
New-AzFirewallPolicyFilterRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallPolicyRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5178e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5178e-105">DESCRIPTION</span></span>
<span data-ttu-id="5178e-106">Polecenie cmdlet **New-AzFirewallPolicyFilterRuleCollection** tworzy kolekcję reguł filtru dla zasad zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5178e-106">The **New-AzFirewallPolicyFilterRuleCollection** cmdlet creates a Filter rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="5178e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5178e-107">EXAMPLES</span></span>

### <span data-ttu-id="5178e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5178e-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyFilterRuleCollection -Name FR1 -Priority 400 -Rule $appRule1 ,$appRule2 -ActionType "Allow"
```

<span data-ttu-id="5178e-109">W tym przykładzie jest tworzona reguła filtru z dwoma warunkami reguły</span><span class="sxs-lookup"><span data-stu-id="5178e-109">This example creates a Filter rule with 2 rule conditions</span></span>

## <span data-ttu-id="5178e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5178e-110">PARAMETERS</span></span>

### <span data-ttu-id="5178e-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="5178e-111">-ActionType</span></span>
<span data-ttu-id="5178e-112">Akcja kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="5178e-112">The action of the rule collection</span></span>

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

### <span data-ttu-id="5178e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5178e-113">-DefaultProfile</span></span>
<span data-ttu-id="5178e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5178e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5178e-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5178e-115">-Name</span></span>
<span data-ttu-id="5178e-116">Nazwa kolekcji reguł aplikacji</span><span class="sxs-lookup"><span data-stu-id="5178e-116">The name of the Application Rule Collection</span></span>

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

### <span data-ttu-id="5178e-117">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="5178e-117">-Priority</span></span>
<span data-ttu-id="5178e-118">Priorytet kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="5178e-118">The priority of the rule collection</span></span>

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

### <span data-ttu-id="5178e-119">— Reguła</span><span class="sxs-lookup"><span data-stu-id="5178e-119">-Rule</span></span>
<span data-ttu-id="5178e-120">Lista reguł aplikacji</span><span class="sxs-lookup"><span data-stu-id="5178e-120">The list of application rules</span></span>

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

### <span data-ttu-id="5178e-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5178e-121">-Confirm</span></span>
<span data-ttu-id="5178e-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5178e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5178e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5178e-123">-WhatIf</span></span>
<span data-ttu-id="5178e-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5178e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5178e-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5178e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5178e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5178e-126">CommonParameters</span></span>
<span data-ttu-id="5178e-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5178e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5178e-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5178e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5178e-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5178e-129">INPUTS</span></span>

### <span data-ttu-id="5178e-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5178e-130">None</span></span>

## <span data-ttu-id="5178e-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5178e-131">OUTPUTS</span></span>

### <span data-ttu-id="5178e-132">Microsoft. Azure. Commands. Network. models. PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="5178e-132">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="5178e-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5178e-133">NOTES</span></span>

## <span data-ttu-id="5178e-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5178e-134">RELATED LINKS</span></span>
