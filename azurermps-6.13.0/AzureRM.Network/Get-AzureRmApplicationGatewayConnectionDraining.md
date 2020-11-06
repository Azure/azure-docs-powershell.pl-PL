---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 147727cffc03de5ba8848705cf79facdbdc43320
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545115"
---
# <span data-ttu-id="2e3e8-101">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2e3e8-101">Get-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="2e3e8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e3e8-102">SYNOPSIS</span></span>
<span data-ttu-id="2e3e8-103">Pobiera konfigurację opróżniania połączenia obiektu ustawień HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="2e3e8-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e3e8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e3e8-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e3e8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2e3e8-105">DESCRIPTION</span></span>
<span data-ttu-id="2e3e8-106">Polecenie cmdlet **Get-AzureRmApplicationGatewayConnectionDraining** Pobiera konfigurację opróżniania połączenia obiektu ustawień http zaplecza.</span><span class="sxs-lookup"><span data-stu-id="2e3e8-106">The **Get-AzureRmApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="2e3e8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e3e8-107">EXAMPLES</span></span>

### <span data-ttu-id="2e3e8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2e3e8-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="2e3e8-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2e3e8-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2e3e8-110">Drugie polecenie pobiera ustawienia HTTP back-end o nazwie Settings01 dla $AppGw i zapisuje ustawienia w zmiennej $Settings.</span><span class="sxs-lookup"><span data-stu-id="2e3e8-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="2e3e8-111">Ostatnie polecenie powoduje wyświetlenie konfiguracji opróżniania połączenia na podstawie ustawień HTTP zaplecza $Settings i zapisanie jej w zmiennej $ConnectionDraining.</span><span class="sxs-lookup"><span data-stu-id="2e3e8-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="2e3e8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e3e8-112">PARAMETERS</span></span>

### <span data-ttu-id="2e3e8-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2e3e8-113">-BackendHttpSettings</span></span>
<span data-ttu-id="2e3e8-114">Ustawienia http zaplecza</span><span class="sxs-lookup"><span data-stu-id="2e3e8-114">The backend http settings</span></span>

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

### <span data-ttu-id="2e3e8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e3e8-115">-DefaultProfile</span></span>
<span data-ttu-id="2e3e8-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2e3e8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e3e8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e3e8-117">CommonParameters</span></span>
<span data-ttu-id="2e3e8-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e3e8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e3e8-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e3e8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e3e8-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e3e8-120">INPUTS</span></span>

### <span data-ttu-id="2e3e8-121">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2e3e8-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>
<span data-ttu-id="2e3e8-122">Parametry: BackendHttpSettings (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2e3e8-122">Parameters: BackendHttpSettings (ByValue)</span></span>

## <span data-ttu-id="2e3e8-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e3e8-123">OUTPUTS</span></span>

### <span data-ttu-id="2e3e8-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2e3e8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="2e3e8-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e3e8-125">NOTES</span></span>

## <span data-ttu-id="2e3e8-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e3e8-126">RELATED LINKS</span></span>

[<span data-ttu-id="2e3e8-127">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2e3e8-127">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="2e3e8-128">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2e3e8-128">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="2e3e8-129">Nowe — AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2e3e8-129">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="2e3e8-130">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2e3e8-130">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="2e3e8-131">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2e3e8-131">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)
