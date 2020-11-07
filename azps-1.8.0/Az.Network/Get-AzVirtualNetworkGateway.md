---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: 4c2d5c4e3c46c79caa4bd8b47fdc178da4fd6450
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709450"
---
# <span data-ttu-id="09a9a-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="09a9a-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="09a9a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="09a9a-102">SYNOPSIS</span></span>
<span data-ttu-id="09a9a-103">Pobiera bramę sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="09a9a-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="09a9a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="09a9a-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09a9a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="09a9a-105">DESCRIPTION</span></span>
<span data-ttu-id="09a9a-106">Brama sieci wirtualnej to obiekt reprezentujący bramę na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="09a9a-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="09a9a-107">Polecenie cmdlet **Get-AzVirtualNetworkGateway** zwraca obiekt bramy na platformie Azure na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="09a9a-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="09a9a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="09a9a-108">EXAMPLES</span></span>

### <span data-ttu-id="09a9a-109">1: uzyskiwanie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="09a9a-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

<span data-ttu-id="09a9a-110">Zwraca obiekt bramy sieci wirtualnej o nazwie "myGateway1" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="09a9a-110">Returns the object of the Virtual Network Gateway with the name "myGateway1" within the resource group "myRG"</span></span>

### <span data-ttu-id="09a9a-111">2: uzyskiwanie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="09a9a-111">2: Get a Virtual Network Gateway</span></span>
```
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

<span data-ttu-id="09a9a-112">Zwraca wszystkie bramy sieci wirtualnej, które zaczynają się od ciągu "Moja brama" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="09a9a-112">Returns all Virtual Network Gateways that start with "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="09a9a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="09a9a-113">PARAMETERS</span></span>

### <span data-ttu-id="09a9a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09a9a-114">-DefaultProfile</span></span>
<span data-ttu-id="09a9a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="09a9a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09a9a-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="09a9a-116">-Name</span></span>
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

### <span data-ttu-id="09a9a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09a9a-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="09a9a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09a9a-118">CommonParameters</span></span>
<span data-ttu-id="09a9a-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09a9a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09a9a-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09a9a-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09a9a-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09a9a-121">INPUTS</span></span>

### <span data-ttu-id="09a9a-122">System. String</span><span class="sxs-lookup"><span data-stu-id="09a9a-122">System.String</span></span>

## <span data-ttu-id="09a9a-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="09a9a-123">OUTPUTS</span></span>

### <span data-ttu-id="09a9a-124">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="09a9a-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="09a9a-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="09a9a-125">NOTES</span></span>

## <span data-ttu-id="09a9a-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09a9a-126">RELATED LINKS</span></span>

[<span data-ttu-id="09a9a-127">Nowe — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="09a9a-127">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="09a9a-128">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="09a9a-128">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="09a9a-129">Resetowanie — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="09a9a-129">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="09a9a-130">Zmienianie rozmiaru — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="09a9a-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="09a9a-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="09a9a-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
