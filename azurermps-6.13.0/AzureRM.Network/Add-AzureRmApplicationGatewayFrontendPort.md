---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 81952db3ce99ea41388d85085d58a2fb54ccc63f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551200"
---
# <span data-ttu-id="a1133-101">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a1133-101">Add-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="a1133-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a1133-102">SYNOPSIS</span></span>
<span data-ttu-id="a1133-103">Dodaje port frontonu do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a1133-103">Adds a front-end port to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1133-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a1133-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1133-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a1133-105">DESCRIPTION</span></span>
<span data-ttu-id="a1133-106">Polecenie cmdlet **Add-AzureRmApplicationGatewayFrontendPort** dodaje port frontonu do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a1133-106">The **Add-AzureRmApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="a1133-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a1133-107">EXAMPLES</span></span>

### <span data-ttu-id="a1133-108">Przykład 1. Dodaj port frontonu do bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="a1133-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="a1133-109">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a1133-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a1133-110">Drugie polecenie dodaje port 80 jako port frontonu dla bramy aplikacji przechowywanej w $AppGw i nadaje nazwę portowi FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="a1133-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="a1133-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a1133-111">PARAMETERS</span></span>

### <span data-ttu-id="a1133-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a1133-112">-ApplicationGateway</span></span>
<span data-ttu-id="a1133-113">Określa bramę aplikacji, z którą to polecenie cmdlet dodaje port frontonu.</span><span class="sxs-lookup"><span data-stu-id="a1133-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1133-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1133-114">-DefaultProfile</span></span>
<span data-ttu-id="a1133-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1133-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1133-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a1133-116">-Name</span></span>
<span data-ttu-id="a1133-117">Określa nazwę portu frontonu.</span><span class="sxs-lookup"><span data-stu-id="a1133-117">Specifies the name of the front-end port.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1133-118">-Port</span><span class="sxs-lookup"><span data-stu-id="a1133-118">-Port</span></span>
<span data-ttu-id="a1133-119">Określa numer portu.</span><span class="sxs-lookup"><span data-stu-id="a1133-119">Specifies the port number.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1133-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1133-120">CommonParameters</span></span>
<span data-ttu-id="a1133-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1133-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1133-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1133-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1133-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1133-123">INPUTS</span></span>

### <span data-ttu-id="a1133-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a1133-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="a1133-125">Parametry: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a1133-125">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="a1133-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a1133-126">OUTPUTS</span></span>

### <span data-ttu-id="a1133-127">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a1133-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a1133-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a1133-128">NOTES</span></span>

## <span data-ttu-id="a1133-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1133-129">RELATED LINKS</span></span>

[<span data-ttu-id="a1133-130">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a1133-130">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="a1133-131">Nowe — AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a1133-131">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="a1133-132">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a1133-132">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="a1133-133">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a1133-133">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


