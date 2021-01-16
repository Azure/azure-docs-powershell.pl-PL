---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 9512d2d2a51e70b2a0b5e7aa2e8240a8aeb1be1a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330241"
---
# <span data-ttu-id="95ab1-101">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="95ab1-101">Set-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="95ab1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="95ab1-102">SYNOPSIS</span></span>
<span data-ttu-id="95ab1-103">Modyfikuje konfigurację uwierzytelniania klienta obiektu profilu SSL.</span><span class="sxs-lookup"><span data-stu-id="95ab1-103">Modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="95ab1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="95ab1-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-VerifyClientCertIssuerDN] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95ab1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="95ab1-105">DESCRIPTION</span></span>
<span data-ttu-id="95ab1-106">Polecenie cmdlet **Set-AzApplicationGatewayClientAuthConfiguration** modyfikuje konfigurację uwierzytelniania klienta obiektu profilu SSL.</span><span class="sxs-lookup"><span data-stu-id="95ab1-106">The **Set-AzApplicationGatewayClientAuthConfiguration** cmdlet modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="95ab1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="95ab1-107">EXAMPLES</span></span>

### <span data-ttu-id="95ab1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="95ab1-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile -VerifyClientCertIssuerDN
```

<span data-ttu-id="95ab1-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="95ab1-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="95ab1-110">Drugie polecenie pobiera profil SSL o nazwie SslProfile01 dla $AppGw i zapisuje ustawienia w zmiennej $profile.</span><span class="sxs-lookup"><span data-stu-id="95ab1-110">The second command gets the ssl profile named SslProfile01 for $AppGw and stores the settings in the $profile variable.</span></span> <span data-ttu-id="95ab1-111">Ostatnie polecenie modyfikuje konfigurację uwierzytelniania klienta w obiekcie profilu SSL przechowywanym w $profile.</span><span class="sxs-lookup"><span data-stu-id="95ab1-111">The last command modifies the client auth configuration of the ssl profile object stored in $profile.</span></span>

## <span data-ttu-id="95ab1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="95ab1-112">PARAMETERS</span></span>

### <span data-ttu-id="95ab1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95ab1-113">-DefaultProfile</span></span>
<span data-ttu-id="95ab1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="95ab1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95ab1-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="95ab1-115">-SslProfile</span></span>
<span data-ttu-id="95ab1-116">Profil SSL</span><span class="sxs-lookup"><span data-stu-id="95ab1-116">The ssl profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95ab1-117">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="95ab1-117">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="95ab1-118">Sprawdź nazwę wystawcy certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="95ab1-118">Verify client certificate issuer name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95ab1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95ab1-119">CommonParameters</span></span>
<span data-ttu-id="95ab1-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95ab1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95ab1-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95ab1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95ab1-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95ab1-122">INPUTS</span></span>

### <span data-ttu-id="95ab1-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="95ab1-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="95ab1-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="95ab1-124">OUTPUTS</span></span>

### <span data-ttu-id="95ab1-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="95ab1-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="95ab1-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="95ab1-126">NOTES</span></span>

## <span data-ttu-id="95ab1-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95ab1-127">RELATED LINKS</span></span>

[<span data-ttu-id="95ab1-128">Dodaj-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="95ab1-128">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="95ab1-129">Nowe — AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="95ab1-129">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="95ab1-130">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="95ab1-130">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="95ab1-131">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="95ab1-131">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)