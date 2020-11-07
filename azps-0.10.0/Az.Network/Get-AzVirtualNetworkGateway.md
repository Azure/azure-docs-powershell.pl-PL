---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: 490e61142bdbc0bcdd64f18aeeb2fa527e5180b9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890670"
---
# <span data-ttu-id="78cc3-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="78cc3-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="78cc3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78cc3-102">SYNOPSIS</span></span>
<span data-ttu-id="78cc3-103">Pobiera bramę sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="78cc3-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="78cc3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78cc3-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78cc3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="78cc3-105">DESCRIPTION</span></span>
<span data-ttu-id="78cc3-106">Brama sieci wirtualnej to obiekt reprezentujący bramę na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="78cc3-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="78cc3-107">Polecenie cmdlet **Get-AzVirtualNetworkGateway** zwraca obiekt bramy na platformie Azure na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="78cc3-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="78cc3-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78cc3-108">EXAMPLES</span></span>

### <span data-ttu-id="78cc3-109">1: uzyskiwanie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="78cc3-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="78cc3-110">Zwraca obiekt bramy sieci wirtualnej o nazwie "Moja brama" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="78cc3-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="78cc3-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78cc3-111">PARAMETERS</span></span>

### <span data-ttu-id="78cc3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78cc3-112">-DefaultProfile</span></span>
<span data-ttu-id="78cc3-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="78cc3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78cc3-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="78cc3-114">-Name</span></span>
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

### <span data-ttu-id="78cc3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78cc3-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="78cc3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78cc3-116">CommonParameters</span></span>
<span data-ttu-id="78cc3-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78cc3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78cc3-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78cc3-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78cc3-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78cc3-119">INPUTS</span></span>

## <span data-ttu-id="78cc3-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78cc3-120">OUTPUTS</span></span>

### <span data-ttu-id="78cc3-121">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="78cc3-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="78cc3-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78cc3-122">NOTES</span></span>

## <span data-ttu-id="78cc3-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78cc3-123">RELATED LINKS</span></span>

