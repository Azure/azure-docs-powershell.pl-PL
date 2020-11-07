---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 3677b580629360a9f38d808af8df9ec0694bcc61
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709654"
---
# <span data-ttu-id="8ac95-101">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8ac95-101">Add-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="8ac95-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ac95-102">SYNOPSIS</span></span>
<span data-ttu-id="8ac95-103">Dodaje definicję zasad punktu końcowego usługi do określonych zasad.</span><span class="sxs-lookup"><span data-stu-id="8ac95-103">Adds a service endpoint policy definition to a specified policy.</span></span>

## <span data-ttu-id="8ac95-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ac95-104">SYNTAX</span></span>

```
Add-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ac95-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8ac95-105">DESCRIPTION</span></span>
<span data-ttu-id="8ac95-106">Polecenie cmdlet **Add-AzServiceEndpointPolicyDefinition** umożliwia dodanie definicji zasad punktu końcowego usługi do zasad.</span><span class="sxs-lookup"><span data-stu-id="8ac95-106">The **Add-AzServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="8ac95-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ac95-107">EXAMPLES</span></span>

### <span data-ttu-id="8ac95-108">Przykład 1: aktualizowanie definicji zasad punktu końcowego usługi w zasadzie punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="8ac95-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="8ac95-109">To polecenie zaktualizowała definicję zasad punktu końcowego usługi o nazwie ServiceEndpointPolicyDefinition1, usłudze Microsoft. Storage, abonamentach/sub1 i opisie "Nowa definicja" należącym do grupy zasobów o nazwie ResourceGroup01 i przechowując ją w zmiennej $policydef.</span><span class="sxs-lookup"><span data-stu-id="8ac95-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="8ac95-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ac95-110">PARAMETERS</span></span>

### <span data-ttu-id="8ac95-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ac95-111">-DefaultProfile</span></span>
<span data-ttu-id="8ac95-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ac95-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ac95-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="8ac95-113">-Description</span></span>
<span data-ttu-id="8ac95-114">Opis definicji</span><span class="sxs-lookup"><span data-stu-id="8ac95-114">The description of the definition</span></span>

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

### <span data-ttu-id="8ac95-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8ac95-115">-Name</span></span>
<span data-ttu-id="8ac95-116">Nazwa definicji zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="8ac95-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="8ac95-117">-Service</span><span class="sxs-lookup"><span data-stu-id="8ac95-117">-Service</span></span>
<span data-ttu-id="8ac95-118">Nazwa usługi</span><span class="sxs-lookup"><span data-stu-id="8ac95-118">Name of the service</span></span>

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

### <span data-ttu-id="8ac95-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8ac95-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="8ac95-120">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8ac95-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="8ac95-121">-Serviceresource</span><span class="sxs-lookup"><span data-stu-id="8ac95-121">-ServiceResource</span></span>
<span data-ttu-id="8ac95-122">Lista zasobów usług</span><span class="sxs-lookup"><span data-stu-id="8ac95-122">List of service resources</span></span>

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

### <span data-ttu-id="8ac95-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8ac95-123">-Confirm</span></span>
<span data-ttu-id="8ac95-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ac95-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ac95-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ac95-125">-WhatIf</span></span>
<span data-ttu-id="8ac95-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ac95-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ac95-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8ac95-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ac95-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ac95-128">CommonParameters</span></span>
<span data-ttu-id="8ac95-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ac95-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ac95-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ac95-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ac95-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ac95-131">INPUTS</span></span>

### <span data-ttu-id="8ac95-132">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8ac95-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="8ac95-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ac95-133">OUTPUTS</span></span>

### <span data-ttu-id="8ac95-134">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8ac95-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="8ac95-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ac95-135">NOTES</span></span>

## <span data-ttu-id="8ac95-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ac95-136">RELATED LINKS</span></span>

[<span data-ttu-id="8ac95-137">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8ac95-137">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="8ac95-138">Nowe — AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8ac95-138">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="8ac95-139">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8ac95-139">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="8ac95-140">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8ac95-140">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
