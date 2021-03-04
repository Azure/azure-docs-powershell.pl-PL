---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
ms.openlocfilehash: eac0d67e2c9ffc77d9387eeb599ad624ac01fbbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006282"
---
# <span data-ttu-id="8eaf8-101">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8eaf8-101">Get-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="8eaf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8eaf8-102">SYNOPSIS</span></span>
<span data-ttu-id="8eaf8-103">Pobiera zasady punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-103">Gets a service endpoint policy.</span></span>

## <span data-ttu-id="8eaf8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8eaf8-104">SYNTAX</span></span>

### <span data-ttu-id="8eaf8-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="8eaf8-105">ListParameterSet (Default)</span></span>
```
Get-AzServiceEndpointPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8eaf8-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8eaf8-106">GetByResourceIdParameterSet</span></span>
```
Get-AzServiceEndpointPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8eaf8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8eaf8-107">DESCRIPTION</span></span>
<span data-ttu-id="8eaf8-108">Polecenie **cmdlet Get-AzServiceEndpointPolicy** pobiera zasady punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-108">The **Get-AzServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="8eaf8-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8eaf8-109">EXAMPLES</span></span>

### <span data-ttu-id="8eaf8-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8eaf8-110">Example 1</span></span>
```
$policy = Get-AzServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8eaf8-111">To polecenie pobiera zasady punktu końcowego usługi o nazwie ServiceEndpointPolicy1, które należą do grupy zasobów o nazwie ResourceGroup01, i zapisuje je w $policy danych.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-111">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="8eaf8-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8eaf8-112">Example 2</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8eaf8-113">To polecenie pobiera listę wszystkich zasad punktu końcowego usługi w grupie zasobów o nazwie ResourceGroup01 i przechowuje je w zmiennej $policyList zasobów.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-113">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

### <span data-ttu-id="8eaf8-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="8eaf8-114">Example 3</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ServiceEndpointPolicy*"
```

<span data-ttu-id="8eaf8-115">To polecenie otrzymuje listę wszystkich zasad punktu końcowego usługi, które zaczynają się od "ServiceEndpointPolicy".</span><span class="sxs-lookup"><span data-stu-id="8eaf8-115">This command gets a list of all the service endpoint policies that start with "ServiceEndpointPolicy".</span></span>

## <span data-ttu-id="8eaf8-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8eaf8-116">PARAMETERS</span></span>

### <span data-ttu-id="8eaf8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eaf8-117">-DefaultProfile</span></span>
<span data-ttu-id="8eaf8-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8eaf8-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8eaf8-119">-Name</span></span>
<span data-ttu-id="8eaf8-120">Nazwa zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="8eaf8-120">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="8eaf8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8eaf8-121">-ResourceGroupName</span></span>
<span data-ttu-id="8eaf8-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="8eaf8-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8eaf8-123">-ResourceId</span></span>
<span data-ttu-id="8eaf8-124">Identyfikator zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-124">The ID of the service endpoint policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eaf8-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8eaf8-125">-Confirm</span></span>
<span data-ttu-id="8eaf8-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8eaf8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8eaf8-127">-WhatIf</span></span>
<span data-ttu-id="8eaf8-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8eaf8-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8eaf8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eaf8-130">CommonParameters</span></span>
<span data-ttu-id="8eaf8-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eaf8-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8eaf8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eaf8-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8eaf8-133">INPUTS</span></span>

### <span data-ttu-id="8eaf8-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8eaf8-134">System.String</span></span>

## <span data-ttu-id="8eaf8-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8eaf8-135">OUTPUTS</span></span>

### <span data-ttu-id="8eaf8-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8eaf8-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="8eaf8-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8eaf8-137">NOTES</span></span>

## <span data-ttu-id="8eaf8-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8eaf8-138">RELATED LINKS</span></span>

[<span data-ttu-id="8eaf8-139">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8eaf8-139">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="8eaf8-140">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8eaf8-140">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="8eaf8-141">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8eaf8-141">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
