---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 1efce67698ca6d2e3a8bc9eeab3d89e00e1833f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203165"
---
# <span data-ttu-id="4a64e-101">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4a64e-101">Get-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="4a64e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a64e-102">SYNOPSIS</span></span>
<span data-ttu-id="4a64e-103">Pobiera konfigurację fronto strony ip bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4a64e-103">Gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="4a64e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4a64e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a64e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4a64e-105">DESCRIPTION</span></span>
<span data-ttu-id="4a64e-106">Polecenie **cmdlet Get-AzApplicationGatewayFrontendIPConfig** pobiera konfigurację frontoletowego adresu IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4a64e-106">The **Get-AzApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="4a64e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4a64e-107">EXAMPLES</span></span>

### <span data-ttu-id="4a64e-108">Przykład 1. Uzyskiwanie określonej konfiguracji frontoronu protokołu IP</span><span class="sxs-lookup"><span data-stu-id="4a64e-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="4a64e-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 z grupy zasobów o nazwie ResourceGroup01 i przechowuje ją w zmiennej $AppGw zasobów. Drugie polecenie pobiera konfigurację frontonu ip o nazwie FrontEndIP01 z programu $AppGw i przechowuje je w $FrontEndIP danych.</span><span class="sxs-lookup"><span data-stu-id="4a64e-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="4a64e-110">Przykład 2. Uzyskiwanie listy konfiguracji frontoronu IP</span><span class="sxs-lookup"><span data-stu-id="4a64e-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="4a64e-111">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 z grupy zasobów o nazwie ResourceGroup01 i przechowuje ją w zmiennej $AppGw zasobów. Drugie polecenie pobiera listę frontonu konfiguracji adresów IP z usługi $AppGw i przechowuje je w $FrontEndIPs danych.</span><span class="sxs-lookup"><span data-stu-id="4a64e-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="4a64e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a64e-112">PARAMETERS</span></span>

### <span data-ttu-id="4a64e-113">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4a64e-113">-ApplicationGateway</span></span>
<span data-ttu-id="4a64e-114">Określa obiekt bramy aplikacji, który zawiera konfigurację frontoronu ip.</span><span class="sxs-lookup"><span data-stu-id="4a64e-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="4a64e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a64e-115">-DefaultProfile</span></span>
<span data-ttu-id="4a64e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a64e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a64e-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4a64e-117">-Name</span></span>
<span data-ttu-id="4a64e-118">Określa nazwę konfiguracji frontoronu ip, która jest otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a64e-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4a64e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a64e-119">CommonParameters</span></span>
<span data-ttu-id="4a64e-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a64e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a64e-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a64e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a64e-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a64e-122">INPUTS</span></span>

### <span data-ttu-id="4a64e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4a64e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4a64e-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a64e-124">OUTPUTS</span></span>

### <span data-ttu-id="4a64e-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a64e-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="4a64e-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4a64e-126">NOTES</span></span>

## <span data-ttu-id="4a64e-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a64e-127">RELATED LINKS</span></span>

[<span data-ttu-id="4a64e-128">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4a64e-128">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="4a64e-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4a64e-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="4a64e-130">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4a64e-130">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="4a64e-131">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4a64e-131">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


