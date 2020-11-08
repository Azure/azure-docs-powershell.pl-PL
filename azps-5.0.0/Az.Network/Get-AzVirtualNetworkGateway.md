---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: b17f6e7245cb79a5b1098463e3c6dc0ca2b01c68
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232810"
---
# <span data-ttu-id="9fa68-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9fa68-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="9fa68-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9fa68-102">SYNOPSIS</span></span>
<span data-ttu-id="9fa68-103">Pobiera bramę sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="9fa68-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="9fa68-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9fa68-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fa68-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9fa68-105">DESCRIPTION</span></span>
<span data-ttu-id="9fa68-106">Brama sieci wirtualnej to obiekt reprezentujący bramę na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="9fa68-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="9fa68-107">Polecenie cmdlet **Get-AzVirtualNetworkGateway** zwraca obiekt bramy na platformie Azure na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9fa68-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="9fa68-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9fa68-108">EXAMPLES</span></span>

### <span data-ttu-id="9fa68-109">Przykład 1: uzyskiwanie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="9fa68-109">Example 1: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

<span data-ttu-id="9fa68-110">Zwraca obiekt bramy sieci wirtualnej o nazwie "myGateway1" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="9fa68-110">Returns the object of the Virtual Network Gateway with the name "myGateway1" within the resource group "myRG"</span></span>

### <span data-ttu-id="9fa68-111">Przykład 2: uzyskiwanie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="9fa68-111">Example 2: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

<span data-ttu-id="9fa68-112">Zwraca wszystkie bramy sieci wirtualnej, które zaczynają się od ciągu "Moja brama" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="9fa68-112">Returns all Virtual Network Gateways that start with "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="9fa68-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9fa68-113">PARAMETERS</span></span>

### <span data-ttu-id="9fa68-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fa68-114">-DefaultProfile</span></span>
<span data-ttu-id="9fa68-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9fa68-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fa68-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9fa68-116">-Name</span></span>
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

### <span data-ttu-id="9fa68-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fa68-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="9fa68-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fa68-118">CommonParameters</span></span>
<span data-ttu-id="9fa68-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fa68-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fa68-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9fa68-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fa68-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9fa68-121">INPUTS</span></span>

### <span data-ttu-id="9fa68-122">System. String</span><span class="sxs-lookup"><span data-stu-id="9fa68-122">System.String</span></span>

## <span data-ttu-id="9fa68-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9fa68-123">OUTPUTS</span></span>

### <span data-ttu-id="9fa68-124">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9fa68-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="9fa68-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9fa68-125">NOTES</span></span>

## <span data-ttu-id="9fa68-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9fa68-126">RELATED LINKS</span></span>

[<span data-ttu-id="9fa68-127">Nowe — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9fa68-127">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="9fa68-128">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9fa68-128">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="9fa68-129">Resetowanie — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9fa68-129">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="9fa68-130">Zmienianie rozmiaru — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9fa68-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="9fa68-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9fa68-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
