---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 64dc67a59b739ac7cab51c9c4a02fd7a73f8b4cc
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407594"
---
# <span data-ttu-id="c7d21-101">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7d21-101">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="c7d21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7d21-102">SYNOPSIS</span></span>
<span data-ttu-id="c7d21-103">Usuwa konfigurację uwierzytelniania klienta obiektu profilu SSL.</span><span class="sxs-lookup"><span data-stu-id="c7d21-103">Removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="c7d21-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c7d21-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7d21-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c7d21-105">DESCRIPTION</span></span>
<span data-ttu-id="c7d21-106">Polecenie **cmdlet Remove-AzApplicationGatewayClientAuthConfiguration** usuwa konfigurację uwierzytelniania klienta obiektu profilu SSL.</span><span class="sxs-lookup"><span data-stu-id="c7d21-106">The **Remove-AzApplicationGatewayClientAuthConfiguration** cmdlet removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="c7d21-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c7d21-107">EXAMPLES</span></span>

### <span data-ttu-id="c7d21-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c7d21-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile
```

<span data-ttu-id="c7d21-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="c7d21-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="c7d21-110">Drugie polecenie pobiera profil SSL o nazwie Profile01 for $AppGw i zapisuje go w $profile danych.</span><span class="sxs-lookup"><span data-stu-id="c7d21-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="c7d21-111">Ostatnie polecenie usuwa konfigurację uwierzytelniania klienta profilu ssl przechowywanego w $profile.</span><span class="sxs-lookup"><span data-stu-id="c7d21-111">The last command removes the client authentication configuration of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="c7d21-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7d21-112">PARAMETERS</span></span>

### <span data-ttu-id="c7d21-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7d21-113">-DefaultProfile</span></span>
<span data-ttu-id="c7d21-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c7d21-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7d21-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="c7d21-115">-SslProfile</span></span>
<span data-ttu-id="c7d21-116">Profil SSL</span><span class="sxs-lookup"><span data-stu-id="c7d21-116">The ssl profile</span></span>

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

### <span data-ttu-id="c7d21-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7d21-117">CommonParameters</span></span>
<span data-ttu-id="c7d21-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7d21-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7d21-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7d21-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7d21-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7d21-120">INPUTS</span></span>

### <span data-ttu-id="c7d21-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="c7d21-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="c7d21-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c7d21-122">OUTPUTS</span></span>

### <span data-ttu-id="c7d21-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="c7d21-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="c7d21-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c7d21-124">NOTES</span></span>

## <span data-ttu-id="c7d21-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c7d21-125">RELATED LINKS</span></span>

[<span data-ttu-id="c7d21-126">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7d21-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)


[<span data-ttu-id="c7d21-127">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7d21-127">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="c7d21-128">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7d21-128">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)
