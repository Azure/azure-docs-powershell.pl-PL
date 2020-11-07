---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: b3e2b3ea03ca0bae0db1bea1606e4ae6b94a597e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890877"
---
# <span data-ttu-id="2c44e-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2c44e-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="2c44e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c44e-102">SYNOPSIS</span></span>
<span data-ttu-id="2c44e-103">Pobiera istniejącą konfigurację badania kondycji z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2c44e-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="2c44e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c44e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c44e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2c44e-105">DESCRIPTION</span></span>
<span data-ttu-id="2c44e-106">Polecenie cmdlet Get-AzApplicationGatewayProbeConfig pobiera istniejącą konfigurację badania kondycji z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2c44e-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="2c44e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c44e-107">EXAMPLES</span></span>

### <span data-ttu-id="2c44e-108">Przykład 1: uzyskiwanie istniejącej sondy od bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="2c44e-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="2c44e-109">To polecenie pobiera badanie kondycji o nazwie Probe02 z bramy Application Gateway o nazwie Gateway.</span><span class="sxs-lookup"><span data-stu-id="2c44e-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="2c44e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c44e-110">PARAMETERS</span></span>

### <span data-ttu-id="2c44e-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c44e-111">-ApplicationGateway</span></span>
<span data-ttu-id="2c44e-112">Określa bramę aplikacji, z którą to polecenie cmdlet pobiera konfigurację sondy.</span><span class="sxs-lookup"><span data-stu-id="2c44e-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="2c44e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c44e-113">-DefaultProfile</span></span>
<span data-ttu-id="2c44e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c44e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c44e-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2c44e-115">-Name</span></span>
<span data-ttu-id="2c44e-116">Określa nazwę sondy.</span><span class="sxs-lookup"><span data-stu-id="2c44e-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="2c44e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c44e-117">CommonParameters</span></span>
<span data-ttu-id="2c44e-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c44e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c44e-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c44e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c44e-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c44e-120">INPUTS</span></span>

### <span data-ttu-id="2c44e-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c44e-121">PSApplicationGateway</span></span>
<span data-ttu-id="2c44e-122">Parametr "ApplicationGateway" akceptuje wartość typu "PSApplicationGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="2c44e-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="2c44e-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c44e-123">OUTPUTS</span></span>

### <span data-ttu-id="2c44e-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="2c44e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="2c44e-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. models. PSApplicationGatewayProbe]</span><span class="sxs-lookup"><span data-stu-id="2c44e-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="2c44e-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c44e-126">NOTES</span></span>

## <span data-ttu-id="2c44e-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c44e-127">RELATED LINKS</span></span>

[<span data-ttu-id="2c44e-128">Dodawanie sondy do istniejącej bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="2c44e-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="2c44e-129">Dodaj-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2c44e-129">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="2c44e-130">Nowe — AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2c44e-130">New-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="2c44e-131">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2c44e-131">Remove-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="2c44e-132">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2c44e-132">Set-AzApplicationGatewayProbeConfig</span></span>]()

