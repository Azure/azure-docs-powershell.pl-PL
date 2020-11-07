---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: b0f459d6884c9588036668743edc58333ecc1275
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719407"
---
# <span data-ttu-id="113a1-101">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="113a1-101">New-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="113a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="113a1-102">SYNOPSIS</span></span>
<span data-ttu-id="113a1-103">Tworzy nową konfigurację opróżniania połączeń dla ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="113a1-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="113a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="113a1-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="113a1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="113a1-105">DESCRIPTION</span></span>
<span data-ttu-id="113a1-106">Polecenie cmdlet **New-AzureRmApplicationGatewayConnectionDraining** umożliwia utworzenie nowej konfiguracji opróżniania połączeń dla ustawień http zaplecza.</span><span class="sxs-lookup"><span data-stu-id="113a1-106">The **New-AzureRmApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="113a1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="113a1-107">EXAMPLES</span></span>

### <span data-ttu-id="113a1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="113a1-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzureRmApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="113a1-109">Polecenie tworzy nową konfigurację opróżniania połączenia z włączonym ustawieniem prawda, a DrainTimeoutInSec jest ustawiona na 42 sekund i zapisuje ją w $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="113a1-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="113a1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="113a1-110">PARAMETERS</span></span>

### <span data-ttu-id="113a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="113a1-111">-DefaultProfile</span></span>
<span data-ttu-id="113a1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="113a1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="113a1-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="113a1-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="113a1-114">Liczba sekund opróżniania połączenia jest aktywna.</span><span class="sxs-lookup"><span data-stu-id="113a1-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="113a1-115">Dopuszczalne wartości wynoszą od 1 do 3600 sekund.</span><span class="sxs-lookup"><span data-stu-id="113a1-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="113a1-116">-Enabled</span><span class="sxs-lookup"><span data-stu-id="113a1-116">-Enabled</span></span>
<span data-ttu-id="113a1-117">Czy opróżnianie połączenia jest włączone, czy nie.</span><span class="sxs-lookup"><span data-stu-id="113a1-117">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="113a1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="113a1-118">CommonParameters</span></span>
<span data-ttu-id="113a1-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="113a1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="113a1-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="113a1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="113a1-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="113a1-121">INPUTS</span></span>

### <span data-ttu-id="113a1-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="113a1-122">None</span></span>

## <span data-ttu-id="113a1-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="113a1-123">OUTPUTS</span></span>

### <span data-ttu-id="113a1-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="113a1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="113a1-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="113a1-125">NOTES</span></span>

## <span data-ttu-id="113a1-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="113a1-126">RELATED LINKS</span></span>

[<span data-ttu-id="113a1-127">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="113a1-127">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="113a1-128">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="113a1-128">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="113a1-129">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="113a1-129">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)

