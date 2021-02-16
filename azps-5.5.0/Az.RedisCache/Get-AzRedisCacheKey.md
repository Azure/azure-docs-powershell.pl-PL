---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
ms.openlocfilehash: 5588a3abecdec741aa6630083c38c01178669bae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178971"
---
# <span data-ttu-id="727a2-101">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="727a2-101">Get-AzRedisCacheKey</span></span>

## <span data-ttu-id="727a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="727a2-102">SYNOPSIS</span></span>
<span data-ttu-id="727a2-103">Pobiera klawisze dostępu dla pamięci podręcznej Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="727a2-103">Gets the access keys for a Redis Cache.</span></span>

## <span data-ttu-id="727a2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="727a2-104">SYNTAX</span></span>

```
Get-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="727a2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="727a2-105">DESCRIPTION</span></span>
<span data-ttu-id="727a2-106">Polecenie **cmdlet Get-AzRedisCacheKey** pobiera klucze dostępu dla funkcji Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="727a2-106">The **Get-AzRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="727a2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="727a2-107">EXAMPLES</span></span>

### <span data-ttu-id="727a2-108">Przykład 1. Uzyskiwanie klawiszy dostępu dla pamięci podręcznej Redis</span><span class="sxs-lookup"><span data-stu-id="727a2-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="727a2-109">To polecenie pobiera klawisze dostępu o nazwie MyCacheKey.</span><span class="sxs-lookup"><span data-stu-id="727a2-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="727a2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="727a2-110">PARAMETERS</span></span>

### <span data-ttu-id="727a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="727a2-111">-DefaultProfile</span></span>
<span data-ttu-id="727a2-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="727a2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="727a2-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="727a2-113">-Name</span></span>
<span data-ttu-id="727a2-114">Określa nazwę pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="727a2-114">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="727a2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="727a2-115">-ResourceGroupName</span></span>
<span data-ttu-id="727a2-116">Określa nazwę grupy zasobów zawierającej pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="727a2-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="727a2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="727a2-117">CommonParameters</span></span>
<span data-ttu-id="727a2-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="727a2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="727a2-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="727a2-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="727a2-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="727a2-120">INPUTS</span></span>

### <span data-ttu-id="727a2-121">System.String</span><span class="sxs-lookup"><span data-stu-id="727a2-121">System.String</span></span>

## <span data-ttu-id="727a2-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="727a2-122">OUTPUTS</span></span>

### <span data-ttu-id="727a2-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="727a2-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="727a2-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="727a2-124">NOTES</span></span>

## <span data-ttu-id="727a2-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="727a2-125">RELATED LINKS</span></span>

[<span data-ttu-id="727a2-126">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="727a2-126">New-AzRedisCacheKey</span></span>](./New-AzRedisCacheKey.md)


