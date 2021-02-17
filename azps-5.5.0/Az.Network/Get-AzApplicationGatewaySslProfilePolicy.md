---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 49d55a48f9e9b769854a5cd01929188fd7993d35
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415567"
---
# <span data-ttu-id="c9e7e-101">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="c9e7e-101">Get-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="c9e7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9e7e-102">SYNOPSIS</span></span>
<span data-ttu-id="c9e7e-103">Pobiera zasady SSL profilu SSL bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-103">Gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="c9e7e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c9e7e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9e7e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c9e7e-105">DESCRIPTION</span></span>
<span data-ttu-id="c9e7e-106">Polecenie **cmdlet Get-AzApplicationGatewaySslProfilePolicy** pobiera zasady SSL profilu SSL bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-106">The **Get-AzApplicationGatewaySslProfilePolicy** cmdlet gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="c9e7e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c9e7e-107">EXAMPLES</span></span>

### <span data-ttu-id="c9e7e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c9e7e-108">Example 1</span></span>
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslProfilePolicy -SslProfile $SslProfile
```

<span data-ttu-id="c9e7e-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="c9e7e-110">Drugie polecenie pobiera profil SSL o nazwie SslProfile01 for $AppGw i przechowuje go $SslProfile zmienną.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="c9e7e-111">Ostatnie polecenie pobiera zasady SSL z profilu SSL i $SslProfile je w $sslpolicy danych.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-111">The last command gets the SSL policy from the SSL profile $SslProfile and stores it in the $sslpolicy variable.</span></span>

## <span data-ttu-id="c9e7e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9e7e-112">PARAMETERS</span></span>

### <span data-ttu-id="c9e7e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9e7e-113">-DefaultProfile</span></span>
<span data-ttu-id="c9e7e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9e7e-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="c9e7e-115">-SslProfile</span></span>
<span data-ttu-id="c9e7e-116">Profil SSL bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="c9e7e-116">The application Gateway SSL profile</span></span>

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

### <span data-ttu-id="c9e7e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9e7e-117">CommonParameters</span></span>
<span data-ttu-id="c9e7e-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9e7e-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9e7e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9e7e-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9e7e-120">INPUTS</span></span>

### <span data-ttu-id="c9e7e-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="c9e7e-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="c9e7e-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c9e7e-122">OUTPUTS</span></span>

### <span data-ttu-id="c9e7e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c9e7e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="c9e7e-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c9e7e-124">NOTES</span></span>

## <span data-ttu-id="c9e7e-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9e7e-125">RELATED LINKS</span></span>



[<span data-ttu-id="c9e7e-126">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="c9e7e-126">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="c9e7e-127">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="c9e7e-127">Set-AzApplicationGatewaySslProfilePolicy</span></span>](./Set-AzApplicationGatewaySslProfilePolicy.md)
