---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: a1e6bd507b7ddcc0a70405136cb76bba9231a7f1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499533"
---
# <span data-ttu-id="490b8-101">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="490b8-101">Get-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="490b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="490b8-102">SYNOPSIS</span></span>
<span data-ttu-id="490b8-103">Pobiera zasady SSL profilu SSL bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="490b8-103">Gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="490b8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="490b8-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="490b8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="490b8-105">DESCRIPTION</span></span>
<span data-ttu-id="490b8-106">Polecenie cmdlet **Get-AzApplicationGatewaySslProfilePolicy** pobiera zasady SSL profilu SSL bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="490b8-106">The **Get-AzApplicationGatewaySslProfilePolicy** cmdlet gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="490b8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="490b8-107">EXAMPLES</span></span>

### <span data-ttu-id="490b8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="490b8-108">Example 1</span></span>
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslProfilePolicy -SslProfile $SslProfile
```

<span data-ttu-id="490b8-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="490b8-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="490b8-110">Drugie polecenie pobiera profil SSL o nazwie SslProfile01 dla $AppGw i zapisuje go $SslProfile zmiennej.</span><span class="sxs-lookup"><span data-stu-id="490b8-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="490b8-111">Ostatnie polecenie pobiera zasady SSL z profilu SSL $SslProfile i zapisuje je w zmiennej $sslpolicy.</span><span class="sxs-lookup"><span data-stu-id="490b8-111">The last command gets the SSL policy from the SSL profile $SslProfile and stores it in the $sslpolicy variable.</span></span>

## <span data-ttu-id="490b8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="490b8-112">PARAMETERS</span></span>

### <span data-ttu-id="490b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="490b8-113">-DefaultProfile</span></span>
<span data-ttu-id="490b8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="490b8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="490b8-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="490b8-115">-SslProfile</span></span>
<span data-ttu-id="490b8-116">Profil SSL bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="490b8-116">The application Gateway SSL profile</span></span>

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

### <span data-ttu-id="490b8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="490b8-117">CommonParameters</span></span>
<span data-ttu-id="490b8-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="490b8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="490b8-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="490b8-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="490b8-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="490b8-120">INPUTS</span></span>

### <span data-ttu-id="490b8-121">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="490b8-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="490b8-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="490b8-122">OUTPUTS</span></span>

### <span data-ttu-id="490b8-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="490b8-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="490b8-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="490b8-124">NOTES</span></span>

## <span data-ttu-id="490b8-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="490b8-125">RELATED LINKS</span></span>

[<span data-ttu-id="490b8-126">Nowe — AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="490b8-126">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="490b8-127">Dodaj-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="490b8-127">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="490b8-128">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="490b8-128">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="490b8-129">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="490b8-129">Set-AzApplicationGatewaySslProfilePolicy</span></span>](./Set-AzApplicationGatewaySslProfilePolicy.md)