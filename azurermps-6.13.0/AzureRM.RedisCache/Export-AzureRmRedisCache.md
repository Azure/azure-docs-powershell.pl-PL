---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/export-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
ms.openlocfilehash: ceba71f729de627e0e7231b9c295d0cad1ccc105
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717912"
---
# <span data-ttu-id="6dfdb-101">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6dfdb-101">Export-AzureRmRedisCache</span></span>

## <span data-ttu-id="6dfdb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6dfdb-102">SYNOPSIS</span></span>
<span data-ttu-id="6dfdb-103">Umożliwia wyeksportowanie danych z pamięci podręcznej platformy Azure Redis do kontenera.</span><span class="sxs-lookup"><span data-stu-id="6dfdb-103">Exports data from Azure Redis Cache to a container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6dfdb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6dfdb-104">SYNTAX</span></span>

```
Export-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6dfdb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6dfdb-105">DESCRIPTION</span></span>
<span data-ttu-id="6dfdb-106">Polecenie cmdlet **Export-AzureRmRedisCache** eksportuje dane z pamięci podręcznej Azure Redis do kontenera.</span><span class="sxs-lookup"><span data-stu-id="6dfdb-106">The **Export-AzureRmRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="6dfdb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6dfdb-107">EXAMPLES</span></span>

### <span data-ttu-id="6dfdb-108">Przykład 1. Eksportowanie danych</span><span class="sxs-lookup"><span data-stu-id="6dfdb-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="6dfdb-109">To polecenie umożliwia wyeksportowanie danych z wystąpienia pamięci podręcznej usługi Azure Redis do kontenera określonego przez adres URL SAS.</span><span class="sxs-lookup"><span data-stu-id="6dfdb-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="6dfdb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6dfdb-110">PARAMETERS</span></span>

### <span data-ttu-id="6dfdb-111">-Kontener</span><span class="sxs-lookup"><span data-stu-id="6dfdb-111">-Container</span></span>
<span data-ttu-id="6dfdb-112">Określa adres URL SAS usługi kontenera, w którym to polecenie cmdlet eksportuje dane.</span><span class="sxs-lookup"><span data-stu-id="6dfdb-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="6dfdb-113">Możesz wygenerować adres URL SAS usługi za pomocą następujących poleceń programu PowerShell: $storageAccountContext = New-AzureStorageContext-StorageAccountName "storagename"-StorageAccountKey "Key" $sasKeyForContainer = New-AzureStorageContainerSASToken-Name "ContainerName"-uprawnienie "rwdl"-StartTime ([System. DateTime]:: Now). Addminut (-15)-ExpiryTime ([System. DateTime]:: teraz). Addgodzin (5)-Context $storageAccountContext-FullUri Export-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-name "cacheName"-prefix "blobprefix"-kontener ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="6dfdb-113">You can generate a Service SAS URL using the following PowerShell commands: $storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzureStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Export-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

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

### <span data-ttu-id="6dfdb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dfdb-114">-DefaultProfile</span></span>
<span data-ttu-id="6dfdb-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6dfdb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6dfdb-116">-Format</span><span class="sxs-lookup"><span data-stu-id="6dfdb-116">-Format</span></span>
<span data-ttu-id="6dfdb-117">Określa format obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="6dfdb-117">Specifies a format for the blob.</span></span>
<span data-ttu-id="6dfdb-118">Obecnie RDB jest jedynym obsługiwanym formatem.</span><span class="sxs-lookup"><span data-stu-id="6dfdb-118">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="6dfdb-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6dfdb-119">-Name</span></span>
<span data-ttu-id="6dfdb-120">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="6dfdb-120">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="6dfdb-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6dfdb-121">-PassThru</span></span>
<span data-ttu-id="6dfdb-122">Wskazuje, że to polecenie cmdlet zwraca wartość logiczną wskazującą, czy operacja kończy się pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="6dfdb-122">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="6dfdb-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="6dfdb-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfdb-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="6dfdb-124">-Prefix</span></span>
<span data-ttu-id="6dfdb-125">Określa prefiks, którego należy użyć w przypadku nazw obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="6dfdb-125">Specifies a prefix to use for blob names.</span></span>

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

### <span data-ttu-id="6dfdb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dfdb-126">-ResourceGroupName</span></span>
<span data-ttu-id="6dfdb-127">Określa nazwę grupy zasobów zawierającej pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="6dfdb-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="6dfdb-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6dfdb-128">-Confirm</span></span>
<span data-ttu-id="6dfdb-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dfdb-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfdb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dfdb-130">-WhatIf</span></span>
<span data-ttu-id="6dfdb-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dfdb-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6dfdb-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6dfdb-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfdb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dfdb-133">CommonParameters</span></span>
<span data-ttu-id="6dfdb-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dfdb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dfdb-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dfdb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dfdb-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6dfdb-136">INPUTS</span></span>

### <span data-ttu-id="6dfdb-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6dfdb-137">System.String</span></span>

## <span data-ttu-id="6dfdb-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6dfdb-138">OUTPUTS</span></span>

### <span data-ttu-id="6dfdb-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6dfdb-139">System.Boolean</span></span>

## <span data-ttu-id="6dfdb-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6dfdb-140">NOTES</span></span>
* <span data-ttu-id="6dfdb-141">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, aplikacji, witryna internetowa</span><span class="sxs-lookup"><span data-stu-id="6dfdb-141">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="6dfdb-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6dfdb-142">RELATED LINKS</span></span>

[<span data-ttu-id="6dfdb-143">Import — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6dfdb-143">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="6dfdb-144">Nowe — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6dfdb-144">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="6dfdb-145">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6dfdb-145">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="6dfdb-146">Resetowanie — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6dfdb-146">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="6dfdb-147">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6dfdb-147">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


