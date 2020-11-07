---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: e8ad9974096f633cd829c4d933f092fd869a4103
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890873"
---
# <span data-ttu-id="716ad-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="716ad-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="716ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="716ad-102">SYNOPSIS</span></span>
<span data-ttu-id="716ad-103">Pobiera jednostkę SKU bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="716ad-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="716ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="716ad-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="716ad-105">Opis</span><span class="sxs-lookup"><span data-stu-id="716ad-105">DESCRIPTION</span></span>
<span data-ttu-id="716ad-106">Polecenie cmdlet **Get-AzApplicationGatewaySku** pobiera jednostkę SKU (Stocking Unit) bramy Application.</span><span class="sxs-lookup"><span data-stu-id="716ad-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="716ad-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="716ad-107">EXAMPLES</span></span>

### <span data-ttu-id="716ad-108">Przykład 1: uzyskiwanie jednostki SKU bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="716ad-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="716ad-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="716ad-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="716ad-110">Drugie polecenie pobiera jednostkę SKU bramy Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $SKU.</span><span class="sxs-lookup"><span data-stu-id="716ad-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="716ad-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="716ad-111">PARAMETERS</span></span>

### <span data-ttu-id="716ad-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="716ad-112">-ApplicationGateway</span></span>
<span data-ttu-id="716ad-113">Określa obiekt bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="716ad-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="716ad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="716ad-114">-DefaultProfile</span></span>
<span data-ttu-id="716ad-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="716ad-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="716ad-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="716ad-116">CommonParameters</span></span>
<span data-ttu-id="716ad-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="716ad-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="716ad-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="716ad-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="716ad-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="716ad-119">INPUTS</span></span>

### <span data-ttu-id="716ad-120">System. String</span><span class="sxs-lookup"><span data-stu-id="716ad-120">System.String</span></span>

## <span data-ttu-id="716ad-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="716ad-121">OUTPUTS</span></span>

### <span data-ttu-id="716ad-122">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="716ad-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="716ad-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="716ad-123">NOTES</span></span>

## <span data-ttu-id="716ad-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="716ad-124">RELATED LINKS</span></span>

[<span data-ttu-id="716ad-125">Nowe — AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="716ad-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="716ad-126">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="716ad-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


