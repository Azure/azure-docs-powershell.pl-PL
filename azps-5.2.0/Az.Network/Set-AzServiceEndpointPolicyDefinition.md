---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 46d86b6a910abcd00257277f61bb44dd426ab945
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357478"
---
# <span data-ttu-id="19d34-101">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="19d34-101">Set-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="19d34-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="19d34-102">SYNOPSIS</span></span>
<span data-ttu-id="19d34-103">Aktualizuje definicję zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="19d34-103">Updates a service endpoint policy definition.</span></span>

## <span data-ttu-id="19d34-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="19d34-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19d34-105">Opis</span><span class="sxs-lookup"><span data-stu-id="19d34-105">DESCRIPTION</span></span>
<span data-ttu-id="19d34-106">Polecenie cmdlet **Set-AzServiceEndpointPolicyDefinition** Tworzenie definicji zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="19d34-106">The **Set-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="19d34-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="19d34-107">EXAMPLES</span></span>

### <span data-ttu-id="19d34-108">Przykład 1: aktualizowanie definicji zasad punktu końcowego usługi w zasadzie punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="19d34-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="19d34-109">To polecenie aktualizuje definicję zasad punktu końcowego usługi o nazwie Policydef1 w zasadach punktu końcowego usługi zdefiniowanych przez $ServiceEndpointPolicy obiektu.</span><span class="sxs-lookup"><span data-stu-id="19d34-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="19d34-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="19d34-110">PARAMETERS</span></span>

### <span data-ttu-id="19d34-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19d34-111">-DefaultProfile</span></span>
<span data-ttu-id="19d34-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="19d34-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19d34-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="19d34-113">-Description</span></span>
<span data-ttu-id="19d34-114">Opis definicji</span><span class="sxs-lookup"><span data-stu-id="19d34-114">The description of the definition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19d34-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="19d34-115">-Name</span></span>
<span data-ttu-id="19d34-116">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="19d34-116">The name of the rule</span></span>

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

### <span data-ttu-id="19d34-117">-Service</span><span class="sxs-lookup"><span data-stu-id="19d34-117">-Service</span></span>
<span data-ttu-id="19d34-118">Nazwa usługi</span><span class="sxs-lookup"><span data-stu-id="19d34-118">Name of the service</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19d34-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="19d34-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="19d34-120">NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="19d34-120">The NetworkSecurityGroup</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19d34-121">-Serviceresource</span><span class="sxs-lookup"><span data-stu-id="19d34-121">-ServiceResource</span></span>
<span data-ttu-id="19d34-122">Lista zasobów usług</span><span class="sxs-lookup"><span data-stu-id="19d34-122">List of service resources</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19d34-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="19d34-123">-Confirm</span></span>
<span data-ttu-id="19d34-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19d34-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19d34-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19d34-125">-WhatIf</span></span>
<span data-ttu-id="19d34-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19d34-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19d34-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="19d34-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19d34-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19d34-128">CommonParameters</span></span>
<span data-ttu-id="19d34-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19d34-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19d34-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19d34-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19d34-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19d34-131">INPUTS</span></span>

### <span data-ttu-id="19d34-132">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="19d34-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="19d34-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="19d34-133">OUTPUTS</span></span>

### <span data-ttu-id="19d34-134">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="19d34-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="19d34-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="19d34-135">NOTES</span></span>

## <span data-ttu-id="19d34-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19d34-136">RELATED LINKS</span></span>

[<span data-ttu-id="19d34-137">Dodaj-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="19d34-137">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="19d34-138">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="19d34-138">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="19d34-139">Nowe — AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="19d34-139">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="19d34-140">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="19d34-140">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)
