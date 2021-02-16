---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d66a684b6cd9b26aa9d616a74a4d2eaabaa891ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189642"
---
# <span data-ttu-id="1904e-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1904e-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="1904e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1904e-102">SYNOPSIS</span></span>
<span data-ttu-id="1904e-103">Tworzy regułę filtrowania trasy dla filtru trasy.</span><span class="sxs-lookup"><span data-stu-id="1904e-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="1904e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1904e-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1904e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1904e-105">DESCRIPTION</span></span>
<span data-ttu-id="1904e-106">Polecenie New-AzRouteFilterRuleConfig cmdlet tworzy regułę filtrowania trasy dla filtru trasy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1904e-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="1904e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1904e-107">EXAMPLES</span></span>

### <span data-ttu-id="1904e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1904e-108">Example 1</span></span>
```powershell
PS C:\> $rule1 = New-AzRouteFilterRuleConfig -Name "Rule01" -Access "Allow" -RouteFilterRuleType "Community" -CommunityList "12076:5040"
```

<span data-ttu-id="1904e-109">Polecenie tworzy nową regułę filtrowania trasy i przechowuje ją w zmiennym $rule 1.</span><span class="sxs-lookup"><span data-stu-id="1904e-109">The command creates a new route filter rule and stores it in variable $rule1.</span></span>

## <span data-ttu-id="1904e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1904e-110">PARAMETERS</span></span>

### <span data-ttu-id="1904e-111">— Access</span><span class="sxs-lookup"><span data-stu-id="1904e-111">-Access</span></span>
<span data-ttu-id="1904e-112">Dostęp do reguły filtrowania trasy.</span><span class="sxs-lookup"><span data-stu-id="1904e-112">Access for route filter rule.</span></span>
<span data-ttu-id="1904e-113">Prawidłowe wartości to Allow (Zezwalaj) lub Deny (Odmów).</span><span class="sxs-lookup"><span data-stu-id="1904e-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="1904e-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="1904e-114">-CommunityList</span></span>
<span data-ttu-id="1904e-115">Lista wartości społeczności, według których będzie filtrowany filtr trasy</span><span class="sxs-lookup"><span data-stu-id="1904e-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="1904e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1904e-116">-DefaultProfile</span></span>
<span data-ttu-id="1904e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1904e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1904e-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="1904e-118">-Force</span></span>
<span data-ttu-id="1904e-119">Nie pytaj o potwierdzenie, czy chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="1904e-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1904e-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1904e-120">-Name</span></span>
<span data-ttu-id="1904e-121">Określa nazwę reguły filtrowania trasy.</span><span class="sxs-lookup"><span data-stu-id="1904e-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="1904e-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="1904e-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="1904e-123">Typ reguły filtru trasy.</span><span class="sxs-lookup"><span data-stu-id="1904e-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="1904e-124">Prawidłowe wartości to: Community</span><span class="sxs-lookup"><span data-stu-id="1904e-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="1904e-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1904e-125">-Confirm</span></span>
<span data-ttu-id="1904e-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1904e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1904e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1904e-127">-WhatIf</span></span>
<span data-ttu-id="1904e-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1904e-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1904e-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1904e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1904e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1904e-130">CommonParameters</span></span>
<span data-ttu-id="1904e-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1904e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1904e-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1904e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1904e-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1904e-133">INPUTS</span></span>

### <span data-ttu-id="1904e-134">Brak</span><span class="sxs-lookup"><span data-stu-id="1904e-134">None</span></span>

## <span data-ttu-id="1904e-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1904e-135">OUTPUTS</span></span>

### <span data-ttu-id="1904e-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="1904e-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="1904e-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1904e-137">NOTES</span></span>
<span data-ttu-id="1904e-138">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="1904e-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="1904e-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1904e-139">RELATED LINKS</span></span>

[<span data-ttu-id="1904e-140">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1904e-140">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1904e-141">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1904e-141">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1904e-142">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1904e-142">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1904e-143">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1904e-143">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1904e-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1904e-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="1904e-145">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1904e-145">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="1904e-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1904e-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="1904e-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1904e-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
