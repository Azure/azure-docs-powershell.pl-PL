---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 72e3cf48f112c5e9bb07a8f7eb57dfe3d4c9ee07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543436"
---
# <span data-ttu-id="8441c-101">Set-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8441c-101">Set-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="8441c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8441c-102">SYNOPSIS</span></span>
<span data-ttu-id="8441c-103">Aktualizuje zasady dostępu do sieci w JIT.</span><span class="sxs-lookup"><span data-stu-id="8441c-103">Updates JIT network access policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8441c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8441c-104">SYNTAX</span></span>

```
Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8441c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8441c-105">DESCRIPTION</span></span>
<span data-ttu-id="8441c-106">Aktualizuje zasady dostępu do sieci w JIT.</span><span class="sxs-lookup"><span data-stu-id="8441c-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="8441c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8441c-107">EXAMPLES</span></span>

### <span data-ttu-id="8441c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8441c-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="8441c-109">Aktualizuje zasady dostępu do sieci w trybie JIT przy użyciu nowych reguł maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8441c-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="8441c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8441c-110">PARAMETERS</span></span>

### <span data-ttu-id="8441c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8441c-111">-DefaultProfile</span></span>
<span data-ttu-id="8441c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8441c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8441c-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="8441c-113">-Kind</span></span>
<span data-ttu-id="8441c-114">Rodzaju.</span><span class="sxs-lookup"><span data-stu-id="8441c-114">Kind.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8441c-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8441c-115">-Location</span></span>
<span data-ttu-id="8441c-116">Pozycję.</span><span class="sxs-lookup"><span data-stu-id="8441c-116">Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8441c-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8441c-117">-Name</span></span>
<span data-ttu-id="8441c-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="8441c-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8441c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8441c-119">-ResourceGroupName</span></span>
<span data-ttu-id="8441c-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8441c-120">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8441c-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8441c-121">-VirtualMachine</span></span>
<span data-ttu-id="8441c-122">Virutal.</span><span class="sxs-lookup"><span data-stu-id="8441c-122">Virutal Machines.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyVirtualMachine[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8441c-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8441c-123">-Confirm</span></span>
<span data-ttu-id="8441c-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8441c-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8441c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8441c-125">-WhatIf</span></span>
<span data-ttu-id="8441c-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8441c-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8441c-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8441c-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8441c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8441c-128">CommonParameters</span></span>
<span data-ttu-id="8441c-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8441c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8441c-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8441c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8441c-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8441c-131">INPUTS</span></span>

### <span data-ttu-id="8441c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8441c-132">System.String</span></span>
<span data-ttu-id="8441c-133">Microsoft. Azure. Commands. Security. models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyVirtualMachine []</span><span class="sxs-lookup"><span data-stu-id="8441c-133">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyVirtualMachine[]</span></span>

## <span data-ttu-id="8441c-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8441c-134">OUTPUTS</span></span>

### <span data-ttu-id="8441c-135">Microsoft. Azure. Commands. Security. models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8441c-135">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="8441c-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8441c-136">NOTES</span></span>

## <span data-ttu-id="8441c-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8441c-137">RELATED LINKS</span></span>
