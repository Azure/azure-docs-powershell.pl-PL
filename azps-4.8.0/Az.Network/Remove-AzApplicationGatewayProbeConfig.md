---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 20704f404d5fe47267f42398ef885fb2c038f84e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063353"
---
# <span data-ttu-id="6c9f4-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6c9f4-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="6c9f4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6c9f4-102">SYNOPSIS</span></span>
<span data-ttu-id="6c9f4-103">Usuwa badanie kondycji z istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6c9f4-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="6c9f4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6c9f4-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c9f4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6c9f4-105">DESCRIPTION</span></span>
<span data-ttu-id="6c9f4-106">Polecenie cmdlet Remove-AzApplicationGatewayProbeConfig usuwa z istniejącej bramy aplikacji sondę Heath.</span><span class="sxs-lookup"><span data-stu-id="6c9f4-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="6c9f4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6c9f4-107">EXAMPLES</span></span>

### <span data-ttu-id="6c9f4-108">Przykład 1: usuwanie sondy kondycji z istniejącej bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="6c9f4-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="6c9f4-109">To polecenie usuwa badanie kondycji o nazwie Probe04 z bramy Application Gateway o nazwie Gateway.</span><span class="sxs-lookup"><span data-stu-id="6c9f4-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="6c9f4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c9f4-110">PARAMETERS</span></span>

### <span data-ttu-id="6c9f4-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c9f4-111">-ApplicationGateway</span></span>
<span data-ttu-id="6c9f4-112">Określa bramę aplikacji, z którą to polecenie cmdlet usuwa sondę.</span><span class="sxs-lookup"><span data-stu-id="6c9f4-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="6c9f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c9f4-113">-DefaultProfile</span></span>
<span data-ttu-id="6c9f4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c9f4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9f4-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6c9f4-115">-Name</span></span>
<span data-ttu-id="6c9f4-116">Określa nazwę sondy, dla której zostanie usunięte to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c9f4-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="6c9f4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c9f4-117">CommonParameters</span></span>
<span data-ttu-id="6c9f4-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c9f4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c9f4-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c9f4-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c9f4-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c9f4-120">INPUTS</span></span>

### <span data-ttu-id="6c9f4-121">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c9f4-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6c9f4-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6c9f4-122">OUTPUTS</span></span>

### <span data-ttu-id="6c9f4-123">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c9f4-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6c9f4-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6c9f4-124">NOTES</span></span>

## <span data-ttu-id="6c9f4-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c9f4-125">RELATED LINKS</span></span>

[<span data-ttu-id="6c9f4-126">Usuwanie sondy z istniejącej bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="6c9f4-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="6c9f4-127">Dodaj-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6c9f4-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="6c9f4-128">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6c9f4-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="6c9f4-129">Nowe — AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6c9f4-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="6c9f4-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6c9f4-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

