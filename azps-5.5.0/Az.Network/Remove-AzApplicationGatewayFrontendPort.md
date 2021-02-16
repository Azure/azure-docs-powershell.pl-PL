---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: fe21bc83fce1e43e036f68ea64c8a10cf2f3c90e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179554"
---
# <span data-ttu-id="025ed-101">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="025ed-101">Remove-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="025ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="025ed-102">SYNOPSIS</span></span>
<span data-ttu-id="025ed-103">Usuwa port frontonie z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="025ed-103">Removes a front-end port from an application gateway.</span></span>

## <span data-ttu-id="025ed-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="025ed-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="025ed-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="025ed-105">DESCRIPTION</span></span>
<span data-ttu-id="025ed-106">Polecenie **cmdlet Remove-AzApplicationGatewayFrontendPort** usuwa port frontoronu z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="025ed-106">The **Remove-AzApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="025ed-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="025ed-107">EXAMPLES</span></span>

### <span data-ttu-id="025ed-108">Przykład: usuwanie portu frontoronu z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="025ed-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="025ed-109">Pierwsze polecenie otrzymuje bramę aplikacji o nazwie ApplicationGateway01, która należy do grupy zasobów o nazwie ResourceGroup01 i przechowuje bramę w $AppGw zmienną.</span><span class="sxs-lookup"><span data-stu-id="025ed-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>
<span data-ttu-id="025ed-110">Drugie polecenie usuwa z bramy aplikacji port o nazwie FrontEndPort02.</span><span class="sxs-lookup"><span data-stu-id="025ed-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="025ed-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="025ed-111">PARAMETERS</span></span>

### <span data-ttu-id="025ed-112">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="025ed-112">-ApplicationGateway</span></span>
<span data-ttu-id="025ed-113">Określa bramę aplikacji, z której ma być usuwany port frontonie.</span><span class="sxs-lookup"><span data-stu-id="025ed-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="025ed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="025ed-114">-DefaultProfile</span></span>
<span data-ttu-id="025ed-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="025ed-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="025ed-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="025ed-116">-Name</span></span>
<span data-ttu-id="025ed-117">Określa nazwę portu frontendu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="025ed-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="025ed-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="025ed-118">CommonParameters</span></span>
<span data-ttu-id="025ed-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="025ed-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="025ed-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="025ed-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="025ed-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="025ed-121">INPUTS</span></span>

### <span data-ttu-id="025ed-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="025ed-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="025ed-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="025ed-123">OUTPUTS</span></span>

### <span data-ttu-id="025ed-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="025ed-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="025ed-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="025ed-125">NOTES</span></span>

## <span data-ttu-id="025ed-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="025ed-126">RELATED LINKS</span></span>

[<span data-ttu-id="025ed-127">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="025ed-127">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="025ed-128">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="025ed-128">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="025ed-129">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="025ed-129">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="025ed-130">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="025ed-130">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


