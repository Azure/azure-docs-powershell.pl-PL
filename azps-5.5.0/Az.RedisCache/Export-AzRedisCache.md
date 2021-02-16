---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/export-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
ms.openlocfilehash: fb44ca997fd3b7599c25c5ba986ed0ca0771b3e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186562"
---
# <span data-ttu-id="1f41e-101">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1f41e-101">Export-AzRedisCache</span></span>

## <span data-ttu-id="1f41e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f41e-102">SYNOPSIS</span></span>
<span data-ttu-id="1f41e-103">Eksportuje dane z pamięci podręcznej Azure Redis Cache do kontenera.</span><span class="sxs-lookup"><span data-stu-id="1f41e-103">Exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="1f41e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1f41e-104">SYNTAX</span></span>

```
Export-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f41e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1f41e-105">DESCRIPTION</span></span>
<span data-ttu-id="1f41e-106">Polecenie **cmdlet Export-AzRedisCache** eksportuje dane z pamięci podręcznej Azure Redis Cache do kontenera.</span><span class="sxs-lookup"><span data-stu-id="1f41e-106">The **Export-AzRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="1f41e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1f41e-107">EXAMPLES</span></span>

### <span data-ttu-id="1f41e-108">Przykład 1. Eksportowanie danych</span><span class="sxs-lookup"><span data-stu-id="1f41e-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="1f41e-109">To polecenie eksportuje dane z wystąpienia usługi Azure Redis Cache do kontenera określonego przez adres URL SAS.</span><span class="sxs-lookup"><span data-stu-id="1f41e-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="1f41e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f41e-110">PARAMETERS</span></span>

### <span data-ttu-id="1f41e-111">— Kontener</span><span class="sxs-lookup"><span data-stu-id="1f41e-111">-Container</span></span>
<span data-ttu-id="1f41e-112">Określa adres URL SAS usługi kontenera, w którym to polecenie cmdlet eksportuje dane.</span><span class="sxs-lookup"><span data-stu-id="1f41e-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="1f41e-113">Adres URL SAS usługi można wygenerować przy użyciu następujących poleceń programu PowerShell: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now). AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now). AddHours(5) -Context $storageAccountContext -FullUri Export-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="1f41e-113">You can generate a Service SAS URL using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Export-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

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

### <span data-ttu-id="1f41e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f41e-114">-DefaultProfile</span></span>
<span data-ttu-id="1f41e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f41e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f41e-116">— Format</span><span class="sxs-lookup"><span data-stu-id="1f41e-116">-Format</span></span>
<span data-ttu-id="1f41e-117">Określa format obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="1f41e-117">Specifies a format for the blob.</span></span>
<span data-ttu-id="1f41e-118">Obecnie jedynym obsługiwanym formatem jest format rdb.</span><span class="sxs-lookup"><span data-stu-id="1f41e-118">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="1f41e-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1f41e-119">-Name</span></span>
<span data-ttu-id="1f41e-120">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="1f41e-120">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="1f41e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f41e-121">-PassThru</span></span>
<span data-ttu-id="1f41e-122">Wskazuje, że to polecenie cmdlet zwraca wartość logiczną wskazującą, czy operacja zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="1f41e-122">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="1f41e-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="1f41e-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1f41e-124">—Prefiks</span><span class="sxs-lookup"><span data-stu-id="1f41e-124">-Prefix</span></span>
<span data-ttu-id="1f41e-125">Określa prefiks do użycia dla nazw obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="1f41e-125">Specifies a prefix to use for blob names.</span></span>

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

### <span data-ttu-id="1f41e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f41e-126">-ResourceGroupName</span></span>
<span data-ttu-id="1f41e-127">Określa nazwę grupy zasobów, która zawiera pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="1f41e-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="1f41e-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1f41e-128">-Confirm</span></span>
<span data-ttu-id="1f41e-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1f41e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f41e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f41e-130">-WhatIf</span></span>
<span data-ttu-id="1f41e-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f41e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f41e-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1f41e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f41e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f41e-133">CommonParameters</span></span>
<span data-ttu-id="1f41e-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f41e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f41e-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f41e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f41e-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f41e-136">INPUTS</span></span>

### <span data-ttu-id="1f41e-137">System.String</span><span class="sxs-lookup"><span data-stu-id="1f41e-137">System.String</span></span>

## <span data-ttu-id="1f41e-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f41e-138">OUTPUTS</span></span>

### <span data-ttu-id="1f41e-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1f41e-139">System.Boolean</span></span>

## <span data-ttu-id="1f41e-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1f41e-140">NOTES</span></span>
* <span data-ttu-id="1f41e-141">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="1f41e-141">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="1f41e-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f41e-142">RELATED LINKS</span></span>

[<span data-ttu-id="1f41e-143">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1f41e-143">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="1f41e-144">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1f41e-144">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="1f41e-145">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1f41e-145">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="1f41e-146">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1f41e-146">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="1f41e-147">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1f41e-147">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


