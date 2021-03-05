---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 1bdee7a9ffb35085f8194d86dc9a9486f5dd7fb6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994092"
---
# <span data-ttu-id="1020f-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1020f-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="1020f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1020f-102">SYNOPSIS</span></span>
<span data-ttu-id="1020f-103">Pobiera istniejącą konfigurację kondycji z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1020f-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="1020f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1020f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1020f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1020f-105">DESCRIPTION</span></span>
<span data-ttu-id="1020f-106">Polecenie Get-AzApplicationGatewayProbeConfig pobiera istniejącą konfigurację kondycji z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1020f-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="1020f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1020f-107">EXAMPLES</span></span>

### <span data-ttu-id="1020f-108">Przykład 1. Uzyskiwanie istniejącego pliku z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="1020f-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="1020f-109">To polecenie pobiera nazwę kondycji o nazwie Łowe02 z bramy aplikacji o nazwie Brama.</span><span class="sxs-lookup"><span data-stu-id="1020f-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="1020f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1020f-110">PARAMETERS</span></span>

### <span data-ttu-id="1020f-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1020f-111">-ApplicationGateway</span></span>
<span data-ttu-id="1020f-112">Określa bramę aplikacji, do której to polecenie cmdlet uzyskuje konfigurację konfiguracji konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="1020f-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="1020f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1020f-113">-DefaultProfile</span></span>
<span data-ttu-id="1020f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1020f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1020f-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1020f-115">-Name</span></span>
<span data-ttu-id="1020f-116">Określa nazwę pliku.</span><span class="sxs-lookup"><span data-stu-id="1020f-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="1020f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1020f-117">CommonParameters</span></span>
<span data-ttu-id="1020f-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1020f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1020f-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1020f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1020f-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1020f-120">INPUTS</span></span>

### <span data-ttu-id="1020f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1020f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1020f-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1020f-122">OUTPUTS</span></span>

### <span data-ttu-id="1020f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="1020f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="1020f-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1020f-124">NOTES</span></span>

## <span data-ttu-id="1020f-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1020f-125">RELATED LINKS</span></span>

[<span data-ttu-id="1020f-126">Dodawanie pliku do istniejącej bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="1020f-126">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="1020f-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1020f-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="1020f-128">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1020f-128">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="1020f-129">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1020f-129">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="1020f-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1020f-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

