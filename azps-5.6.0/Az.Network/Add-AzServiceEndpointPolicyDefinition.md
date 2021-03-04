---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 9a9795547a1d9699a185ae8957852b41d26ca321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979770"
---
# <span data-ttu-id="72076-101">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="72076-101">Add-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="72076-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72076-102">SYNOPSIS</span></span>
<span data-ttu-id="72076-103">Dodaje definicję zasad punktu końcowego usługi do określonych zasad.</span><span class="sxs-lookup"><span data-stu-id="72076-103">Adds a service endpoint policy definition to a specified policy.</span></span>

## <span data-ttu-id="72076-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="72076-104">SYNTAX</span></span>

```
Add-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72076-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="72076-105">DESCRIPTION</span></span>
<span data-ttu-id="72076-106">Polecenie **cmdlet Add-AzServiceEndpointPolicyDefinition** dodaj do zasad definicję zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="72076-106">The **Add-AzServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="72076-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="72076-107">EXAMPLES</span></span>

### <span data-ttu-id="72076-108">Przykład 1. Aktualizacja definicji zasad punktu końcowego usługi w zasadach punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="72076-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="72076-109">To polecenie zaktualizowało definicję zasad punktu końcowego usługi o nazwę ServiceEndpointPolicyDefinition1, service Microsoft.Storage, subskrypcje/pod1 zasobów usługi i opis "Nowa definicja", który należy do grupy zasobów o nazwie ResourceGroup01 i przechowuje ją w zmiennej $policydef.</span><span class="sxs-lookup"><span data-stu-id="72076-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="72076-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72076-110">PARAMETERS</span></span>

### <span data-ttu-id="72076-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72076-111">-DefaultProfile</span></span>
<span data-ttu-id="72076-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="72076-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72076-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="72076-113">-Description</span></span>
<span data-ttu-id="72076-114">Opis definicji</span><span class="sxs-lookup"><span data-stu-id="72076-114">The description of the definition</span></span>

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

### <span data-ttu-id="72076-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="72076-115">-Name</span></span>
<span data-ttu-id="72076-116">Nazwa definicji zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="72076-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="72076-117">— Usługa</span><span class="sxs-lookup"><span data-stu-id="72076-117">-Service</span></span>
<span data-ttu-id="72076-118">Nazwa usługi</span><span class="sxs-lookup"><span data-stu-id="72076-118">Name of the service</span></span>

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

### <span data-ttu-id="72076-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="72076-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="72076-120">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="72076-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="72076-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="72076-121">-ServiceResource</span></span>
<span data-ttu-id="72076-122">Lista zasobów usługi</span><span class="sxs-lookup"><span data-stu-id="72076-122">List of service resources</span></span>

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

### <span data-ttu-id="72076-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="72076-123">-Confirm</span></span>
<span data-ttu-id="72076-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="72076-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72076-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72076-125">-WhatIf</span></span>
<span data-ttu-id="72076-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72076-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72076-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="72076-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72076-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72076-128">CommonParameters</span></span>
<span data-ttu-id="72076-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72076-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72076-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72076-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72076-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72076-131">INPUTS</span></span>

### <span data-ttu-id="72076-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="72076-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="72076-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72076-133">OUTPUTS</span></span>

### <span data-ttu-id="72076-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="72076-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="72076-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="72076-135">NOTES</span></span>

## <span data-ttu-id="72076-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72076-136">RELATED LINKS</span></span>

[<span data-ttu-id="72076-137">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="72076-137">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="72076-138">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="72076-138">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="72076-139">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="72076-139">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="72076-140">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="72076-140">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
