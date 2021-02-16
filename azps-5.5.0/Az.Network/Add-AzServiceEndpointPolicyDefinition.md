---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: eaab1bdf26fb1cb99bfa7e947a4b7140971fda53
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189963"
---
# <span data-ttu-id="b5779-101">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b5779-101">Add-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="b5779-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5779-102">SYNOPSIS</span></span>
<span data-ttu-id="b5779-103">Dodaje definicję zasad punktu końcowego usługi do określonych zasad.</span><span class="sxs-lookup"><span data-stu-id="b5779-103">Adds a service endpoint policy definition to a specified policy.</span></span>

## <span data-ttu-id="b5779-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b5779-104">SYNTAX</span></span>

```
Add-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5779-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b5779-105">DESCRIPTION</span></span>
<span data-ttu-id="b5779-106">Polecenie **cmdlet Add-AzServiceEndpointPolicyDefinition** dodaj do zasad definicję zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="b5779-106">The **Add-AzServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="b5779-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b5779-107">EXAMPLES</span></span>

### <span data-ttu-id="b5779-108">Przykład 1. Aktualizacja definicji zasad punktu końcowego usługi w zasadach punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="b5779-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="b5779-109">To polecenie zaktualizowało definicję zasad punktu końcowego usługi o nazwę ServiceEndpointPolicyDefinition1, service Microsoft.Storage, service resources subscriptions/sub1 i opis "New Definition" należący do grupy zasobów o nazwie ResourceGroup01 i przechowuje ją w zmiennej $policydef.</span><span class="sxs-lookup"><span data-stu-id="b5779-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="b5779-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5779-110">PARAMETERS</span></span>

### <span data-ttu-id="b5779-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5779-111">-DefaultProfile</span></span>
<span data-ttu-id="b5779-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b5779-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5779-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="b5779-113">-Description</span></span>
<span data-ttu-id="b5779-114">Opis definicji</span><span class="sxs-lookup"><span data-stu-id="b5779-114">The description of the definition</span></span>

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

### <span data-ttu-id="b5779-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b5779-115">-Name</span></span>
<span data-ttu-id="b5779-116">Nazwa definicji zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="b5779-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="b5779-117">— Usługa</span><span class="sxs-lookup"><span data-stu-id="b5779-117">-Service</span></span>
<span data-ttu-id="b5779-118">Nazwa usługi</span><span class="sxs-lookup"><span data-stu-id="b5779-118">Name of the service</span></span>

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

### <span data-ttu-id="b5779-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b5779-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="b5779-120">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b5779-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="b5779-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="b5779-121">-ServiceResource</span></span>
<span data-ttu-id="b5779-122">Lista zasobów usługi</span><span class="sxs-lookup"><span data-stu-id="b5779-122">List of service resources</span></span>

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

### <span data-ttu-id="b5779-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b5779-123">-Confirm</span></span>
<span data-ttu-id="b5779-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b5779-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5779-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5779-125">-WhatIf</span></span>
<span data-ttu-id="b5779-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5779-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5779-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b5779-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5779-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5779-128">CommonParameters</span></span>
<span data-ttu-id="b5779-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5779-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5779-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5779-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5779-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5779-131">INPUTS</span></span>

### <span data-ttu-id="b5779-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b5779-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="b5779-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5779-133">OUTPUTS</span></span>

### <span data-ttu-id="b5779-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b5779-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="b5779-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b5779-135">NOTES</span></span>

## <span data-ttu-id="b5779-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5779-136">RELATED LINKS</span></span>

[<span data-ttu-id="b5779-137">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b5779-137">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="b5779-138">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b5779-138">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="b5779-139">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b5779-139">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="b5779-140">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b5779-140">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
