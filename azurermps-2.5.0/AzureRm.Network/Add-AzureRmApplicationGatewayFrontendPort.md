---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayfrontendport
schema: 2.0.0
ms.openlocfilehash: 7c4684dd2461446d2e04b1bca3f835647101c960
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898727"
---
# <span data-ttu-id="240fa-101">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="240fa-101">Add-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="240fa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="240fa-102">SYNOPSIS</span></span>
<span data-ttu-id="240fa-103">Dodaje port frontonu do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="240fa-103">Adds a front-end port to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="240fa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="240fa-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="240fa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="240fa-105">DESCRIPTION</span></span>
<span data-ttu-id="240fa-106">Polecenie cmdlet **Add-AzureRmApplicationGatewayFrontendPort** dodaje port frontonu do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="240fa-106">The **Add-AzureRmApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="240fa-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="240fa-107">EXAMPLES</span></span>

### <span data-ttu-id="240fa-108">Przykład 1. Dodaj port frontonu do bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="240fa-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $ AppGw = Add-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="240fa-109">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="240fa-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="240fa-110">Drugie polecenie dodaje port 80 jako port frontonu dla bramy aplikacji przechowywanej w $AppGw i nadaje nazwę portowi FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="240fa-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="240fa-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="240fa-111">PARAMETERS</span></span>

### <span data-ttu-id="240fa-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="240fa-112">-ApplicationGateway</span></span>
<span data-ttu-id="240fa-113">Określa bramę aplikacji, z którą to polecenie cmdlet dodaje port frontonu.</span><span class="sxs-lookup"><span data-stu-id="240fa-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="240fa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="240fa-114">-DefaultProfile</span></span>
<span data-ttu-id="240fa-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="240fa-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="240fa-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="240fa-116">-Name</span></span>
<span data-ttu-id="240fa-117">Określa nazwę portu frontonu.</span><span class="sxs-lookup"><span data-stu-id="240fa-117">Specifies the name of the front-end port.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="240fa-118">-Port</span><span class="sxs-lookup"><span data-stu-id="240fa-118">-Port</span></span>
<span data-ttu-id="240fa-119">Określa numer portu.</span><span class="sxs-lookup"><span data-stu-id="240fa-119">Specifies the port number.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="240fa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="240fa-120">CommonParameters</span></span>
<span data-ttu-id="240fa-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="240fa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="240fa-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="240fa-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="240fa-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="240fa-123">INPUTS</span></span>

### <span data-ttu-id="240fa-124">System. String</span><span class="sxs-lookup"><span data-stu-id="240fa-124">System.String</span></span>

## <span data-ttu-id="240fa-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="240fa-125">OUTPUTS</span></span>

### <span data-ttu-id="240fa-126">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="240fa-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="240fa-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="240fa-127">NOTES</span></span>

## <span data-ttu-id="240fa-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="240fa-128">RELATED LINKS</span></span>

[<span data-ttu-id="240fa-129">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="240fa-129">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="240fa-130">Nowe — AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="240fa-130">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="240fa-131">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="240fa-131">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="240fa-132">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="240fa-132">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


