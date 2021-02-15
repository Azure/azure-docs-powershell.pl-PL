---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: def44c0925239aed345eed84b4f34690d2db8746
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100395694"
---
# <span data-ttu-id="6e40a-101">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e40a-101">Set-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="6e40a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e40a-102">SYNOPSIS</span></span>
<span data-ttu-id="6e40a-103">Modyfikuje konfigurację uwierzytelniania klienta obiektu profilu ssl.</span><span class="sxs-lookup"><span data-stu-id="6e40a-103">Modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="6e40a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6e40a-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-VerifyClientCertIssuerDN] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e40a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6e40a-105">DESCRIPTION</span></span>
<span data-ttu-id="6e40a-106">Polecenie **cmdlet Set-AzApplicationGatewayClientAuthConfiguration** modyfikuje konfigurację uwierzytelniania klienta obiektu profilu ssl.</span><span class="sxs-lookup"><span data-stu-id="6e40a-106">The **Set-AzApplicationGatewayClientAuthConfiguration** cmdlet modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="6e40a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6e40a-107">EXAMPLES</span></span>

### <span data-ttu-id="6e40a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6e40a-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile -VerifyClientCertIssuerDN
```

<span data-ttu-id="6e40a-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="6e40a-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="6e40a-110">Drugie polecenie pobiera profil ssl o nazwie SslProfile01 for $AppGw i zapisuje ustawienia w $profile pliku.</span><span class="sxs-lookup"><span data-stu-id="6e40a-110">The second command gets the ssl profile named SslProfile01 for $AppGw and stores the settings in the $profile variable.</span></span> <span data-ttu-id="6e40a-111">Ostatnie polecenie modyfikuje konfigurację uwierzytelniania klienta obiektu profilu ssl przechowywanego w $profile.</span><span class="sxs-lookup"><span data-stu-id="6e40a-111">The last command modifies the client auth configuration of the ssl profile object stored in $profile.</span></span>

## <span data-ttu-id="6e40a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e40a-112">PARAMETERS</span></span>

### <span data-ttu-id="6e40a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e40a-113">-DefaultProfile</span></span>
<span data-ttu-id="6e40a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6e40a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e40a-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="6e40a-115">-SslProfile</span></span>
<span data-ttu-id="6e40a-116">Profil SSL</span><span class="sxs-lookup"><span data-stu-id="6e40a-116">The ssl profile</span></span>

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

### <span data-ttu-id="6e40a-117">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="6e40a-117">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="6e40a-118">Sprawdź nazwę wystawcy certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="6e40a-118">Verify client certificate issuer name.</span></span>

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

### <span data-ttu-id="6e40a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e40a-119">CommonParameters</span></span>
<span data-ttu-id="6e40a-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e40a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e40a-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e40a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e40a-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e40a-122">INPUTS</span></span>

### <span data-ttu-id="6e40a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="6e40a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="6e40a-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6e40a-124">OUTPUTS</span></span>

### <span data-ttu-id="6e40a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="6e40a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="6e40a-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6e40a-126">NOTES</span></span>

## <span data-ttu-id="6e40a-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e40a-127">RELATED LINKS</span></span>


[<span data-ttu-id="6e40a-128">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e40a-128">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="6e40a-129">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e40a-129">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="6e40a-130">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e40a-130">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)
