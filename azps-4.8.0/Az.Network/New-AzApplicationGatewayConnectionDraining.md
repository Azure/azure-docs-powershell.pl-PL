---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 679a1311526f7fa5028c83e6571001d14b2ff3f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223364"
---
# <span data-ttu-id="0cba6-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0cba6-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="0cba6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0cba6-102">SYNOPSIS</span></span>
<span data-ttu-id="0cba6-103">Tworzy nową konfigurację opróżniania połączeń dla ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="0cba6-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="0cba6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0cba6-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cba6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0cba6-105">DESCRIPTION</span></span>
<span data-ttu-id="0cba6-106">Polecenie cmdlet **New-AzApplicationGatewayConnectionDraining** umożliwia utworzenie nowej konfiguracji opróżniania połączeń dla ustawień http zaplecza.</span><span class="sxs-lookup"><span data-stu-id="0cba6-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="0cba6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0cba6-107">EXAMPLES</span></span>

### <span data-ttu-id="0cba6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0cba6-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="0cba6-109">Polecenie tworzy nową konfigurację opróżniania połączenia z włączonym ustawieniem prawda, a DrainTimeoutInSec jest ustawiona na 42 sekund i zapisuje ją w $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="0cba6-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="0cba6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0cba6-110">PARAMETERS</span></span>

### <span data-ttu-id="0cba6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cba6-111">-DefaultProfile</span></span>
<span data-ttu-id="0cba6-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0cba6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cba6-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="0cba6-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="0cba6-114">Liczba sekund opróżniania połączenia jest aktywna.</span><span class="sxs-lookup"><span data-stu-id="0cba6-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="0cba6-115">Dopuszczalne wartości wynoszą od 1 do 3600 sekund.</span><span class="sxs-lookup"><span data-stu-id="0cba6-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="0cba6-116">-Enabled</span><span class="sxs-lookup"><span data-stu-id="0cba6-116">-Enabled</span></span>
<span data-ttu-id="0cba6-117">Czy opróżnianie połączenia jest włączone, czy nie.</span><span class="sxs-lookup"><span data-stu-id="0cba6-117">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="0cba6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cba6-118">CommonParameters</span></span>
<span data-ttu-id="0cba6-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cba6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cba6-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cba6-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cba6-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0cba6-121">INPUTS</span></span>

### <span data-ttu-id="0cba6-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0cba6-122">None</span></span>

## <span data-ttu-id="0cba6-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0cba6-123">OUTPUTS</span></span>

### <span data-ttu-id="0cba6-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0cba6-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="0cba6-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0cba6-125">NOTES</span></span>

## <span data-ttu-id="0cba6-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0cba6-126">RELATED LINKS</span></span>

[<span data-ttu-id="0cba6-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0cba6-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="0cba6-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0cba6-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="0cba6-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0cba6-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

