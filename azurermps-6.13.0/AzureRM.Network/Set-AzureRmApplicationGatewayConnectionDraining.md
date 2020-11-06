---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 421bc74fb110aa48ff72388462e5496d9ceb1434
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545015"
---
# <span data-ttu-id="4c25f-101">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="4c25f-101">Set-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="4c25f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4c25f-102">SYNOPSIS</span></span>
<span data-ttu-id="4c25f-103">Modyfikuje konfigurację opróżniania połączenia obiektu ustawień HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="4c25f-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c25f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4c25f-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c25f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4c25f-105">DESCRIPTION</span></span>
<span data-ttu-id="4c25f-106">Polecenie cmdlet **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** modyfikuje konfigurację opróżniania połączenia obiektu ustawień http zaplecza.</span><span class="sxs-lookup"><span data-stu-id="4c25f-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="4c25f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4c25f-107">EXAMPLES</span></span>

### <span data-ttu-id="4c25f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4c25f-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="4c25f-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4c25f-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4c25f-110">Drugie polecenie pobiera ustawienia HTTP back-end o nazwie Settings01 dla $AppGw i zapisuje ustawienia w zmiennej $Settings.</span><span class="sxs-lookup"><span data-stu-id="4c25f-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="4c25f-111">Ostatnie polecenie modyfikuje konfigurację opróżniania połączenia obiektu ustawień https zaplecza przechowywanego w $Settings przez ustawienie wartości FAŁSZ i DrainTimeoutInSec na 3600.</span><span class="sxs-lookup"><span data-stu-id="4c25f-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="4c25f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4c25f-112">PARAMETERS</span></span>

### <span data-ttu-id="4c25f-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4c25f-113">-BackendHttpSettings</span></span>
<span data-ttu-id="4c25f-114">Ustawienia http zaplecza</span><span class="sxs-lookup"><span data-stu-id="4c25f-114">The backend http settings</span></span>

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

### <span data-ttu-id="4c25f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c25f-115">-DefaultProfile</span></span>
<span data-ttu-id="4c25f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4c25f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c25f-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="4c25f-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="4c25f-118">Liczba sekund opróżniania połączenia jest aktywna.</span><span class="sxs-lookup"><span data-stu-id="4c25f-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="4c25f-119">Dopuszczalne wartości wynoszą od 1 do 3600 sekund.</span><span class="sxs-lookup"><span data-stu-id="4c25f-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="4c25f-120">-Enabled</span><span class="sxs-lookup"><span data-stu-id="4c25f-120">-Enabled</span></span>
<span data-ttu-id="4c25f-121">Czy opróżnianie połączenia jest włączone, czy nie.</span><span class="sxs-lookup"><span data-stu-id="4c25f-121">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="4c25f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c25f-122">CommonParameters</span></span>
<span data-ttu-id="4c25f-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c25f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c25f-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c25f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c25f-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c25f-125">INPUTS</span></span>

### <span data-ttu-id="4c25f-126">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4c25f-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>
<span data-ttu-id="4c25f-127">Parametry: BackendHttpSettings (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4c25f-127">Parameters: BackendHttpSettings (ByValue)</span></span>

## <span data-ttu-id="4c25f-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4c25f-128">OUTPUTS</span></span>

### <span data-ttu-id="4c25f-129">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4c25f-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="4c25f-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4c25f-130">NOTES</span></span>

## <span data-ttu-id="4c25f-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c25f-131">RELATED LINKS</span></span>

[<span data-ttu-id="4c25f-132">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c25f-132">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="4c25f-133">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4c25f-133">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="4c25f-134">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="4c25f-134">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="4c25f-135">Nowe — AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="4c25f-135">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="4c25f-136">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="4c25f-136">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

