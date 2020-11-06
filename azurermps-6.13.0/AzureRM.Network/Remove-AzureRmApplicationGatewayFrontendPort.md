---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: de99be99c7b393af6cbbcac8ad9d293c93f4d5c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527837"
---
# <span data-ttu-id="f395e-101">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f395e-101">Remove-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="f395e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f395e-102">SYNOPSIS</span></span>
<span data-ttu-id="f395e-103">Usuwa port frontonu z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f395e-103">Removes a front-end port from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f395e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f395e-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f395e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f395e-105">DESCRIPTION</span></span>
<span data-ttu-id="f395e-106">Polecenie cmdlet **Remove-AzureRmApplicationGatewayFrontendPort** usuwa port frontonu z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f395e-106">The **Remove-AzureRmApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="f395e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f395e-107">EXAMPLES</span></span>

### <span data-ttu-id="f395e-108">Przykład: usuwanie portu frontonu z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="f395e-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="f395e-109">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje bramę w $AppGw zmiennej.</span><span class="sxs-lookup"><span data-stu-id="f395e-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>
<span data-ttu-id="f395e-110">Drugie polecenie usuwa port o nazwie FrontEndPort02 z bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f395e-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="f395e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f395e-111">PARAMETERS</span></span>

### <span data-ttu-id="f395e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f395e-112">-ApplicationGateway</span></span>
<span data-ttu-id="f395e-113">Określa bramę aplikacji, z której ma zostać usunięty port frontonu.</span><span class="sxs-lookup"><span data-stu-id="f395e-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="f395e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f395e-114">-DefaultProfile</span></span>
<span data-ttu-id="f395e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f395e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f395e-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f395e-116">-Name</span></span>
<span data-ttu-id="f395e-117">Określa nazwę portu frontonu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f395e-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="f395e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f395e-118">CommonParameters</span></span>
<span data-ttu-id="f395e-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f395e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f395e-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f395e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f395e-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f395e-121">INPUTS</span></span>

### <span data-ttu-id="f395e-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f395e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="f395e-123">Parametry: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f395e-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="f395e-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f395e-124">OUTPUTS</span></span>

### <span data-ttu-id="f395e-125">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f395e-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f395e-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f395e-126">NOTES</span></span>

## <span data-ttu-id="f395e-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f395e-127">RELATED LINKS</span></span>

[<span data-ttu-id="f395e-128">Dodaj-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f395e-128">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f395e-129">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f395e-129">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f395e-130">Nowe — AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f395e-130">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f395e-131">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f395e-131">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


