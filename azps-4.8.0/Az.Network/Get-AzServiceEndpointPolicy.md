---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
ms.openlocfilehash: a74edbec0051e3a77ab3ac10595f787dd45a2dfc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220020"
---
# <span data-ttu-id="b4259-101">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b4259-101">Get-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="b4259-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b4259-102">SYNOPSIS</span></span>
<span data-ttu-id="b4259-103">Pobiera zasadę punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="b4259-103">Gets a service endpoint policy.</span></span>

## <span data-ttu-id="b4259-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b4259-104">SYNTAX</span></span>

### <span data-ttu-id="b4259-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b4259-105">ListParameterSet (Default)</span></span>
```
Get-AzServiceEndpointPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4259-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4259-106">GetByResourceIdParameterSet</span></span>
```
Get-AzServiceEndpointPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4259-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b4259-107">DESCRIPTION</span></span>
<span data-ttu-id="b4259-108">Polecenie cmdlet **Get-AzServiceEndpointPolicy** pobiera zasadę punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="b4259-108">The **Get-AzServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="b4259-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b4259-109">EXAMPLES</span></span>

### <span data-ttu-id="b4259-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b4259-110">Example 1</span></span>
```
$policy = Get-AzServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b4259-111">To polecenie pobiera zasady punktu końcowego usługi o nazwie ServiceEndpointPolicy1 należące do grupy zasobów o nazwie ResourceGroup01 i zapisuje je w zmiennej $policy.</span><span class="sxs-lookup"><span data-stu-id="b4259-111">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="b4259-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b4259-112">Example 2</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b4259-113">To polecenie pobiera listę wszystkich zasad punktu końcowego usługi w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $policyList.</span><span class="sxs-lookup"><span data-stu-id="b4259-113">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

### <span data-ttu-id="b4259-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b4259-114">Example 3</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ServiceEndpointPolicy*"
```

<span data-ttu-id="b4259-115">To polecenie powoduje wyświetlenie listy wszystkich zasad punktu końcowego usługi, które zaczynają się od "ServiceEndpointPolicy".</span><span class="sxs-lookup"><span data-stu-id="b4259-115">This command gets a list of all the service endpoint policies that start with "ServiceEndpointPolicy".</span></span>

## <span data-ttu-id="b4259-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4259-116">PARAMETERS</span></span>

### <span data-ttu-id="b4259-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4259-117">-DefaultProfile</span></span>
<span data-ttu-id="b4259-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4259-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4259-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b4259-119">-Name</span></span>
<span data-ttu-id="b4259-120">Nazwa zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="b4259-120">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="b4259-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4259-121">-ResourceGroupName</span></span>
<span data-ttu-id="b4259-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b4259-122">The resource group name.</span></span>

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

### <span data-ttu-id="b4259-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4259-123">-ResourceId</span></span>
<span data-ttu-id="b4259-124">Identyfikator zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="b4259-124">The ID of the service endpoint policy.</span></span>

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

### <span data-ttu-id="b4259-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b4259-125">-Confirm</span></span>
<span data-ttu-id="b4259-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4259-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4259-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4259-127">-WhatIf</span></span>
<span data-ttu-id="b4259-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4259-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4259-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b4259-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4259-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4259-130">CommonParameters</span></span>
<span data-ttu-id="b4259-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4259-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4259-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4259-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4259-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4259-133">INPUTS</span></span>

### <span data-ttu-id="b4259-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b4259-134">System.String</span></span>

## <span data-ttu-id="b4259-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b4259-135">OUTPUTS</span></span>

### <span data-ttu-id="b4259-136">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b4259-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="b4259-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b4259-137">NOTES</span></span>

## <span data-ttu-id="b4259-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4259-138">RELATED LINKS</span></span>

[<span data-ttu-id="b4259-139">Nowe — AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b4259-139">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="b4259-140">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b4259-140">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="b4259-141">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b4259-141">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
