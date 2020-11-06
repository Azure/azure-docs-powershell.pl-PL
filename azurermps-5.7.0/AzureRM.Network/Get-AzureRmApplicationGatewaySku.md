---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: 425955dd9b39b78c599262f7681c97dd15c93fb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526793"
---
# <span data-ttu-id="97a64-101">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="97a64-101">Get-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="97a64-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="97a64-102">SYNOPSIS</span></span>
<span data-ttu-id="97a64-103">Pobiera jednostkę SKU bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="97a64-103">Gets the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97a64-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="97a64-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97a64-105">Opis</span><span class="sxs-lookup"><span data-stu-id="97a64-105">DESCRIPTION</span></span>
<span data-ttu-id="97a64-106">Polecenie cmdlet **Get-AzureRmApplicationGatewaySku** pobiera jednostkę SKU (Stocking Unit) bramy Application.</span><span class="sxs-lookup"><span data-stu-id="97a64-106">The **Get-AzureRmApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="97a64-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="97a64-107">EXAMPLES</span></span>

### <span data-ttu-id="97a64-108">Przykład 1: uzyskiwanie jednostki SKU bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="97a64-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzureRmApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="97a64-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="97a64-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="97a64-110">Drugie polecenie pobiera jednostkę SKU bramy Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $SKU.</span><span class="sxs-lookup"><span data-stu-id="97a64-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="97a64-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="97a64-111">PARAMETERS</span></span>

### <span data-ttu-id="97a64-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97a64-112">-ApplicationGateway</span></span>
<span data-ttu-id="97a64-113">Określa obiekt bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="97a64-113">Specifies the application gateway object.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97a64-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a64-114">-DefaultProfile</span></span>
<span data-ttu-id="97a64-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="97a64-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97a64-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a64-116">CommonParameters</span></span>
<span data-ttu-id="97a64-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97a64-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a64-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97a64-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a64-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97a64-119">INPUTS</span></span>

### <span data-ttu-id="97a64-120">System. String</span><span class="sxs-lookup"><span data-stu-id="97a64-120">System.String</span></span>

## <span data-ttu-id="97a64-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="97a64-121">OUTPUTS</span></span>

### <span data-ttu-id="97a64-122">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="97a64-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="97a64-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="97a64-123">NOTES</span></span>

## <span data-ttu-id="97a64-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97a64-124">RELATED LINKS</span></span>

[<span data-ttu-id="97a64-125">Nowe — AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="97a64-125">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="97a64-126">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="97a64-126">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)


