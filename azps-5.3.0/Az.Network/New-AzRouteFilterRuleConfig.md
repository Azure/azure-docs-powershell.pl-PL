---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d66a684b6cd9b26aa9d616a74a4d2eaabaa891ff
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490957"
---
# <span data-ttu-id="2edbc-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2edbc-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="2edbc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2edbc-102">SYNOPSIS</span></span>
<span data-ttu-id="2edbc-103">Tworzy regułę filtru tras dla filtru tras.</span><span class="sxs-lookup"><span data-stu-id="2edbc-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="2edbc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2edbc-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2edbc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2edbc-105">DESCRIPTION</span></span>
<span data-ttu-id="2edbc-106">Polecenie cmdlet New-AzRouteFilterRuleConfig powoduje utworzenie reguły filtru tras dla filtru tras platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2edbc-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="2edbc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2edbc-107">EXAMPLES</span></span>

### <span data-ttu-id="2edbc-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2edbc-108">Example 1</span></span>
```powershell
PS C:\> $rule1 = New-AzRouteFilterRuleConfig -Name "Rule01" -Access "Allow" -RouteFilterRuleType "Community" -CommunityList "12076:5040"
```

<span data-ttu-id="2edbc-109">Polecenie tworzy nową regułę filtru tras i zapisuje ją w zmiennej $rule 1.</span><span class="sxs-lookup"><span data-stu-id="2edbc-109">The command creates a new route filter rule and stores it in variable $rule1.</span></span>

## <span data-ttu-id="2edbc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2edbc-110">PARAMETERS</span></span>

### <span data-ttu-id="2edbc-111">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="2edbc-111">-Access</span></span>
<span data-ttu-id="2edbc-112">Dostęp do reguły filtrowania tras.</span><span class="sxs-lookup"><span data-stu-id="2edbc-112">Access for route filter rule.</span></span>
<span data-ttu-id="2edbc-113">Prawidłowe wartości to allow lub Deny.</span><span class="sxs-lookup"><span data-stu-id="2edbc-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="2edbc-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="2edbc-114">-CommunityList</span></span>
<span data-ttu-id="2edbc-115">Lista wartości społeczności, według której filtr trasy będzie filtrować.</span><span class="sxs-lookup"><span data-stu-id="2edbc-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2edbc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2edbc-116">-DefaultProfile</span></span>
<span data-ttu-id="2edbc-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2edbc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2edbc-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2edbc-118">-Force</span></span>
<span data-ttu-id="2edbc-119">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="2edbc-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2edbc-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2edbc-120">-Name</span></span>
<span data-ttu-id="2edbc-121">Określa nazwę reguły filtru tras.</span><span class="sxs-lookup"><span data-stu-id="2edbc-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="2edbc-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="2edbc-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="2edbc-123">Typ reguły filtrowania tras.</span><span class="sxs-lookup"><span data-stu-id="2edbc-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="2edbc-124">Prawidłowe wartości: społeczność</span><span class="sxs-lookup"><span data-stu-id="2edbc-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="2edbc-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2edbc-125">-Confirm</span></span>
<span data-ttu-id="2edbc-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2edbc-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2edbc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2edbc-127">-WhatIf</span></span>
<span data-ttu-id="2edbc-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2edbc-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2edbc-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2edbc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2edbc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2edbc-130">CommonParameters</span></span>
<span data-ttu-id="2edbc-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2edbc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2edbc-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2edbc-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2edbc-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2edbc-133">INPUTS</span></span>

### <span data-ttu-id="2edbc-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2edbc-134">None</span></span>

## <span data-ttu-id="2edbc-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2edbc-135">OUTPUTS</span></span>

### <span data-ttu-id="2edbc-136">Microsoft. Azure. Commands. Network. models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="2edbc-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="2edbc-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2edbc-137">NOTES</span></span>
<span data-ttu-id="2edbc-138">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="2edbc-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="2edbc-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2edbc-139">RELATED LINKS</span></span>

[<span data-ttu-id="2edbc-140">Dodaj-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2edbc-140">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2edbc-141">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2edbc-141">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2edbc-142">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2edbc-142">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2edbc-143">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2edbc-143">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2edbc-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2edbc-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="2edbc-145">Nowe — AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2edbc-145">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="2edbc-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2edbc-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="2edbc-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2edbc-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
