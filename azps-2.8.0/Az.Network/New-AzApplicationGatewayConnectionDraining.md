---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 3401010e1b65dbd0ad24f634c32b06449671419f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870027"
---
# <span data-ttu-id="9768f-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9768f-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="9768f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9768f-102">SYNOPSIS</span></span>
<span data-ttu-id="9768f-103">Tworzy nową konfigurację opróżniania połączeń dla ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="9768f-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="9768f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9768f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9768f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9768f-105">DESCRIPTION</span></span>
<span data-ttu-id="9768f-106">Polecenie cmdlet **New-AzApplicationGatewayConnectionDraining** umożliwia utworzenie nowej konfiguracji opróżniania połączeń dla ustawień http zaplecza.</span><span class="sxs-lookup"><span data-stu-id="9768f-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="9768f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9768f-107">EXAMPLES</span></span>

### <span data-ttu-id="9768f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9768f-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="9768f-109">Polecenie tworzy nową konfigurację opróżniania połączenia z włączonym ustawieniem prawda, a DrainTimeoutInSec jest ustawiona na 42 sekund i zapisuje ją w $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="9768f-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="9768f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9768f-110">PARAMETERS</span></span>

### <span data-ttu-id="9768f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9768f-111">-DefaultProfile</span></span>
<span data-ttu-id="9768f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9768f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9768f-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="9768f-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="9768f-114">Liczba sekund opróżniania połączenia jest aktywna.</span><span class="sxs-lookup"><span data-stu-id="9768f-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="9768f-115">Dopuszczalne wartości wynoszą od 1 do 3600 sekund.</span><span class="sxs-lookup"><span data-stu-id="9768f-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="9768f-116">-Enabled</span><span class="sxs-lookup"><span data-stu-id="9768f-116">-Enabled</span></span>
<span data-ttu-id="9768f-117">Czy opróżnianie połączenia jest włączone, czy nie.</span><span class="sxs-lookup"><span data-stu-id="9768f-117">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="9768f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9768f-118">CommonParameters</span></span>
<span data-ttu-id="9768f-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9768f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9768f-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9768f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9768f-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9768f-121">INPUTS</span></span>

### <span data-ttu-id="9768f-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9768f-122">None</span></span>

## <span data-ttu-id="9768f-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9768f-123">OUTPUTS</span></span>

### <span data-ttu-id="9768f-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9768f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="9768f-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9768f-125">NOTES</span></span>

## <span data-ttu-id="9768f-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9768f-126">RELATED LINKS</span></span>

[<span data-ttu-id="9768f-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9768f-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="9768f-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9768f-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="9768f-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9768f-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

