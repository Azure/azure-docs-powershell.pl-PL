---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: eaab1bdf26fb1cb99bfa7e947a4b7140971fda53
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359709"
---
# <span data-ttu-id="6dc78-101">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6dc78-101">Add-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="6dc78-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6dc78-102">SYNOPSIS</span></span>
<span data-ttu-id="6dc78-103">Dodaje definicję zasad punktu końcowego usługi do określonych zasad.</span><span class="sxs-lookup"><span data-stu-id="6dc78-103">Adds a service endpoint policy definition to a specified policy.</span></span>

## <span data-ttu-id="6dc78-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6dc78-104">SYNTAX</span></span>

```
Add-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dc78-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6dc78-105">DESCRIPTION</span></span>
<span data-ttu-id="6dc78-106">Polecenie cmdlet **Add-AzServiceEndpointPolicyDefinition** umożliwia dodanie definicji zasad punktu końcowego usługi do zasad.</span><span class="sxs-lookup"><span data-stu-id="6dc78-106">The **Add-AzServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="6dc78-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6dc78-107">EXAMPLES</span></span>

### <span data-ttu-id="6dc78-108">Przykład 1: aktualizowanie definicji zasad punktu końcowego usługi w zasadzie punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="6dc78-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="6dc78-109">To polecenie zaktualizowała definicję zasad punktu końcowego usługi o nazwie ServiceEndpointPolicyDefinition1, usłudze Microsoft. Storage, abonamentach/sub1 i opisie "Nowa definicja" należącym do grupy zasobów o nazwie ResourceGroup01 i przechowując ją w zmiennej $policydef.</span><span class="sxs-lookup"><span data-stu-id="6dc78-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="6dc78-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6dc78-110">PARAMETERS</span></span>

### <span data-ttu-id="6dc78-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dc78-111">-DefaultProfile</span></span>
<span data-ttu-id="6dc78-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6dc78-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dc78-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="6dc78-113">-Description</span></span>
<span data-ttu-id="6dc78-114">Opis definicji</span><span class="sxs-lookup"><span data-stu-id="6dc78-114">The description of the definition</span></span>

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

### <span data-ttu-id="6dc78-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6dc78-115">-Name</span></span>
<span data-ttu-id="6dc78-116">Nazwa definicji zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="6dc78-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="6dc78-117">-Service</span><span class="sxs-lookup"><span data-stu-id="6dc78-117">-Service</span></span>
<span data-ttu-id="6dc78-118">Nazwa usługi</span><span class="sxs-lookup"><span data-stu-id="6dc78-118">Name of the service</span></span>

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

### <span data-ttu-id="6dc78-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="6dc78-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="6dc78-120">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="6dc78-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="6dc78-121">-Serviceresource</span><span class="sxs-lookup"><span data-stu-id="6dc78-121">-ServiceResource</span></span>
<span data-ttu-id="6dc78-122">Lista zasobów usług</span><span class="sxs-lookup"><span data-stu-id="6dc78-122">List of service resources</span></span>

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

### <span data-ttu-id="6dc78-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6dc78-123">-Confirm</span></span>
<span data-ttu-id="6dc78-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dc78-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dc78-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dc78-125">-WhatIf</span></span>
<span data-ttu-id="6dc78-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dc78-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6dc78-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6dc78-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dc78-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dc78-128">CommonParameters</span></span>
<span data-ttu-id="6dc78-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dc78-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dc78-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dc78-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dc78-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6dc78-131">INPUTS</span></span>

### <span data-ttu-id="6dc78-132">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="6dc78-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="6dc78-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6dc78-133">OUTPUTS</span></span>

### <span data-ttu-id="6dc78-134">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="6dc78-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="6dc78-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6dc78-135">NOTES</span></span>

## <span data-ttu-id="6dc78-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6dc78-136">RELATED LINKS</span></span>

[<span data-ttu-id="6dc78-137">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6dc78-137">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="6dc78-138">Nowe — AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6dc78-138">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="6dc78-139">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6dc78-139">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="6dc78-140">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6dc78-140">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
