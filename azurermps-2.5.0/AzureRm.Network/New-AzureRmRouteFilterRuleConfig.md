---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: 2309d49dcd91ddefbcbe0e40379a759d50d5ba2a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899104"
---
# <span data-ttu-id="cc153-101">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cc153-101">New-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="cc153-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc153-102">SYNOPSIS</span></span>
<span data-ttu-id="cc153-103">Tworzy regułę filtru tras dla filtru tras.</span><span class="sxs-lookup"><span data-stu-id="cc153-103">Creates a route filter rule for a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc153-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc153-104">SYNTAX</span></span>

```
New-AzureRmRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc153-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cc153-105">DESCRIPTION</span></span>
<span data-ttu-id="cc153-106">Polecenie cmdlet New-AzureRmRouteFilterRuleConfig powoduje utworzenie reguły filtru tras dla filtru tras platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cc153-106">The New-AzureRmRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="cc153-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc153-107">EXAMPLES</span></span>

### <span data-ttu-id="cc153-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cc153-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="cc153-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="cc153-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="cc153-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc153-110">PARAMETERS</span></span>

### <span data-ttu-id="cc153-111">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="cc153-111">-Access</span></span>
<span data-ttu-id="cc153-112">Dostęp do reguły filtrowania tras.</span><span class="sxs-lookup"><span data-stu-id="cc153-112">Access for route filter rule.</span></span>
<span data-ttu-id="cc153-113">Prawidłowe wartości to allow lub Deny.</span><span class="sxs-lookup"><span data-stu-id="cc153-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="cc153-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="cc153-114">-CommunityList</span></span>
<span data-ttu-id="cc153-115">Lista wartości społeczności, według której filtr trasy będzie filtrować.</span><span class="sxs-lookup"><span data-stu-id="cc153-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="cc153-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc153-116">-DefaultProfile</span></span>
<span data-ttu-id="cc153-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cc153-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc153-118">-Force</span><span class="sxs-lookup"><span data-stu-id="cc153-118">-Force</span></span>
<span data-ttu-id="cc153-119">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="cc153-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="cc153-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cc153-120">-Name</span></span>
<span data-ttu-id="cc153-121">Określa nazwę reguły filtru tras.</span><span class="sxs-lookup"><span data-stu-id="cc153-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="cc153-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="cc153-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="cc153-123">Typ reguły filtrowania tras.</span><span class="sxs-lookup"><span data-stu-id="cc153-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="cc153-124">Prawidłowe wartości: społeczność</span><span class="sxs-lookup"><span data-stu-id="cc153-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="cc153-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cc153-125">-Confirm</span></span>
<span data-ttu-id="cc153-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc153-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc153-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc153-127">-WhatIf</span></span>
<span data-ttu-id="cc153-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc153-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc153-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cc153-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc153-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc153-130">CommonParameters</span></span>
<span data-ttu-id="cc153-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc153-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc153-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc153-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc153-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc153-133">INPUTS</span></span>

## <span data-ttu-id="cc153-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc153-134">OUTPUTS</span></span>

### <span data-ttu-id="cc153-135">Microsoft. Azure. Commands. Network. models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="cc153-135">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="cc153-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc153-136">NOTES</span></span>
<span data-ttu-id="cc153-137">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="cc153-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="cc153-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc153-138">RELATED LINKS</span></span>

[<span data-ttu-id="cc153-139">Dodaj-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cc153-139">Add-AzureRmRouteFilterRuleConfig</span></span>](./Add-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="cc153-140">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cc153-140">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="cc153-141">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cc153-141">Remove-AzureRmRouteFilterRuleConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="cc153-142">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cc153-142">Set-AzureRmRouteFilterRuleConfig</span></span>](./Set-AzureRmRouteFilterRuleConfig.md)

