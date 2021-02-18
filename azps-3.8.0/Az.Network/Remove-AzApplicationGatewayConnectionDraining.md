---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 4b0eb6188f75b71e3e56107138b6d5e2f9fc7b93
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406078"
---
# <span data-ttu-id="c3dcd-101">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c3dcd-101">Remove-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="c3dcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3dcd-102">SYNOPSIS</span></span>
<span data-ttu-id="c3dcd-103">Usuwa konfigurację wyczerpania połączenia obiektu ustawień protokołu HTTP na zawczasu.</span><span class="sxs-lookup"><span data-stu-id="c3dcd-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="c3dcd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c3dcd-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3dcd-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c3dcd-105">DESCRIPTION</span></span>
<span data-ttu-id="c3dcd-106">Polecenie **cmdlet Remove-AzApplicationGatewayConnectionDraining** usuwa konfigurację opróżniania połączenia obiektu ustawień protokołu HTTP na zawczasu.</span><span class="sxs-lookup"><span data-stu-id="c3dcd-106">The **Remove-AzApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="c3dcd-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c3dcd-107">EXAMPLES</span></span>

### <span data-ttu-id="c3dcd-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c3dcd-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="c3dcd-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="c3dcd-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c3dcd-110">Drugie polecenie pobiera ustawienia protokołu HTTP z końca strony o nazwie Ustawienia01 dla protokołu $AppGw i zapisuje ustawienia w $Settings sieci.</span><span class="sxs-lookup"><span data-stu-id="c3dcd-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="c3dcd-111">Ostatnie polecenie usuwa konfigurację rozładowania połączenia dla ustawień protokołu HTTP na zawczasu przechowywanych w $Settings.</span><span class="sxs-lookup"><span data-stu-id="c3dcd-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="c3dcd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3dcd-112">PARAMETERS</span></span>

### <span data-ttu-id="c3dcd-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c3dcd-113">-BackendHttpSettings</span></span>
<span data-ttu-id="c3dcd-114">Ustawienia protokołu HTTP zaplecza</span><span class="sxs-lookup"><span data-stu-id="c3dcd-114">The backend http settings</span></span>

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

### <span data-ttu-id="c3dcd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3dcd-115">-DefaultProfile</span></span>
<span data-ttu-id="c3dcd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3dcd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3dcd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3dcd-117">CommonParameters</span></span>
<span data-ttu-id="c3dcd-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3dcd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3dcd-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3dcd-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3dcd-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3dcd-120">INPUTS</span></span>

### <span data-ttu-id="c3dcd-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c3dcd-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="c3dcd-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3dcd-122">OUTPUTS</span></span>

### <span data-ttu-id="c3dcd-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c3dcd-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="c3dcd-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c3dcd-124">NOTES</span></span>

## <span data-ttu-id="c3dcd-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3dcd-125">RELATED LINKS</span></span>

[<span data-ttu-id="c3dcd-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3dcd-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)


[<span data-ttu-id="c3dcd-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c3dcd-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="c3dcd-128">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c3dcd-128">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="c3dcd-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c3dcd-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

