---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 320588b81791c033b94a07261f769fa0886d2f2c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890350"
---
# <span data-ttu-id="ece53-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ece53-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="ece53-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ece53-102">SYNOPSIS</span></span>
<span data-ttu-id="ece53-103">Usuwa badanie kondycji z istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ece53-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="ece53-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ece53-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ece53-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ece53-105">DESCRIPTION</span></span>
<span data-ttu-id="ece53-106">Polecenie cmdlet Remove-AzApplicationGatewayProbeConfig usuwa z istniejącej bramy aplikacji sondę Heath.</span><span class="sxs-lookup"><span data-stu-id="ece53-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="ece53-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ece53-107">EXAMPLES</span></span>

### <span data-ttu-id="ece53-108">Przykład 1: usuwanie sondy kondycji z istniejącej bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="ece53-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="ece53-109">To polecenie usuwa badanie kondycji o nazwie Probe04 z bramy Application Gateway o nazwie Gateway.</span><span class="sxs-lookup"><span data-stu-id="ece53-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="ece53-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ece53-110">PARAMETERS</span></span>

### <span data-ttu-id="ece53-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ece53-111">-ApplicationGateway</span></span>
<span data-ttu-id="ece53-112">Określa bramę aplikacji, z którą to polecenie cmdlet usuwa sondę.</span><span class="sxs-lookup"><span data-stu-id="ece53-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="ece53-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ece53-113">-DefaultProfile</span></span>
<span data-ttu-id="ece53-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ece53-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ece53-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ece53-115">-Name</span></span>
<span data-ttu-id="ece53-116">Określa nazwę sondy, dla której zostanie usunięte to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ece53-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="ece53-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece53-117">CommonParameters</span></span>
<span data-ttu-id="ece53-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ece53-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece53-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ece53-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece53-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ece53-120">INPUTS</span></span>

### <span data-ttu-id="ece53-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ece53-121">PSApplicationGateway</span></span>
<span data-ttu-id="ece53-122">Parametr "ApplicationGateway" akceptuje wartość typu "PSApplicationGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="ece53-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="ece53-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ece53-123">OUTPUTS</span></span>

### <span data-ttu-id="ece53-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ece53-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ece53-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ece53-125">NOTES</span></span>

## <span data-ttu-id="ece53-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ece53-126">RELATED LINKS</span></span>

[<span data-ttu-id="ece53-127">Usuwanie sondy z istniejącej bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="ece53-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="ece53-128">Dodaj-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ece53-128">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="ece53-129">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ece53-129">Get-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="ece53-130">Nowe — AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ece53-130">New-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="ece53-131">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ece53-131">Set-AzApplicationGatewayProbeConfig</span></span>]()

