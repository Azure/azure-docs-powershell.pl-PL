---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 5357b8a0a59fade3e9ff7439da9ac1eeb63f6035
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871299"
---
# <span data-ttu-id="d12df-101">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="d12df-101">Remove-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="d12df-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d12df-102">SYNOPSIS</span></span>
<span data-ttu-id="d12df-103">Usuwa konfigurację opróżniania połączenia obiektu ustawień HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="d12df-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="d12df-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d12df-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d12df-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d12df-105">DESCRIPTION</span></span>
<span data-ttu-id="d12df-106">Polecenie cmdlet **Remove-AzApplicationGatewayConnectionDraining** usuwa konfigurację opróżniania połączenia obiektu ustawień http zaplecza.</span><span class="sxs-lookup"><span data-stu-id="d12df-106">The **Remove-AzApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="d12df-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d12df-107">EXAMPLES</span></span>

### <span data-ttu-id="d12df-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d12df-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="d12df-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d12df-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d12df-110">Drugie polecenie pobiera ustawienia HTTP back-end o nazwie Settings01 dla $AppGw i zapisuje ustawienia w zmiennej $Settings.</span><span class="sxs-lookup"><span data-stu-id="d12df-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="d12df-111">Ostatnie polecenie usuwa konfigurację opróżniania połączeń ustawień HTTP zaplecza przechowywanych w $Settings.</span><span class="sxs-lookup"><span data-stu-id="d12df-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="d12df-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d12df-112">PARAMETERS</span></span>

### <span data-ttu-id="d12df-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d12df-113">-BackendHttpSettings</span></span>
<span data-ttu-id="d12df-114">Ustawienia http zaplecza</span><span class="sxs-lookup"><span data-stu-id="d12df-114">The backend http settings</span></span>

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

### <span data-ttu-id="d12df-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d12df-115">-DefaultProfile</span></span>
<span data-ttu-id="d12df-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d12df-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d12df-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d12df-117">CommonParameters</span></span>
<span data-ttu-id="d12df-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d12df-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d12df-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d12df-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d12df-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d12df-120">INPUTS</span></span>

### <span data-ttu-id="d12df-121">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d12df-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="d12df-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d12df-122">OUTPUTS</span></span>

### <span data-ttu-id="d12df-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d12df-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="d12df-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d12df-124">NOTES</span></span>

## <span data-ttu-id="d12df-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d12df-125">RELATED LINKS</span></span>

[<span data-ttu-id="d12df-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d12df-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="d12df-127">Get-AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d12df-127">Get-AzApplicationGatewayBackendHttpSettings</span></span>](./Get-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="d12df-128">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="d12df-128">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="d12df-129">Nowe — AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="d12df-129">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="d12df-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="d12df-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

