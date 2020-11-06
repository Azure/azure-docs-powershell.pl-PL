---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: ca23e58b173ee67917099f2743dac7dbd3d1bc4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554129"
---
# <span data-ttu-id="abaa4-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="abaa4-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="abaa4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="abaa4-102">SYNOPSIS</span></span>
<span data-ttu-id="abaa4-103">Pobiera bramę sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="abaa4-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abaa4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="abaa4-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abaa4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="abaa4-105">DESCRIPTION</span></span>
<span data-ttu-id="abaa4-106">Lokalna Brama sieci to obiekt reprezentujący urządzenie VPN.</span><span class="sxs-lookup"><span data-stu-id="abaa4-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="abaa4-107">Polecenie cmdlet **Get-AzureRmLocalNetworkGateway** zwraca obiekt reprezentujący bramę on-środowisku na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="abaa4-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="abaa4-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="abaa4-108">EXAMPLES</span></span>

### <span data-ttu-id="abaa4-109">1: uzyskiwanie bramy sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="abaa4-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="abaa4-110">Zwraca obiekt bramy sieci lokalnej o nazwie "myLocalGW" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="abaa4-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="abaa4-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="abaa4-111">PARAMETERS</span></span>

### <span data-ttu-id="abaa4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abaa4-112">-DefaultProfile</span></span>
<span data-ttu-id="abaa4-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="abaa4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abaa4-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="abaa4-114">-Name</span></span>
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

### <span data-ttu-id="abaa4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abaa4-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="abaa4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abaa4-116">CommonParameters</span></span>
<span data-ttu-id="abaa4-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abaa4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abaa4-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abaa4-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abaa4-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="abaa4-119">INPUTS</span></span>

### <span data-ttu-id="abaa4-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="abaa4-120">None</span></span>
<span data-ttu-id="abaa4-121">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="abaa4-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="abaa4-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="abaa4-122">OUTPUTS</span></span>

### <span data-ttu-id="abaa4-123">Microsoft. Azure. Commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="abaa4-123">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="abaa4-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="abaa4-124">NOTES</span></span>

## <span data-ttu-id="abaa4-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="abaa4-125">RELATED LINKS</span></span>

