---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: af925c1de08a5a615f5435bb20377582fedc0089
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554264"
---
# <span data-ttu-id="b8556-101">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b8556-101">Get-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="b8556-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b8556-102">SYNOPSIS</span></span>
<span data-ttu-id="b8556-103">Pobiera bramę sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b8556-103">Gets a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8556-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b8556-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8556-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b8556-105">DESCRIPTION</span></span>
<span data-ttu-id="b8556-106">Brama sieci wirtualnej to obiekt reprezentujący bramę na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="b8556-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="b8556-107">Polecenie cmdlet **Get-AzureRmVirtualNetworkGateway** zwraca obiekt bramy na platformie Azure na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b8556-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="b8556-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b8556-108">EXAMPLES</span></span>

### <span data-ttu-id="b8556-109">1: uzyskiwanie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b8556-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="b8556-110">Zwraca obiekt bramy sieci wirtualnej o nazwie "Moja brama" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="b8556-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="b8556-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b8556-111">PARAMETERS</span></span>

### <span data-ttu-id="b8556-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8556-112">-DefaultProfile</span></span>
<span data-ttu-id="b8556-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b8556-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8556-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b8556-114">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8556-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8556-115">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8556-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8556-116">CommonParameters</span></span>
<span data-ttu-id="b8556-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8556-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8556-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8556-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8556-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8556-119">INPUTS</span></span>

### <span data-ttu-id="b8556-120">System. String</span><span class="sxs-lookup"><span data-stu-id="b8556-120">System.String</span></span>

## <span data-ttu-id="b8556-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b8556-121">OUTPUTS</span></span>

### <span data-ttu-id="b8556-122">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b8556-122">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="b8556-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b8556-123">NOTES</span></span>

## <span data-ttu-id="b8556-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8556-124">RELATED LINKS</span></span>
