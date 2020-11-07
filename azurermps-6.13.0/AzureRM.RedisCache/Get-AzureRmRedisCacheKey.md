---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
ms.openlocfilehash: 297d02fcb77c8fc537831b2b1995bfe43ca90e73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544896"
---
# <span data-ttu-id="29eb6-101">Get-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="29eb6-101">Get-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="29eb6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29eb6-102">SYNOPSIS</span></span>
<span data-ttu-id="29eb6-103">Pobiera klucze dostępu dla pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="29eb6-103">Gets the access keys for a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29eb6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29eb6-104">SYNTAX</span></span>

```
Get-AzureRmRedisCacheKey [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29eb6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="29eb6-105">DESCRIPTION</span></span>
<span data-ttu-id="29eb6-106">Polecenie cmdlet **Get-AzureRmRedisCacheKey** pobiera klucze dostępu w pamięci podręcznej platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="29eb6-106">The **Get-AzureRmRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="29eb6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29eb6-107">EXAMPLES</span></span>

### <span data-ttu-id="29eb6-108">Przykład 1: uzyskiwanie klawiszy dostępu dla pamięci podręcznej Redis</span><span class="sxs-lookup"><span data-stu-id="29eb6-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzureRmRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="29eb6-109">To polecenie pobiera klawisze dostępu o nazwie MyCacheKey.</span><span class="sxs-lookup"><span data-stu-id="29eb6-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="29eb6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29eb6-110">PARAMETERS</span></span>

### <span data-ttu-id="29eb6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29eb6-111">-DefaultProfile</span></span>
<span data-ttu-id="29eb6-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="29eb6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29eb6-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="29eb6-113">-Name</span></span>
<span data-ttu-id="29eb6-114">Określa nazwę pamięci podręcznej Redis.</span><span class="sxs-lookup"><span data-stu-id="29eb6-114">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="29eb6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29eb6-115">-ResourceGroupName</span></span>
<span data-ttu-id="29eb6-116">Określa nazwę grupy zasobów zawierającej pamięć podręczną Redis.</span><span class="sxs-lookup"><span data-stu-id="29eb6-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="29eb6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29eb6-117">CommonParameters</span></span>
<span data-ttu-id="29eb6-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29eb6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29eb6-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29eb6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29eb6-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29eb6-120">INPUTS</span></span>

### <span data-ttu-id="29eb6-121">System. String</span><span class="sxs-lookup"><span data-stu-id="29eb6-121">System.String</span></span>

## <span data-ttu-id="29eb6-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29eb6-122">OUTPUTS</span></span>

### <span data-ttu-id="29eb6-123">Microsoft. Azure. Management. Redis. MODELES. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="29eb6-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="29eb6-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29eb6-124">NOTES</span></span>

## <span data-ttu-id="29eb6-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29eb6-125">RELATED LINKS</span></span>

[<span data-ttu-id="29eb6-126">Nowe — AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="29eb6-126">New-AzureRmRedisCacheKey</span></span>](./New-AzureRmRedisCacheKey.md)

