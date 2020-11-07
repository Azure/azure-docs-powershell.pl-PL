---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 14d1aea928923d9da4eee089ae1e95c75289eb3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719173"
---
# <span data-ttu-id="00dd4-101">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="00dd4-101">Remove-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="00dd4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="00dd4-102">SYNOPSIS</span></span>
<span data-ttu-id="00dd4-103">Usuwa badanie kondycji z istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="00dd4-103">Removes a health probe from an existing application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00dd4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="00dd4-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00dd4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="00dd4-105">DESCRIPTION</span></span>
<span data-ttu-id="00dd4-106">Polecenie cmdlet Remove-AzureRmApplicationGatewayProbeConfig usuwa z istniejącej bramy aplikacji sondę Heath.</span><span class="sxs-lookup"><span data-stu-id="00dd4-106">The Remove-AzureRmApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="00dd4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="00dd4-107">EXAMPLES</span></span>

### <span data-ttu-id="00dd4-108">Przykład 1: usuwanie sondy kondycji z istniejącej bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="00dd4-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="00dd4-109">To polecenie usuwa badanie kondycji o nazwie Probe04 z bramy Application Gateway o nazwie Gateway.</span><span class="sxs-lookup"><span data-stu-id="00dd4-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="00dd4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="00dd4-110">PARAMETERS</span></span>

### <span data-ttu-id="00dd4-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="00dd4-111">-ApplicationGateway</span></span>
<span data-ttu-id="00dd4-112">Określa bramę aplikacji, z którą to polecenie cmdlet usuwa sondę.</span><span class="sxs-lookup"><span data-stu-id="00dd4-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00dd4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00dd4-113">-DefaultProfile</span></span>
<span data-ttu-id="00dd4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="00dd4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dd4-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="00dd4-115">-Name</span></span>
<span data-ttu-id="00dd4-116">Określa nazwę sondy, dla której zostanie usunięte to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00dd4-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dd4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00dd4-117">CommonParameters</span></span>
<span data-ttu-id="00dd4-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00dd4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00dd4-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00dd4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00dd4-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00dd4-120">INPUTS</span></span>

### <span data-ttu-id="00dd4-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="00dd4-121">PSApplicationGateway</span></span>
<span data-ttu-id="00dd4-122">Parametr "ApplicationGateway" akceptuje wartość typu "PSApplicationGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="00dd4-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="00dd4-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="00dd4-123">OUTPUTS</span></span>

### <span data-ttu-id="00dd4-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="00dd4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="00dd4-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="00dd4-125">NOTES</span></span>

## <span data-ttu-id="00dd4-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00dd4-126">RELATED LINKS</span></span>

[<span data-ttu-id="00dd4-127">Usuwanie sondy z istniejącej bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="00dd4-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="00dd4-128">Dodaj-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="00dd4-128">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="00dd4-129">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="00dd4-129">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="00dd4-130">Nowe — AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="00dd4-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="00dd4-131">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="00dd4-131">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

