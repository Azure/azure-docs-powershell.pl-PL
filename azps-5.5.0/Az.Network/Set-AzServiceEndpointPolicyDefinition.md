---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 46d86b6a910abcd00257277f61bb44dd426ab945
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240555"
---
# <span data-ttu-id="a69f8-101">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a69f8-101">Set-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="a69f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a69f8-102">SYNOPSIS</span></span>
<span data-ttu-id="a69f8-103">Aktualizuje definicję zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="a69f8-103">Updates a service endpoint policy definition.</span></span>

## <span data-ttu-id="a69f8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a69f8-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a69f8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a69f8-105">DESCRIPTION</span></span>
<span data-ttu-id="a69f8-106">Polecenie **cmdlet Set-AzServiceEndpointPolicyDefinition** umożliwia utworzenie definicji zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="a69f8-106">The **Set-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="a69f8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a69f8-107">EXAMPLES</span></span>

### <span data-ttu-id="a69f8-108">Przykład 1. Aktualizacja definicji zasad punktu końcowego usługi w zasadach punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="a69f8-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="a69f8-109">To polecenie aktualizuje definicję zasad punktu końcowego usługi o nazwie Policydef1 w zasadach punktu końcowego usługi zdefiniowanych przez obiekt $ServiceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="a69f8-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="a69f8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a69f8-110">PARAMETERS</span></span>

### <span data-ttu-id="a69f8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a69f8-111">-DefaultProfile</span></span>
<span data-ttu-id="a69f8-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a69f8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a69f8-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="a69f8-113">-Description</span></span>
<span data-ttu-id="a69f8-114">Opis definicji</span><span class="sxs-lookup"><span data-stu-id="a69f8-114">The description of the definition</span></span>

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

### <span data-ttu-id="a69f8-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a69f8-115">-Name</span></span>
<span data-ttu-id="a69f8-116">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="a69f8-116">The name of the rule</span></span>

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

### <span data-ttu-id="a69f8-117">— Usługa</span><span class="sxs-lookup"><span data-stu-id="a69f8-117">-Service</span></span>
<span data-ttu-id="a69f8-118">Nazwa usługi</span><span class="sxs-lookup"><span data-stu-id="a69f8-118">Name of the service</span></span>

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

### <span data-ttu-id="a69f8-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a69f8-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="a69f8-120">The NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a69f8-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="a69f8-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="a69f8-121">-ServiceResource</span></span>
<span data-ttu-id="a69f8-122">Lista zasobów usługi</span><span class="sxs-lookup"><span data-stu-id="a69f8-122">List of service resources</span></span>

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

### <span data-ttu-id="a69f8-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a69f8-123">-Confirm</span></span>
<span data-ttu-id="a69f8-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a69f8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a69f8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a69f8-125">-WhatIf</span></span>
<span data-ttu-id="a69f8-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a69f8-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a69f8-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a69f8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a69f8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a69f8-128">CommonParameters</span></span>
<span data-ttu-id="a69f8-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a69f8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a69f8-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a69f8-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a69f8-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a69f8-131">INPUTS</span></span>

### <span data-ttu-id="a69f8-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a69f8-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="a69f8-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a69f8-133">OUTPUTS</span></span>

### <span data-ttu-id="a69f8-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a69f8-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="a69f8-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a69f8-135">NOTES</span></span>

## <span data-ttu-id="a69f8-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a69f8-136">RELATED LINKS</span></span>

[<span data-ttu-id="a69f8-137">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a69f8-137">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="a69f8-138">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a69f8-138">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="a69f8-139">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a69f8-139">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="a69f8-140">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a69f8-140">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)
