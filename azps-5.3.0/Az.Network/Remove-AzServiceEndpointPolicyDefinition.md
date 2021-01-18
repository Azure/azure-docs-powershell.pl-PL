---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 146e43ce5f1816994a1d408e215e4b3e27c2bbca
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501215"
---
# <span data-ttu-id="bdf19-101">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bdf19-101">Remove-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="bdf19-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bdf19-102">SYNOPSIS</span></span>
<span data-ttu-id="bdf19-103">Usuwa definicję zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="bdf19-103">Removes a service endpoint policy definition.</span></span>

## <span data-ttu-id="bdf19-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bdf19-104">SYNTAX</span></span>

### <span data-ttu-id="bdf19-105">RemoveByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bdf19-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdf19-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdf19-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -ResourceId <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdf19-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdf19-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -InputObject <PSServiceEndpointPolicyDefinition>
 -ServiceEndpointPolicy <PSServiceEndpointPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdf19-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bdf19-108">DESCRIPTION</span></span>
<span data-ttu-id="bdf19-109">Polecenie cmdlet **Remove-AzServiceEndpointPolicy** usuwa zasadę punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="bdf19-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="bdf19-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bdf19-110">EXAMPLES</span></span>

### <span data-ttu-id="bdf19-111">Przykład 1. usuwa zasadę punktu końcowego usługi przy użyciu nazwy</span><span class="sxs-lookup"><span data-stu-id="bdf19-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="bdf19-112">To polecenie usuwa zasadę punktu końcowego usługi o nazwie PolicyDef1</span><span class="sxs-lookup"><span data-stu-id="bdf19-112">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="bdf19-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bdf19-113">PARAMETERS</span></span>

### <span data-ttu-id="bdf19-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdf19-114">-DefaultProfile</span></span>
<span data-ttu-id="bdf19-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bdf19-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdf19-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bdf19-116">-InputObject</span></span>
<span data-ttu-id="bdf19-117">Obiekt definicji zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="bdf19-117">The service endpoint policy definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdf19-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bdf19-118">-Name</span></span>
<span data-ttu-id="bdf19-119">Nazwa definicji punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="bdf19-119">The name of the service endpoint definition</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf19-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdf19-120">-ResourceId</span></span>
<span data-ttu-id="bdf19-121">Identyfikator definicji punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="bdf19-121">The ID of the service endpoint definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdf19-122">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="bdf19-122">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="bdf19-123">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="bdf19-123">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="bdf19-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bdf19-124">-Confirm</span></span>
<span data-ttu-id="bdf19-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdf19-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdf19-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdf19-126">-WhatIf</span></span>
<span data-ttu-id="bdf19-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdf19-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bdf19-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bdf19-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdf19-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdf19-129">CommonParameters</span></span>
<span data-ttu-id="bdf19-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdf19-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdf19-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdf19-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdf19-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdf19-132">INPUTS</span></span>

### <span data-ttu-id="bdf19-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bdf19-133">System.String</span></span>

### <span data-ttu-id="bdf19-134">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bdf19-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

### <span data-ttu-id="bdf19-135">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="bdf19-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="bdf19-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bdf19-136">OUTPUTS</span></span>

### <span data-ttu-id="bdf19-137">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="bdf19-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="bdf19-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bdf19-138">NOTES</span></span>

## <span data-ttu-id="bdf19-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bdf19-139">RELATED LINKS</span></span>

[<span data-ttu-id="bdf19-140">Dodaj-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bdf19-140">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="bdf19-141">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bdf19-141">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="bdf19-142">Nowe — AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bdf19-142">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="bdf19-143">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bdf19-143">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
