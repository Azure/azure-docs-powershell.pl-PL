---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 12667316df99e19fbc0535a2b5e3fca3082d4484
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527389"
---
# <span data-ttu-id="bdffe-101">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="bdffe-101">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="bdffe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bdffe-102">SYNOPSIS</span></span>
<span data-ttu-id="bdffe-103">Usuwa konfigurację opróżniania połączenia obiektu ustawień HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="bdffe-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdffe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bdffe-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayConnectionDraining
 -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bdffe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bdffe-105">DESCRIPTION</span></span>
<span data-ttu-id="bdffe-106">Polecenie cmdlet **Remove-AzureRmApplicationGatewayConnectionDraining** usuwa konfigurację opróżniania połączenia obiektu ustawień http zaplecza.</span><span class="sxs-lookup"><span data-stu-id="bdffe-106">The **Remove-AzureRmApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="bdffe-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bdffe-107">EXAMPLES</span></span>

### <span data-ttu-id="bdffe-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bdffe-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="bdffe-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="bdffe-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="bdffe-110">Drugie polecenie pobiera ustawienia HTTP back-end o nazwie Settings01 dla $AppGw i zapisuje ustawienia w zmiennej $Settings.</span><span class="sxs-lookup"><span data-stu-id="bdffe-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="bdffe-111">Ostatnie polecenie usuwa konfigurację opróżniania połączeń ustawień HTTP zaplecza przechowywanych w $Settings.</span><span class="sxs-lookup"><span data-stu-id="bdffe-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="bdffe-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bdffe-112">PARAMETERS</span></span>

### <span data-ttu-id="bdffe-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="bdffe-113">-BackendHttpSettings</span></span>
<span data-ttu-id="bdffe-114">Ustawienia http zaplecza</span><span class="sxs-lookup"><span data-stu-id="bdffe-114">The backend http settings</span></span>

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

### <span data-ttu-id="bdffe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdffe-115">-DefaultProfile</span></span>
<span data-ttu-id="bdffe-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bdffe-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdffe-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdffe-117">CommonParameters</span></span>
<span data-ttu-id="bdffe-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdffe-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdffe-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdffe-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdffe-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdffe-120">INPUTS</span></span>

### <span data-ttu-id="bdffe-121">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="bdffe-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="bdffe-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bdffe-122">OUTPUTS</span></span>

### <span data-ttu-id="bdffe-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="bdffe-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="bdffe-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bdffe-124">NOTES</span></span>

## <span data-ttu-id="bdffe-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bdffe-125">RELATED LINKS</span></span>

[<span data-ttu-id="bdffe-126">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bdffe-126">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="bdffe-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="bdffe-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="bdffe-128">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="bdffe-128">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="bdffe-129">Nowe — AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="bdffe-129">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="bdffe-130">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="bdffe-130">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)

