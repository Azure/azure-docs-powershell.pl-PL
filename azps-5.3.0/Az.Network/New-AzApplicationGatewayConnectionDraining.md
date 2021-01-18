---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 679a1311526f7fa5028c83e6571001d14b2ff3f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499498"
---
# <span data-ttu-id="e5e74-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="e5e74-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="e5e74-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e5e74-102">SYNOPSIS</span></span>
<span data-ttu-id="e5e74-103">Tworzy nową konfigurację opróżniania połączeń dla ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e5e74-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="e5e74-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e5e74-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5e74-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e5e74-105">DESCRIPTION</span></span>
<span data-ttu-id="e5e74-106">Polecenie cmdlet **New-AzApplicationGatewayConnectionDraining** umożliwia utworzenie nowej konfiguracji opróżniania połączeń dla ustawień http zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e5e74-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="e5e74-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e5e74-107">EXAMPLES</span></span>

### <span data-ttu-id="e5e74-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e5e74-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="e5e74-109">Polecenie tworzy nową konfigurację opróżniania połączenia z włączonym ustawieniem prawda, a DrainTimeoutInSec jest ustawiona na 42 sekund i zapisuje ją w $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="e5e74-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="e5e74-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e5e74-110">PARAMETERS</span></span>

### <span data-ttu-id="e5e74-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5e74-111">-DefaultProfile</span></span>
<span data-ttu-id="e5e74-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e5e74-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5e74-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="e5e74-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="e5e74-114">Liczba sekund opróżniania połączenia jest aktywna.</span><span class="sxs-lookup"><span data-stu-id="e5e74-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="e5e74-115">Dopuszczalne wartości wynoszą od 1 do 3600 sekund.</span><span class="sxs-lookup"><span data-stu-id="e5e74-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="e5e74-116">-Enabled</span><span class="sxs-lookup"><span data-stu-id="e5e74-116">-Enabled</span></span>
<span data-ttu-id="e5e74-117">Czy opróżnianie połączenia jest włączone, czy nie.</span><span class="sxs-lookup"><span data-stu-id="e5e74-117">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="e5e74-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5e74-118">CommonParameters</span></span>
<span data-ttu-id="e5e74-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5e74-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5e74-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5e74-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5e74-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5e74-121">INPUTS</span></span>

### <span data-ttu-id="e5e74-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e5e74-122">None</span></span>

## <span data-ttu-id="e5e74-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e5e74-123">OUTPUTS</span></span>

### <span data-ttu-id="e5e74-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="e5e74-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="e5e74-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e5e74-125">NOTES</span></span>

## <span data-ttu-id="e5e74-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5e74-126">RELATED LINKS</span></span>

[<span data-ttu-id="e5e74-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="e5e74-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="e5e74-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="e5e74-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="e5e74-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="e5e74-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

