---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: b17f6e7245cb79a5b1098463e3c6dc0ca2b01c68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179850"
---
# <span data-ttu-id="85b8b-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="85b8b-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="85b8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85b8b-102">SYNOPSIS</span></span>
<span data-ttu-id="85b8b-103">Pobiera wirtualną bramę sieciową</span><span class="sxs-lookup"><span data-stu-id="85b8b-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="85b8b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="85b8b-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85b8b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="85b8b-105">DESCRIPTION</span></span>
<span data-ttu-id="85b8b-106">Wirtualna brama sieciowa to obiekt reprezentujący bramę na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="85b8b-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="85b8b-107">Polecenie **cmdlet Get-AzVirtualNetworkGateway** zwraca obiekt bramy na platformie Azure na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="85b8b-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="85b8b-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="85b8b-108">EXAMPLES</span></span>

### <span data-ttu-id="85b8b-109">Przykład 1. Uzyskiwanie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="85b8b-109">Example 1: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

<span data-ttu-id="85b8b-110">Zwraca obiekt wirtualnej bramy sieciowej o nazwie "myGateway1" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="85b8b-110">Returns the object of the Virtual Network Gateway with the name "myGateway1" within the resource group "myRG"</span></span>

### <span data-ttu-id="85b8b-111">Przykład 2. Uzyskiwanie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="85b8b-111">Example 2: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

<span data-ttu-id="85b8b-112">Zwraca wszystkie wirtualne bramy sieciowe, które zaczynają się od ciągu "myGateway" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="85b8b-112">Returns all Virtual Network Gateways that start with "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="85b8b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85b8b-113">PARAMETERS</span></span>

### <span data-ttu-id="85b8b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85b8b-114">-DefaultProfile</span></span>
<span data-ttu-id="85b8b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="85b8b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85b8b-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="85b8b-116">-Name</span></span>
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

### <span data-ttu-id="85b8b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85b8b-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="85b8b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85b8b-118">CommonParameters</span></span>
<span data-ttu-id="85b8b-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85b8b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85b8b-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85b8b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85b8b-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85b8b-121">INPUTS</span></span>

### <span data-ttu-id="85b8b-122">System.String</span><span class="sxs-lookup"><span data-stu-id="85b8b-122">System.String</span></span>

## <span data-ttu-id="85b8b-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85b8b-123">OUTPUTS</span></span>

### <span data-ttu-id="85b8b-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="85b8b-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="85b8b-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="85b8b-125">NOTES</span></span>

## <span data-ttu-id="85b8b-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85b8b-126">RELATED LINKS</span></span>

[<span data-ttu-id="85b8b-127">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="85b8b-127">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="85b8b-128">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="85b8b-128">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="85b8b-129">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="85b8b-129">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="85b8b-130">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="85b8b-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="85b8b-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="85b8b-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
