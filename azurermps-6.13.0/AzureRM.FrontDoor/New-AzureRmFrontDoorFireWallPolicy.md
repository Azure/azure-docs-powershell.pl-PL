---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: b18f17830dd08f95c3d887ce272ff31e080001a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553579"
---
# <span data-ttu-id="7cfdf-101">New-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="7cfdf-101">New-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="7cfdf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7cfdf-102">SYNOPSIS</span></span>
<span data-ttu-id="7cfdf-103">Tworzenie zasad WAF</span><span class="sxs-lookup"><span data-stu-id="7cfdf-103">Create WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cfdf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7cfdf-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cfdf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7cfdf-105">DESCRIPTION</span></span>
<span data-ttu-id="7cfdf-106">Polecenie cmdlet **New-AzureRmFrontDoorFireWallPolicy** tworzy nowe zasady usługi Azure WAF w określonej grupie zasobów w obszarze bieżący abonament.</span><span class="sxs-lookup"><span data-stu-id="7cfdf-106">The **New-AzureRmFrontDoorFireWallPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="7cfdf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7cfdf-107">EXAMPLES</span></span>

### <span data-ttu-id="7cfdf-108">Przykład 1: Tworzenie zasad WAF</span><span class="sxs-lookup"><span data-stu-id="7cfdf-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorFireWallPolicy -Name $Name -ResourceGroupName $resourceGroupName -Customrule $customRule1 -ManagedRule $managedRule1 -En
abledState Enabled -Mode Prevention


PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="7cfdf-109">Tworzenie zasad WAF</span><span class="sxs-lookup"><span data-stu-id="7cfdf-109">Create WAF policy</span></span>

## <span data-ttu-id="7cfdf-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7cfdf-110">PARAMETERS</span></span>

### <span data-ttu-id="7cfdf-111">-Customrule</span><span class="sxs-lookup"><span data-stu-id="7cfdf-111">-Customrule</span></span>
<span data-ttu-id="7cfdf-112">Reguły niestandardowe w zasadach</span><span class="sxs-lookup"><span data-stu-id="7cfdf-112">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="7cfdf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cfdf-113">-DefaultProfile</span></span>
<span data-ttu-id="7cfdf-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7cfdf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cfdf-115">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="7cfdf-115">-EnabledState</span></span>
<span data-ttu-id="7cfdf-116">Czy zasady są w stanie włączonym, czy wyłączone.</span><span class="sxs-lookup"><span data-stu-id="7cfdf-116">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="7cfdf-117">Możliwe wartości obejmują: "wyłączone", "włączone"</span><span class="sxs-lookup"><span data-stu-id="7cfdf-117">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="7cfdf-118">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="7cfdf-118">-ManagedRule</span></span>
<span data-ttu-id="7cfdf-119">Reguły zarządzane w zasadach</span><span class="sxs-lookup"><span data-stu-id="7cfdf-119">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="7cfdf-120">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="7cfdf-120">-Mode</span></span>
<span data-ttu-id="7cfdf-121">Opisuje, czy jest w trybie wykrywania, czy w trybie zapobiegania na poziomie zasad.</span><span class="sxs-lookup"><span data-stu-id="7cfdf-121">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="7cfdf-122">Możliwe wartości obejmują: "Zapobieganie", "wykrywanie".</span><span class="sxs-lookup"><span data-stu-id="7cfdf-122">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="7cfdf-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7cfdf-123">-Name</span></span>
<span data-ttu-id="7cfdf-124">Nazwa WebApplicationFireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="7cfdf-124">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="7cfdf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cfdf-125">-ResourceGroupName</span></span>
<span data-ttu-id="7cfdf-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7cfdf-126">The resource group name</span></span>

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

### <span data-ttu-id="7cfdf-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7cfdf-127">-Confirm</span></span>
<span data-ttu-id="7cfdf-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cfdf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cfdf-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cfdf-129">-WhatIf</span></span>
<span data-ttu-id="7cfdf-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cfdf-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cfdf-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7cfdf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cfdf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cfdf-132">CommonParameters</span></span>
<span data-ttu-id="7cfdf-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cfdf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cfdf-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cfdf-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cfdf-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7cfdf-135">INPUTS</span></span>

### <span data-ttu-id="7cfdf-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7cfdf-136">System.String</span></span>

## <span data-ttu-id="7cfdf-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7cfdf-137">OUTPUTS</span></span>

### <span data-ttu-id="7cfdf-138">Microsoft. Azure. Commands. FrontDoor. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="7cfdf-138">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="7cfdf-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7cfdf-139">NOTES</span></span>

## <span data-ttu-id="7cfdf-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7cfdf-140">RELATED LINKS</span></span>

<span data-ttu-id="7cfdf-141">[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md) 
 [Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md) 
 [Nowe — AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md) 
 [Nowe — AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="7cfdf-141">[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)
[Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)
[New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span></span>
