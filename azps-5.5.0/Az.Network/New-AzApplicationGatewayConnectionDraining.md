---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 679a1311526f7fa5028c83e6571001d14b2ff3f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184539"
---
# <span data-ttu-id="47988-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="47988-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="47988-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47988-102">SYNOPSIS</span></span>
<span data-ttu-id="47988-103">Tworzy nową konfigurację wyczerpania połączenia dla ustawień protokołu HTTP na zawczasu.</span><span class="sxs-lookup"><span data-stu-id="47988-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="47988-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="47988-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47988-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="47988-105">DESCRIPTION</span></span>
<span data-ttu-id="47988-106">Polecenie **cmdlet New-AzApplicationGatewayConnectionDraining** tworzy nową konfigurację opróżniania połączenia dla końcowych ustawień HTTP.</span><span class="sxs-lookup"><span data-stu-id="47988-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="47988-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="47988-107">EXAMPLES</span></span>

### <span data-ttu-id="47988-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="47988-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="47988-109">To polecenie tworzy nową konfigurację rozładowania połączenia z włączonymi wartościami Prawda i DrainTimeoutInSec ustawioną na 42 sekundy i zapisuje ją w $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="47988-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="47988-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47988-110">PARAMETERS</span></span>

### <span data-ttu-id="47988-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47988-111">-DefaultProfile</span></span>
<span data-ttu-id="47988-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="47988-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47988-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="47988-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="47988-114">Liczba sekund wyczerpu połączenia jest aktywna.</span><span class="sxs-lookup"><span data-stu-id="47988-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="47988-115">Dopuszczalne wartości to od 1 sekundy do 3600 sekund.</span><span class="sxs-lookup"><span data-stu-id="47988-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="47988-116">— włączone</span><span class="sxs-lookup"><span data-stu-id="47988-116">-Enabled</span></span>
<span data-ttu-id="47988-117">Czy włączono wyczerpanie połączenia, czy nie.</span><span class="sxs-lookup"><span data-stu-id="47988-117">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="47988-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47988-118">CommonParameters</span></span>
<span data-ttu-id="47988-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47988-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47988-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47988-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47988-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47988-121">INPUTS</span></span>

### <span data-ttu-id="47988-122">Brak</span><span class="sxs-lookup"><span data-stu-id="47988-122">None</span></span>

## <span data-ttu-id="47988-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47988-123">OUTPUTS</span></span>

### <span data-ttu-id="47988-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="47988-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="47988-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="47988-125">NOTES</span></span>

## <span data-ttu-id="47988-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47988-126">RELATED LINKS</span></span>

[<span data-ttu-id="47988-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="47988-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="47988-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="47988-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="47988-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="47988-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

