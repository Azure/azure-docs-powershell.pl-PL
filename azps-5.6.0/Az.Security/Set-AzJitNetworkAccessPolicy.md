---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 0588929d8f45c04275e2d79823ed86c9db787060
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977770"
---
# <span data-ttu-id="967b3-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="967b3-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="967b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="967b3-102">SYNOPSIS</span></span>
<span data-ttu-id="967b3-103">Aktualizuje zasady dostępu do sieci JIT.</span><span class="sxs-lookup"><span data-stu-id="967b3-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="967b3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="967b3-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="967b3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="967b3-105">DESCRIPTION</span></span>
<span data-ttu-id="967b3-106">Aktualizuje zasady dostępu do sieci JIT.</span><span class="sxs-lookup"><span data-stu-id="967b3-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="967b3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="967b3-107">EXAMPLES</span></span>

### <span data-ttu-id="967b3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="967b3-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="967b3-109">Aktualizuje zasady dostępu sieciowego JIT przy użyciu nowych reguł maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="967b3-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="967b3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="967b3-110">PARAMETERS</span></span>

### <span data-ttu-id="967b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="967b3-111">-DefaultProfile</span></span>
<span data-ttu-id="967b3-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="967b3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="967b3-113">— Rodzaj</span><span class="sxs-lookup"><span data-stu-id="967b3-113">-Kind</span></span>
<span data-ttu-id="967b3-114">Jit Network Access Policy Kind.</span><span class="sxs-lookup"><span data-stu-id="967b3-114">Jit Network Access Policy Kind.</span></span>

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

### <span data-ttu-id="967b3-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="967b3-115">-Location</span></span>
<span data-ttu-id="967b3-116">Lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="967b3-116">Location.</span></span>

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

### <span data-ttu-id="967b3-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="967b3-117">-Name</span></span>
<span data-ttu-id="967b3-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="967b3-118">Resource name.</span></span>

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

### <span data-ttu-id="967b3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="967b3-119">-ResourceGroupName</span></span>
<span data-ttu-id="967b3-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="967b3-120">Resource group name.</span></span>

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

### <span data-ttu-id="967b3-121">- VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="967b3-121">-VirtualMachine</span></span>
<span data-ttu-id="967b3-122">Maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="967b3-122">Virtual Machines.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyVirtualMachine[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="967b3-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="967b3-123">-Confirm</span></span>
<span data-ttu-id="967b3-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="967b3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="967b3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="967b3-125">-WhatIf</span></span>
<span data-ttu-id="967b3-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="967b3-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="967b3-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="967b3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="967b3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="967b3-128">CommonParameters</span></span>
<span data-ttu-id="967b3-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="967b3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="967b3-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="967b3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="967b3-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="967b3-131">INPUTS</span></span>

### <span data-ttu-id="967b3-132">Brak</span><span class="sxs-lookup"><span data-stu-id="967b3-132">None</span></span>

## <span data-ttu-id="967b3-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="967b3-133">OUTPUTS</span></span>

### <span data-ttu-id="967b3-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="967b3-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="967b3-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="967b3-135">NOTES</span></span>

## <span data-ttu-id="967b3-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="967b3-136">RELATED LINKS</span></span>
