---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: b5bfedea118aa3770bac3141d05db379a4655906
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006218"
---
# <span data-ttu-id="be98b-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="be98b-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="be98b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be98b-102">SYNOPSIS</span></span>
<span data-ttu-id="be98b-103">Tworzy nową konfigurację opróżniania połączenia dla ustawień protokołu HTTP na zawczasu.</span><span class="sxs-lookup"><span data-stu-id="be98b-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="be98b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="be98b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be98b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="be98b-105">DESCRIPTION</span></span>
<span data-ttu-id="be98b-106">Polecenie **cmdlet New-AzApplicationGatewayConnectionDraining** tworzy nową konfigurację opróżniania połączenia dla końcowych ustawień HTTP.</span><span class="sxs-lookup"><span data-stu-id="be98b-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="be98b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="be98b-107">EXAMPLES</span></span>

### <span data-ttu-id="be98b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="be98b-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="be98b-109">To polecenie tworzy nową konfigurację rozładowania połączenia z włączonymi wartościami Prawda i DrainTimeoutInSec ustawioną na 42 sekundy i zapisuje ją w $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="be98b-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="be98b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be98b-110">PARAMETERS</span></span>

### <span data-ttu-id="be98b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be98b-111">-DefaultProfile</span></span>
<span data-ttu-id="be98b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="be98b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be98b-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="be98b-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="be98b-114">Liczba sekund wyczerpu połączenia jest aktywna.</span><span class="sxs-lookup"><span data-stu-id="be98b-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="be98b-115">Dopuszczalne wartości to od 1 sekundy do 3600 sekund.</span><span class="sxs-lookup"><span data-stu-id="be98b-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="be98b-116">— włączone</span><span class="sxs-lookup"><span data-stu-id="be98b-116">-Enabled</span></span>
<span data-ttu-id="be98b-117">Czy włączono wyczerpanie połączenia, czy nie.</span><span class="sxs-lookup"><span data-stu-id="be98b-117">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="be98b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be98b-118">CommonParameters</span></span>
<span data-ttu-id="be98b-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be98b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be98b-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be98b-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be98b-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be98b-121">INPUTS</span></span>

### <span data-ttu-id="be98b-122">Brak</span><span class="sxs-lookup"><span data-stu-id="be98b-122">None</span></span>

## <span data-ttu-id="be98b-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be98b-123">OUTPUTS</span></span>

### <span data-ttu-id="be98b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="be98b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="be98b-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="be98b-125">NOTES</span></span>

## <span data-ttu-id="be98b-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be98b-126">RELATED LINKS</span></span>

[<span data-ttu-id="be98b-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="be98b-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="be98b-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="be98b-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="be98b-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="be98b-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

