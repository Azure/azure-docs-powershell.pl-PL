---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: eee7040dab93a4f73bacdf440c6450a525fab9a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189850"
---
# <span data-ttu-id="68745-101">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="68745-101">Get-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="68745-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68745-102">SYNOPSIS</span></span>
<span data-ttu-id="68745-103">Pobiera konfigurację uwierzytelniania klienta obiektu profilu SSL.</span><span class="sxs-lookup"><span data-stu-id="68745-103">Gets the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="68745-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="68745-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68745-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="68745-105">DESCRIPTION</span></span>
<span data-ttu-id="68745-106">Polecenie **cmdlet Get-AzApplicationGatewayClientAuthConfiguration** pobiera konfigurację uwierzytelniania klienta obiektu profilu SSL.</span><span class="sxs-lookup"><span data-stu-id="68745-106">The **Get-AzApplicationGatewayClientAuthConfiguration** cmdlet gets the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="68745-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="68745-107">EXAMPLES</span></span>

### <span data-ttu-id="68745-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="68745-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $ClientAuthConfig = Get-AzApplicationGatewayClientAuthConfiguration -SslProfile $SslProfile
```

<span data-ttu-id="68745-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="68745-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="68745-110">Drugie polecenie pobiera profil SSL o nazwie SslProfile01 for $AppGw i przechowuje go $SslProfile zmienną.</span><span class="sxs-lookup"><span data-stu-id="68745-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="68745-111">Ostatnie polecenie pobiera konfigurację uwierzytelniania klienta z profilu SSL $SslProfile i zapisuje je w $ClientAuthConfig danych.</span><span class="sxs-lookup"><span data-stu-id="68745-111">The last command gets the client authentication configuration from the SSL profile $SslProfile and stores it in the $ClientAuthConfig variable.</span></span>

## <span data-ttu-id="68745-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68745-112">PARAMETERS</span></span>

### <span data-ttu-id="68745-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68745-113">-DefaultProfile</span></span>
<span data-ttu-id="68745-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="68745-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68745-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="68745-115">-SslProfile</span></span>
<span data-ttu-id="68745-116">Profil SSL</span><span class="sxs-lookup"><span data-stu-id="68745-116">The ssl profile</span></span>

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

### <span data-ttu-id="68745-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68745-117">CommonParameters</span></span>
<span data-ttu-id="68745-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68745-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68745-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68745-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68745-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68745-120">INPUTS</span></span>

### <span data-ttu-id="68745-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="68745-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="68745-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="68745-122">OUTPUTS</span></span>

### <span data-ttu-id="68745-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="68745-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="68745-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="68745-124">NOTES</span></span>

## <span data-ttu-id="68745-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68745-125">RELATED LINKS</span></span>

[<span data-ttu-id="68745-126">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="68745-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="68745-127">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="68745-127">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="68745-128">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="68745-128">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="68745-129">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="68745-129">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)