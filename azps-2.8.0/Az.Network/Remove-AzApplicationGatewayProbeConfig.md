---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: eedb3eb0df28b3f02690a2462b9367995235fcc7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869772"
---
# <span data-ttu-id="2d44b-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2d44b-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="2d44b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2d44b-102">SYNOPSIS</span></span>
<span data-ttu-id="2d44b-103">Usuwa badanie kondycji z istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2d44b-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="2d44b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2d44b-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d44b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2d44b-105">DESCRIPTION</span></span>
<span data-ttu-id="2d44b-106">Polecenie cmdlet Remove-AzApplicationGatewayProbeConfig usuwa z istniejącej bramy aplikacji sondę Heath.</span><span class="sxs-lookup"><span data-stu-id="2d44b-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="2d44b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2d44b-107">EXAMPLES</span></span>

### <span data-ttu-id="2d44b-108">Przykład 1: usuwanie sondy kondycji z istniejącej bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="2d44b-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="2d44b-109">To polecenie usuwa badanie kondycji o nazwie Probe04 z bramy Application Gateway o nazwie Gateway.</span><span class="sxs-lookup"><span data-stu-id="2d44b-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="2d44b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2d44b-110">PARAMETERS</span></span>

### <span data-ttu-id="2d44b-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2d44b-111">-ApplicationGateway</span></span>
<span data-ttu-id="2d44b-112">Określa bramę aplikacji, z którą to polecenie cmdlet usuwa sondę.</span><span class="sxs-lookup"><span data-stu-id="2d44b-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="2d44b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d44b-113">-DefaultProfile</span></span>
<span data-ttu-id="2d44b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d44b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d44b-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2d44b-115">-Name</span></span>
<span data-ttu-id="2d44b-116">Określa nazwę sondy, dla której zostanie usunięte to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d44b-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="2d44b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d44b-117">CommonParameters</span></span>
<span data-ttu-id="2d44b-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d44b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d44b-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d44b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d44b-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d44b-120">INPUTS</span></span>

### <span data-ttu-id="2d44b-121">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2d44b-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2d44b-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2d44b-122">OUTPUTS</span></span>

### <span data-ttu-id="2d44b-123">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2d44b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2d44b-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2d44b-124">NOTES</span></span>

## <span data-ttu-id="2d44b-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d44b-125">RELATED LINKS</span></span>

[<span data-ttu-id="2d44b-126">Usuwanie sondy z istniejącej bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="2d44b-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="2d44b-127">Dodaj-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2d44b-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="2d44b-128">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2d44b-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="2d44b-129">Nowe — AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2d44b-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="2d44b-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2d44b-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

