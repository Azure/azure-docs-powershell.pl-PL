---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecacheoperationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
ms.openlocfilehash: 8416c18ac945eaab5ae9dbd758d2660c4f950417
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378240"
---
# <span data-ttu-id="6f59e-101">Get-AzRedisEnterpriseCacheOperationStatus</span><span class="sxs-lookup"><span data-stu-id="6f59e-101">Get-AzRedisEnterpriseCacheOperationStatus</span></span>

## <span data-ttu-id="6f59e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6f59e-102">SYNOPSIS</span></span>
<span data-ttu-id="6f59e-103">Pobiera stan operacji.</span><span class="sxs-lookup"><span data-stu-id="6f59e-103">Gets the status of operation.</span></span>

## <span data-ttu-id="6f59e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6f59e-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheOperationStatus -Location <String> -OperationId <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6f59e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6f59e-105">DESCRIPTION</span></span>
<span data-ttu-id="6f59e-106">Pobiera stan operacji.</span><span class="sxs-lookup"><span data-stu-id="6f59e-106">Gets the status of operation.</span></span>

## <span data-ttu-id="6f59e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6f59e-107">EXAMPLES</span></span>

### <span data-ttu-id="6f59e-108">Przykład 1: pobieranie stanu operacji</span><span class="sxs-lookup"><span data-stu-id="6f59e-108">Example 1: Get operation status</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheOperationStatus -Location "East US" -OperationId "6432a8f9-0fe6-4339-9303-772c92f35d02"

EndTime                           Name                                 StartTime                         Status
-------                           ----                                 ---------                         ------
2020-12-01T00:12:45.7107366+00:00 6432a8f9-0fe6-4339-9303-772c92f35d02 2020-12-01T00:04:35.7061294+00:00 Succeeded

```

<span data-ttu-id="6f59e-109">To polecenie uzyskuje stan operacji.</span><span class="sxs-lookup"><span data-stu-id="6f59e-109">This command gets the status of an operation.</span></span>

## <span data-ttu-id="6f59e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6f59e-110">PARAMETERS</span></span>

### <span data-ttu-id="6f59e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f59e-111">-DefaultProfile</span></span>
<span data-ttu-id="6f59e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6f59e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f59e-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6f59e-113">-Location</span></span>
<span data-ttu-id="6f59e-114">Region, w którym znajduje się operacja.</span><span class="sxs-lookup"><span data-stu-id="6f59e-114">The region the operation is in.</span></span>

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

### <span data-ttu-id="6f59e-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="6f59e-115">-OperationId</span></span>
<span data-ttu-id="6f59e-116">Unikatowy identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="6f59e-116">The operation's unique identifier.</span></span>

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

### <span data-ttu-id="6f59e-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6f59e-117">-SubscriptionId</span></span>
<span data-ttu-id="6f59e-118">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6f59e-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6f59e-119">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="6f59e-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6f59e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f59e-120">CommonParameters</span></span>
<span data-ttu-id="6f59e-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f59e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f59e-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f59e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f59e-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f59e-123">INPUTS</span></span>

## <span data-ttu-id="6f59e-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6f59e-124">OUTPUTS</span></span>

### <span data-ttu-id="6f59e-125">Microsoft. Azure. PowerShell. polecenia. RedisEnterpriseCache. models. Api20201001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="6f59e-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IOperationStatus</span></span>

## <span data-ttu-id="6f59e-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6f59e-126">NOTES</span></span>

<span data-ttu-id="6f59e-127">PISUJE</span><span class="sxs-lookup"><span data-stu-id="6f59e-127">ALIASES</span></span>

## <span data-ttu-id="6f59e-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6f59e-128">RELATED LINKS</span></span>

