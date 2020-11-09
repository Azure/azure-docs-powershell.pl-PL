---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 164fc5edb4bac3b90debde0aaf6205c719f5c95c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317238"
---
# <span data-ttu-id="3595f-101">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3595f-101">Get-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="3595f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3595f-102">SYNOPSIS</span></span>
<span data-ttu-id="3595f-103">Pobiera definicję zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="3595f-103">Gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="3595f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3595f-104">SYNTAX</span></span>

```
Get-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3595f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3595f-105">DESCRIPTION</span></span>
<span data-ttu-id="3595f-106">Polecenie cmdlet **Get-AzServiceEndpointPolicyDefinition** pobiera definicję zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="3595f-106">The **Get-AzServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="3595f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3595f-107">EXAMPLES</span></span>

### <span data-ttu-id="3595f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3595f-108">Example 1</span></span>
```
$policydef= Get-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="3595f-109">To polecenie pobiera definicję zasad punktu końcowego usługi o nazwie ServiceEndpointPolicyDefinition1 w ServiceEndpointPolicy $Policy zapisuje ją w zmiennej $policydef.</span><span class="sxs-lookup"><span data-stu-id="3595f-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="3595f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3595f-110">PARAMETERS</span></span>

### <span data-ttu-id="3595f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3595f-111">-DefaultProfile</span></span>
<span data-ttu-id="3595f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3595f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3595f-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3595f-113">-Name</span></span>
<span data-ttu-id="3595f-114">Nazwa definicji zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="3595f-114">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="3595f-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3595f-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="3595f-116">Zasady punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="3595f-116">The Service endpoint policy</span></span>

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

### <span data-ttu-id="3595f-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3595f-117">-Confirm</span></span>
<span data-ttu-id="3595f-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3595f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3595f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3595f-119">-WhatIf</span></span>
<span data-ttu-id="3595f-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3595f-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3595f-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3595f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3595f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3595f-122">CommonParameters</span></span>
<span data-ttu-id="3595f-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3595f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3595f-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3595f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3595f-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3595f-125">INPUTS</span></span>

### <span data-ttu-id="3595f-126">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3595f-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="3595f-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3595f-127">OUTPUTS</span></span>

### <span data-ttu-id="3595f-128">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3595f-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="3595f-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3595f-129">NOTES</span></span>

## <span data-ttu-id="3595f-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3595f-130">RELATED LINKS</span></span>

[<span data-ttu-id="3595f-131">Dodaj-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3595f-131">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="3595f-132">Nowe — AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3595f-132">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="3595f-133">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3595f-133">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="3595f-134">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3595f-134">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
