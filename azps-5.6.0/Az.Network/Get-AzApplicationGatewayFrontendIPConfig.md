---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: cab20e2b92343549b5138f14f88505c70624effb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996549"
---
# <span data-ttu-id="abb20-101">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="abb20-101">Get-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="abb20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abb20-102">SYNOPSIS</span></span>
<span data-ttu-id="abb20-103">Pobiera konfigurację fronto strony ip bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="abb20-103">Gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="abb20-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="abb20-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abb20-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="abb20-105">DESCRIPTION</span></span>
<span data-ttu-id="abb20-106">Polecenie **cmdlet Get-AzApplicationGatewayFrontendIPConfig** pobiera konfigurację frontoletowego adresu IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="abb20-106">The **Get-AzApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="abb20-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="abb20-107">EXAMPLES</span></span>

### <span data-ttu-id="abb20-108">Przykład 1. Uzyskiwanie określonej konfiguracji frontoronu protokołu IP</span><span class="sxs-lookup"><span data-stu-id="abb20-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="abb20-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 z grupy zasobów o nazwie ResourceGroup01 i przechowuje ją w zmiennej $AppGw zasobów. Drugie polecenie pobiera z programu $AppGw frontonu konfigurację adresów IP o nazwie FrontEndIP01 i zapisuje ją w $FrontEndIP sieci.</span><span class="sxs-lookup"><span data-stu-id="abb20-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="abb20-110">Przykład 2. Uzyskiwanie listy konfiguracji frontoronu IP</span><span class="sxs-lookup"><span data-stu-id="abb20-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="abb20-111">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 z grupy zasobów o nazwie ResourceGroup01 i przechowuje ją w zmiennej $AppGw zasobów. Drugie polecenie pobiera listę frontonu konfiguracji adresów IP z usługi $AppGw i przechowuje je w $FrontEndIPs danych.</span><span class="sxs-lookup"><span data-stu-id="abb20-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="abb20-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="abb20-112">PARAMETERS</span></span>

### <span data-ttu-id="abb20-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="abb20-113">-ApplicationGateway</span></span>
<span data-ttu-id="abb20-114">Określa obiekt bramy aplikacji, który zawiera konfigurację frontoronu ip.</span><span class="sxs-lookup"><span data-stu-id="abb20-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="abb20-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abb20-115">-DefaultProfile</span></span>
<span data-ttu-id="abb20-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="abb20-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abb20-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="abb20-117">-Name</span></span>
<span data-ttu-id="abb20-118">Określa nazwę konfiguracji frontoronu ip, która jest owana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abb20-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb20-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abb20-119">CommonParameters</span></span>
<span data-ttu-id="abb20-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abb20-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abb20-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="abb20-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abb20-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="abb20-122">INPUTS</span></span>

### <span data-ttu-id="abb20-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="abb20-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="abb20-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="abb20-124">OUTPUTS</span></span>

### <span data-ttu-id="abb20-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="abb20-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="abb20-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="abb20-126">NOTES</span></span>

## <span data-ttu-id="abb20-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="abb20-127">RELATED LINKS</span></span>

[<span data-ttu-id="abb20-128">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="abb20-128">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="abb20-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="abb20-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="abb20-130">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="abb20-130">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="abb20-131">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="abb20-131">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


