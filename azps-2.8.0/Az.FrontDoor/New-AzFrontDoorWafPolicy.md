---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 242478245188e68fe0a5d86ee7c54aba57d4d056
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705373"
---
# <span data-ttu-id="85947-101">New-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="85947-101">New-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="85947-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85947-102">SYNOPSIS</span></span>
<span data-ttu-id="85947-103">Tworzenie zasad WAF</span><span class="sxs-lookup"><span data-stu-id="85947-103">Create WAF policy</span></span>

## <span data-ttu-id="85947-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85947-104">SYNTAX</span></span>

```
New-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85947-105">Opis</span><span class="sxs-lookup"><span data-stu-id="85947-105">DESCRIPTION</span></span>
<span data-ttu-id="85947-106">Polecenie cmdlet **New-AzFrontDoorWafPolicy** tworzy nowe zasady usługi Azure WAF w określonej grupie zasobów w obszarze bieżący abonament.</span><span class="sxs-lookup"><span data-stu-id="85947-106">The **New-AzFrontDoorWafPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="85947-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85947-107">EXAMPLES</span></span>

### <span data-ttu-id="85947-108">Przykład 1: Tworzenie zasad WAF</span><span class="sxs-lookup"><span data-stu-id="85947-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="85947-109">Tworzenie zasad WAF</span><span class="sxs-lookup"><span data-stu-id="85947-109">Create WAF policy</span></span>

## <span data-ttu-id="85947-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85947-110">PARAMETERS</span></span>

### <span data-ttu-id="85947-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="85947-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="85947-112">Treść niestandardowej odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="85947-112">Custom Response Body</span></span>

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

### <span data-ttu-id="85947-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="85947-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="85947-114">Niestandardowy kod stanu odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="85947-114">Custom Response Status Code</span></span>

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

### <span data-ttu-id="85947-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="85947-115">-Customrule</span></span>
<span data-ttu-id="85947-116">Reguły niestandardowe w zasadach</span><span class="sxs-lookup"><span data-stu-id="85947-116">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="85947-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85947-117">-DefaultProfile</span></span>
<span data-ttu-id="85947-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="85947-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85947-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="85947-119">-EnabledState</span></span>
<span data-ttu-id="85947-120">Czy zasady są w stanie włączonym, czy wyłączone.</span><span class="sxs-lookup"><span data-stu-id="85947-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="85947-121">Możliwe wartości obejmują: "wyłączone", "włączone"</span><span class="sxs-lookup"><span data-stu-id="85947-121">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="85947-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="85947-122">-ManagedRule</span></span>
<span data-ttu-id="85947-123">Reguły zarządzane w zasadach</span><span class="sxs-lookup"><span data-stu-id="85947-123">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="85947-124">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="85947-124">-Mode</span></span>
<span data-ttu-id="85947-125">Opisuje, czy jest w trybie wykrywania, czy w trybie zapobiegania na poziomie zasad.</span><span class="sxs-lookup"><span data-stu-id="85947-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="85947-126">Możliwe wartości obejmują: "Zapobieganie", "wykrywanie".</span><span class="sxs-lookup"><span data-stu-id="85947-126">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="85947-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="85947-127">-Name</span></span>
<span data-ttu-id="85947-128">Nazwa WebApplicationFireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="85947-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="85947-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="85947-129">-RedirectUrl</span></span>
<span data-ttu-id="85947-130">Adres URL przekierowania</span><span class="sxs-lookup"><span data-stu-id="85947-130">Redirect URL</span></span>

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

### <span data-ttu-id="85947-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85947-131">-ResourceGroupName</span></span>
<span data-ttu-id="85947-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="85947-132">The resource group name</span></span>

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

### <span data-ttu-id="85947-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="85947-133">-Confirm</span></span>
<span data-ttu-id="85947-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85947-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85947-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85947-135">-WhatIf</span></span>
<span data-ttu-id="85947-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85947-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85947-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="85947-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85947-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85947-138">CommonParameters</span></span>
<span data-ttu-id="85947-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85947-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85947-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85947-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85947-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85947-141">INPUTS</span></span>

### <span data-ttu-id="85947-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="85947-142">None</span></span>

## <span data-ttu-id="85947-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85947-143">OUTPUTS</span></span>

### <span data-ttu-id="85947-144">Microsoft. Azure. Commands. FrontDoor. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="85947-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="85947-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85947-145">NOTES</span></span>

## <span data-ttu-id="85947-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85947-146">RELATED LINKS</span></span>

<span data-ttu-id="85947-147">[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [Nowe — AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [Nowe — AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="85947-147">[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
