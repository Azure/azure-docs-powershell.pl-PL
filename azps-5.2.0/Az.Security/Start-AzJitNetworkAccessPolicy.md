---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: b992f3a41278ba66c54eeefc0b548eef76b50980
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368034"
---
# <span data-ttu-id="65000-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="65000-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="65000-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="65000-102">SYNOPSIS</span></span>
<span data-ttu-id="65000-103">Wywołuje tymczasowe żądanie dostępu do sieci.</span><span class="sxs-lookup"><span data-stu-id="65000-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="65000-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="65000-104">SYNTAX</span></span>

### <span data-ttu-id="65000-105">ResourceGroupLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="65000-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65000-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="65000-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65000-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="65000-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65000-108">Opis</span><span class="sxs-lookup"><span data-stu-id="65000-108">DESCRIPTION</span></span>
<span data-ttu-id="65000-109">Wywołuje tymczasowe żądanie dostępu do sieci.</span><span class="sxs-lookup"><span data-stu-id="65000-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="65000-110">Żądanie jest weryfikowane na podstawie skonfigurowanych zasad dostępu do sieci JIT i jeśli jest to dozwolone, otwiera połączenie sieciowe zgodnie z żądaniem użytkownika.</span><span class="sxs-lookup"><span data-stu-id="65000-110">The request is validated against the configured JIT network access policy and if permitted, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="65000-111">Żądanie zostanie zarejestrowane w zasadach w celu późniejszego przejrzenia i zostanie zakończone po przekroczeniu określonego czasu trwania.</span><span class="sxs-lookup"><span data-stu-id="65000-111">The request will be logged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="65000-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="65000-112">EXAMPLES</span></span>

### <span data-ttu-id="65000-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="65000-113">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -Kind "Basic" -VirtualMachine $vms

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.S
                    ecurity/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                    Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="65000-114">Otwiera połączenie sieciowe zgodnie z określonymi danymi żądań połączeń.</span><span class="sxs-lookup"><span data-stu-id="65000-114">Opens up a network connection according to the specified connection request data.</span></span>

## <span data-ttu-id="65000-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="65000-115">PARAMETERS</span></span>

### <span data-ttu-id="65000-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65000-116">-DefaultProfile</span></span>
<span data-ttu-id="65000-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="65000-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65000-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="65000-118">-InputObject</span></span>
<span data-ttu-id="65000-119">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="65000-119">Input Object.</span></span>

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

### <span data-ttu-id="65000-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="65000-120">-Location</span></span>
<span data-ttu-id="65000-121">Pozycję.</span><span class="sxs-lookup"><span data-stu-id="65000-121">Location.</span></span>

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

### <span data-ttu-id="65000-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="65000-122">-Name</span></span>
<span data-ttu-id="65000-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="65000-123">Resource name.</span></span>

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

### <span data-ttu-id="65000-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65000-124">-ResourceGroupName</span></span>
<span data-ttu-id="65000-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="65000-125">Resource group name.</span></span>

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

### <span data-ttu-id="65000-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65000-126">-ResourceId</span></span>
<span data-ttu-id="65000-127">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="65000-127">Resource ID.</span></span>

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

### <span data-ttu-id="65000-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="65000-128">-VirtualMachine</span></span>
<span data-ttu-id="65000-129">Automatyczne Inicjowanie obsługi.</span><span class="sxs-lookup"><span data-stu-id="65000-129">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="65000-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="65000-130">-Confirm</span></span>
<span data-ttu-id="65000-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65000-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65000-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65000-132">-WhatIf</span></span>
<span data-ttu-id="65000-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65000-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65000-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="65000-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65000-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65000-135">CommonParameters</span></span>
<span data-ttu-id="65000-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65000-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65000-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65000-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65000-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65000-138">INPUTS</span></span>

### <span data-ttu-id="65000-139">System. String</span><span class="sxs-lookup"><span data-stu-id="65000-139">System.String</span></span>

### <span data-ttu-id="65000-140">Microsoft. Azure. polecenia. Security. cmdlets. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyInitiateInputObject</span><span class="sxs-lookup"><span data-stu-id="65000-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="65000-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="65000-141">OUTPUTS</span></span>

### <span data-ttu-id="65000-142">Microsoft. Azure. Commands. Security. models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="65000-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="65000-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="65000-143">NOTES</span></span>

## <span data-ttu-id="65000-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65000-144">RELATED LINKS</span></span>
