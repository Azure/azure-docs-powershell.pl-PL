---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: 657c18a02f05f2e318fe676a672e894a4aec9e50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551160"
---
# <span data-ttu-id="03ba7-101">New-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="03ba7-101">New-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="03ba7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="03ba7-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="03ba7-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03ba7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03ba7-104">SYNTAX</span></span>

```
New-AzureRmServiceEndpointPolicy -Name <String>
 [-ServiceEndpointDefinitions <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition]>]
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03ba7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="03ba7-105">DESCRIPTION</span></span>
<span data-ttu-id="03ba7-106">Polecenie cmdlet **New-AzureRmServiceEndpointPolicy** Utwórz zasadę punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="03ba7-106">The **New-AzureRmServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="03ba7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03ba7-107">EXAMPLES</span></span>

### <span data-ttu-id="03ba7-108">Przykład 1. Tworzenie zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="03ba7-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzureRmServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="03ba7-109">To polecenie tworzy zasadę punktu końcowego usługi o nazwie Policy1 z definicjami zdefiniowanymi przez obiekt $serviceEndpointDefinition i zapisuje je w zmiennej $serviceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="03ba7-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="03ba7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03ba7-110">PARAMETERS</span></span>

### <span data-ttu-id="03ba7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03ba7-111">-DefaultProfile</span></span>
<span data-ttu-id="03ba7-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="03ba7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03ba7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="03ba7-113">-Force</span></span>
<span data-ttu-id="03ba7-114">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="03ba7-114">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ba7-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="03ba7-115">-Name</span></span>
<span data-ttu-id="03ba7-116">Nazwa podsieci</span><span class="sxs-lookup"><span data-stu-id="03ba7-116">The name of the subnet</span></span>

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

### <span data-ttu-id="03ba7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03ba7-117">-ResourceGroupName</span></span>
<span data-ttu-id="03ba7-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="03ba7-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ba7-119">-ServiceEndpointDefinitions</span><span class="sxs-lookup"><span data-stu-id="03ba7-119">-ServiceEndpointDefinitions</span></span>
<span data-ttu-id="03ba7-120">Lista definicji punktów końcowych usługi</span><span class="sxs-lookup"><span data-stu-id="03ba7-120">List of service endpoint definitions</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ba7-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="03ba7-121">-Confirm</span></span>
<span data-ttu-id="03ba7-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03ba7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03ba7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03ba7-123">-WhatIf</span></span>
<span data-ttu-id="03ba7-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03ba7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03ba7-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="03ba7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03ba7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03ba7-126">CommonParameters</span></span>
<span data-ttu-id="03ba7-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03ba7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="03ba7-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03ba7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03ba7-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03ba7-129">INPUTS</span></span>

### <span data-ttu-id="03ba7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="03ba7-130">System.String</span></span>


## <span data-ttu-id="03ba7-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03ba7-131">OUTPUTS</span></span>

### <span data-ttu-id="03ba7-132">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="03ba7-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="03ba7-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03ba7-133">NOTES</span></span>

## <span data-ttu-id="03ba7-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03ba7-134">RELATED LINKS</span></span>
