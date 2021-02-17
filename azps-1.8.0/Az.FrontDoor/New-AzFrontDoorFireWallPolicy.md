---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: 9b1339d138087207b84a7f515c66bd9964420dcd
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401491"
---
# <span data-ttu-id="b40f2-101">New-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="b40f2-101">New-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="b40f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b40f2-102">SYNOPSIS</span></span>
<span data-ttu-id="b40f2-103">Tworzenie zasad SAF</span><span class="sxs-lookup"><span data-stu-id="b40f2-103">Create WAF policy</span></span>

## <span data-ttu-id="b40f2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b40f2-104">SYNTAX</span></span>

```
New-AzFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b40f2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b40f2-105">DESCRIPTION</span></span>
<span data-ttu-id="b40f2-106">Polecenie **cmdlet New-AzFrontDoorFireWallPolicy** tworzy nowe zasady Azure WAF w określonej grupie zasobów w ramach bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b40f2-106">The **New-AzFrontDoorFireWallPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="b40f2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b40f2-107">EXAMPLES</span></span>

### <span data-ttu-id="b40f2-108">Przykład 1. Tworzenie zasad SAF</span><span class="sxs-lookup"><span data-stu-id="b40f2-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="b40f2-109">Tworzenie zasad SAF</span><span class="sxs-lookup"><span data-stu-id="b40f2-109">Create WAF policy</span></span>

## <span data-ttu-id="b40f2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b40f2-110">PARAMETERS</span></span>

### <span data-ttu-id="b40f2-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="b40f2-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="b40f2-112">Niestandardowa treść odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="b40f2-112">Custom Response Body</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b40f2-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="b40f2-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="b40f2-114">Niestandardowy kod stanu odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="b40f2-114">Custom Response Status Code</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b40f2-115">— Customrule</span><span class="sxs-lookup"><span data-stu-id="b40f2-115">-Customrule</span></span>
<span data-ttu-id="b40f2-116">Reguły niestandardowe w zasadach</span><span class="sxs-lookup"><span data-stu-id="b40f2-116">Custom rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b40f2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b40f2-117">-DefaultProfile</span></span>
<span data-ttu-id="b40f2-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b40f2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b40f2-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="b40f2-119">-EnabledState</span></span>
<span data-ttu-id="b40f2-120">Czy zasady są w stanie włączonym, czy wyłączonym.</span><span class="sxs-lookup"><span data-stu-id="b40f2-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="b40f2-121">Możliwe wartości: "Wyłączone", "Włączone"</span><span class="sxs-lookup"><span data-stu-id="b40f2-121">Possible values include: 'Disabled', 'Enabled'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b40f2-122">- ManagedRule</span><span class="sxs-lookup"><span data-stu-id="b40f2-122">-ManagedRule</span></span>
<span data-ttu-id="b40f2-123">Reguły zarządzane w zasadach</span><span class="sxs-lookup"><span data-stu-id="b40f2-123">Managed rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b40f2-124">— tryb</span><span class="sxs-lookup"><span data-stu-id="b40f2-124">-Mode</span></span>
<span data-ttu-id="b40f2-125">W tym artykule opisano, czy jest on w trybie wykrywania, czy w trybie zapobiegania na poziomie zasad.</span><span class="sxs-lookup"><span data-stu-id="b40f2-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="b40f2-126">Możliwe wartości to: 'Zapobieganie', 'Wykrywanie'.</span><span class="sxs-lookup"><span data-stu-id="b40f2-126">Possible values include:'Prevention', 'Detection'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMode
Parameter Sets: (All)
Aliases:
Accepted values: Prevention, Detection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b40f2-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b40f2-127">-Name</span></span>
<span data-ttu-id="b40f2-128">Nazwa witryny WebApplicationFireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="b40f2-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="b40f2-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="b40f2-129">-RedirectUrl</span></span>
<span data-ttu-id="b40f2-130">Adres URL przekierowania</span><span class="sxs-lookup"><span data-stu-id="b40f2-130">Redirect URL</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b40f2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b40f2-131">-ResourceGroupName</span></span>
<span data-ttu-id="b40f2-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b40f2-132">The resource group name</span></span>

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

### <span data-ttu-id="b40f2-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b40f2-133">-Confirm</span></span>
<span data-ttu-id="b40f2-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b40f2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b40f2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b40f2-135">-WhatIf</span></span>
<span data-ttu-id="b40f2-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b40f2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b40f2-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b40f2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b40f2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b40f2-138">CommonParameters</span></span>
<span data-ttu-id="b40f2-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b40f2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b40f2-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b40f2-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b40f2-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b40f2-141">INPUTS</span></span>

### <span data-ttu-id="b40f2-142">Brak</span><span class="sxs-lookup"><span data-stu-id="b40f2-142">None</span></span>

## <span data-ttu-id="b40f2-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b40f2-143">OUTPUTS</span></span>

### <span data-ttu-id="b40f2-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="b40f2-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="b40f2-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b40f2-145">NOTES</span></span>

## <span data-ttu-id="b40f2-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b40f2-146">RELATED LINKS</span></span>

<span data-ttu-id="b40f2-147">[Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md) 
 [Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md) 
 [Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md) 
 [New-AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md) 
 [New-AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="b40f2-147">[Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md)
[Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md)
[Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)
[New-AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md)
[New-AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span></span>
