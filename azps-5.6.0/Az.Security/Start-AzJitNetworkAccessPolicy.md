---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 674f88a30ea036fc496cd6931b3d856a20a25c0a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986483"
---
# <span data-ttu-id="ae82d-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ae82d-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="ae82d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae82d-102">SYNOPSIS</span></span>
<span data-ttu-id="ae82d-103">Wywołuje tymczasowe żądanie dostępu do sieci.</span><span class="sxs-lookup"><span data-stu-id="ae82d-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="ae82d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ae82d-104">SYNTAX</span></span>

### <span data-ttu-id="ae82d-105">ResourceGroupLevelResource (Default)</span><span class="sxs-lookup"><span data-stu-id="ae82d-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae82d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae82d-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae82d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ae82d-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae82d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ae82d-108">DESCRIPTION</span></span>
<span data-ttu-id="ae82d-109">Wywołuje tymczasowe żądanie dostępu do sieci.</span><span class="sxs-lookup"><span data-stu-id="ae82d-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="ae82d-110">Żądanie jest weryfikowane na podstawie skonfigurowanych zasad dostępu sieciowego JIT i, jeśli jest to dozwolone, otwiera połączenie sieciowe zgodnie z żądaniem użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ae82d-110">The request is validated against the configured JIT network access policy and if permitted, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="ae82d-111">Żądanie zostanie zarejestrowane w zasadach do późniejszego przejrzenia i zakończy się po przekroczeniu określonego czasu trwania.</span><span class="sxs-lookup"><span data-stu-id="ae82d-111">The request will be logged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="ae82d-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ae82d-112">EXAMPLES</span></span>

### <span data-ttu-id="ae82d-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ae82d-113">Example 1</span></span>
```powershell
$MyResource = Get-AzResource -Id /subscriptions/xxxxxxx-xxxxx-xxxxx-xxxxxxx/resourceGroups/PolicyDemo/providers/Microsoft.Compute/virtualMachines/PolicyDemoVM1
$JitPolicy = (@{
        id    = $MyResource.ResourceId; 
        ports = (@{
                number                     = 22
                endTimeUtc                 = Get-Date (Get-Date -AsUTC).AddHours(1) -Format O
                allowedSourceAddressPrefix = @($MyPublicIP) 
            })
    })
$ActivationVM = @($JitPolicy)
Start-AzJitNetworkAccessPolicy -ResourceGroupName $($MyResource.ResourceGroupName) -Location $MyResource.Location -Name "default" -VirtualMachine $ActivationVM

```

<span data-ttu-id="ae82d-114">Otwiera połączenie sieciowe na 1 godzinę przez port 22 z mojego publicznego adresu IP (nie jest wyświetlany).</span><span class="sxs-lookup"><span data-stu-id="ae82d-114">Opens up a network connection for 1 hour over port 22 from my public IP (not shown).</span></span>

## <span data-ttu-id="ae82d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae82d-115">PARAMETERS</span></span>

### <span data-ttu-id="ae82d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae82d-116">-DefaultProfile</span></span>
<span data-ttu-id="ae82d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae82d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae82d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae82d-118">-InputObject</span></span>
<span data-ttu-id="ae82d-119">Obiekt Input.</span><span class="sxs-lookup"><span data-stu-id="ae82d-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae82d-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ae82d-120">-Location</span></span>
<span data-ttu-id="ae82d-121">Lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="ae82d-121">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae82d-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ae82d-122">-Name</span></span>
<span data-ttu-id="ae82d-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="ae82d-123">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae82d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae82d-124">-ResourceGroupName</span></span>
<span data-ttu-id="ae82d-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ae82d-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae82d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae82d-126">-ResourceId</span></span>
<span data-ttu-id="ae82d-127">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="ae82d-127">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae82d-128">- VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ae82d-128">-VirtualMachine</span></span>
<span data-ttu-id="ae82d-129">Automatyczne inicjowanie obsługi administracyjnej.</span><span class="sxs-lookup"><span data-stu-id="ae82d-129">Automatic Provisioning.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae82d-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ae82d-130">-Confirm</span></span>
<span data-ttu-id="ae82d-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ae82d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae82d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae82d-132">-WhatIf</span></span>
<span data-ttu-id="ae82d-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae82d-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae82d-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ae82d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae82d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae82d-135">CommonParameters</span></span>
<span data-ttu-id="ae82d-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae82d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae82d-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae82d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae82d-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae82d-138">INPUTS</span></span>

### <span data-ttu-id="ae82d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ae82d-139">System.String</span></span>

### <span data-ttu-id="ae82d-140">Microsoft.Azure.Commands.Security.Cmdlet.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span><span class="sxs-lookup"><span data-stu-id="ae82d-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="ae82d-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae82d-141">OUTPUTS</span></span>

### <span data-ttu-id="ae82d-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ae82d-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="ae82d-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ae82d-143">NOTES</span></span>

## <span data-ttu-id="ae82d-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae82d-144">RELATED LINKS</span></span>
