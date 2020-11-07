---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 1a2a8aa8405be5dfc5275a07d253f06f1134e3e7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898723"
---
# <span data-ttu-id="31ddb-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="31ddb-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="31ddb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="31ddb-102">SYNOPSIS</span></span>
<span data-ttu-id="31ddb-103">Pobiera bramę sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="31ddb-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31ddb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="31ddb-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31ddb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="31ddb-105">DESCRIPTION</span></span>
<span data-ttu-id="31ddb-106">Lokalna Brama sieci to obiekt reprezentujący urządzenie VPN.</span><span class="sxs-lookup"><span data-stu-id="31ddb-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="31ddb-107">Polecenie cmdlet **Get-AzureRmLocalNetworkGateway** zwraca obiekt reprezentujący bramę on-środowisku na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="31ddb-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="31ddb-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="31ddb-108">EXAMPLES</span></span>

### <span data-ttu-id="31ddb-109">1: uzyskiwanie bramy sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="31ddb-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="31ddb-110">Zwraca obiekt bramy sieci lokalnej o nazwie "myLocalGW" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="31ddb-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="31ddb-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31ddb-111">PARAMETERS</span></span>

### <span data-ttu-id="31ddb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31ddb-112">-DefaultProfile</span></span>
<span data-ttu-id="31ddb-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="31ddb-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ddb-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="31ddb-114">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31ddb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31ddb-115">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31ddb-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31ddb-116">CommonParameters</span></span>
<span data-ttu-id="31ddb-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31ddb-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31ddb-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31ddb-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31ddb-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31ddb-119">INPUTS</span></span>

## <span data-ttu-id="31ddb-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="31ddb-120">OUTPUTS</span></span>

### <span data-ttu-id="31ddb-121">Microsoft. Azure. Commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="31ddb-121">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="31ddb-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="31ddb-122">NOTES</span></span>

## <span data-ttu-id="31ddb-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31ddb-123">RELATED LINKS</span></span>

