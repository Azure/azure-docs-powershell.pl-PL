---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 554d3285c80370559bbedfb91430d2b6801a6f51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959498"
---
# <span data-ttu-id="cfc8b-101">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cfc8b-101">Get-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="cfc8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfc8b-102">SYNOPSIS</span></span>
<span data-ttu-id="cfc8b-103">Pobiera definicję zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="cfc8b-103">Gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="cfc8b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cfc8b-104">SYNTAX</span></span>

```
Get-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfc8b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="cfc8b-105">DESCRIPTION</span></span>
<span data-ttu-id="cfc8b-106">Polecenie **cmdlet Get-AzServiceEndpointPolicyDefinition** otrzymuje definicję zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="cfc8b-106">The **Get-AzServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="cfc8b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cfc8b-107">EXAMPLES</span></span>

### <span data-ttu-id="cfc8b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cfc8b-108">Example 1</span></span>
```
$policydef= Get-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="cfc8b-109">To polecenie pobiera definicję zasad punktu końcowego usługi o nazwie ServiceEndpointPolicyDefinition1 w usłudze ServiceEndpointPolicy $Policy przechowuje ją w $policydef danych.</span><span class="sxs-lookup"><span data-stu-id="cfc8b-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="cfc8b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cfc8b-110">PARAMETERS</span></span>

### <span data-ttu-id="cfc8b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfc8b-111">-DefaultProfile</span></span>
<span data-ttu-id="cfc8b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cfc8b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfc8b-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cfc8b-113">-Name</span></span>
<span data-ttu-id="cfc8b-114">Nazwa definicji zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="cfc8b-114">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="cfc8b-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="cfc8b-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="cfc8b-116">Zasady punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="cfc8b-116">The Service endpoint policy</span></span>

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

### <span data-ttu-id="cfc8b-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cfc8b-117">-Confirm</span></span>
<span data-ttu-id="cfc8b-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cfc8b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfc8b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfc8b-119">-WhatIf</span></span>
<span data-ttu-id="cfc8b-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfc8b-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cfc8b-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cfc8b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfc8b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfc8b-122">CommonParameters</span></span>
<span data-ttu-id="cfc8b-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfc8b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfc8b-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cfc8b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfc8b-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cfc8b-125">INPUTS</span></span>

### <span data-ttu-id="cfc8b-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="cfc8b-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="cfc8b-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cfc8b-127">OUTPUTS</span></span>

### <span data-ttu-id="cfc8b-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cfc8b-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="cfc8b-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cfc8b-129">NOTES</span></span>

## <span data-ttu-id="cfc8b-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cfc8b-130">RELATED LINKS</span></span>

[<span data-ttu-id="cfc8b-131">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cfc8b-131">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="cfc8b-132">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cfc8b-132">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="cfc8b-133">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cfc8b-133">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="cfc8b-134">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cfc8b-134">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
