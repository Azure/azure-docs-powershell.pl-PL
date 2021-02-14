---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecacheoperationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
ms.openlocfilehash: 8416c18ac945eaab5ae9dbd758d2660c4f950417
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183762"
---
# <span data-ttu-id="62816-101">Get-AzRedisEnterpriseCacheOperationStatus</span><span class="sxs-lookup"><span data-stu-id="62816-101">Get-AzRedisEnterpriseCacheOperationStatus</span></span>

## <span data-ttu-id="62816-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62816-102">SYNOPSIS</span></span>
<span data-ttu-id="62816-103">Pobiera stan operacji.</span><span class="sxs-lookup"><span data-stu-id="62816-103">Gets the status of operation.</span></span>

## <span data-ttu-id="62816-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="62816-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheOperationStatus -Location <String> -OperationId <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="62816-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="62816-105">DESCRIPTION</span></span>
<span data-ttu-id="62816-106">Pobiera stan operacji.</span><span class="sxs-lookup"><span data-stu-id="62816-106">Gets the status of operation.</span></span>

## <span data-ttu-id="62816-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="62816-107">EXAMPLES</span></span>

### <span data-ttu-id="62816-108">Przykład 1. Uzyskiwanie stanu operacji</span><span class="sxs-lookup"><span data-stu-id="62816-108">Example 1: Get operation status</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheOperationStatus -Location "East US" -OperationId "6432a8f9-0fe6-4339-9303-772c92f35d02"

EndTime                           Name                                 StartTime                         Status
-------                           ----                                 ---------                         ------
2020-12-01T00:12:45.7107366+00:00 6432a8f9-0fe6-4339-9303-772c92f35d02 2020-12-01T00:04:35.7061294+00:00 Succeeded

```

<span data-ttu-id="62816-109">To polecenie otrzymuje stan operacji.</span><span class="sxs-lookup"><span data-stu-id="62816-109">This command gets the status of an operation.</span></span>

## <span data-ttu-id="62816-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62816-110">PARAMETERS</span></span>

### <span data-ttu-id="62816-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62816-111">-DefaultProfile</span></span>
<span data-ttu-id="62816-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="62816-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62816-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="62816-113">-Location</span></span>
<span data-ttu-id="62816-114">Region, w który znajduje się operacja.</span><span class="sxs-lookup"><span data-stu-id="62816-114">The region the operation is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62816-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="62816-115">-OperationId</span></span>
<span data-ttu-id="62816-116">Czas identyfikator unikatowy.</span><span class="sxs-lookup"><span data-stu-id="62816-116">The operation's unique identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62816-117">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="62816-117">-SubscriptionId</span></span>
<span data-ttu-id="62816-118">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="62816-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="62816-119">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="62816-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62816-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62816-120">CommonParameters</span></span>
<span data-ttu-id="62816-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62816-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62816-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62816-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62816-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62816-123">INPUTS</span></span>

## <span data-ttu-id="62816-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62816-124">OUTPUTS</span></span>

### <span data-ttu-id="62816-125">Microsoft.Azure.PowerShell.Cmdlet.RedisEnterpriseCache.Models.Api20201001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="62816-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IOperationStatus</span></span>

## <span data-ttu-id="62816-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="62816-126">NOTES</span></span>

<span data-ttu-id="62816-127">ALIASY</span><span class="sxs-lookup"><span data-stu-id="62816-127">ALIASES</span></span>

## <span data-ttu-id="62816-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62816-128">RELATED LINKS</span></span>

