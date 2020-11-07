---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: ec568878c6ecd1d7f80caeb3a77c16c0838373a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717041"
---
# <span data-ttu-id="7fd3c-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fd3c-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="7fd3c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7fd3c-102">SYNOPSIS</span></span>
<span data-ttu-id="7fd3c-103">Pobiera konfigurację WAF bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7fd3c-103">Gets the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fd3c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7fd3c-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fd3c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7fd3c-105">DESCRIPTION</span></span>
<span data-ttu-id="7fd3c-106">Polecenie cmdlet **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** Pobiera konfigurację zapory aplikacji sieci Web (WAF) bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7fd3c-106">The **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="7fd3c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7fd3c-107">EXAMPLES</span></span>

### <span data-ttu-id="7fd3c-108">Przykład 1: Uzyskiwanie konfiguracji zapory aplikacji sieci Web bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="7fd3c-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="7fd3c-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01, a następnie zapisuje ją w zmiennej $AppGW.</span><span class="sxs-lookup"><span data-stu-id="7fd3c-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>

<span data-ttu-id="7fd3c-110">Drugie polecenie pobiera konfigurację zapory bramy Application Gateway w $AppGW, a następnie przechowuje ją w $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="7fd3c-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="7fd3c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7fd3c-111">PARAMETERS</span></span>

### <span data-ttu-id="7fd3c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7fd3c-112">-ApplicationGateway</span></span>
<span data-ttu-id="7fd3c-113">Określa obiekt bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7fd3c-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="7fd3c-114">Możesz użyć polecenia cmdlet Get-AzureRmApplicationGateway, aby uzyskać obiekt bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7fd3c-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="7fd3c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fd3c-115">-DefaultProfile</span></span>
<span data-ttu-id="7fd3c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7fd3c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fd3c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fd3c-117">CommonParameters</span></span>
<span data-ttu-id="7fd3c-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fd3c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fd3c-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fd3c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fd3c-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7fd3c-120">INPUTS</span></span>

### <span data-ttu-id="7fd3c-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7fd3c-121">PSApplicationGateway</span></span>
<span data-ttu-id="7fd3c-122">Parametr "ApplicationGateway" akceptuje wartość typu "PSApplicationGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="7fd3c-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="7fd3c-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7fd3c-123">OUTPUTS</span></span>

### <span data-ttu-id="7fd3c-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fd3c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="7fd3c-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7fd3c-125">NOTES</span></span>

## <span data-ttu-id="7fd3c-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7fd3c-126">RELATED LINKS</span></span>

[<span data-ttu-id="7fd3c-127">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7fd3c-127">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="7fd3c-128">Nowe — AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fd3c-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="7fd3c-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fd3c-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


