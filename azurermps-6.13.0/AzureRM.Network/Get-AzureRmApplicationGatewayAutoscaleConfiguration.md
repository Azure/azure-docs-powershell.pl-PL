---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: f9be647a4c6cb9d5198edcc766a20b3588e7626b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527870"
---
# <span data-ttu-id="63900-101">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="63900-101">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="63900-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63900-102">SYNOPSIS</span></span>
<span data-ttu-id="63900-103">Pobiera konfigurację skalowania bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="63900-103">Gets the Autoscale Configuration of the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63900-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63900-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63900-105">Opis</span><span class="sxs-lookup"><span data-stu-id="63900-105">DESCRIPTION</span></span>
<span data-ttu-id="63900-106">Polecenie cmdlet **Get-AzureRmApplicationGatewayAutoscaleConfiguration umożliwia wyświetlenie** konfiguracji autoskalowania bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="63900-106">The **Get-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet gets Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="63900-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63900-107">EXAMPLES</span></span>

### <span data-ttu-id="63900-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="63900-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $autoscaleConfiguration = Get-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $autoscaleConfiguration.MinCapacity
```

<span data-ttu-id="63900-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $gw.</span><span class="sxs-lookup"><span data-stu-id="63900-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="63900-110">Drugie polecenie wyodrębnia konfigurację autoskalowania z bramy applicationg.</span><span class="sxs-lookup"><span data-stu-id="63900-110">The second command extracts out the autoscale configuration from the applicationg gateway.</span></span>

## <span data-ttu-id="63900-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63900-111">PARAMETERS</span></span>

### <span data-ttu-id="63900-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63900-112">-ApplicationGateway</span></span>
<span data-ttu-id="63900-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63900-113">The applicationGateway</span></span>

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

### <span data-ttu-id="63900-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63900-114">-DefaultProfile</span></span>
<span data-ttu-id="63900-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="63900-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63900-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63900-116">CommonParameters</span></span>
<span data-ttu-id="63900-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63900-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63900-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63900-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63900-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63900-119">INPUTS</span></span>

### <span data-ttu-id="63900-120">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63900-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="63900-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63900-121">OUTPUTS</span></span>

### <span data-ttu-id="63900-122">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="63900-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="63900-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63900-123">NOTES</span></span>

## <span data-ttu-id="63900-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63900-124">RELATED LINKS</span></span>
