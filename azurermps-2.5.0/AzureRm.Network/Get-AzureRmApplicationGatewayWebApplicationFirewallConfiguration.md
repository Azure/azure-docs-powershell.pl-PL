---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
ms.openlocfilehash: 7b83e7f8ca372faf8158e248d326595a0d162d6a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897617"
---
# <span data-ttu-id="d9853-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9853-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="d9853-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d9853-102">SYNOPSIS</span></span>
<span data-ttu-id="d9853-103">Pobiera konfigurację WAF bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d9853-103">Gets the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9853-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d9853-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9853-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d9853-105">DESCRIPTION</span></span>
<span data-ttu-id="d9853-106">Polecenie cmdlet **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** Pobiera konfigurację zapory aplikacji sieci Web (WAF) bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d9853-106">The **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="d9853-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d9853-107">EXAMPLES</span></span>

### <span data-ttu-id="d9853-108">Przykład 1: Uzyskiwanie konfiguracji zapory aplikacji sieci Web bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="d9853-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="d9853-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01, a następnie zapisuje ją w zmiennej $AppGW.</span><span class="sxs-lookup"><span data-stu-id="d9853-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>

<span data-ttu-id="d9853-110">Drugie polecenie pobiera konfigurację zapory bramy Application Gateway w $AppGW, a następnie przechowuje ją w $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="d9853-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="d9853-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d9853-111">PARAMETERS</span></span>

### <span data-ttu-id="d9853-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d9853-112">-ApplicationGateway</span></span>
<span data-ttu-id="d9853-113">Określa obiekt bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d9853-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="d9853-114">Możesz użyć polecenia cmdlet Get-AzureRmApplicationGateway, aby uzyskać obiekt bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d9853-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="d9853-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9853-115">-DefaultProfile</span></span>
<span data-ttu-id="d9853-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9853-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9853-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9853-117">CommonParameters</span></span>
<span data-ttu-id="d9853-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9853-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9853-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9853-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9853-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9853-120">INPUTS</span></span>

### <span data-ttu-id="d9853-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d9853-121">PSApplicationGateway</span></span>
<span data-ttu-id="d9853-122">Parametr "ApplicationGateway" akceptuje wartość typu "PSApplicationGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="d9853-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="d9853-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d9853-123">OUTPUTS</span></span>

### <span data-ttu-id="d9853-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9853-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="d9853-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d9853-125">NOTES</span></span>

## <span data-ttu-id="d9853-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9853-126">RELATED LINKS</span></span>

[<span data-ttu-id="d9853-127">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d9853-127">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="d9853-128">Nowe — AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9853-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="d9853-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9853-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


