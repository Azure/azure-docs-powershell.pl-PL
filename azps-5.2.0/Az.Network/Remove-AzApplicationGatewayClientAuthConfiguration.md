---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 92d3945e92dc4996fbbe3fc0abbcc296ab141621
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335185"
---
# <span data-ttu-id="90a78-101">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="90a78-101">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="90a78-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90a78-102">SYNOPSIS</span></span>
<span data-ttu-id="90a78-103">Usuwa konfigurację uwierzytelniania klienta obiektu profilu SSL.</span><span class="sxs-lookup"><span data-stu-id="90a78-103">Removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="90a78-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90a78-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90a78-105">Opis</span><span class="sxs-lookup"><span data-stu-id="90a78-105">DESCRIPTION</span></span>
<span data-ttu-id="90a78-106">Polecenie cmdlet **Remove-AzApplicationGatewayClientAuthConfiguration** usuwa konfigurację uwierzytelniania klienta obiektu profilu SSL.</span><span class="sxs-lookup"><span data-stu-id="90a78-106">The **Remove-AzApplicationGatewayClientAuthConfiguration** cmdlet removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="90a78-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90a78-107">EXAMPLES</span></span>

### <span data-ttu-id="90a78-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="90a78-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile
```

<span data-ttu-id="90a78-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="90a78-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="90a78-110">Drugie polecenie pobiera profil SSL o nazwie Profile01 dla $AppGw i zapisuje go w zmiennej $profile.</span><span class="sxs-lookup"><span data-stu-id="90a78-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="90a78-111">Ostatnie polecenie usuwa konfigurację uwierzytelniania klienta profilu SSL przechowywanego w $profile.</span><span class="sxs-lookup"><span data-stu-id="90a78-111">The last command removes the client authentication configuration of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="90a78-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90a78-112">PARAMETERS</span></span>

### <span data-ttu-id="90a78-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90a78-113">-DefaultProfile</span></span>
<span data-ttu-id="90a78-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="90a78-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90a78-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="90a78-115">-SslProfile</span></span>
<span data-ttu-id="90a78-116">Profil SSL</span><span class="sxs-lookup"><span data-stu-id="90a78-116">The ssl profile</span></span>

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

### <span data-ttu-id="90a78-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90a78-117">CommonParameters</span></span>
<span data-ttu-id="90a78-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90a78-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90a78-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90a78-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90a78-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90a78-120">INPUTS</span></span>

### <span data-ttu-id="90a78-121">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="90a78-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="90a78-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90a78-122">OUTPUTS</span></span>

### <span data-ttu-id="90a78-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="90a78-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="90a78-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90a78-124">NOTES</span></span>

## <span data-ttu-id="90a78-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90a78-125">RELATED LINKS</span></span>

[<span data-ttu-id="90a78-126">Nowe — AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="90a78-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="90a78-127">Dodaj-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="90a78-127">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="90a78-128">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="90a78-128">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="90a78-129">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="90a78-129">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)