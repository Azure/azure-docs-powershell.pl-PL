---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: f542783ce1edcebf0c0c4e70116423836ddff736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543663"
---
# <span data-ttu-id="50c0b-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="50c0b-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="50c0b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="50c0b-102">SYNOPSIS</span></span>
<span data-ttu-id="50c0b-103">Usuwa konfigurację przekierowania z istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="50c0b-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50c0b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="50c0b-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50c0b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="50c0b-105">DESCRIPTION</span></span>
<span data-ttu-id="50c0b-106">Polecenie cmdlet **Remove-AzureRmApplicationGatewayRedirectConfiguration** usuwa konfigurację przekierowania z istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="50c0b-106">The **Remove-AzureRmApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="50c0b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="50c0b-107">EXAMPLES</span></span>

### <span data-ttu-id="50c0b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="50c0b-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="50c0b-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="50c0b-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="50c0b-110">Drugie polecenie usuwa konfigurację przekierowania o nazwie Redirect01 z bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="50c0b-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="50c0b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="50c0b-111">PARAMETERS</span></span>

### <span data-ttu-id="50c0b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50c0b-112">-ApplicationGateway</span></span>
<span data-ttu-id="50c0b-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50c0b-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50c0b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50c0b-114">-DefaultProfile</span></span>
<span data-ttu-id="50c0b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="50c0b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50c0b-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="50c0b-116">-Name</span></span>
<span data-ttu-id="50c0b-117">Nazwa konfiguracji przekierowania</span><span class="sxs-lookup"><span data-stu-id="50c0b-117">The name of the redirect configuration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50c0b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50c0b-118">CommonParameters</span></span>
<span data-ttu-id="50c0b-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50c0b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50c0b-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50c0b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50c0b-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50c0b-121">INPUTS</span></span>

### <span data-ttu-id="50c0b-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50c0b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="50c0b-123">Parametry: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="50c0b-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="50c0b-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="50c0b-124">OUTPUTS</span></span>

### <span data-ttu-id="50c0b-125">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50c0b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="50c0b-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="50c0b-126">NOTES</span></span>

## <span data-ttu-id="50c0b-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50c0b-127">RELATED LINKS</span></span>