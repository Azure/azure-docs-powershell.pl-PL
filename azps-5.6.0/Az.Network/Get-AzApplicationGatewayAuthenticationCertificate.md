---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 7f5dbd73158e5328ece78b1064a78ff5c4627035
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962801"
---
# <span data-ttu-id="d5995-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d5995-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="d5995-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5995-102">SYNOPSIS</span></span>
<span data-ttu-id="d5995-103">Pobiera certyfikat uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d5995-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="d5995-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d5995-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5995-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d5995-105">DESCRIPTION</span></span>
<span data-ttu-id="d5995-106">Polecenie **cmdlet Get-AzApplicationGatewayAuthenticationCertificate** otrzymuje certyfikat uwierzytelniania dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d5995-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="d5995-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d5995-107">EXAMPLES</span></span>

### <span data-ttu-id="d5995-108">Przykład 1. Uzyskiwanie określonego certyfikatu uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="d5995-108">Example 1: Get a specified authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $cert = Get-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -ApplicationGateway $appgw
```

<span data-ttu-id="d5995-109">Pierwsze polecenie pobiera nazwę bramy aplikacji appGwName i zapisuje ją w $appgw zmienną.</span><span class="sxs-lookup"><span data-stu-id="d5995-109">The first command gets the application gateway named appGwName and stores it in the $appgw variable.</span></span>
<span data-ttu-id="d5995-110">Drugie polecenie pobiera certyfikat uwierzytelniania o nazwie cert01 i przechowuje go w $cert danych.</span><span class="sxs-lookup"><span data-stu-id="d5995-110">The second command gets the authentication certificate named cert01 and stores it in the $cert variable.</span></span>

## <span data-ttu-id="d5995-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5995-111">PARAMETERS</span></span>

### <span data-ttu-id="d5995-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d5995-112">-ApplicationGateway</span></span>
<span data-ttu-id="d5995-113">Określa nazwę bramy aplikacji, dla której to polecenie cmdlet uzyskuje certyfikat uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="d5995-113">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="d5995-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5995-114">-DefaultProfile</span></span>
<span data-ttu-id="d5995-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5995-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5995-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d5995-116">-Name</span></span>
<span data-ttu-id="d5995-117">Określa nazwę certyfikatu uwierzytelniania, który otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5995-117">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d5995-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5995-118">CommonParameters</span></span>
<span data-ttu-id="d5995-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5995-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5995-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5995-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5995-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5995-121">INPUTS</span></span>

### <span data-ttu-id="d5995-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d5995-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d5995-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5995-123">OUTPUTS</span></span>

### <span data-ttu-id="d5995-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d5995-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="d5995-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d5995-125">NOTES</span></span>
* <span data-ttu-id="d5995-126">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="d5995-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d5995-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5995-127">RELATED LINKS</span></span>

[<span data-ttu-id="d5995-128">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d5995-128">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d5995-129">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d5995-129">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d5995-130">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d5995-130">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d5995-131">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d5995-131">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


