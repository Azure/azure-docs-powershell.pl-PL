---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
ms.openlocfilehash: 9b03a33ebea52e57950e46c894e95ffefe520b4e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869851"
---
# <span data-ttu-id="6be49-101">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="6be49-101">New-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="6be49-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6be49-102">SYNOPSIS</span></span>
<span data-ttu-id="6be49-103">Tworzy zasadę punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="6be49-103">Creates a service endpoint policy.</span></span>

## <span data-ttu-id="6be49-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6be49-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicy -Name <String>
 [-ServiceEndpointPolicyDefinition <PSServiceEndpointPolicyDefinition[]>] -ResourceGroupName <String>
 -Location <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6be49-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6be49-105">DESCRIPTION</span></span>
<span data-ttu-id="6be49-106">Polecenie cmdlet **New-AzServiceEndpointPolicy** Utwórz zasadę punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="6be49-106">The **New-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="6be49-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6be49-107">EXAMPLES</span></span>

### <span data-ttu-id="6be49-108">Przykład 1. Tworzenie zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="6be49-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="6be49-109">To polecenie tworzy zasadę punktu końcowego usługi o nazwie Policy1 z definicjami zdefiniowanymi przez obiekt $serviceEndpointDefinition i zapisuje je w zmiennej $serviceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="6be49-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="6be49-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6be49-110">PARAMETERS</span></span>

### <span data-ttu-id="6be49-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6be49-111">-DefaultProfile</span></span>
<span data-ttu-id="6be49-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6be49-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6be49-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6be49-113">-Force</span></span>
<span data-ttu-id="6be49-114">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="6be49-114">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6be49-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6be49-115">-Location</span></span>
<span data-ttu-id="6be49-116">pozycję.</span><span class="sxs-lookup"><span data-stu-id="6be49-116">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6be49-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6be49-117">-Name</span></span>
<span data-ttu-id="6be49-118">Nazwa podsieci</span><span class="sxs-lookup"><span data-stu-id="6be49-118">The name of the subnet</span></span>

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

### <span data-ttu-id="6be49-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6be49-119">-ResourceGroupName</span></span>
<span data-ttu-id="6be49-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6be49-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6be49-121">-ServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6be49-121">-ServiceEndpointPolicyDefinition</span></span>
<span data-ttu-id="6be49-122">Lista definicji punktów końcowych usługi</span><span class="sxs-lookup"><span data-stu-id="6be49-122">List of service endpoint definitions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6be49-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6be49-123">-Confirm</span></span>
<span data-ttu-id="6be49-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6be49-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6be49-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6be49-125">-WhatIf</span></span>
<span data-ttu-id="6be49-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6be49-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6be49-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6be49-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6be49-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6be49-128">CommonParameters</span></span>
<span data-ttu-id="6be49-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6be49-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6be49-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6be49-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6be49-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6be49-131">INPUTS</span></span>

### <span data-ttu-id="6be49-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6be49-132">System.String</span></span>

## <span data-ttu-id="6be49-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6be49-133">OUTPUTS</span></span>

### <span data-ttu-id="6be49-134">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="6be49-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="6be49-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6be49-135">NOTES</span></span>

## <span data-ttu-id="6be49-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6be49-136">RELATED LINKS</span></span>

[<span data-ttu-id="6be49-137">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="6be49-137">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="6be49-138">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="6be49-138">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="6be49-139">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="6be49-139">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
