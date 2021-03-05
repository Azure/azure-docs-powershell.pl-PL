---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: 70002f85191cda1259cd3b29aa6ee5c6b76a7b94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964298"
---
# <span data-ttu-id="49834-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="49834-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="49834-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49834-102">SYNOPSIS</span></span>
<span data-ttu-id="49834-103">Pobiera wirtualną bramę sieciową</span><span class="sxs-lookup"><span data-stu-id="49834-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="49834-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="49834-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49834-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="49834-105">DESCRIPTION</span></span>
<span data-ttu-id="49834-106">Wirtualna brama sieciowa to obiekt reprezentujący bramę na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="49834-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="49834-107">Polecenie **cmdlet Get-AzVirtualNetworkGateway** zwraca obiekt bramy na platformie Azure na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="49834-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="49834-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="49834-108">EXAMPLES</span></span>

### <span data-ttu-id="49834-109">Przykład 1. Uzyskiwanie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="49834-109">Example 1: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

<span data-ttu-id="49834-110">Zwraca obiekt wirtualnej bramy sieciowej o nazwie "myGateway1" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="49834-110">Returns the object of the Virtual Network Gateway with the name "myGateway1" within the resource group "myRG"</span></span>

### <span data-ttu-id="49834-111">Przykład 2. Uzyskiwanie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="49834-111">Example 2: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

<span data-ttu-id="49834-112">Zwraca wszystkie bramy sieci wirtualnej, których wartość rozpoczyna się od ciągu "myGateway" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="49834-112">Returns all Virtual Network Gateways that start with "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="49834-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49834-113">PARAMETERS</span></span>

### <span data-ttu-id="49834-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49834-114">-DefaultProfile</span></span>
<span data-ttu-id="49834-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="49834-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49834-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="49834-116">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="49834-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49834-117">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="49834-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49834-118">CommonParameters</span></span>
<span data-ttu-id="49834-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49834-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49834-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49834-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49834-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49834-121">INPUTS</span></span>

### <span data-ttu-id="49834-122">System.String</span><span class="sxs-lookup"><span data-stu-id="49834-122">System.String</span></span>

## <span data-ttu-id="49834-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49834-123">OUTPUTS</span></span>

### <span data-ttu-id="49834-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="49834-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="49834-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="49834-125">NOTES</span></span>

## <span data-ttu-id="49834-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49834-126">RELATED LINKS</span></span>

[<span data-ttu-id="49834-127">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="49834-127">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="49834-128">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="49834-128">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="49834-129">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="49834-129">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="49834-130">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="49834-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="49834-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="49834-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
