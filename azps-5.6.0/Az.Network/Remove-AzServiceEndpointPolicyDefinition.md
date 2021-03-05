---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 65303db1c76f6e7c6e1323ed0cfc88132e4c1c23
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006129"
---
# <span data-ttu-id="ea270-101">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ea270-101">Remove-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="ea270-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea270-102">SYNOPSIS</span></span>
<span data-ttu-id="ea270-103">Usuwa definicję zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="ea270-103">Removes a service endpoint policy definition.</span></span>

## <span data-ttu-id="ea270-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ea270-104">SYNTAX</span></span>

### <span data-ttu-id="ea270-105">RemoveByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ea270-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea270-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea270-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -ResourceId <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea270-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea270-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -InputObject <PSServiceEndpointPolicyDefinition>
 -ServiceEndpointPolicy <PSServiceEndpointPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea270-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ea270-108">DESCRIPTION</span></span>
<span data-ttu-id="ea270-109">Polecenie **cmdlet Remove-AzServiceEndpointPolicy** usuwa zasady punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="ea270-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="ea270-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ea270-110">EXAMPLES</span></span>

### <span data-ttu-id="ea270-111">Przykład 1. Usuwanie zasad punktu końcowego usługi przy użyciu nazwy</span><span class="sxs-lookup"><span data-stu-id="ea270-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="ea270-112">To polecenie usuwa zasady punktu końcowego usługi o nazwie PolicyDef1</span><span class="sxs-lookup"><span data-stu-id="ea270-112">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="ea270-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea270-113">PARAMETERS</span></span>

### <span data-ttu-id="ea270-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea270-114">-DefaultProfile</span></span>
<span data-ttu-id="ea270-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea270-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea270-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea270-116">-InputObject</span></span>
<span data-ttu-id="ea270-117">Obiekt definicji zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="ea270-117">The service endpoint policy definition object.</span></span>

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

### <span data-ttu-id="ea270-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ea270-118">-Name</span></span>
<span data-ttu-id="ea270-119">Nazwa definicji punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="ea270-119">The name of the service endpoint definition</span></span>

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

### <span data-ttu-id="ea270-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea270-120">-ResourceId</span></span>
<span data-ttu-id="ea270-121">Identyfikator definicji punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="ea270-121">The ID of the service endpoint definition.</span></span>

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

### <span data-ttu-id="ea270-122">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ea270-122">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="ea270-123">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ea270-123">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="ea270-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ea270-124">-Confirm</span></span>
<span data-ttu-id="ea270-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ea270-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea270-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea270-126">-WhatIf</span></span>
<span data-ttu-id="ea270-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea270-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea270-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ea270-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea270-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea270-129">CommonParameters</span></span>
<span data-ttu-id="ea270-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea270-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea270-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea270-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea270-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea270-132">INPUTS</span></span>

### <span data-ttu-id="ea270-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ea270-133">System.String</span></span>

### <span data-ttu-id="ea270-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ea270-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

### <span data-ttu-id="ea270-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ea270-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="ea270-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea270-136">OUTPUTS</span></span>

### <span data-ttu-id="ea270-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ea270-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="ea270-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ea270-138">NOTES</span></span>

## <span data-ttu-id="ea270-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea270-139">RELATED LINKS</span></span>

[<span data-ttu-id="ea270-140">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ea270-140">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="ea270-141">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ea270-141">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="ea270-142">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ea270-142">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="ea270-143">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ea270-143">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
