---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 0efde69aec3b30c58aee8c42aeb1703215219c2e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502998"
---
# <span data-ttu-id="163f3-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="163f3-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="163f3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="163f3-102">SYNOPSIS</span></span>
<span data-ttu-id="163f3-103">Wywołuje tymczasowe żądanie dostępu do sieci.</span><span class="sxs-lookup"><span data-stu-id="163f3-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="163f3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="163f3-104">SYNTAX</span></span>

### <span data-ttu-id="163f3-105">ResourceGroupLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="163f3-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="163f3-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="163f3-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="163f3-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="163f3-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="163f3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="163f3-108">DESCRIPTION</span></span>
<span data-ttu-id="163f3-109">Wywołuje tymczasowe żądanie dostępu do sieci.</span><span class="sxs-lookup"><span data-stu-id="163f3-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="163f3-110">Żądanie jest weryfikowane na podstawie skonfigurowanych zasad dostępu do sieci JIT i jeśli jest to dozwolone, otwiera połączenie sieciowe zgodnie z żądaniem użytkownika.</span><span class="sxs-lookup"><span data-stu-id="163f3-110">The request is validated against the configured JIT network access policy and if permitted, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="163f3-111">Żądanie zostanie zarejestrowane w zasadach w celu późniejszego przejrzenia i zostanie zakończone po przekroczeniu określonego czasu trwania.</span><span class="sxs-lookup"><span data-stu-id="163f3-111">The request will be logged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="163f3-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="163f3-112">EXAMPLES</span></span>

### <span data-ttu-id="163f3-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="163f3-113">Example 1</span></span>
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

<span data-ttu-id="163f3-114">Otwiera połączenie sieciowe na 1 godzinę w porcie 22 z mojego publicznego adresu IP (niewyświetlanego).</span><span class="sxs-lookup"><span data-stu-id="163f3-114">Opens up a network connection for 1 hour over port 22 from my public IP (not shown).</span></span>

## <span data-ttu-id="163f3-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="163f3-115">PARAMETERS</span></span>

### <span data-ttu-id="163f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="163f3-116">-DefaultProfile</span></span>
<span data-ttu-id="163f3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="163f3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="163f3-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="163f3-118">-InputObject</span></span>
<span data-ttu-id="163f3-119">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="163f3-119">Input Object.</span></span>

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

### <span data-ttu-id="163f3-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="163f3-120">-Location</span></span>
<span data-ttu-id="163f3-121">Pozycję.</span><span class="sxs-lookup"><span data-stu-id="163f3-121">Location.</span></span>

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

### <span data-ttu-id="163f3-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="163f3-122">-Name</span></span>
<span data-ttu-id="163f3-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="163f3-123">Resource name.</span></span>

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

### <span data-ttu-id="163f3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="163f3-124">-ResourceGroupName</span></span>
<span data-ttu-id="163f3-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="163f3-125">Resource group name.</span></span>

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

### <span data-ttu-id="163f3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="163f3-126">-ResourceId</span></span>
<span data-ttu-id="163f3-127">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="163f3-127">Resource ID.</span></span>

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

### <span data-ttu-id="163f3-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="163f3-128">-VirtualMachine</span></span>
<span data-ttu-id="163f3-129">Automatyczne Inicjowanie obsługi.</span><span class="sxs-lookup"><span data-stu-id="163f3-129">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="163f3-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="163f3-130">-Confirm</span></span>
<span data-ttu-id="163f3-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="163f3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="163f3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="163f3-132">-WhatIf</span></span>
<span data-ttu-id="163f3-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="163f3-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="163f3-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="163f3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="163f3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="163f3-135">CommonParameters</span></span>
<span data-ttu-id="163f3-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="163f3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="163f3-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="163f3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="163f3-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="163f3-138">INPUTS</span></span>

### <span data-ttu-id="163f3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="163f3-139">System.String</span></span>

### <span data-ttu-id="163f3-140">Microsoft. Azure. polecenia. Security. cmdlets. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyInitiateInputObject</span><span class="sxs-lookup"><span data-stu-id="163f3-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="163f3-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="163f3-141">OUTPUTS</span></span>

### <span data-ttu-id="163f3-142">Microsoft. Azure. Commands. Security. models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="163f3-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="163f3-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="163f3-143">NOTES</span></span>

## <span data-ttu-id="163f3-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="163f3-144">RELATED LINKS</span></span>
