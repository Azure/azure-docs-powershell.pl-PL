---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: eee7040dab93a4f73bacdf440c6450a525fab9a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326354"
---
# <span data-ttu-id="b5c17-101">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5c17-101">Get-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="b5c17-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5c17-102">SYNOPSIS</span></span>
<span data-ttu-id="b5c17-103">Pobiera konfigurację uwierzytelniania klienta obiektu profilu SSL.</span><span class="sxs-lookup"><span data-stu-id="b5c17-103">Gets the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="b5c17-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5c17-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5c17-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b5c17-105">DESCRIPTION</span></span>
<span data-ttu-id="b5c17-106">Polecenie cmdlet **Get-AzApplicationGatewayClientAuthConfiguration** Pobiera konfigurację uwierzytelniania klienta obiektu profilu SSL.</span><span class="sxs-lookup"><span data-stu-id="b5c17-106">The **Get-AzApplicationGatewayClientAuthConfiguration** cmdlet gets the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="b5c17-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5c17-107">EXAMPLES</span></span>

### <span data-ttu-id="b5c17-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b5c17-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $ClientAuthConfig = Get-AzApplicationGatewayClientAuthConfiguration -SslProfile $SslProfile
```

<span data-ttu-id="b5c17-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b5c17-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="b5c17-110">Drugie polecenie pobiera profil SSL o nazwie SslProfile01 dla $AppGw i zapisuje go $SslProfile zmiennej.</span><span class="sxs-lookup"><span data-stu-id="b5c17-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="b5c17-111">Ostatnie polecenie pobiera konfigurację uwierzytelniania klienta z profilu SSL $SslProfile i zapisuje ją w zmiennej $ClientAuthConfig.</span><span class="sxs-lookup"><span data-stu-id="b5c17-111">The last command gets the client authentication configuration from the SSL profile $SslProfile and stores it in the $ClientAuthConfig variable.</span></span>

## <span data-ttu-id="b5c17-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5c17-112">PARAMETERS</span></span>

### <span data-ttu-id="b5c17-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5c17-113">-DefaultProfile</span></span>
<span data-ttu-id="b5c17-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b5c17-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5c17-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="b5c17-115">-SslProfile</span></span>
<span data-ttu-id="b5c17-116">Profil SSL</span><span class="sxs-lookup"><span data-stu-id="b5c17-116">The ssl profile</span></span>

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

### <span data-ttu-id="b5c17-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5c17-117">CommonParameters</span></span>
<span data-ttu-id="b5c17-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5c17-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5c17-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5c17-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5c17-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5c17-120">INPUTS</span></span>

### <span data-ttu-id="b5c17-121">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="b5c17-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="b5c17-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5c17-122">OUTPUTS</span></span>

### <span data-ttu-id="b5c17-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5c17-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="b5c17-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5c17-124">NOTES</span></span>

## <span data-ttu-id="b5c17-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5c17-125">RELATED LINKS</span></span>

[<span data-ttu-id="b5c17-126">Nowe — AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5c17-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="b5c17-127">Dodaj-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5c17-127">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="b5c17-128">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5c17-128">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="b5c17-129">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5c17-129">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)