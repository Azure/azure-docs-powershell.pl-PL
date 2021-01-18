---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: fe21bc83fce1e43e036f68ea64c8a10cf2f3c90e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503233"
---
# <span data-ttu-id="cef1a-101">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="cef1a-101">Remove-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="cef1a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cef1a-102">SYNOPSIS</span></span>
<span data-ttu-id="cef1a-103">Usuwa port frontonu z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cef1a-103">Removes a front-end port from an application gateway.</span></span>

## <span data-ttu-id="cef1a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cef1a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cef1a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cef1a-105">DESCRIPTION</span></span>
<span data-ttu-id="cef1a-106">Polecenie cmdlet **Remove-AzApplicationGatewayFrontendPort** usuwa port frontonu z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cef1a-106">The **Remove-AzApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="cef1a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cef1a-107">EXAMPLES</span></span>

### <span data-ttu-id="cef1a-108">Przykład: usuwanie portu frontonu z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="cef1a-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="cef1a-109">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje bramę w $AppGw zmiennej.</span><span class="sxs-lookup"><span data-stu-id="cef1a-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>
<span data-ttu-id="cef1a-110">Drugie polecenie usuwa port o nazwie FrontEndPort02 z bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="cef1a-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="cef1a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cef1a-111">PARAMETERS</span></span>

### <span data-ttu-id="cef1a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cef1a-112">-ApplicationGateway</span></span>
<span data-ttu-id="cef1a-113">Określa bramę aplikacji, z której ma zostać usunięty port frontonu.</span><span class="sxs-lookup"><span data-stu-id="cef1a-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="cef1a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cef1a-114">-DefaultProfile</span></span>
<span data-ttu-id="cef1a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cef1a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef1a-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cef1a-116">-Name</span></span>
<span data-ttu-id="cef1a-117">Określa nazwę portu frontonu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="cef1a-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="cef1a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef1a-118">CommonParameters</span></span>
<span data-ttu-id="cef1a-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cef1a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef1a-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cef1a-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef1a-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cef1a-121">INPUTS</span></span>

### <span data-ttu-id="cef1a-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cef1a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cef1a-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cef1a-123">OUTPUTS</span></span>

### <span data-ttu-id="cef1a-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cef1a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cef1a-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cef1a-125">NOTES</span></span>

## <span data-ttu-id="cef1a-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cef1a-126">RELATED LINKS</span></span>

[<span data-ttu-id="cef1a-127">Dodaj-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="cef1a-127">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="cef1a-128">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="cef1a-128">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="cef1a-129">Nowe — AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="cef1a-129">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="cef1a-130">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="cef1a-130">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


