---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 634beeaf33515ac5e89011ab47eaea34eccaa581
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709241"
---
# <span data-ttu-id="eaee4-101">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="eaee4-101">New-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="eaee4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eaee4-102">SYNOPSIS</span></span>
<span data-ttu-id="eaee4-103">Tworzy definicję zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="eaee4-103">Creates a service endpoint policy definition.</span></span>

## <span data-ttu-id="eaee4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eaee4-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicyDefinition -Name <String> [-Description <String>] [-ServiceResource <String[]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eaee4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eaee4-105">DESCRIPTION</span></span>
<span data-ttu-id="eaee4-106">Polecenie cmdlet **New-AzServiceEndpointPolicyDefinition** umożliwia utworzenie definicji zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="eaee4-106">The **New-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="eaee4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eaee4-107">EXAMPLES</span></span>

### <span data-ttu-id="eaee4-108">Przykład 1. Tworzenie zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="eaee4-108">Example 1: Creates a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="eaee4-109">To polecenie tworzy definicję zasad punktu końcowego usługi o nazwie ServiceEndpointPolicyDefinition1, usłudze Microsoft. Storage, abonamentach/sub1 i opisie "Nowa definicja" należącym do grupy zasobów o nazwie ResourceGroup01 i przechowując ją w zmiennej $policydef.</span><span class="sxs-lookup"><span data-stu-id="eaee4-109">This command creates the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="eaee4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eaee4-110">PARAMETERS</span></span>

### <span data-ttu-id="eaee4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaee4-111">-DefaultProfile</span></span>
<span data-ttu-id="eaee4-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eaee4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eaee4-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="eaee4-113">-Description</span></span>
<span data-ttu-id="eaee4-114">Opis definicji</span><span class="sxs-lookup"><span data-stu-id="eaee4-114">The description of the definition</span></span>

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

### <span data-ttu-id="eaee4-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eaee4-115">-Name</span></span>
<span data-ttu-id="eaee4-116">Nazwa zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="eaee4-116">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="eaee4-117">-Service</span><span class="sxs-lookup"><span data-stu-id="eaee4-117">-Service</span></span>
<span data-ttu-id="eaee4-118">Nazwa usługi</span><span class="sxs-lookup"><span data-stu-id="eaee4-118">Name of the service</span></span>

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

### <span data-ttu-id="eaee4-119">-Serviceresource</span><span class="sxs-lookup"><span data-stu-id="eaee4-119">-ServiceResource</span></span>
<span data-ttu-id="eaee4-120">Lista zasobów usług</span><span class="sxs-lookup"><span data-stu-id="eaee4-120">List of service resources</span></span>

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

### <span data-ttu-id="eaee4-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eaee4-121">-Confirm</span></span>
<span data-ttu-id="eaee4-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eaee4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaee4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaee4-123">-WhatIf</span></span>
<span data-ttu-id="eaee4-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eaee4-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eaee4-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eaee4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaee4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaee4-126">CommonParameters</span></span>
<span data-ttu-id="eaee4-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaee4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaee4-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaee4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaee4-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eaee4-129">INPUTS</span></span>

### <span data-ttu-id="eaee4-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="eaee4-130">None</span></span>

## <span data-ttu-id="eaee4-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eaee4-131">OUTPUTS</span></span>

### <span data-ttu-id="eaee4-132">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="eaee4-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="eaee4-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eaee4-133">NOTES</span></span>

## <span data-ttu-id="eaee4-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eaee4-134">RELATED LINKS</span></span>

[<span data-ttu-id="eaee4-135">Dodaj-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="eaee4-135">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="eaee4-136">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="eaee4-136">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="eaee4-137">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="eaee4-137">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="eaee4-138">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="eaee4-138">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
