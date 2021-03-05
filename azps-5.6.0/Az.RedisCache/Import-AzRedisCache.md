---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/powershell/module/az.rediscache/import-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
ms.openlocfilehash: 34ea5ccc662514b3a2807924c932fb2e11b5b214
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000945"
---
# <span data-ttu-id="bab6a-101">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bab6a-101">Import-AzRedisCache</span></span>

## <span data-ttu-id="bab6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bab6a-102">SYNOPSIS</span></span>
<span data-ttu-id="bab6a-103">Importuje dane z obiektów blob do usługi Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="bab6a-103">Imports data from blobs to Azure Redis Cache.</span></span>

## <span data-ttu-id="bab6a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bab6a-104">SYNTAX</span></span>

```
Import-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bab6a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bab6a-105">DESCRIPTION</span></span>
<span data-ttu-id="bab6a-106">Polecenie **cmdlet Import-AzRedisCache** importuje dane z obiektów blob do usługi Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="bab6a-106">The **Import-AzRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="bab6a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bab6a-107">EXAMPLES</span></span>

### <span data-ttu-id="bab6a-108">Przykład 1. Importowanie danych</span><span class="sxs-lookup"><span data-stu-id="bab6a-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="bab6a-109">To polecenie importuje dane z obiektu blob określonego przez adres URL SAS do usługi Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="bab6a-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="bab6a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bab6a-110">PARAMETERS</span></span>

### <span data-ttu-id="bab6a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bab6a-111">-DefaultProfile</span></span>
<span data-ttu-id="bab6a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bab6a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bab6a-113">— Pliki</span><span class="sxs-lookup"><span data-stu-id="bab6a-113">-Files</span></span>
<span data-ttu-id="bab6a-114">Określa adresy URL SAS obiektów blob, których zawartość jest importowana do pamięci podręcznej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bab6a-114">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="bab6a-115">Adresy URL SAS można wygenerować przy użyciu następujących poleceń programu PowerShell: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now). AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now). AddHours(5) - Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span><span class="sxs-lookup"><span data-stu-id="bab6a-115">You can generate the SAS URLs using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bab6a-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="bab6a-116">-Force</span></span>
<span data-ttu-id="bab6a-117">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bab6a-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bab6a-118">— Format</span><span class="sxs-lookup"><span data-stu-id="bab6a-118">-Format</span></span>
<span data-ttu-id="bab6a-119">Określa format obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="bab6a-119">Specifies the format of the blob.</span></span>
<span data-ttu-id="bab6a-120">Obecnie jedynym obsługiwanym formatem jest format rdb.</span><span class="sxs-lookup"><span data-stu-id="bab6a-120">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="bab6a-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bab6a-121">-Name</span></span>
<span data-ttu-id="bab6a-122">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="bab6a-122">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="bab6a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bab6a-123">-PassThru</span></span>
<span data-ttu-id="bab6a-124">Wskazuje, że to polecenie cmdlet zwraca wartość logiczną wskazującą, czy operacja zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="bab6a-124">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="bab6a-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="bab6a-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bab6a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bab6a-126">-ResourceGroupName</span></span>
<span data-ttu-id="bab6a-127">Określa nazwę grupy zasobów, która zawiera pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="bab6a-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="bab6a-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bab6a-128">-Confirm</span></span>
<span data-ttu-id="bab6a-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bab6a-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bab6a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bab6a-130">-WhatIf</span></span>
<span data-ttu-id="bab6a-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bab6a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bab6a-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bab6a-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bab6a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bab6a-133">CommonParameters</span></span>
<span data-ttu-id="bab6a-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bab6a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bab6a-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bab6a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bab6a-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bab6a-136">INPUTS</span></span>

### <span data-ttu-id="bab6a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="bab6a-137">System.String</span></span>

### <span data-ttu-id="bab6a-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="bab6a-138">System.String[]</span></span>

## <span data-ttu-id="bab6a-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bab6a-139">OUTPUTS</span></span>

### <span data-ttu-id="bab6a-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bab6a-140">System.Boolean</span></span>

## <span data-ttu-id="bab6a-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bab6a-141">NOTES</span></span>
* <span data-ttu-id="bab6a-142">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="bab6a-142">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="bab6a-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bab6a-143">RELATED LINKS</span></span>

[<span data-ttu-id="bab6a-144">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bab6a-144">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="bab6a-145">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bab6a-145">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="bab6a-146">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bab6a-146">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="bab6a-147">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bab6a-147">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="bab6a-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bab6a-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


