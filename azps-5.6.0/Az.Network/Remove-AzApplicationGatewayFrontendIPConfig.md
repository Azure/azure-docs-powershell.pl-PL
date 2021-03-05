---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 0c226cf7dabbc170e137f1a809cee0afe3c7e76f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992538"
---
# <span data-ttu-id="6dcf7-101">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6dcf7-101">Remove-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="6dcf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dcf7-102">SYNOPSIS</span></span>
<span data-ttu-id="6dcf7-103">Usuwa konfigurację frontoronu ip z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6dcf7-103">Removes a front-end IP configuration from an application gateway.</span></span>

## <span data-ttu-id="6dcf7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6dcf7-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6dcf7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6dcf7-105">DESCRIPTION</span></span>
<span data-ttu-id="6dcf7-106">Polecenie **cmdlet Remove-AzApplicationGatewayFrontendIPConfig** usuwa adres IP frontendu z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6dcf7-106">The **Remove-AzApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="6dcf7-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6dcf7-107">EXAMPLES</span></span>

### <span data-ttu-id="6dcf7-108">Przykład 1. Usuwanie konfiguracji frontoronu adresu IP</span><span class="sxs-lookup"><span data-stu-id="6dcf7-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="6dcf7-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 i przechowuje ją w $AppGw zmienną.</span><span class="sxs-lookup"><span data-stu-id="6dcf7-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6dcf7-110">Drugie polecenie usuwa konfigurację frontoronu IP o nazwie FrontEndIP02 z bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="6dcf7-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="6dcf7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6dcf7-111">PARAMETERS</span></span>

### <span data-ttu-id="6dcf7-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6dcf7-112">-ApplicationGateway</span></span>
<span data-ttu-id="6dcf7-113">Określa bramę aplikacji, z której należy usunąć konfigurację frontoronu IP.</span><span class="sxs-lookup"><span data-stu-id="6dcf7-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="6dcf7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dcf7-114">-DefaultProfile</span></span>
<span data-ttu-id="6dcf7-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6dcf7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dcf7-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6dcf7-116">-Name</span></span>
<span data-ttu-id="6dcf7-117">Określa nazwę konfiguracji frontoronu IP do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="6dcf7-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="6dcf7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dcf7-118">CommonParameters</span></span>
<span data-ttu-id="6dcf7-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dcf7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dcf7-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6dcf7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dcf7-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6dcf7-121">INPUTS</span></span>

### <span data-ttu-id="6dcf7-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6dcf7-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6dcf7-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6dcf7-123">OUTPUTS</span></span>

### <span data-ttu-id="6dcf7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6dcf7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6dcf7-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6dcf7-125">NOTES</span></span>

## <span data-ttu-id="6dcf7-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6dcf7-126">RELATED LINKS</span></span>

[<span data-ttu-id="6dcf7-127">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6dcf7-127">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="6dcf7-128">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6dcf7-128">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="6dcf7-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6dcf7-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="6dcf7-130">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6dcf7-130">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


