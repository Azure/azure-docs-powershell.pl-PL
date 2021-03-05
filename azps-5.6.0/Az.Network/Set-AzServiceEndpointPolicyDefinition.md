---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: bc68a57437bae2af10b5ee39221459aebf82a2df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010298"
---
# <span data-ttu-id="b2f6d-101">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b2f6d-101">Set-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="b2f6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2f6d-102">SYNOPSIS</span></span>
<span data-ttu-id="b2f6d-103">Aktualizuje definicję zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="b2f6d-103">Updates a service endpoint policy definition.</span></span>

## <span data-ttu-id="b2f6d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b2f6d-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2f6d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b2f6d-105">DESCRIPTION</span></span>
<span data-ttu-id="b2f6d-106">Polecenie **cmdlet Set-AzServiceEndpointPolicyDefinition** umożliwia utworzenie definicji zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="b2f6d-106">The **Set-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="b2f6d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b2f6d-107">EXAMPLES</span></span>

### <span data-ttu-id="b2f6d-108">Przykład 1. Aktualizacja definicji zasad punktu końcowego usługi w zasadach punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="b2f6d-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="b2f6d-109">To polecenie aktualizuje definicję zasad punktu końcowego usługi o nazwie Policydef1 w zasadach punktu końcowego usługi zdefiniowanych przez $ServiceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="b2f6d-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="b2f6d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2f6d-110">PARAMETERS</span></span>

### <span data-ttu-id="b2f6d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2f6d-111">-DefaultProfile</span></span>
<span data-ttu-id="b2f6d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b2f6d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2f6d-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="b2f6d-113">-Description</span></span>
<span data-ttu-id="b2f6d-114">Opis definicji</span><span class="sxs-lookup"><span data-stu-id="b2f6d-114">The description of the definition</span></span>

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

### <span data-ttu-id="b2f6d-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b2f6d-115">-Name</span></span>
<span data-ttu-id="b2f6d-116">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="b2f6d-116">The name of the rule</span></span>

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

### <span data-ttu-id="b2f6d-117">— Usługa</span><span class="sxs-lookup"><span data-stu-id="b2f6d-117">-Service</span></span>
<span data-ttu-id="b2f6d-118">Nazwa usługi</span><span class="sxs-lookup"><span data-stu-id="b2f6d-118">Name of the service</span></span>

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

### <span data-ttu-id="b2f6d-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b2f6d-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="b2f6d-120">The NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b2f6d-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="b2f6d-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="b2f6d-121">-ServiceResource</span></span>
<span data-ttu-id="b2f6d-122">Lista zasobów usługi</span><span class="sxs-lookup"><span data-stu-id="b2f6d-122">List of service resources</span></span>

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

### <span data-ttu-id="b2f6d-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b2f6d-123">-Confirm</span></span>
<span data-ttu-id="b2f6d-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b2f6d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2f6d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2f6d-125">-WhatIf</span></span>
<span data-ttu-id="b2f6d-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2f6d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2f6d-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b2f6d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2f6d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2f6d-128">CommonParameters</span></span>
<span data-ttu-id="b2f6d-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2f6d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2f6d-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2f6d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2f6d-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2f6d-131">INPUTS</span></span>

### <span data-ttu-id="b2f6d-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b2f6d-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="b2f6d-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2f6d-133">OUTPUTS</span></span>

### <span data-ttu-id="b2f6d-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b2f6d-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="b2f6d-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b2f6d-135">NOTES</span></span>

## <span data-ttu-id="b2f6d-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2f6d-136">RELATED LINKS</span></span>

[<span data-ttu-id="b2f6d-137">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b2f6d-137">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="b2f6d-138">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b2f6d-138">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="b2f6d-139">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b2f6d-139">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="b2f6d-140">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b2f6d-140">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)
