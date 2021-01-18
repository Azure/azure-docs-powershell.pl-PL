---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
ms.openlocfilehash: 207a07186cd7284059e0824da1f86afbc22873f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504450"
---
# <span data-ttu-id="69599-101">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="69599-101">Remove-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="69599-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="69599-102">SYNOPSIS</span></span>
<span data-ttu-id="69599-103">Usuwa zasadę punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="69599-103">Removes a service endpoint policy.</span></span>

## <span data-ttu-id="69599-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="69599-104">SYNTAX</span></span>

### <span data-ttu-id="69599-105">RemoveByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="69599-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69599-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69599-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69599-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69599-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject <PSServiceEndpointPolicy> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69599-108">Opis</span><span class="sxs-lookup"><span data-stu-id="69599-108">DESCRIPTION</span></span>
<span data-ttu-id="69599-109">Polecenie cmdlet **Remove-AzServiceEndpointPolicy** usuwa zasadę punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="69599-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="69599-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="69599-110">EXAMPLES</span></span>

### <span data-ttu-id="69599-111">Przykład 1. usuwa zasadę punktu końcowego usługi przy użyciu nazwy</span><span class="sxs-lookup"><span data-stu-id="69599-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="69599-112">To polecenie usuwa zasadę punktu końcowego usługi o nazwie Policy1 należącej do źródła danych o nazwie "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="69599-112">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="69599-113">Przykład 2: usuwanie zasad punktu końcowego usługi za pomocą obiektu wejściowego</span><span class="sxs-lookup"><span data-stu-id="69599-113">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="69599-114">To polecenie usuwa obiekt zasad punktu końcowego usługi Policy1, który należy do obiektu resourceName o nazwie "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="69599-114">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="69599-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="69599-115">PARAMETERS</span></span>

### <span data-ttu-id="69599-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69599-116">-DefaultProfile</span></span>
<span data-ttu-id="69599-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="69599-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69599-118">-Force</span><span class="sxs-lookup"><span data-stu-id="69599-118">-Force</span></span>
<span data-ttu-id="69599-119">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="69599-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="69599-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="69599-120">-InputObject</span></span>
<span data-ttu-id="69599-121">Obiekt zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="69599-121">The service endpoint policy object.</span></span>

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

### <span data-ttu-id="69599-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="69599-122">-Name</span></span>
<span data-ttu-id="69599-123">Nazwa zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="69599-123">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="69599-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69599-124">-PassThru</span></span>
<span data-ttu-id="69599-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="69599-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="69599-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69599-126">-ResourceGroupName</span></span>
<span data-ttu-id="69599-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="69599-127">The resource group name.</span></span>

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

### <span data-ttu-id="69599-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69599-128">-ResourceId</span></span>
<span data-ttu-id="69599-129">Identyfikator zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="69599-129">The ID of service endpoint policy.</span></span>

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

### <span data-ttu-id="69599-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69599-130">-Confirm</span></span>
<span data-ttu-id="69599-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69599-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69599-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69599-132">-WhatIf</span></span>
<span data-ttu-id="69599-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69599-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69599-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="69599-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69599-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69599-135">CommonParameters</span></span>
<span data-ttu-id="69599-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69599-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69599-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69599-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69599-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69599-138">INPUTS</span></span>

### <span data-ttu-id="69599-139">System. String</span><span class="sxs-lookup"><span data-stu-id="69599-139">System.String</span></span>

### <span data-ttu-id="69599-140">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="69599-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="69599-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="69599-141">OUTPUTS</span></span>

### <span data-ttu-id="69599-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="69599-142">System.Boolean</span></span>

## <span data-ttu-id="69599-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="69599-143">NOTES</span></span>

## <span data-ttu-id="69599-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69599-144">RELATED LINKS</span></span>

[<span data-ttu-id="69599-145">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="69599-145">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="69599-146">Nowe — AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="69599-146">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="69599-147">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="69599-147">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
