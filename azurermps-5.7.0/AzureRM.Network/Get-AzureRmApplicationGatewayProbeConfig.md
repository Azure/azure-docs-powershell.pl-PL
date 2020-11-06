---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: d8086718ef9d4b009bc785a3017c38e8d29047c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545600"
---
# <span data-ttu-id="6f922-101">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6f922-101">Get-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="6f922-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6f922-102">SYNOPSIS</span></span>
<span data-ttu-id="6f922-103">Pobiera istniejącą konfigurację badania kondycji z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6f922-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f922-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6f922-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f922-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6f922-105">DESCRIPTION</span></span>
<span data-ttu-id="6f922-106">Polecenie cmdlet Get-AzureRmApplicationGatewayProbeConfig pobiera istniejącą konfigurację badania kondycji z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6f922-106">The Get-AzureRmApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="6f922-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6f922-107">EXAMPLES</span></span>

### <span data-ttu-id="6f922-108">Przykład 1: uzyskiwanie istniejącej sondy od bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="6f922-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="6f922-109">To polecenie pobiera badanie kondycji o nazwie Probe02 z bramy Application Gateway o nazwie Gateway.</span><span class="sxs-lookup"><span data-stu-id="6f922-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="6f922-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6f922-110">PARAMETERS</span></span>

### <span data-ttu-id="6f922-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f922-111">-ApplicationGateway</span></span>
<span data-ttu-id="6f922-112">Określa bramę aplikacji, z którą to polecenie cmdlet pobiera konfigurację sondy.</span><span class="sxs-lookup"><span data-stu-id="6f922-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="6f922-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f922-113">-DefaultProfile</span></span>
<span data-ttu-id="6f922-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6f922-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f922-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6f922-115">-Name</span></span>
<span data-ttu-id="6f922-116">Określa nazwę sondy.</span><span class="sxs-lookup"><span data-stu-id="6f922-116">Specifies the name of the probe.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f922-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f922-117">CommonParameters</span></span>
<span data-ttu-id="6f922-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f922-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f922-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f922-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f922-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f922-120">INPUTS</span></span>

### <span data-ttu-id="6f922-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f922-121">PSApplicationGateway</span></span>
<span data-ttu-id="6f922-122">Parametr "ApplicationGateway" akceptuje wartość typu "PSApplicationGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="6f922-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="6f922-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6f922-123">OUTPUTS</span></span>

### <span data-ttu-id="6f922-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="6f922-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="6f922-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. models. PSApplicationGatewayProbe]</span><span class="sxs-lookup"><span data-stu-id="6f922-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="6f922-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6f922-126">NOTES</span></span>

## <span data-ttu-id="6f922-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6f922-127">RELATED LINKS</span></span>

[<span data-ttu-id="6f922-128">Dodawanie sondy do istniejącej bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="6f922-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="6f922-129">Dodaj-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6f922-129">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="6f922-130">Nowe — AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6f922-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="6f922-131">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6f922-131">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="6f922-132">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6f922-132">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

