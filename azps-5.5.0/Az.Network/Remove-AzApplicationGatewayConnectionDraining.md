---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 98b097e0be8d4b08ba16d5af06fbec1a2f3d66de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184339"
---
# <span data-ttu-id="9b19d-101">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9b19d-101">Remove-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="9b19d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b19d-102">SYNOPSIS</span></span>
<span data-ttu-id="9b19d-103">Usuwa konfigurację rozładowania połączenia obiektu ustawień protokołu HTTP na zawczasu.</span><span class="sxs-lookup"><span data-stu-id="9b19d-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="9b19d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9b19d-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b19d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9b19d-105">DESCRIPTION</span></span>
<span data-ttu-id="9b19d-106">Polecenie **cmdlet Remove-AzApplicationGatewayConnectionDraining** usuwa konfigurację opróżniania połączenia obiektu ustawień protokołu HTTP na zawczasu.</span><span class="sxs-lookup"><span data-stu-id="9b19d-106">The **Remove-AzApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="9b19d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9b19d-107">EXAMPLES</span></span>

### <span data-ttu-id="9b19d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9b19d-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="9b19d-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="9b19d-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9b19d-110">Drugie polecenie pobiera ustawienia protokołu HTTP z końca strony o nazwie Ustawienia01 dla protokołu $AppGw i zapisuje ustawienia w $Settings sieci.</span><span class="sxs-lookup"><span data-stu-id="9b19d-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="9b19d-111">Ostatnie polecenie usuwa konfigurację rozładowania połączenia dla ustawień protokołu HTTP na zawęzie przechowywanych w $Settings.</span><span class="sxs-lookup"><span data-stu-id="9b19d-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="9b19d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b19d-112">PARAMETERS</span></span>

### <span data-ttu-id="9b19d-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9b19d-113">-BackendHttpSettings</span></span>
<span data-ttu-id="9b19d-114">Ustawienia protokołu HTTP zaplecza</span><span class="sxs-lookup"><span data-stu-id="9b19d-114">The backend http settings</span></span>

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

### <span data-ttu-id="9b19d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b19d-115">-DefaultProfile</span></span>
<span data-ttu-id="9b19d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b19d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b19d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b19d-117">CommonParameters</span></span>
<span data-ttu-id="9b19d-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b19d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b19d-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b19d-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b19d-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b19d-120">INPUTS</span></span>

### <span data-ttu-id="9b19d-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9b19d-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="9b19d-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b19d-122">OUTPUTS</span></span>

### <span data-ttu-id="9b19d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9b19d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="9b19d-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9b19d-124">NOTES</span></span>

## <span data-ttu-id="9b19d-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b19d-125">RELATED LINKS</span></span>

[<span data-ttu-id="9b19d-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b19d-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="9b19d-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="9b19d-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="9b19d-128">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9b19d-128">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="9b19d-129">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9b19d-129">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="9b19d-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9b19d-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

