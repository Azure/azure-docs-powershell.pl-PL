---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: cbe38933cb4c2c75b5219bf0deccc0b28052a61f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898370"
---
# <span data-ttu-id="5b549-101">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5b549-101">Get-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="5b549-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5b549-102">SYNOPSIS</span></span>
<span data-ttu-id="5b549-103">Pobiera istniejącą konfigurację badania kondycji z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5b549-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b549-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5b549-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b549-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5b549-105">DESCRIPTION</span></span>
<span data-ttu-id="5b549-106">Polecenie cmdlet Get-AzureRmApplicationGatewayProbeConfig pobiera istniejącą konfigurację badania kondycji z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5b549-106">The Get-AzureRmApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="5b549-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5b549-107">EXAMPLES</span></span>

### <span data-ttu-id="5b549-108">Przykład 1: uzyskiwanie istniejącej sondy od bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="5b549-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="5b549-109">To polecenie pobiera badanie kondycji o nazwie Probe02 z bramy Application Gateway o nazwie Gateway.</span><span class="sxs-lookup"><span data-stu-id="5b549-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="5b549-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5b549-110">PARAMETERS</span></span>

### <span data-ttu-id="5b549-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5b549-111">-ApplicationGateway</span></span>
<span data-ttu-id="5b549-112">Określa bramę aplikacji, z którą to polecenie cmdlet pobiera konfigurację sondy.</span><span class="sxs-lookup"><span data-stu-id="5b549-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="5b549-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b549-113">-DefaultProfile</span></span>
<span data-ttu-id="5b549-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5b549-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b549-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5b549-115">-Name</span></span>
<span data-ttu-id="5b549-116">Określa nazwę sondy.</span><span class="sxs-lookup"><span data-stu-id="5b549-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="5b549-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b549-117">CommonParameters</span></span>
<span data-ttu-id="5b549-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b549-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b549-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b549-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b549-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b549-120">INPUTS</span></span>

### <span data-ttu-id="5b549-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5b549-121">PSApplicationGateway</span></span>
<span data-ttu-id="5b549-122">Parametr "ApplicationGateway" akceptuje wartość typu "PSApplicationGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="5b549-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="5b549-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5b549-123">OUTPUTS</span></span>

### <span data-ttu-id="5b549-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="5b549-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="5b549-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. models. PSApplicationGatewayProbe]</span><span class="sxs-lookup"><span data-stu-id="5b549-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="5b549-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5b549-126">NOTES</span></span>

## <span data-ttu-id="5b549-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b549-127">RELATED LINKS</span></span>

[<span data-ttu-id="5b549-128">Dodawanie sondy do istniejącej bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="5b549-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="5b549-129">Dodaj-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5b549-129">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="5b549-130">Nowe — AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5b549-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="5b549-131">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5b549-131">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="5b549-132">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5b549-132">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

