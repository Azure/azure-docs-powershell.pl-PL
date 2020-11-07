---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 88393e7c40ba9888602f144410263e7210a3db9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709622"
---
# <span data-ttu-id="45b06-101">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="45b06-101">Get-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="45b06-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45b06-102">SYNOPSIS</span></span>
<span data-ttu-id="45b06-103">Pobiera konfigurację IP frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="45b06-103">Gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="45b06-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45b06-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45b06-105">Opis</span><span class="sxs-lookup"><span data-stu-id="45b06-105">DESCRIPTION</span></span>
<span data-ttu-id="45b06-106">Polecenie cmdlet **Get-AzApplicationGatewayFrontendIPConfig** Pobiera konfigurację IP frontonu bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="45b06-106">The **Get-AzApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="45b06-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45b06-107">EXAMPLES</span></span>

### <span data-ttu-id="45b06-108">Przykład 1: uzyskiwanie określonej konfiguracji frontonu IP</span><span class="sxs-lookup"><span data-stu-id="45b06-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="45b06-109">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 z grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw. Drugie polecenie pobiera konfigurację IP frontonu o nazwie FrontEndIP01 z $AppGw i zapisuje ją w zmiennej $FrontEndIP.</span><span class="sxs-lookup"><span data-stu-id="45b06-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="45b06-110">Przykład 2: uzyskiwanie listy konfiguracji adresów IP frontonu</span><span class="sxs-lookup"><span data-stu-id="45b06-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="45b06-111">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 z grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw. Drugie polecenie pobiera listę konfiguracji adresów IP frontonu z $AppGw i zapisuje ją w zmiennej $FrontEndIPs.</span><span class="sxs-lookup"><span data-stu-id="45b06-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="45b06-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45b06-112">PARAMETERS</span></span>

### <span data-ttu-id="45b06-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="45b06-113">-ApplicationGateway</span></span>
<span data-ttu-id="45b06-114">Określa obiekt bramy aplikacji, który zawiera konfigurację adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="45b06-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="45b06-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45b06-115">-DefaultProfile</span></span>
<span data-ttu-id="45b06-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="45b06-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45b06-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="45b06-117">-Name</span></span>
<span data-ttu-id="45b06-118">Określa nazwę konfiguracji adresu IP frontonu, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45b06-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b06-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b06-119">CommonParameters</span></span>
<span data-ttu-id="45b06-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45b06-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b06-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45b06-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b06-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45b06-122">INPUTS</span></span>

### <span data-ttu-id="45b06-123">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="45b06-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="45b06-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45b06-124">OUTPUTS</span></span>

### <span data-ttu-id="45b06-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="45b06-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="45b06-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45b06-126">NOTES</span></span>

## <span data-ttu-id="45b06-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45b06-127">RELATED LINKS</span></span>

[<span data-ttu-id="45b06-128">Dodaj-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="45b06-128">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="45b06-129">Nowe — AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="45b06-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="45b06-130">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="45b06-130">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="45b06-131">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="45b06-131">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)

