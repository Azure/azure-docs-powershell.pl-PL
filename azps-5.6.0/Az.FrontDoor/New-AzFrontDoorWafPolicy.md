---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 5c39a86b29ce27ea57d51e7e3bfb048560ef1ee6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970833"
---
# <span data-ttu-id="52c6b-101">New-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="52c6b-101">New-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="52c6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52c6b-102">SYNOPSIS</span></span>
<span data-ttu-id="52c6b-103">Tworzenie zasad SAF</span><span class="sxs-lookup"><span data-stu-id="52c6b-103">Create WAF policy</span></span>

## <span data-ttu-id="52c6b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="52c6b-104">SYNTAX</span></span>

```
New-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52c6b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="52c6b-105">DESCRIPTION</span></span>
<span data-ttu-id="52c6b-106">Polecenie **cmdlet New-AzFrontDoorWafPolicy** tworzy nowe zasady Azure WAF w określonej grupie zasobów w ramach bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="52c6b-106">The **New-AzFrontDoorWafPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="52c6b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="52c6b-107">EXAMPLES</span></span>

### <span data-ttu-id="52c6b-108">Przykład 1. Tworzenie zasad WAF</span><span class="sxs-lookup"><span data-stu-id="52c6b-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="52c6b-109">Tworzenie zasad SAF</span><span class="sxs-lookup"><span data-stu-id="52c6b-109">Create WAF policy</span></span>

## <span data-ttu-id="52c6b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52c6b-110">PARAMETERS</span></span>

### <span data-ttu-id="52c6b-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="52c6b-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="52c6b-112">Niestandardowa treść odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="52c6b-112">Custom Response Body</span></span>

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

### <span data-ttu-id="52c6b-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="52c6b-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="52c6b-114">Niestandardowy kod stanu odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="52c6b-114">Custom Response Status Code</span></span>

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

### <span data-ttu-id="52c6b-115">— Customrule</span><span class="sxs-lookup"><span data-stu-id="52c6b-115">-Customrule</span></span>
<span data-ttu-id="52c6b-116">Reguły niestandardowe w zasadach</span><span class="sxs-lookup"><span data-stu-id="52c6b-116">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="52c6b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52c6b-117">-DefaultProfile</span></span>
<span data-ttu-id="52c6b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="52c6b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52c6b-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="52c6b-119">-EnabledState</span></span>
<span data-ttu-id="52c6b-120">Czy zasady są w stanie włączonym, czy wyłączonym.</span><span class="sxs-lookup"><span data-stu-id="52c6b-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="52c6b-121">Możliwe wartości: "Wyłączone", "Włączone"</span><span class="sxs-lookup"><span data-stu-id="52c6b-121">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="52c6b-122">- ManagedRule</span><span class="sxs-lookup"><span data-stu-id="52c6b-122">-ManagedRule</span></span>
<span data-ttu-id="52c6b-123">Reguły zarządzane w zasadach</span><span class="sxs-lookup"><span data-stu-id="52c6b-123">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="52c6b-124">— tryb</span><span class="sxs-lookup"><span data-stu-id="52c6b-124">-Mode</span></span>
<span data-ttu-id="52c6b-125">W tym artykule opisano, czy jest on w trybie wykrywania, czy w trybie zapobiegania na poziomie zasad.</span><span class="sxs-lookup"><span data-stu-id="52c6b-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="52c6b-126">Możliwe wartości to:'Zapobieganie', 'Wykrywanie'</span><span class="sxs-lookup"><span data-stu-id="52c6b-126">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="52c6b-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="52c6b-127">-Name</span></span>
<span data-ttu-id="52c6b-128">Nazwa witryny WebApplicationFireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="52c6b-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="52c6b-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="52c6b-129">-RedirectUrl</span></span>
<span data-ttu-id="52c6b-130">Adres URL przekierowania</span><span class="sxs-lookup"><span data-stu-id="52c6b-130">Redirect URL</span></span>

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

### <span data-ttu-id="52c6b-131">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="52c6b-131">-RequestBodyCheck</span></span>
<span data-ttu-id="52c6b-132">Definiuje, czy treść powinna być sprawdzana przez reguły zarządzane.</span><span class="sxs-lookup"><span data-stu-id="52c6b-132">Defines if the body should be inspected by managed rules.</span></span> <span data-ttu-id="52c6b-133">Możliwe wartości: "Włączone", "Wyłączone"</span><span class="sxs-lookup"><span data-stu-id="52c6b-133">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="52c6b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52c6b-134">-ResourceGroupName</span></span>
<span data-ttu-id="52c6b-135">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="52c6b-135">The resource group name</span></span>

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

### <span data-ttu-id="52c6b-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="52c6b-136">-Confirm</span></span>
<span data-ttu-id="52c6b-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="52c6b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52c6b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52c6b-138">-WhatIf</span></span>
<span data-ttu-id="52c6b-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52c6b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52c6b-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="52c6b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52c6b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52c6b-141">CommonParameters</span></span>
<span data-ttu-id="52c6b-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52c6b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52c6b-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52c6b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52c6b-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52c6b-144">INPUTS</span></span>

### <span data-ttu-id="52c6b-145">Brak</span><span class="sxs-lookup"><span data-stu-id="52c6b-145">None</span></span>

## <span data-ttu-id="52c6b-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52c6b-146">OUTPUTS</span></span>

### <span data-ttu-id="52c6b-147">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="52c6b-147">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="52c6b-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="52c6b-148">NOTES</span></span>

## <span data-ttu-id="52c6b-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52c6b-149">RELATED LINKS</span></span>

<span data-ttu-id="52c6b-150">[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="52c6b-150">[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
