---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 6f8943fb4e75c96a97ad2b7f128d671a8be7c906
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890433"
---
# <span data-ttu-id="ad4e5-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad4e5-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="ad4e5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad4e5-102">SYNOPSIS</span></span>
<span data-ttu-id="ad4e5-103">Tworzy regułę filtru tras dla filtru tras.</span><span class="sxs-lookup"><span data-stu-id="ad4e5-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="ad4e5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad4e5-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad4e5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ad4e5-105">DESCRIPTION</span></span>
<span data-ttu-id="ad4e5-106">Polecenie cmdlet New-AzRouteFilterRuleConfig powoduje utworzenie reguły filtru tras dla filtru tras platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ad4e5-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="ad4e5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad4e5-107">EXAMPLES</span></span>

### <span data-ttu-id="ad4e5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ad4e5-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ad4e5-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="ad4e5-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="ad4e5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad4e5-110">PARAMETERS</span></span>

### <span data-ttu-id="ad4e5-111">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="ad4e5-111">-Access</span></span>
<span data-ttu-id="ad4e5-112">Dostęp do reguły filtrowania tras.</span><span class="sxs-lookup"><span data-stu-id="ad4e5-112">Access for route filter rule.</span></span>
<span data-ttu-id="ad4e5-113">Prawidłowe wartości to allow lub Deny.</span><span class="sxs-lookup"><span data-stu-id="ad4e5-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="ad4e5-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="ad4e5-114">-CommunityList</span></span>
<span data-ttu-id="ad4e5-115">Lista wartości społeczności, według której filtr trasy będzie filtrować.</span><span class="sxs-lookup"><span data-stu-id="ad4e5-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad4e5-116">-DefaultProfile</span></span>
<span data-ttu-id="ad4e5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad4e5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4e5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ad4e5-118">-Force</span></span>
<span data-ttu-id="ad4e5-119">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="ad4e5-119">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4e5-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ad4e5-120">-Name</span></span>
<span data-ttu-id="ad4e5-121">Określa nazwę reguły filtru tras.</span><span class="sxs-lookup"><span data-stu-id="ad4e5-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="ad4e5-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="ad4e5-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="ad4e5-123">Typ reguły filtrowania tras.</span><span class="sxs-lookup"><span data-stu-id="ad4e5-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="ad4e5-124">Prawidłowe wartości: społeczność</span><span class="sxs-lookup"><span data-stu-id="ad4e5-124">Valid values are: Community</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4e5-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad4e5-125">-Confirm</span></span>
<span data-ttu-id="ad4e5-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad4e5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad4e5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad4e5-127">-WhatIf</span></span>
<span data-ttu-id="ad4e5-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad4e5-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad4e5-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ad4e5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad4e5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad4e5-130">CommonParameters</span></span>
<span data-ttu-id="ad4e5-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad4e5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad4e5-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad4e5-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad4e5-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad4e5-133">INPUTS</span></span>

## <span data-ttu-id="ad4e5-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad4e5-134">OUTPUTS</span></span>

### <span data-ttu-id="ad4e5-135">Microsoft. Azure. Commands. Network. models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="ad4e5-135">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="ad4e5-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad4e5-136">NOTES</span></span>
<span data-ttu-id="ad4e5-137">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="ad4e5-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ad4e5-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad4e5-138">RELATED LINKS</span></span>

[<span data-ttu-id="ad4e5-139">Dodaj-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad4e5-139">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ad4e5-140">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad4e5-140">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ad4e5-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad4e5-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ad4e5-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad4e5-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

