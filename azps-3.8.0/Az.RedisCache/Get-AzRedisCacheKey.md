---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
ms.openlocfilehash: 5588a3abecdec741aa6630083c38c01178669bae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052535"
---
# <span data-ttu-id="c7818-101">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="c7818-101">Get-AzRedisCacheKey</span></span>

## <span data-ttu-id="c7818-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c7818-102">SYNOPSIS</span></span>
<span data-ttu-id="c7818-103">Pobiera klucze dostępu dla pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="c7818-103">Gets the access keys for a Redis Cache.</span></span>

## <span data-ttu-id="c7818-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c7818-104">SYNTAX</span></span>

```
Get-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7818-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c7818-105">DESCRIPTION</span></span>
<span data-ttu-id="c7818-106">Polecenie cmdlet **Get-AzRedisCacheKey** pobiera klucze dostępu w pamięci podręcznej platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="c7818-106">The **Get-AzRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="c7818-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c7818-107">EXAMPLES</span></span>

### <span data-ttu-id="c7818-108">Przykład 1: uzyskiwanie klawiszy dostępu dla pamięci podręcznej Redis</span><span class="sxs-lookup"><span data-stu-id="c7818-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="c7818-109">To polecenie pobiera klawisze dostępu o nazwie MyCacheKey.</span><span class="sxs-lookup"><span data-stu-id="c7818-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="c7818-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c7818-110">PARAMETERS</span></span>

### <span data-ttu-id="c7818-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7818-111">-DefaultProfile</span></span>
<span data-ttu-id="c7818-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c7818-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7818-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c7818-113">-Name</span></span>
<span data-ttu-id="c7818-114">Określa nazwę pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="c7818-114">Specifies the name of a Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7818-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7818-115">-ResourceGroupName</span></span>
<span data-ttu-id="c7818-116">Określa nazwę grupy zasobów zawierającej pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="c7818-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7818-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7818-117">CommonParameters</span></span>
<span data-ttu-id="c7818-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7818-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7818-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7818-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7818-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7818-120">INPUTS</span></span>

### <span data-ttu-id="c7818-121">System. String</span><span class="sxs-lookup"><span data-stu-id="c7818-121">System.String</span></span>

## <span data-ttu-id="c7818-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c7818-122">OUTPUTS</span></span>

### <span data-ttu-id="c7818-123">Microsoft. Azure. Management. Redis. MODELES. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="c7818-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="c7818-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c7818-124">NOTES</span></span>

## <span data-ttu-id="c7818-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c7818-125">RELATED LINKS</span></span>

[<span data-ttu-id="c7818-126">Nowe — AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="c7818-126">New-AzRedisCacheKey</span></span>](./New-AzRedisCacheKey.md)


