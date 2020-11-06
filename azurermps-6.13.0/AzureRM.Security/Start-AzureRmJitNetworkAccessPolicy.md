---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 62dccdc3b55caa5d63036ed3298caa5a01514342
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550223"
---
# <span data-ttu-id="5ffb9-101">Start-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5ffb9-101">Start-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="5ffb9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ffb9-102">SYNOPSIS</span></span>
<span data-ttu-id="5ffb9-103">Wywołuje tymczasowe żądanie dostępu do sieci.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-103">Invokes a temporary network access request.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ffb9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ffb9-104">SYNTAX</span></span>

### <span data-ttu-id="5ffb9-105">ResourceGroupLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5ffb9-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ffb9-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="5ffb9-106">ResourceId</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ffb9-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="5ffb9-107">InputObject</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ffb9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5ffb9-108">DESCRIPTION</span></span>
<span data-ttu-id="5ffb9-109">Wywołuje tymczasowe żądanie dostępu do sieci.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="5ffb9-110">Żądanie jest weryfikowane na podstawie skonfigurowanych zasad dostępu do sieci JIT i jeśli permittet, otwiera połączenie sieciowe zgodnie z żądaniem użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-110">The request is validated against the configured JIT network access policy and if permittet, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="5ffb9-111">Żądanie zostanie loged w zasadach w celu późniejszego przejrzenia i zostanie zakończone, gdy określony czas trwania zostanie przekroczony.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-111">The request will be loged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="5ffb9-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ffb9-112">EXAMPLES</span></span>

### <span data-ttu-id="5ffb9-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5ffb9-113">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -Kind "Basic" -VirtualMachine $vms

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.S
                    ecurity/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                    Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="5ffb9-114">Otwiera połączenie sieciowe zgodnie z określonymi danymi żądań połączeń.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-114">Opens up a network connection according to the specified connection request data.</span></span>

## <span data-ttu-id="5ffb9-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ffb9-115">PARAMETERS</span></span>

### <span data-ttu-id="5ffb9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ffb9-116">-DefaultProfile</span></span>
<span data-ttu-id="5ffb9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ffb9-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5ffb9-118">-InputObject</span></span>
<span data-ttu-id="5ffb9-119">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-119">Input Object.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyInitiateInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ffb9-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5ffb9-120">-Location</span></span>
<span data-ttu-id="5ffb9-121">Pozycję.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-121">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ffb9-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5ffb9-122">-Name</span></span>
<span data-ttu-id="5ffb9-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-123">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ffb9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ffb9-124">-ResourceGroupName</span></span>
<span data-ttu-id="5ffb9-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ffb9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ffb9-126">-ResourceId</span></span>
<span data-ttu-id="5ffb9-127">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ffb9-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5ffb9-128">-VirtualMachine</span></span>
<span data-ttu-id="5ffb9-129">Automatyczne Inicjowanie obsługi.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-129">Automatic Provisioning.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ffb9-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ffb9-130">-Confirm</span></span>
<span data-ttu-id="5ffb9-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ffb9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ffb9-132">-WhatIf</span></span>
<span data-ttu-id="5ffb9-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ffb9-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ffb9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ffb9-135">CommonParameters</span></span>
<span data-ttu-id="5ffb9-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ffb9-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ffb9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ffb9-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ffb9-138">INPUTS</span></span>

### <span data-ttu-id="5ffb9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5ffb9-139">System.String</span></span>
<span data-ttu-id="5ffb9-140">Microsoft. Azure. Commands. Security. models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine []</span><span class="sxs-lookup"><span data-stu-id="5ffb9-140">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]</span></span>

## <span data-ttu-id="5ffb9-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ffb9-141">OUTPUTS</span></span>

### <span data-ttu-id="5ffb9-142">Microsoft. Azure. Commands. Security. models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5ffb9-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="5ffb9-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ffb9-143">NOTES</span></span>

## <span data-ttu-id="5ffb9-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ffb9-144">RELATED LINKS</span></span>
