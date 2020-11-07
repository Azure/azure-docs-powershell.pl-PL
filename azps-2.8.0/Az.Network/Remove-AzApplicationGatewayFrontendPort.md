---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: bb37c72368832ee4bbccb6e4c10a227e72ba127f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871292"
---
# <span data-ttu-id="b95af-101">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b95af-101">Remove-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="b95af-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b95af-102">SYNOPSIS</span></span>
<span data-ttu-id="b95af-103">Usuwa port frontonu z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b95af-103">Removes a front-end port from an application gateway.</span></span>

## <span data-ttu-id="b95af-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b95af-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b95af-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b95af-105">DESCRIPTION</span></span>
<span data-ttu-id="b95af-106">Polecenie cmdlet **Remove-AzApplicationGatewayFrontendPort** usuwa port frontonu z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b95af-106">The **Remove-AzApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="b95af-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b95af-107">EXAMPLES</span></span>

### <span data-ttu-id="b95af-108">Przykład: usuwanie portu frontonu z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="b95af-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="b95af-109">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje bramę w $AppGw zmiennej.</span><span class="sxs-lookup"><span data-stu-id="b95af-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>
<span data-ttu-id="b95af-110">Drugie polecenie usuwa port o nazwie FrontEndPort02 z bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="b95af-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="b95af-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b95af-111">PARAMETERS</span></span>

### <span data-ttu-id="b95af-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b95af-112">-ApplicationGateway</span></span>
<span data-ttu-id="b95af-113">Określa bramę aplikacji, z której ma zostać usunięty port frontonu.</span><span class="sxs-lookup"><span data-stu-id="b95af-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="b95af-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b95af-114">-DefaultProfile</span></span>
<span data-ttu-id="b95af-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b95af-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b95af-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b95af-116">-Name</span></span>
<span data-ttu-id="b95af-117">Określa nazwę portu frontonu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="b95af-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="b95af-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b95af-118">CommonParameters</span></span>
<span data-ttu-id="b95af-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b95af-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b95af-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b95af-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b95af-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b95af-121">INPUTS</span></span>

### <span data-ttu-id="b95af-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b95af-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b95af-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b95af-123">OUTPUTS</span></span>

### <span data-ttu-id="b95af-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b95af-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b95af-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b95af-125">NOTES</span></span>

## <span data-ttu-id="b95af-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b95af-126">RELATED LINKS</span></span>

[<span data-ttu-id="b95af-127">Dodaj-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b95af-127">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="b95af-128">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b95af-128">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="b95af-129">Nowe — AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b95af-129">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="b95af-130">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b95af-130">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


