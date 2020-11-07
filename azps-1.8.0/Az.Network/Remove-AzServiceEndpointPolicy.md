---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
ms.openlocfilehash: 645eed141375dce0c27d389b721f7487c8a7c71f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709085"
---
# <span data-ttu-id="ab017-101">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ab017-101">Remove-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="ab017-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab017-102">SYNOPSIS</span></span>
<span data-ttu-id="ab017-103">Usuwa zasadę punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="ab017-103">Removes a service endpoint policy.</span></span>

## <span data-ttu-id="ab017-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab017-104">SYNTAX</span></span>

### <span data-ttu-id="ab017-105">RemoveByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ab017-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab017-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab017-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab017-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab017-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject <PSServiceEndpointPolicy> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab017-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ab017-108">DESCRIPTION</span></span>
<span data-ttu-id="ab017-109">Polecenie cmdlet **Remove-AzServiceEndpointPolicy** usuwa zasadę punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="ab017-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="ab017-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab017-110">EXAMPLES</span></span>

### <span data-ttu-id="ab017-111">Przykład 1. usuwa zasadę punktu końcowego usługi przy użyciu nazwy</span><span class="sxs-lookup"><span data-stu-id="ab017-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="ab017-112">To polecenie usuwa zasadę punktu końcowego usługi o nazwie Policy1 należącej do źródła danych o nazwie "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="ab017-112">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="ab017-113">Przykład 2: usuwanie zasad punktu końcowego usługi za pomocą obiektu wejściowego</span><span class="sxs-lookup"><span data-stu-id="ab017-113">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="ab017-114">To polecenie usuwa obiekt zasad punktu końcowego usługi Policy1, który należy do obiektu resourceName o nazwie "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="ab017-114">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="ab017-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab017-115">PARAMETERS</span></span>

### <span data-ttu-id="ab017-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab017-116">-DefaultProfile</span></span>
<span data-ttu-id="ab017-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab017-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab017-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ab017-118">-Force</span></span>
<span data-ttu-id="ab017-119">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="ab017-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="ab017-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ab017-120">-InputObject</span></span>
<span data-ttu-id="ab017-121">Obiekt zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="ab017-121">The service endpoint policy object.</span></span>

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

### <span data-ttu-id="ab017-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ab017-122">-Name</span></span>
<span data-ttu-id="ab017-123">Nazwa zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="ab017-123">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="ab017-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab017-124">-PassThru</span></span>
<span data-ttu-id="ab017-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="ab017-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="ab017-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab017-126">-ResourceGroupName</span></span>
<span data-ttu-id="ab017-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ab017-127">The resource group name.</span></span>

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

### <span data-ttu-id="ab017-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab017-128">-ResourceId</span></span>
<span data-ttu-id="ab017-129">Identyfikator zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="ab017-129">The ID of service endpoint policy.</span></span>

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

### <span data-ttu-id="ab017-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ab017-130">-Confirm</span></span>
<span data-ttu-id="ab017-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab017-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab017-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab017-132">-WhatIf</span></span>
<span data-ttu-id="ab017-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab017-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab017-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ab017-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab017-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab017-135">CommonParameters</span></span>
<span data-ttu-id="ab017-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab017-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab017-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab017-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab017-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab017-138">INPUTS</span></span>

### <span data-ttu-id="ab017-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ab017-139">System.String</span></span>

### <span data-ttu-id="ab017-140">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ab017-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="ab017-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab017-141">OUTPUTS</span></span>

### <span data-ttu-id="ab017-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab017-142">System.Boolean</span></span>

## <span data-ttu-id="ab017-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab017-143">NOTES</span></span>

## <span data-ttu-id="ab017-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab017-144">RELATED LINKS</span></span>

[<span data-ttu-id="ab017-145">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ab017-145">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="ab017-146">Nowe — AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ab017-146">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="ab017-147">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ab017-147">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
