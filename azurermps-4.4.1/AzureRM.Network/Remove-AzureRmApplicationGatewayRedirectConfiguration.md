---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: bd9ab62406d033eefe3fb3723d2a2ebf2f9dbb8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546223"
---
# <span data-ttu-id="2b2f5-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b2f5-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="2b2f5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b2f5-102">SYNOPSIS</span></span>
<span data-ttu-id="2b2f5-103">Usuwa konfigurację przekierowania z istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2b2f5-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b2f5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b2f5-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b2f5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2b2f5-105">DESCRIPTION</span></span>
<span data-ttu-id="2b2f5-106">Polecenie cmdlet **Remove-AzureRmApplicationGatewayRedirectConfiguration** usuwa konfigurację przekierowania z istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2b2f5-106">The **Remove-AzureRmApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="2b2f5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b2f5-107">EXAMPLES</span></span>

### <span data-ttu-id="2b2f5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2b2f5-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="2b2f5-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2b2f5-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="2b2f5-110">Drugie polecenie usuwa konfigurację przekierowania o nazwie Redirect01 z bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2b2f5-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="2b2f5-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b2f5-111">PARAMETERS</span></span>

### <span data-ttu-id="2b2f5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2b2f5-112">-ApplicationGateway</span></span>
<span data-ttu-id="2b2f5-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2b2f5-113">The applicationGateway</span></span>

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

### <span data-ttu-id="2b2f5-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2b2f5-114">-Name</span></span>
<span data-ttu-id="2b2f5-115">Nazwa konfiguracji przekierowania</span><span class="sxs-lookup"><span data-stu-id="2b2f5-115">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="2b2f5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b2f5-116">-DefaultProfile</span></span>
<span data-ttu-id="2b2f5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b2f5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b2f5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b2f5-118">CommonParameters</span></span>
<span data-ttu-id="2b2f5-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b2f5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b2f5-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b2f5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b2f5-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b2f5-121">INPUTS</span></span>

### <span data-ttu-id="2b2f5-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2b2f5-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2b2f5-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b2f5-123">OUTPUTS</span></span>

### <span data-ttu-id="2b2f5-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2b2f5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2b2f5-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b2f5-125">NOTES</span></span>

## <span data-ttu-id="2b2f5-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b2f5-126">RELATED LINKS</span></span>

