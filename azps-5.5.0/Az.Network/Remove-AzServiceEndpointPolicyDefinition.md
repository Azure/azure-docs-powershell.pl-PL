---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 146e43ce5f1816994a1d408e215e4b3e27c2bbca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240634"
---
# <span data-ttu-id="4ca9e-101">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4ca9e-101">Remove-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="4ca9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ca9e-102">SYNOPSIS</span></span>
<span data-ttu-id="4ca9e-103">Usuwa definicję zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-103">Removes a service endpoint policy definition.</span></span>

## <span data-ttu-id="4ca9e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4ca9e-104">SYNTAX</span></span>

### <span data-ttu-id="4ca9e-105">RemoveByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="4ca9e-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ca9e-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ca9e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -ResourceId <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ca9e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ca9e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -InputObject <PSServiceEndpointPolicyDefinition>
 -ServiceEndpointPolicy <PSServiceEndpointPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ca9e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="4ca9e-108">DESCRIPTION</span></span>
<span data-ttu-id="4ca9e-109">Polecenie **cmdlet Remove-AzServiceEndpointPolicy** usuwa zasady punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="4ca9e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4ca9e-110">EXAMPLES</span></span>

### <span data-ttu-id="4ca9e-111">Przykład 1. Usuwanie zasad punktu końcowego usługi przy użyciu nazwy</span><span class="sxs-lookup"><span data-stu-id="4ca9e-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="4ca9e-112">To polecenie usuwa zasady punktu końcowego usługi o nazwie PolicyDef1</span><span class="sxs-lookup"><span data-stu-id="4ca9e-112">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="4ca9e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ca9e-113">PARAMETERS</span></span>

### <span data-ttu-id="4ca9e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ca9e-114">-DefaultProfile</span></span>
<span data-ttu-id="4ca9e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ca9e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ca9e-116">-InputObject</span></span>
<span data-ttu-id="4ca9e-117">Obiekt definicji zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-117">The service endpoint policy definition object.</span></span>

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

### <span data-ttu-id="4ca9e-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4ca9e-118">-Name</span></span>
<span data-ttu-id="4ca9e-119">Nazwa definicji punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="4ca9e-119">The name of the service endpoint definition</span></span>

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

### <span data-ttu-id="4ca9e-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ca9e-120">-ResourceId</span></span>
<span data-ttu-id="4ca9e-121">Identyfikator definicji punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-121">The ID of the service endpoint definition.</span></span>

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

### <span data-ttu-id="4ca9e-122">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4ca9e-122">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="4ca9e-123">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4ca9e-123">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="4ca9e-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4ca9e-124">-Confirm</span></span>
<span data-ttu-id="4ca9e-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ca9e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ca9e-126">-WhatIf</span></span>
<span data-ttu-id="4ca9e-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ca9e-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ca9e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ca9e-129">CommonParameters</span></span>
<span data-ttu-id="4ca9e-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ca9e-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ca9e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ca9e-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ca9e-132">INPUTS</span></span>

### <span data-ttu-id="4ca9e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4ca9e-133">System.String</span></span>

### <span data-ttu-id="4ca9e-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4ca9e-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

### <span data-ttu-id="4ca9e-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4ca9e-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="4ca9e-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ca9e-136">OUTPUTS</span></span>

### <span data-ttu-id="4ca9e-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4ca9e-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="4ca9e-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4ca9e-138">NOTES</span></span>

## <span data-ttu-id="4ca9e-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ca9e-139">RELATED LINKS</span></span>

[<span data-ttu-id="4ca9e-140">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4ca9e-140">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="4ca9e-141">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4ca9e-141">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="4ca9e-142">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4ca9e-142">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="4ca9e-143">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4ca9e-143">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
