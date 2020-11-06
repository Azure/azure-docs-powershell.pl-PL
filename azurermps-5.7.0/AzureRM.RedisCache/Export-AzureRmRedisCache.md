---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/export-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
ms.openlocfilehash: cd19fe8052ae95f547971452f4364f279f365cac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542396"
---
# <span data-ttu-id="cd4ef-101">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="cd4ef-101">Export-AzureRmRedisCache</span></span>

## <span data-ttu-id="cd4ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd4ef-102">SYNOPSIS</span></span>
<span data-ttu-id="cd4ef-103">Umożliwia wyeksportowanie danych z pamięci podręcznej platformy Azure Redis do kontenera.</span><span class="sxs-lookup"><span data-stu-id="cd4ef-103">Exports data from Azure Redis Cache to a container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd4ef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd4ef-104">SYNTAX</span></span>

```
Export-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd4ef-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cd4ef-105">DESCRIPTION</span></span>
<span data-ttu-id="cd4ef-106">Polecenie cmdlet **Export-AzureRmRedisCache** eksportuje dane z pamięci podręcznej Azure Redis do kontenera.</span><span class="sxs-lookup"><span data-stu-id="cd4ef-106">The **Export-AzureRmRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="cd4ef-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd4ef-107">EXAMPLES</span></span>

### <span data-ttu-id="cd4ef-108">Przykład 1. Eksportowanie danych</span><span class="sxs-lookup"><span data-stu-id="cd4ef-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="cd4ef-109">To polecenie umożliwia wyeksportowanie danych z wystąpienia pamięci podręcznej usługi Azure Redis do kontenera określonego przez adres URL SAS.</span><span class="sxs-lookup"><span data-stu-id="cd4ef-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="cd4ef-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd4ef-110">PARAMETERS</span></span>

### <span data-ttu-id="cd4ef-111">-Kontener</span><span class="sxs-lookup"><span data-stu-id="cd4ef-111">-Container</span></span>
<span data-ttu-id="cd4ef-112">Określa adres URL SAS usługi kontenera, w którym to polecenie cmdlet eksportuje dane.</span><span class="sxs-lookup"><span data-stu-id="cd4ef-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="cd4ef-113">Możesz wygenerować adres URL SAS usługi za pomocą następujących poleceń programu PowerShell:</span><span class="sxs-lookup"><span data-stu-id="cd4ef-113">You can generate a Service SAS URL using the following PowerShell commands:</span></span>

<span data-ttu-id="cd4ef-114">$storageAccountContext = New-AzureStorageContext-StorageAccountName "storagename"-StorageAccountKey "Key"</span><span class="sxs-lookup"><span data-stu-id="cd4ef-114">$storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key"</span></span>

<span data-ttu-id="cd4ef-115">$sasKeyForContainer = New-AzureStorageContainerSASToken-Name "ContainerName"-uprawnienie "rwdl"-StartTime ([System. DateTime]:: Now). Addminut (-15)-ExpiryTime ([System. DateTime]:: teraz). Addgodzin (5)-Context $storageAccountContext-FullUri</span><span class="sxs-lookup"><span data-stu-id="cd4ef-115">$sasKeyForContainer = New-AzureStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri</span></span> 

<span data-ttu-id="cd4ef-116">Export-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-name "cacheName"-prefix "blobprefix"-Container ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="cd4ef-116">Export-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd4ef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd4ef-117">-DefaultProfile</span></span>
<span data-ttu-id="cd4ef-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd4ef-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4ef-119">-Format</span><span class="sxs-lookup"><span data-stu-id="cd4ef-119">-Format</span></span>
<span data-ttu-id="cd4ef-120">Określa format obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="cd4ef-120">Specifies a format for the blob.</span></span>
<span data-ttu-id="cd4ef-121">Obecnie RDB jest jedynym obsługiwanym formatem.</span><span class="sxs-lookup"><span data-stu-id="cd4ef-121">Currently rdb is the only supported format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd4ef-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cd4ef-122">-Name</span></span>
<span data-ttu-id="cd4ef-123">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="cd4ef-123">Specifies the name of a cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd4ef-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd4ef-124">-PassThru</span></span>
<span data-ttu-id="cd4ef-125">Wskazuje, że to polecenie cmdlet zwraca wartość logiczną wskazującą, czy operacja kończy się pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="cd4ef-125">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="cd4ef-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="cd4ef-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4ef-127">-Prefix</span><span class="sxs-lookup"><span data-stu-id="cd4ef-127">-Prefix</span></span>
<span data-ttu-id="cd4ef-128">Określa prefiks, którego należy użyć w przypadku nazw obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="cd4ef-128">Specifies a prefix to use for blob names.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd4ef-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd4ef-129">-ResourceGroupName</span></span>
<span data-ttu-id="cd4ef-130">Określa nazwę grupy zasobów zawierającej pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="cd4ef-130">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd4ef-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd4ef-131">-Confirm</span></span>
<span data-ttu-id="cd4ef-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd4ef-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4ef-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd4ef-133">-WhatIf</span></span>
<span data-ttu-id="cd4ef-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd4ef-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd4ef-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cd4ef-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4ef-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd4ef-136">CommonParameters</span></span>
<span data-ttu-id="cd4ef-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd4ef-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd4ef-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd4ef-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd4ef-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd4ef-139">INPUTS</span></span>

### <span data-ttu-id="cd4ef-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="cd4ef-140">None</span></span>
<span data-ttu-id="cd4ef-141">Możesz popotokować dane wejściowe tego polecenia cmdlet, korzystając z nazwy właściwości, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="cd4ef-141">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="cd4ef-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd4ef-142">OUTPUTS</span></span>

### <span data-ttu-id="cd4ef-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="cd4ef-143">None</span></span>

## <span data-ttu-id="cd4ef-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd4ef-144">NOTES</span></span>
* <span data-ttu-id="cd4ef-145">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, aplikacji, witryna internetowa</span><span class="sxs-lookup"><span data-stu-id="cd4ef-145">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="cd4ef-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd4ef-146">RELATED LINKS</span></span>

[<span data-ttu-id="cd4ef-147">Import — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="cd4ef-147">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="cd4ef-148">Nowe — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="cd4ef-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="cd4ef-149">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="cd4ef-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="cd4ef-150">Resetowanie — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="cd4ef-150">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="cd4ef-151">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="cd4ef-151">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


