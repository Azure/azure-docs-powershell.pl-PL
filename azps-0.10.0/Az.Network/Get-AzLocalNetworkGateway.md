---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 88c17626da87608a1086331289cb99f8e7668e5a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890761"
---
# <span data-ttu-id="4cbbb-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4cbbb-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="4cbbb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4cbbb-102">SYNOPSIS</span></span>
<span data-ttu-id="4cbbb-103">Pobiera bramę sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="4cbbb-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="4cbbb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4cbbb-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cbbb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4cbbb-105">DESCRIPTION</span></span>
<span data-ttu-id="4cbbb-106">Lokalna Brama sieci to obiekt reprezentujący urządzenie VPN.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="4cbbb-107">Polecenie cmdlet **Get-AzLocalNetworkGateway** zwraca obiekt reprezentujący bramę on-środowisku na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="4cbbb-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4cbbb-108">EXAMPLES</span></span>

### <span data-ttu-id="4cbbb-109">1: uzyskiwanie bramy sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="4cbbb-109">1: Get a Local Network Gateway</span></span>
```
Get-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="4cbbb-110">Zwraca obiekt bramy sieci lokalnej o nazwie "myLocalGW" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="4cbbb-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="4cbbb-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4cbbb-111">PARAMETERS</span></span>

### <span data-ttu-id="4cbbb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cbbb-112">-DefaultProfile</span></span>
<span data-ttu-id="4cbbb-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cbbb-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4cbbb-114">-Name</span></span>
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

### <span data-ttu-id="4cbbb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cbbb-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="4cbbb-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cbbb-116">CommonParameters</span></span>
<span data-ttu-id="4cbbb-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cbbb-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cbbb-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cbbb-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cbbb-119">INPUTS</span></span>

## <span data-ttu-id="4cbbb-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4cbbb-120">OUTPUTS</span></span>

### <span data-ttu-id="4cbbb-121">Microsoft. Azure. Commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4cbbb-121">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="4cbbb-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4cbbb-122">NOTES</span></span>

## <span data-ttu-id="4cbbb-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4cbbb-123">RELATED LINKS</span></span>

