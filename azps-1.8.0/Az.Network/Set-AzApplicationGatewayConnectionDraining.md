---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 042eb9bdff35cb406a879b454b3b78451a89d789
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401763"
---
# <span data-ttu-id="c26ed-101">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c26ed-101">Set-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="c26ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c26ed-102">SYNOPSIS</span></span>
<span data-ttu-id="c26ed-103">Modyfikuje konfigurację wyczerpania połączenia obiektu ustawień protokołu HTTP na zawczasu.</span><span class="sxs-lookup"><span data-stu-id="c26ed-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="c26ed-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c26ed-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c26ed-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c26ed-105">DESCRIPTION</span></span>
<span data-ttu-id="c26ed-106">Polecenie **cmdlet Set-AzApplicationGatewayWebApplicationFirewallConfiguration** zmodyfikuje konfigurację opróżniania połączenia obiektu ustawień protokołu HTTP na zawczasu.</span><span class="sxs-lookup"><span data-stu-id="c26ed-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="c26ed-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c26ed-107">EXAMPLES</span></span>

### <span data-ttu-id="c26ed-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c26ed-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="c26ed-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="c26ed-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c26ed-110">Drugie polecenie pobiera ustawienia protokołu HTTP z końca strony o nazwie Ustawienia01 dla protokołu $AppGw i zapisuje ustawienia w $Settings sieci.</span><span class="sxs-lookup"><span data-stu-id="c26ed-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="c26ed-111">Ostatnie polecenie modyfikuje konfigurację rozładowania połączenia obiektu ustawień protokołu HTTP na zawęzie przechowywanego w programie $Settings przez ustawienie wartości Enabled (Fałsz) i DrainTimeoutInSec (Wyczerpanie) na 3600.</span><span class="sxs-lookup"><span data-stu-id="c26ed-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="c26ed-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c26ed-112">PARAMETERS</span></span>

### <span data-ttu-id="c26ed-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c26ed-113">-BackendHttpSettings</span></span>
<span data-ttu-id="c26ed-114">Ustawienia protokołu HTTP zaplecza</span><span class="sxs-lookup"><span data-stu-id="c26ed-114">The backend http settings</span></span>

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

### <span data-ttu-id="c26ed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c26ed-115">-DefaultProfile</span></span>
<span data-ttu-id="c26ed-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c26ed-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c26ed-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="c26ed-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="c26ed-118">Liczba sekund wyczerpu połączenia jest aktywna.</span><span class="sxs-lookup"><span data-stu-id="c26ed-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="c26ed-119">Dopuszczalne wartości to od 1 sekundy do 3600 sekund.</span><span class="sxs-lookup"><span data-stu-id="c26ed-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c26ed-120">— włączone</span><span class="sxs-lookup"><span data-stu-id="c26ed-120">-Enabled</span></span>
<span data-ttu-id="c26ed-121">Czy włączono wyczerpanie połączenia, czy nie.</span><span class="sxs-lookup"><span data-stu-id="c26ed-121">Whether connection draining is enabled or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c26ed-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c26ed-122">CommonParameters</span></span>
<span data-ttu-id="c26ed-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c26ed-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c26ed-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c26ed-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c26ed-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c26ed-125">INPUTS</span></span>

### <span data-ttu-id="c26ed-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c26ed-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="c26ed-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c26ed-127">OUTPUTS</span></span>

### <span data-ttu-id="c26ed-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c26ed-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="c26ed-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c26ed-129">NOTES</span></span>

## <span data-ttu-id="c26ed-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c26ed-130">RELATED LINKS</span></span>

[<span data-ttu-id="c26ed-131">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c26ed-131">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)


[<span data-ttu-id="c26ed-132">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c26ed-132">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="c26ed-133">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c26ed-133">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="c26ed-134">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c26ed-134">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

