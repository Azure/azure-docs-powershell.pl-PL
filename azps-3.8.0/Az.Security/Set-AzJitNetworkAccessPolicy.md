---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: a40fba16bd7d361544ca10867d2c575965447c12
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050548"
---
# <span data-ttu-id="cdd26-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cdd26-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="cdd26-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cdd26-102">SYNOPSIS</span></span>
<span data-ttu-id="cdd26-103">Aktualizuje zasady dostępu do sieci w JIT.</span><span class="sxs-lookup"><span data-stu-id="cdd26-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="cdd26-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cdd26-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdd26-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cdd26-105">DESCRIPTION</span></span>
<span data-ttu-id="cdd26-106">Aktualizuje zasady dostępu do sieci w JIT.</span><span class="sxs-lookup"><span data-stu-id="cdd26-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="cdd26-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cdd26-107">EXAMPLES</span></span>

### <span data-ttu-id="cdd26-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cdd26-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="cdd26-109">Aktualizuje zasady dostępu do sieci w trybie JIT przy użyciu nowych reguł maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cdd26-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="cdd26-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cdd26-110">PARAMETERS</span></span>

### <span data-ttu-id="cdd26-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdd26-111">-DefaultProfile</span></span>
<span data-ttu-id="cdd26-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cdd26-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdd26-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="cdd26-113">-Kind</span></span>
<span data-ttu-id="cdd26-114">Rodzaju.</span><span class="sxs-lookup"><span data-stu-id="cdd26-114">Kind.</span></span>

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

### <span data-ttu-id="cdd26-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cdd26-115">-Location</span></span>
<span data-ttu-id="cdd26-116">Pozycję.</span><span class="sxs-lookup"><span data-stu-id="cdd26-116">Location.</span></span>

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

### <span data-ttu-id="cdd26-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cdd26-117">-Name</span></span>
<span data-ttu-id="cdd26-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="cdd26-118">Resource name.</span></span>

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

### <span data-ttu-id="cdd26-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdd26-119">-ResourceGroupName</span></span>
<span data-ttu-id="cdd26-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cdd26-120">Resource group name.</span></span>

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

### <span data-ttu-id="cdd26-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cdd26-121">-VirtualMachine</span></span>
<span data-ttu-id="cdd26-122">Maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="cdd26-122">Virtual Machines.</span></span>

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

### <span data-ttu-id="cdd26-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cdd26-123">-Confirm</span></span>
<span data-ttu-id="cdd26-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdd26-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdd26-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdd26-125">-WhatIf</span></span>
<span data-ttu-id="cdd26-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdd26-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cdd26-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cdd26-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdd26-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdd26-128">CommonParameters</span></span>
<span data-ttu-id="cdd26-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdd26-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdd26-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdd26-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdd26-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cdd26-131">INPUTS</span></span>

### <span data-ttu-id="cdd26-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="cdd26-132">None</span></span>

## <span data-ttu-id="cdd26-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cdd26-133">OUTPUTS</span></span>

### <span data-ttu-id="cdd26-134">Microsoft. Azure. Commands. Security. models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cdd26-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="cdd26-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cdd26-135">NOTES</span></span>

## <span data-ttu-id="cdd26-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cdd26-136">RELATED LINKS</span></span>
