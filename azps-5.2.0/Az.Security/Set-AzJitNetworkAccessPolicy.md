---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: a316a59492034f0effd2d233ce386cbd6a256c75
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335437"
---
# <span data-ttu-id="2a558-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2a558-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="2a558-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a558-102">SYNOPSIS</span></span>
<span data-ttu-id="2a558-103">Aktualizuje zasady dostępu do sieci w JIT.</span><span class="sxs-lookup"><span data-stu-id="2a558-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="2a558-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a558-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a558-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2a558-105">DESCRIPTION</span></span>
<span data-ttu-id="2a558-106">Aktualizuje zasady dostępu do sieci w JIT.</span><span class="sxs-lookup"><span data-stu-id="2a558-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="2a558-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a558-107">EXAMPLES</span></span>

### <span data-ttu-id="2a558-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2a558-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="2a558-109">Aktualizuje zasady dostępu do sieci w trybie JIT przy użyciu nowych reguł maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2a558-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="2a558-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a558-110">PARAMETERS</span></span>

### <span data-ttu-id="2a558-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a558-111">-DefaultProfile</span></span>
<span data-ttu-id="2a558-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a558-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a558-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="2a558-113">-Kind</span></span>
<span data-ttu-id="2a558-114">Rodzaju.</span><span class="sxs-lookup"><span data-stu-id="2a558-114">Kind.</span></span>

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

### <span data-ttu-id="2a558-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2a558-115">-Location</span></span>
<span data-ttu-id="2a558-116">Pozycję.</span><span class="sxs-lookup"><span data-stu-id="2a558-116">Location.</span></span>

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

### <span data-ttu-id="2a558-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2a558-117">-Name</span></span>
<span data-ttu-id="2a558-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="2a558-118">Resource name.</span></span>

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

### <span data-ttu-id="2a558-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a558-119">-ResourceGroupName</span></span>
<span data-ttu-id="2a558-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2a558-120">Resource group name.</span></span>

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

### <span data-ttu-id="2a558-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2a558-121">-VirtualMachine</span></span>
<span data-ttu-id="2a558-122">Maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="2a558-122">Virtual Machines.</span></span>

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

### <span data-ttu-id="2a558-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a558-123">-Confirm</span></span>
<span data-ttu-id="2a558-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a558-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a558-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a558-125">-WhatIf</span></span>
<span data-ttu-id="2a558-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a558-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a558-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2a558-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a558-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a558-128">CommonParameters</span></span>
<span data-ttu-id="2a558-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a558-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a558-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a558-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a558-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a558-131">INPUTS</span></span>

### <span data-ttu-id="2a558-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2a558-132">None</span></span>

## <span data-ttu-id="2a558-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a558-133">OUTPUTS</span></span>

### <span data-ttu-id="2a558-134">Microsoft. Azure. Commands. Security. models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2a558-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="2a558-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a558-135">NOTES</span></span>

## <span data-ttu-id="2a558-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a558-136">RELATED LINKS</span></span>
