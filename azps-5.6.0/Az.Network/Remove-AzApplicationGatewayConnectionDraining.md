---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: ddcec36e8561196b31dd94eb15d99a7e2a92a378
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964081"
---
# <span data-ttu-id="52f3b-101">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="52f3b-101">Remove-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="52f3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52f3b-102">SYNOPSIS</span></span>
<span data-ttu-id="52f3b-103">Usuwa konfigurację wyczerpania połączenia obiektu ustawień protokołu HTTP na zawczasu.</span><span class="sxs-lookup"><span data-stu-id="52f3b-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="52f3b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="52f3b-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52f3b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="52f3b-105">DESCRIPTION</span></span>
<span data-ttu-id="52f3b-106">Polecenie **cmdlet Remove-AzApplicationGatewayConnectionDraining** usuwa konfigurację rozładowania połączenia obiektu ustawień protokołu HTTP na zawczasu.</span><span class="sxs-lookup"><span data-stu-id="52f3b-106">The **Remove-AzApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="52f3b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="52f3b-107">EXAMPLES</span></span>

### <span data-ttu-id="52f3b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="52f3b-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="52f3b-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="52f3b-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="52f3b-110">Drugie polecenie pobiera ustawienia serwera HTTP o nazwie Ustawienia01 dla protokołu $AppGw i zapisuje ustawienia w $Settings sieci.</span><span class="sxs-lookup"><span data-stu-id="52f3b-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="52f3b-111">Ostatnie polecenie usuwa konfigurację rozładowania połączenia dla ustawień protokołu HTTP na zawczasu przechowywanych w $Settings.</span><span class="sxs-lookup"><span data-stu-id="52f3b-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="52f3b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52f3b-112">PARAMETERS</span></span>

### <span data-ttu-id="52f3b-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="52f3b-113">-BackendHttpSettings</span></span>
<span data-ttu-id="52f3b-114">Ustawienia protokołu HTTP zaplecza</span><span class="sxs-lookup"><span data-stu-id="52f3b-114">The backend http settings</span></span>

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

### <span data-ttu-id="52f3b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52f3b-115">-DefaultProfile</span></span>
<span data-ttu-id="52f3b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="52f3b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52f3b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52f3b-117">CommonParameters</span></span>
<span data-ttu-id="52f3b-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52f3b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52f3b-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52f3b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52f3b-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52f3b-120">INPUTS</span></span>

### <span data-ttu-id="52f3b-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="52f3b-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="52f3b-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52f3b-122">OUTPUTS</span></span>

### <span data-ttu-id="52f3b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="52f3b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="52f3b-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="52f3b-124">NOTES</span></span>

## <span data-ttu-id="52f3b-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52f3b-125">RELATED LINKS</span></span>

[<span data-ttu-id="52f3b-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="52f3b-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="52f3b-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="52f3b-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="52f3b-128">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="52f3b-128">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="52f3b-129">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="52f3b-129">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="52f3b-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="52f3b-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

