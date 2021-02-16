---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 1630b0177efbccbf4d1cba674f0cf11ab457307e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402120"
---
# <span data-ttu-id="ca581-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ca581-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="ca581-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca581-102">SYNOPSIS</span></span>
<span data-ttu-id="ca581-103">Pobiera konfigurację rozładowania połączenia obiektu ustawień protokołu HTTP na zawczasu.</span><span class="sxs-lookup"><span data-stu-id="ca581-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="ca581-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ca581-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca581-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ca581-105">DESCRIPTION</span></span>
<span data-ttu-id="ca581-106">Polecenie **cmdlet Get-AzApplicationGatewayConnectionDraining** pobiera konfigurację wyczerpu połączenia obiektu ustawień protokołu HTTP na zawczasu.</span><span class="sxs-lookup"><span data-stu-id="ca581-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="ca581-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ca581-107">EXAMPLES</span></span>

### <span data-ttu-id="ca581-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ca581-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="ca581-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="ca581-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ca581-110">Drugie polecenie pobiera ustawienia protokołu HTTP z końca strony o nazwie Ustawienia01 dla protokołu $AppGw i zapisuje ustawienia w $Settings sieci.</span><span class="sxs-lookup"><span data-stu-id="ca581-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="ca581-111">Ostatnie polecenie pobiera konfigurację rozładowania połączenia z ustawień protokołu HTTP na zawęzie oraz zapisuje je $Settings w $ConnectionDraining sieci.</span><span class="sxs-lookup"><span data-stu-id="ca581-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="ca581-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca581-112">PARAMETERS</span></span>

### <span data-ttu-id="ca581-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ca581-113">-BackendHttpSettings</span></span>
<span data-ttu-id="ca581-114">Ustawienia protokołu HTTP zaplecza</span><span class="sxs-lookup"><span data-stu-id="ca581-114">The backend http settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca581-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca581-115">-DefaultProfile</span></span>
<span data-ttu-id="ca581-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca581-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca581-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca581-117">CommonParameters</span></span>
<span data-ttu-id="ca581-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca581-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca581-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca581-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca581-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca581-120">INPUTS</span></span>

### <span data-ttu-id="ca581-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ca581-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="ca581-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca581-122">OUTPUTS</span></span>

### <span data-ttu-id="ca581-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ca581-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="ca581-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ca581-124">NOTES</span></span>

## <span data-ttu-id="ca581-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca581-125">RELATED LINKS</span></span>

[<span data-ttu-id="ca581-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ca581-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)


[<span data-ttu-id="ca581-127">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ca581-127">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="ca581-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ca581-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="ca581-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ca581-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
