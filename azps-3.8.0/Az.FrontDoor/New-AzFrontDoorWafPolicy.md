---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 2d3811b5605b6f4923abd58c64d8d870ede8d334
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403854"
---
# <span data-ttu-id="39bef-101">New-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="39bef-101">New-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="39bef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39bef-102">SYNOPSIS</span></span>
<span data-ttu-id="39bef-103">Tworzenie zasad SAF</span><span class="sxs-lookup"><span data-stu-id="39bef-103">Create WAF policy</span></span>

## <span data-ttu-id="39bef-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="39bef-104">SYNTAX</span></span>

```
New-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39bef-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="39bef-105">DESCRIPTION</span></span>
<span data-ttu-id="39bef-106">Polecenie **cmdlet New-AzFrontDoorWafPolicy** tworzy nowe zasady Azure WAF w określonej grupie zasobów w ramach bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="39bef-106">The **New-AzFrontDoorWafPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="39bef-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="39bef-107">EXAMPLES</span></span>

### <span data-ttu-id="39bef-108">Przykład 1. Tworzenie zasad SAF</span><span class="sxs-lookup"><span data-stu-id="39bef-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="39bef-109">Tworzenie zasad SAF</span><span class="sxs-lookup"><span data-stu-id="39bef-109">Create WAF policy</span></span>

## <span data-ttu-id="39bef-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39bef-110">PARAMETERS</span></span>

### <span data-ttu-id="39bef-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="39bef-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="39bef-112">Niestandardowa treść odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="39bef-112">Custom Response Body</span></span>

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

### <span data-ttu-id="39bef-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="39bef-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="39bef-114">Niestandardowy kod stanu odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="39bef-114">Custom Response Status Code</span></span>

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

### <span data-ttu-id="39bef-115">— Customrule</span><span class="sxs-lookup"><span data-stu-id="39bef-115">-Customrule</span></span>
<span data-ttu-id="39bef-116">Reguły niestandardowe w zasadach</span><span class="sxs-lookup"><span data-stu-id="39bef-116">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="39bef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39bef-117">-DefaultProfile</span></span>
<span data-ttu-id="39bef-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="39bef-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39bef-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="39bef-119">-EnabledState</span></span>
<span data-ttu-id="39bef-120">Czy zasady są w stanie włączonym, czy wyłączonym.</span><span class="sxs-lookup"><span data-stu-id="39bef-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="39bef-121">Możliwe wartości: "Wyłączone", "Włączone"</span><span class="sxs-lookup"><span data-stu-id="39bef-121">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="39bef-122">- ManagedRule</span><span class="sxs-lookup"><span data-stu-id="39bef-122">-ManagedRule</span></span>
<span data-ttu-id="39bef-123">Reguły zarządzane w zasadach</span><span class="sxs-lookup"><span data-stu-id="39bef-123">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="39bef-124">— tryb</span><span class="sxs-lookup"><span data-stu-id="39bef-124">-Mode</span></span>
<span data-ttu-id="39bef-125">W tym artykule opisano, czy jest on w trybie wykrywania, czy w trybie zapobiegania na poziomie zasad.</span><span class="sxs-lookup"><span data-stu-id="39bef-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="39bef-126">Możliwe wartości to:'Zapobieganie', 'Wykrywanie'</span><span class="sxs-lookup"><span data-stu-id="39bef-126">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="39bef-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="39bef-127">-Name</span></span>
<span data-ttu-id="39bef-128">Nazwa witryny WebApplicationFireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="39bef-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="39bef-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="39bef-129">-RedirectUrl</span></span>
<span data-ttu-id="39bef-130">Adres URL przekierowania</span><span class="sxs-lookup"><span data-stu-id="39bef-130">Redirect URL</span></span>

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

### <span data-ttu-id="39bef-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39bef-131">-ResourceGroupName</span></span>
<span data-ttu-id="39bef-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="39bef-132">The resource group name</span></span>

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

### <span data-ttu-id="39bef-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="39bef-133">-Confirm</span></span>
<span data-ttu-id="39bef-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="39bef-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39bef-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39bef-135">-WhatIf</span></span>
<span data-ttu-id="39bef-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39bef-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39bef-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="39bef-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39bef-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39bef-138">CommonParameters</span></span>
<span data-ttu-id="39bef-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39bef-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39bef-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39bef-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39bef-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39bef-141">INPUTS</span></span>

### <span data-ttu-id="39bef-142">Brak</span><span class="sxs-lookup"><span data-stu-id="39bef-142">None</span></span>

## <span data-ttu-id="39bef-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39bef-143">OUTPUTS</span></span>

### <span data-ttu-id="39bef-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="39bef-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="39bef-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="39bef-145">NOTES</span></span>

## <span data-ttu-id="39bef-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39bef-146">RELATED LINKS</span></span>

<span data-ttu-id="39bef-147">[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="39bef-147">[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
