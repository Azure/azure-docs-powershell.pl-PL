---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/powershell/module/az.rediscache/export-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
ms.openlocfilehash: 664ee6dcefde0890244e390f0e828bad57f532d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985685"
---
# <span data-ttu-id="418cd-101">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="418cd-101">Export-AzRedisCache</span></span>

## <span data-ttu-id="418cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="418cd-102">SYNOPSIS</span></span>
<span data-ttu-id="418cd-103">Eksportuje dane z pamięci podręcznej Azure Redis Cache do kontenera.</span><span class="sxs-lookup"><span data-stu-id="418cd-103">Exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="418cd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="418cd-104">SYNTAX</span></span>

```
Export-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="418cd-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="418cd-105">DESCRIPTION</span></span>
<span data-ttu-id="418cd-106">Polecenie **cmdlet Export-AzRedisCache** eksportuje dane z pamięci podręcznej Azure Redis Cache do kontenera.</span><span class="sxs-lookup"><span data-stu-id="418cd-106">The **Export-AzRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="418cd-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="418cd-107">EXAMPLES</span></span>

### <span data-ttu-id="418cd-108">Przykład 1. Eksportowanie danych</span><span class="sxs-lookup"><span data-stu-id="418cd-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="418cd-109">To polecenie eksportuje dane z wystąpienia usługi Azure Redis Cache do kontenera określonego przez adres URL SAS.</span><span class="sxs-lookup"><span data-stu-id="418cd-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="418cd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="418cd-110">PARAMETERS</span></span>

### <span data-ttu-id="418cd-111">— Kontener</span><span class="sxs-lookup"><span data-stu-id="418cd-111">-Container</span></span>
<span data-ttu-id="418cd-112">Określa adres URL SAS usługi kontenera, w którym to polecenie cmdlet eksportuje dane.</span><span class="sxs-lookup"><span data-stu-id="418cd-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="418cd-113">Adres URL SAS usługi można wygenerować przy użyciu następujących poleceń programu PowerShell: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now). AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now). AddHours(5) -Context $storageAccountContext -FullUri Export-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="418cd-113">You can generate a Service SAS URL using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Export-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

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

### <span data-ttu-id="418cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="418cd-114">-DefaultProfile</span></span>
<span data-ttu-id="418cd-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="418cd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="418cd-116">— Format</span><span class="sxs-lookup"><span data-stu-id="418cd-116">-Format</span></span>
<span data-ttu-id="418cd-117">Określa format obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="418cd-117">Specifies a format for the blob.</span></span>
<span data-ttu-id="418cd-118">Obecnie jedynym obsługiwanym formatem jest format rdb.</span><span class="sxs-lookup"><span data-stu-id="418cd-118">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="418cd-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="418cd-119">-Name</span></span>
<span data-ttu-id="418cd-120">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="418cd-120">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="418cd-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="418cd-121">-PassThru</span></span>
<span data-ttu-id="418cd-122">Wskazuje, że to polecenie cmdlet zwraca wartość logiczną wskazującą, czy operacja zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="418cd-122">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="418cd-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="418cd-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="418cd-124">—Prefiks</span><span class="sxs-lookup"><span data-stu-id="418cd-124">-Prefix</span></span>
<span data-ttu-id="418cd-125">Określa prefiks do użycia dla nazw obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="418cd-125">Specifies a prefix to use for blob names.</span></span>

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

### <span data-ttu-id="418cd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="418cd-126">-ResourceGroupName</span></span>
<span data-ttu-id="418cd-127">Określa nazwę grupy zasobów, która zawiera pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="418cd-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="418cd-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="418cd-128">-Confirm</span></span>
<span data-ttu-id="418cd-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="418cd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="418cd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="418cd-130">-WhatIf</span></span>
<span data-ttu-id="418cd-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="418cd-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="418cd-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="418cd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="418cd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="418cd-133">CommonParameters</span></span>
<span data-ttu-id="418cd-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="418cd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="418cd-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="418cd-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="418cd-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="418cd-136">INPUTS</span></span>

### <span data-ttu-id="418cd-137">System.String</span><span class="sxs-lookup"><span data-stu-id="418cd-137">System.String</span></span>

## <span data-ttu-id="418cd-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="418cd-138">OUTPUTS</span></span>

### <span data-ttu-id="418cd-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="418cd-139">System.Boolean</span></span>

## <span data-ttu-id="418cd-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="418cd-140">NOTES</span></span>
* <span data-ttu-id="418cd-141">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="418cd-141">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="418cd-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="418cd-142">RELATED LINKS</span></span>

[<span data-ttu-id="418cd-143">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="418cd-143">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="418cd-144">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="418cd-144">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="418cd-145">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="418cd-145">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="418cd-146">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="418cd-146">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="418cd-147">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="418cd-147">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


