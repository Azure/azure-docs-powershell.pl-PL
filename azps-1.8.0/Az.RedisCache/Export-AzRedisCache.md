---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/export-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
ms.openlocfilehash: ec6abf13cf4f14a8d0cdaab75d5816d87f0540ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708530"
---
# <span data-ttu-id="f15ec-101">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f15ec-101">Export-AzRedisCache</span></span>

## <span data-ttu-id="f15ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f15ec-102">SYNOPSIS</span></span>
<span data-ttu-id="f15ec-103">Umożliwia wyeksportowanie danych z pamięci podręcznej platformy Azure Redis do kontenera.</span><span class="sxs-lookup"><span data-stu-id="f15ec-103">Exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="f15ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f15ec-104">SYNTAX</span></span>

```
Export-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f15ec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f15ec-105">DESCRIPTION</span></span>
<span data-ttu-id="f15ec-106">Polecenie cmdlet **Export-AzRedisCache** eksportuje dane z pamięci podręcznej Azure Redis do kontenera.</span><span class="sxs-lookup"><span data-stu-id="f15ec-106">The **Export-AzRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="f15ec-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f15ec-107">EXAMPLES</span></span>

### <span data-ttu-id="f15ec-108">Przykład 1. Eksportowanie danych</span><span class="sxs-lookup"><span data-stu-id="f15ec-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="f15ec-109">To polecenie umożliwia wyeksportowanie danych z wystąpienia pamięci podręcznej usługi Azure Redis do kontenera określonego przez adres URL SAS.</span><span class="sxs-lookup"><span data-stu-id="f15ec-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="f15ec-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f15ec-110">PARAMETERS</span></span>

### <span data-ttu-id="f15ec-111">-Kontener</span><span class="sxs-lookup"><span data-stu-id="f15ec-111">-Container</span></span>
<span data-ttu-id="f15ec-112">Określa adres URL SAS usługi kontenera, w którym to polecenie cmdlet eksportuje dane.</span><span class="sxs-lookup"><span data-stu-id="f15ec-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="f15ec-113">Możesz wygenerować adres URL SAS usługi za pomocą następujących poleceń programu PowerShell: $storageAccountContext = New-AzStorageContext-StorageAccountName "storagename"-StorageAccountKey "Key" $sasKeyForContainer = New-AzStorageContainerSASToken-Name "ContainerName"-uprawnienie "rwdl"-StartTime ([System. DateTime]:: Now). Addminut (-15)-ExpiryTime ([System. DateTime]:: teraz). Addgodzin (5)-Context $storageAccountContext-FullUri Export-AzRedisCache-ResourceGroupName "ResourceGroupName"-name "cacheName"-prefix "blobprefix"-kontener ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="f15ec-113">You can generate a Service SAS URL using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Export-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

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

### <span data-ttu-id="f15ec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f15ec-114">-DefaultProfile</span></span>
<span data-ttu-id="f15ec-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f15ec-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f15ec-116">-Format</span><span class="sxs-lookup"><span data-stu-id="f15ec-116">-Format</span></span>
<span data-ttu-id="f15ec-117">Określa format obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="f15ec-117">Specifies a format for the blob.</span></span>
<span data-ttu-id="f15ec-118">Obecnie RDB jest jedynym obsługiwanym formatem.</span><span class="sxs-lookup"><span data-stu-id="f15ec-118">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="f15ec-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f15ec-119">-Name</span></span>
<span data-ttu-id="f15ec-120">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="f15ec-120">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="f15ec-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f15ec-121">-PassThru</span></span>
<span data-ttu-id="f15ec-122">Wskazuje, że to polecenie cmdlet zwraca wartość logiczną wskazującą, czy operacja kończy się pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="f15ec-122">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="f15ec-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="f15ec-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f15ec-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="f15ec-124">-Prefix</span></span>
<span data-ttu-id="f15ec-125">Określa prefiks, którego należy użyć w przypadku nazw obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="f15ec-125">Specifies a prefix to use for blob names.</span></span>

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

### <span data-ttu-id="f15ec-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f15ec-126">-ResourceGroupName</span></span>
<span data-ttu-id="f15ec-127">Określa nazwę grupy zasobów zawierającej pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="f15ec-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="f15ec-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f15ec-128">-Confirm</span></span>
<span data-ttu-id="f15ec-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f15ec-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f15ec-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f15ec-130">-WhatIf</span></span>
<span data-ttu-id="f15ec-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f15ec-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f15ec-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f15ec-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f15ec-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f15ec-133">CommonParameters</span></span>
<span data-ttu-id="f15ec-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f15ec-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f15ec-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f15ec-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f15ec-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f15ec-136">INPUTS</span></span>

### <span data-ttu-id="f15ec-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f15ec-137">System.String</span></span>

## <span data-ttu-id="f15ec-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f15ec-138">OUTPUTS</span></span>

### <span data-ttu-id="f15ec-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f15ec-139">System.Boolean</span></span>

## <span data-ttu-id="f15ec-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f15ec-140">NOTES</span></span>
* <span data-ttu-id="f15ec-141">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, aplikacji, witryna internetowa</span><span class="sxs-lookup"><span data-stu-id="f15ec-141">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="f15ec-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f15ec-142">RELATED LINKS</span></span>

[<span data-ttu-id="f15ec-143">Import — AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f15ec-143">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="f15ec-144">Nowe — AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f15ec-144">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="f15ec-145">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f15ec-145">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="f15ec-146">Resetowanie — AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f15ec-146">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="f15ec-147">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f15ec-147">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


