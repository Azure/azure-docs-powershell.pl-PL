---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
ms.openlocfilehash: 103567021d7317a6777ca5fdb01c53d1f9f023a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553119"
---
# <span data-ttu-id="035fa-101">Set-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="035fa-101">Set-AzureRmRedisCacheDiagnostics</span></span>

## <span data-ttu-id="035fa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="035fa-102">SYNOPSIS</span></span>
<span data-ttu-id="035fa-103">Włącza diagnostykę w pamięci podręcznej platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="035fa-103">Enables diagnostics on an Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="035fa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="035fa-104">SYNTAX</span></span>

```
Set-AzureRmRedisCacheDiagnostics -ResourceGroupName <String> -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="035fa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="035fa-105">DESCRIPTION</span></span>
<span data-ttu-id="035fa-106">Polecenie cmdlet **Set-AzureRmRedisCacheDiagnostics** włącza diagnostykę pamięci podręcznej usługi Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="035fa-106">The **Set-AzureRmRedisCacheDiagnostics** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="035fa-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="035fa-107">EXAMPLES</span></span>

### <span data-ttu-id="035fa-108">Przykład 1: Włączanie diagnostyki</span><span class="sxs-lookup"><span data-stu-id="035fa-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzureRmRedisCacheDiagnostics -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="035fa-109">To polecenie włącza diagnostykę w pamięci podręcznej usługi Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="035fa-109">This command enables diagnostics for an Azure Redis cache.</span></span>

<span data-ttu-id="035fa-110">To polecenie umożliwia diagnostykę lub zaktualizowanie konta magazynu dla wszystkich pamięci podręcznej usługi Azure Redis w tym samym regionie dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="035fa-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="035fa-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="035fa-111">PARAMETERS</span></span>

### <span data-ttu-id="035fa-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="035fa-112">-Name</span></span>
<span data-ttu-id="035fa-113">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="035fa-113">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="035fa-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="035fa-114">-ResourceGroupName</span></span>
<span data-ttu-id="035fa-115">Określa nazwę grupy zasobów zawierającej pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="035fa-115">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="035fa-116">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="035fa-116">-StorageAccountId</span></span>
<span data-ttu-id="035fa-117">Określa identyfikator zasobu konta magazynu służącego do przechowywania danych diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="035fa-117">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="035fa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="035fa-118">-DefaultProfile</span></span>
<span data-ttu-id="035fa-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="035fa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="035fa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="035fa-120">CommonParameters</span></span>
<span data-ttu-id="035fa-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="035fa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="035fa-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="035fa-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="035fa-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="035fa-123">INPUTS</span></span>

### <span data-ttu-id="035fa-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="035fa-124">None</span></span>

## <span data-ttu-id="035fa-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="035fa-125">OUTPUTS</span></span>

### <span data-ttu-id="035fa-126">Utratę</span><span class="sxs-lookup"><span data-stu-id="035fa-126">Void</span></span>

## <span data-ttu-id="035fa-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="035fa-127">NOTES</span></span>
* <span data-ttu-id="035fa-128">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, aplikacji, witryna internetowa</span><span class="sxs-lookup"><span data-stu-id="035fa-128">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="035fa-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="035fa-129">RELATED LINKS</span></span>

[<span data-ttu-id="035fa-130">Remove-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="035fa-130">Remove-AzureRmRedisCacheDiagnostics</span></span>](./Remove-AzureRmRedisCacheDiagnostics.md)


