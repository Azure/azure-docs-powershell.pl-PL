---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: a1e6bd507b7ddcc0a70405136cb76bba9231a7f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193931"
---
# <span data-ttu-id="57ccb-101">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="57ccb-101">Get-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="57ccb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="57ccb-103">Pobiera zasady SSL profilu SSL bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="57ccb-103">Gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="57ccb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="57ccb-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57ccb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="57ccb-105">DESCRIPTION</span></span>
<span data-ttu-id="57ccb-106">Polecenie **cmdlet Get-AzApplicationGatewaySslProfilePolicy** pobiera zasady SSL profilu SSL bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="57ccb-106">The **Get-AzApplicationGatewaySslProfilePolicy** cmdlet gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="57ccb-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="57ccb-107">EXAMPLES</span></span>

### <span data-ttu-id="57ccb-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="57ccb-108">Example 1</span></span>
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslProfilePolicy -SslProfile $SslProfile
```

<span data-ttu-id="57ccb-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="57ccb-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="57ccb-110">Drugie polecenie pobiera profil SSL o nazwie SslProfile01 for $AppGw i przechowuje go $SslProfile zmienną.</span><span class="sxs-lookup"><span data-stu-id="57ccb-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="57ccb-111">Ostatnie polecenie pobiera zasady SSL z profilu SSL i $SslProfile je w $sslpolicy danych.</span><span class="sxs-lookup"><span data-stu-id="57ccb-111">The last command gets the SSL policy from the SSL profile $SslProfile and stores it in the $sslpolicy variable.</span></span>

## <span data-ttu-id="57ccb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57ccb-112">PARAMETERS</span></span>

### <span data-ttu-id="57ccb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57ccb-113">-DefaultProfile</span></span>
<span data-ttu-id="57ccb-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="57ccb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57ccb-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="57ccb-115">-SslProfile</span></span>
<span data-ttu-id="57ccb-116">Profil SSL bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="57ccb-116">The application Gateway SSL profile</span></span>

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

### <span data-ttu-id="57ccb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57ccb-117">CommonParameters</span></span>
<span data-ttu-id="57ccb-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57ccb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57ccb-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57ccb-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57ccb-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57ccb-120">INPUTS</span></span>

### <span data-ttu-id="57ccb-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="57ccb-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="57ccb-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="57ccb-122">OUTPUTS</span></span>

### <span data-ttu-id="57ccb-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="57ccb-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="57ccb-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="57ccb-124">NOTES</span></span>

## <span data-ttu-id="57ccb-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57ccb-125">RELATED LINKS</span></span>

[<span data-ttu-id="57ccb-126">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="57ccb-126">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="57ccb-127">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="57ccb-127">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="57ccb-128">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="57ccb-128">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="57ccb-129">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="57ccb-129">Set-AzApplicationGatewaySslProfilePolicy</span></span>](./Set-AzApplicationGatewaySslProfilePolicy.md)