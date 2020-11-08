---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: fbab2b1b9887fa7a5d509b46909f29eb741959bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232836"
---
# <span data-ttu-id="5da87-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5da87-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="5da87-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5da87-102">SYNOPSIS</span></span>
<span data-ttu-id="5da87-103">Pobiera certyfikat uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5da87-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="5da87-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5da87-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5da87-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5da87-105">DESCRIPTION</span></span>
<span data-ttu-id="5da87-106">Polecenie cmdlet **Get-AzApplicationGatewayAuthenticationCertificate** pobiera certyfikat uwierzytelniania dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5da87-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="5da87-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5da87-107">EXAMPLES</span></span>

### <span data-ttu-id="5da87-108">Przykład 1: uzyskiwanie określonego certyfikatu uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="5da87-108">Example 1: Get a specified authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -Name "pool01" -ApplicationGateway $appgw
```

<span data-ttu-id="5da87-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie appGwName i zapisuje ją w zmiennej $appgw.</span><span class="sxs-lookup"><span data-stu-id="5da87-109">The first command gets the application gateway named appGwName and stores it in the $appgw variable.</span></span>
<span data-ttu-id="5da87-110">Drugie polecenie pobiera certyfikat uwierzytelniania o nazwie pool01 i zapisuje go w zmiennej $pool.</span><span class="sxs-lookup"><span data-stu-id="5da87-110">The second command gets the authentication certificate named pool01 and stores it in the $pool variable.</span></span>

## <span data-ttu-id="5da87-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5da87-111">PARAMETERS</span></span>

### <span data-ttu-id="5da87-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5da87-112">-ApplicationGateway</span></span>
<span data-ttu-id="5da87-113">Określa nazwę bramy aplikacji, dla której to polecenie cmdlet pobiera certyfikat uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="5da87-113">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="5da87-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5da87-114">-DefaultProfile</span></span>
<span data-ttu-id="5da87-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5da87-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5da87-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5da87-116">-Name</span></span>
<span data-ttu-id="5da87-117">Określa nazwę certyfikatu uwierzytelniania, który ma być pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5da87-117">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5da87-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5da87-118">CommonParameters</span></span>
<span data-ttu-id="5da87-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5da87-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5da87-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5da87-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5da87-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5da87-121">INPUTS</span></span>

### <span data-ttu-id="5da87-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5da87-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5da87-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5da87-123">OUTPUTS</span></span>

### <span data-ttu-id="5da87-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5da87-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="5da87-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5da87-125">NOTES</span></span>
* <span data-ttu-id="5da87-126">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="5da87-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="5da87-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5da87-127">RELATED LINKS</span></span>

[<span data-ttu-id="5da87-128">Dodaj-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5da87-128">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5da87-129">Nowe — AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5da87-129">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5da87-130">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5da87-130">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5da87-131">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5da87-131">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


