---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: ec20d7caafe110f03e5a0ce3130247ec877d6af9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499570"
---
# <span data-ttu-id="b7886-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b7886-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="b7886-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7886-102">SYNOPSIS</span></span>
<span data-ttu-id="b7886-103">Pobiera istniejącą konfigurację badania kondycji z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b7886-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="b7886-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7886-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7886-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b7886-105">DESCRIPTION</span></span>
<span data-ttu-id="b7886-106">Polecenie cmdlet Get-AzApplicationGatewayProbeConfig pobiera istniejącą konfigurację badania kondycji z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b7886-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="b7886-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7886-107">EXAMPLES</span></span>

### <span data-ttu-id="b7886-108">Przykład 1: uzyskiwanie istniejącej sondy od bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="b7886-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="b7886-109">To polecenie pobiera badanie kondycji o nazwie Probe02 z bramy Application Gateway o nazwie Gateway.</span><span class="sxs-lookup"><span data-stu-id="b7886-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="b7886-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7886-110">PARAMETERS</span></span>

### <span data-ttu-id="b7886-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7886-111">-ApplicationGateway</span></span>
<span data-ttu-id="b7886-112">Określa bramę aplikacji, z którą to polecenie cmdlet pobiera konfigurację sondy.</span><span class="sxs-lookup"><span data-stu-id="b7886-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="b7886-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7886-113">-DefaultProfile</span></span>
<span data-ttu-id="b7886-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b7886-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7886-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b7886-115">-Name</span></span>
<span data-ttu-id="b7886-116">Określa nazwę sondy.</span><span class="sxs-lookup"><span data-stu-id="b7886-116">Specifies the name of the probe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7886-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7886-117">CommonParameters</span></span>
<span data-ttu-id="b7886-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7886-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7886-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7886-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7886-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7886-120">INPUTS</span></span>

### <span data-ttu-id="b7886-121">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7886-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b7886-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7886-122">OUTPUTS</span></span>

### <span data-ttu-id="b7886-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="b7886-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="b7886-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7886-124">NOTES</span></span>

## <span data-ttu-id="b7886-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7886-125">RELATED LINKS</span></span>

[<span data-ttu-id="b7886-126">Dodawanie sondy do istniejącej bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="b7886-126">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="b7886-127">Dodaj-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b7886-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="b7886-128">Nowe — AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b7886-128">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="b7886-129">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b7886-129">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="b7886-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b7886-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

