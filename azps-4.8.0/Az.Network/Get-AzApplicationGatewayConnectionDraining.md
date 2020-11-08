---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: b6fe7d8be92e2d82762557a05bf88ef053e0d407
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063970"
---
# <span data-ttu-id="0ddce-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0ddce-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="0ddce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0ddce-102">SYNOPSIS</span></span>
<span data-ttu-id="0ddce-103">Pobiera konfigurację opróżniania połączenia obiektu ustawień HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="0ddce-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="0ddce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0ddce-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ddce-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0ddce-105">DESCRIPTION</span></span>
<span data-ttu-id="0ddce-106">Polecenie cmdlet **Get-AzApplicationGatewayConnectionDraining** Pobiera konfigurację opróżniania połączenia obiektu ustawień http zaplecza.</span><span class="sxs-lookup"><span data-stu-id="0ddce-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="0ddce-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0ddce-107">EXAMPLES</span></span>

### <span data-ttu-id="0ddce-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0ddce-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="0ddce-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="0ddce-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0ddce-110">Drugie polecenie pobiera ustawienia HTTP back-end o nazwie Settings01 dla $AppGw i zapisuje ustawienia w zmiennej $Settings.</span><span class="sxs-lookup"><span data-stu-id="0ddce-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="0ddce-111">Ostatnie polecenie powoduje wyświetlenie konfiguracji opróżniania połączenia na podstawie ustawień HTTP zaplecza $Settings i zapisanie jej w zmiennej $ConnectionDraining.</span><span class="sxs-lookup"><span data-stu-id="0ddce-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="0ddce-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0ddce-112">PARAMETERS</span></span>

### <span data-ttu-id="0ddce-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0ddce-113">-BackendHttpSettings</span></span>
<span data-ttu-id="0ddce-114">Ustawienia http zaplecza</span><span class="sxs-lookup"><span data-stu-id="0ddce-114">The backend http settings</span></span>

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

### <span data-ttu-id="0ddce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ddce-115">-DefaultProfile</span></span>
<span data-ttu-id="0ddce-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ddce-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ddce-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ddce-117">CommonParameters</span></span>
<span data-ttu-id="0ddce-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ddce-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ddce-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ddce-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ddce-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ddce-120">INPUTS</span></span>

### <span data-ttu-id="0ddce-121">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0ddce-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="0ddce-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0ddce-122">OUTPUTS</span></span>

### <span data-ttu-id="0ddce-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0ddce-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="0ddce-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0ddce-124">NOTES</span></span>

## <span data-ttu-id="0ddce-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ddce-125">RELATED LINKS</span></span>

[<span data-ttu-id="0ddce-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0ddce-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="0ddce-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="0ddce-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="0ddce-128">Nowe — AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0ddce-128">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="0ddce-129">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0ddce-129">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="0ddce-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0ddce-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
