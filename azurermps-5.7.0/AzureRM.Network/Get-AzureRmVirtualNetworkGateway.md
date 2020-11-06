---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 29d5ad86d9df7bddec8be600d8b7c680c7bcd7fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528054"
---
# <span data-ttu-id="e3c94-101">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e3c94-101">Get-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="e3c94-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e3c94-102">SYNOPSIS</span></span>
<span data-ttu-id="e3c94-103">Pobiera bramę sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e3c94-103">Gets a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3c94-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e3c94-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3c94-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e3c94-105">DESCRIPTION</span></span>
<span data-ttu-id="e3c94-106">Brama sieci wirtualnej to obiekt reprezentujący bramę na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="e3c94-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="e3c94-107">Polecenie cmdlet **Get-AzureRmVirtualNetworkGateway** zwraca obiekt bramy na platformie Azure na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e3c94-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="e3c94-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e3c94-108">EXAMPLES</span></span>

### <span data-ttu-id="e3c94-109">1: uzyskiwanie bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e3c94-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="e3c94-110">Zwraca obiekt bramy sieci wirtualnej o nazwie "Moja brama" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="e3c94-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="e3c94-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3c94-111">PARAMETERS</span></span>

### <span data-ttu-id="e3c94-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3c94-112">-DefaultProfile</span></span>
<span data-ttu-id="e3c94-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e3c94-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3c94-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e3c94-114">-Name</span></span>
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

### <span data-ttu-id="e3c94-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3c94-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="e3c94-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3c94-116">CommonParameters</span></span>
<span data-ttu-id="e3c94-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3c94-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3c94-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3c94-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3c94-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3c94-119">INPUTS</span></span>

### <span data-ttu-id="e3c94-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e3c94-120">None</span></span>
<span data-ttu-id="e3c94-121">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e3c94-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e3c94-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e3c94-122">OUTPUTS</span></span>

### <span data-ttu-id="e3c94-123">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e3c94-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="e3c94-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e3c94-124">NOTES</span></span>

## <span data-ttu-id="e3c94-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3c94-125">RELATED LINKS</span></span>

