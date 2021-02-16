---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
ms.openlocfilehash: 207a07186cd7284059e0824da1f86afbc22873f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186930"
---
# <span data-ttu-id="75ef0-101">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="75ef0-101">Remove-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="75ef0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75ef0-102">SYNOPSIS</span></span>
<span data-ttu-id="75ef0-103">Usuwa zasady punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="75ef0-103">Removes a service endpoint policy.</span></span>

## <span data-ttu-id="75ef0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="75ef0-104">SYNTAX</span></span>

### <span data-ttu-id="75ef0-105">RemoveByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="75ef0-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75ef0-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75ef0-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75ef0-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75ef0-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject <PSServiceEndpointPolicy> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75ef0-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="75ef0-108">DESCRIPTION</span></span>
<span data-ttu-id="75ef0-109">Polecenie **cmdlet Remove-AzServiceEndpointPolicy** usuwa zasady punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="75ef0-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="75ef0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="75ef0-110">EXAMPLES</span></span>

### <span data-ttu-id="75ef0-111">Przykład 1. Usuwanie zasad punktu końcowego usługi przy użyciu nazwy</span><span class="sxs-lookup"><span data-stu-id="75ef0-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="75ef0-112">To polecenie usuwa zasady punktu końcowego usługi o nazwie Zasady1, które należą do grupy zasobów o nazwie "grupa zasobów1".</span><span class="sxs-lookup"><span data-stu-id="75ef0-112">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="75ef0-113">Przykład 2. Usuwanie zasad punktu końcowego usługi przy użyciu obiektu wejściowego</span><span class="sxs-lookup"><span data-stu-id="75ef0-113">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="75ef0-114">To polecenie usuwa obiekt Zasad1 zasad punktu końcowego usługi, który należy do grupy zasobów o nazwie "grupa zasobów1"</span><span class="sxs-lookup"><span data-stu-id="75ef0-114">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="75ef0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75ef0-115">PARAMETERS</span></span>

### <span data-ttu-id="75ef0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75ef0-116">-DefaultProfile</span></span>
<span data-ttu-id="75ef0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="75ef0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75ef0-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="75ef0-118">-Force</span></span>
<span data-ttu-id="75ef0-119">Nie pytaj o potwierdzenie, czy chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="75ef0-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75ef0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75ef0-120">-InputObject</span></span>
<span data-ttu-id="75ef0-121">Obiekt zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="75ef0-121">The service endpoint policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75ef0-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="75ef0-122">-Name</span></span>
<span data-ttu-id="75ef0-123">Nazwa zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="75ef0-123">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75ef0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75ef0-124">-PassThru</span></span>
<span data-ttu-id="75ef0-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="75ef0-125">Returns an object representing the item with which you are working.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75ef0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75ef0-126">-ResourceGroupName</span></span>
<span data-ttu-id="75ef0-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="75ef0-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75ef0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75ef0-128">-ResourceId</span></span>
<span data-ttu-id="75ef0-129">Identyfikator zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="75ef0-129">The ID of service endpoint policy.</span></span>

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

### <span data-ttu-id="75ef0-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="75ef0-130">-Confirm</span></span>
<span data-ttu-id="75ef0-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="75ef0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75ef0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75ef0-132">-WhatIf</span></span>
<span data-ttu-id="75ef0-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75ef0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75ef0-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="75ef0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75ef0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75ef0-135">CommonParameters</span></span>
<span data-ttu-id="75ef0-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75ef0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75ef0-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75ef0-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75ef0-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75ef0-138">INPUTS</span></span>

### <span data-ttu-id="75ef0-139">System.String</span><span class="sxs-lookup"><span data-stu-id="75ef0-139">System.String</span></span>

### <span data-ttu-id="75ef0-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="75ef0-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="75ef0-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75ef0-141">OUTPUTS</span></span>

### <span data-ttu-id="75ef0-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="75ef0-142">System.Boolean</span></span>

## <span data-ttu-id="75ef0-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="75ef0-143">NOTES</span></span>

## <span data-ttu-id="75ef0-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75ef0-144">RELATED LINKS</span></span>

[<span data-ttu-id="75ef0-145">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="75ef0-145">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="75ef0-146">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="75ef0-146">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="75ef0-147">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="75ef0-147">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
