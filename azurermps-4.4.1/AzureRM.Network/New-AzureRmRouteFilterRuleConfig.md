---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 3c3e20762bcf8e48fc3f01d750419493a81ca8aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716905"
---
# <span data-ttu-id="fce7b-101">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fce7b-101">New-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="fce7b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fce7b-102">SYNOPSIS</span></span>
<span data-ttu-id="fce7b-103">Tworzy regułę filtru tras dla filtru tras.</span><span class="sxs-lookup"><span data-stu-id="fce7b-103">Creates a route filter rule for a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fce7b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fce7b-104">SYNTAX</span></span>

```
New-AzureRmRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fce7b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fce7b-105">DESCRIPTION</span></span>
<span data-ttu-id="fce7b-106">Polecenie cmdlet New-AzureRmRouteFilterRuleConfig powoduje utworzenie reguły filtru tras dla filtru tras platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fce7b-106">The New-AzureRmRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="fce7b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fce7b-107">EXAMPLES</span></span>

### <span data-ttu-id="fce7b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fce7b-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="fce7b-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="fce7b-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="fce7b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fce7b-110">PARAMETERS</span></span>

### <span data-ttu-id="fce7b-111">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="fce7b-111">-Access</span></span>
<span data-ttu-id="fce7b-112">Dostęp do reguły filtrowania tras.</span><span class="sxs-lookup"><span data-stu-id="fce7b-112">Access for route filter rule.</span></span>
<span data-ttu-id="fce7b-113">Prawidłowe wartości to allow lub Deny.</span><span class="sxs-lookup"><span data-stu-id="fce7b-113">Valid values are Allow or Deny.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fce7b-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="fce7b-114">-CommunityList</span></span>
<span data-ttu-id="fce7b-115">Lista wartości społeczności, według której filtr trasy będzie filtrować.</span><span class="sxs-lookup"><span data-stu-id="fce7b-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="fce7b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="fce7b-116">-Force</span></span>
<span data-ttu-id="fce7b-117">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="fce7b-117">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fce7b-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fce7b-118">-Name</span></span>
<span data-ttu-id="fce7b-119">Określa nazwę reguły filtru tras.</span><span class="sxs-lookup"><span data-stu-id="fce7b-119">Specifies a name for the route filter rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fce7b-120">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="fce7b-120">-RouteFilterRuleType</span></span>
<span data-ttu-id="fce7b-121">Typ reguły filtrowania tras.</span><span class="sxs-lookup"><span data-stu-id="fce7b-121">Route Filter Rule Type.</span></span>
<span data-ttu-id="fce7b-122">Prawidłowe wartości: społeczność</span><span class="sxs-lookup"><span data-stu-id="fce7b-122">Valid values are: Community</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fce7b-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fce7b-123">-Confirm</span></span>
<span data-ttu-id="fce7b-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fce7b-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fce7b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fce7b-125">-WhatIf</span></span>
<span data-ttu-id="fce7b-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fce7b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fce7b-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fce7b-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fce7b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fce7b-128">-DefaultProfile</span></span>
<span data-ttu-id="fce7b-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fce7b-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fce7b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fce7b-130">CommonParameters</span></span>
<span data-ttu-id="fce7b-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fce7b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fce7b-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fce7b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fce7b-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fce7b-133">INPUTS</span></span>

## <span data-ttu-id="fce7b-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fce7b-134">OUTPUTS</span></span>

### <span data-ttu-id="fce7b-135">Microsoft. Azure. Commands. Network. models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="fce7b-135">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="fce7b-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fce7b-136">NOTES</span></span>
<span data-ttu-id="fce7b-137">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="fce7b-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="fce7b-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fce7b-138">RELATED LINKS</span></span>

[<span data-ttu-id="fce7b-139">Dodaj-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fce7b-139">Add-AzureRmRouteFilterRuleConfig</span></span>](./Add-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="fce7b-140">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fce7b-140">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="fce7b-141">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fce7b-141">Remove-AzureRmRouteFilterRuleConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="fce7b-142">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fce7b-142">Set-AzureRmRouteFilterRuleConfig</span></span>](./Set-AzureRmRouteFilterRuleConfig.md)

