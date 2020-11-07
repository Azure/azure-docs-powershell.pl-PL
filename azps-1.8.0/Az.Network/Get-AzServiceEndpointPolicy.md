---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
ms.openlocfilehash: fdff53931891ce62b2182f2c8c78d54312141f5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709462"
---
# <span data-ttu-id="b3226-101">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b3226-101">Get-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="b3226-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3226-102">SYNOPSIS</span></span>
<span data-ttu-id="b3226-103">Pobiera zasadę punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="b3226-103">Gets a service endpoint policy.</span></span>

## <span data-ttu-id="b3226-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3226-104">SYNTAX</span></span>

### <span data-ttu-id="b3226-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b3226-105">ListParameterSet (Default)</span></span>
```
Get-AzServiceEndpointPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3226-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3226-106">GetByResourceIdParameterSet</span></span>
```
Get-AzServiceEndpointPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3226-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b3226-107">DESCRIPTION</span></span>
<span data-ttu-id="b3226-108">Polecenie cmdlet **Get-AzServiceEndpointPolicy** pobiera zasadę punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="b3226-108">The **Get-AzServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="b3226-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3226-109">EXAMPLES</span></span>

### <span data-ttu-id="b3226-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b3226-110">Example 1</span></span>
```
$policy = Get-AzServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b3226-111">To polecenie pobiera zasady punktu końcowego usługi o nazwie ServiceEndpointPolicy1 należące do grupy zasobów o nazwie ResourceGroup01 i zapisuje je w zmiennej $policy.</span><span class="sxs-lookup"><span data-stu-id="b3226-111">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="b3226-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b3226-112">Example 2</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b3226-113">To polecenie pobiera listę wszystkich zasad punktu końcowego usługi w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $policyList.</span><span class="sxs-lookup"><span data-stu-id="b3226-113">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

### <span data-ttu-id="b3226-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b3226-114">Example 3</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ServiceEndpointPolicy*"
```

<span data-ttu-id="b3226-115">To polecenie powoduje wyświetlenie listy wszystkich zasad punktu końcowego usługi, które zaczynają się od "ServiceEndpointPolicy".</span><span class="sxs-lookup"><span data-stu-id="b3226-115">This command gets a list of all the service endpoint policies that start with "ServiceEndpointPolicy".</span></span>

## <span data-ttu-id="b3226-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3226-116">PARAMETERS</span></span>

### <span data-ttu-id="b3226-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3226-117">-DefaultProfile</span></span>
<span data-ttu-id="b3226-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3226-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3226-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b3226-119">-Name</span></span>
<span data-ttu-id="b3226-120">Nazwa zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="b3226-120">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="b3226-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3226-121">-ResourceGroupName</span></span>
<span data-ttu-id="b3226-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b3226-122">The resource group name.</span></span>

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

### <span data-ttu-id="b3226-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3226-123">-ResourceId</span></span>
<span data-ttu-id="b3226-124">Identyfikator zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="b3226-124">The ID of the service endpoint policy.</span></span>

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

### <span data-ttu-id="b3226-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b3226-125">-Confirm</span></span>
<span data-ttu-id="b3226-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3226-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3226-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3226-127">-WhatIf</span></span>
<span data-ttu-id="b3226-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3226-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3226-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b3226-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3226-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3226-130">CommonParameters</span></span>
<span data-ttu-id="b3226-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3226-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3226-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3226-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3226-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3226-133">INPUTS</span></span>

### <span data-ttu-id="b3226-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b3226-134">System.String</span></span>

## <span data-ttu-id="b3226-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3226-135">OUTPUTS</span></span>

### <span data-ttu-id="b3226-136">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b3226-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="b3226-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3226-137">NOTES</span></span>

## <span data-ttu-id="b3226-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3226-138">RELATED LINKS</span></span>

[<span data-ttu-id="b3226-139">Nowe — AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b3226-139">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="b3226-140">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b3226-140">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="b3226-141">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b3226-141">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)