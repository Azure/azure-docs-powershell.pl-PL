---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/import-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
ms.openlocfilehash: 1f51f156a0f45b014e9ff521adb959bdbd86bef7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183810"
---
# <span data-ttu-id="0077e-101">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="0077e-101">Import-AzRedisCache</span></span>

## <span data-ttu-id="0077e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0077e-102">SYNOPSIS</span></span>
<span data-ttu-id="0077e-103">Importuje dane z obiektów blob do usługi Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="0077e-103">Imports data from blobs to Azure Redis Cache.</span></span>

## <span data-ttu-id="0077e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0077e-104">SYNTAX</span></span>

```
Import-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0077e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0077e-105">DESCRIPTION</span></span>
<span data-ttu-id="0077e-106">Polecenie **cmdlet Import-AzRedisCache** importuje dane z obiektów blob do usługi Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="0077e-106">The **Import-AzRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="0077e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0077e-107">EXAMPLES</span></span>

### <span data-ttu-id="0077e-108">Przykład 1. Importowanie danych</span><span class="sxs-lookup"><span data-stu-id="0077e-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="0077e-109">To polecenie importuje dane z obiektu blob określonego przez adres URL SAS do usługi Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="0077e-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="0077e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0077e-110">PARAMETERS</span></span>

### <span data-ttu-id="0077e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0077e-111">-DefaultProfile</span></span>
<span data-ttu-id="0077e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0077e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0077e-113">— Pliki</span><span class="sxs-lookup"><span data-stu-id="0077e-113">-Files</span></span>
<span data-ttu-id="0077e-114">Określa adresy URL SAS obiektów blob, których zawartość jest importowana do pamięci podręcznej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0077e-114">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="0077e-115">Adresy URL SAS można wygenerować przy użyciu następujących poleceń programu PowerShell: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now). AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now). AddHours(5) -Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span><span class="sxs-lookup"><span data-stu-id="0077e-115">You can generate the SAS URLs using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

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

### <span data-ttu-id="0077e-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="0077e-116">-Force</span></span>
<span data-ttu-id="0077e-117">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0077e-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0077e-118">— Format</span><span class="sxs-lookup"><span data-stu-id="0077e-118">-Format</span></span>
<span data-ttu-id="0077e-119">Określa format obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="0077e-119">Specifies the format of the blob.</span></span>
<span data-ttu-id="0077e-120">Obecnie jedynym obsługiwanym formatem jest format rdb.</span><span class="sxs-lookup"><span data-stu-id="0077e-120">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="0077e-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0077e-121">-Name</span></span>
<span data-ttu-id="0077e-122">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="0077e-122">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="0077e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0077e-123">-PassThru</span></span>
<span data-ttu-id="0077e-124">Wskazuje, że to polecenie cmdlet zwraca wartość logiczną wskazującą, czy operacja zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="0077e-124">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="0077e-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="0077e-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0077e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0077e-126">-ResourceGroupName</span></span>
<span data-ttu-id="0077e-127">Określa nazwę grupy zasobów, która zawiera pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="0077e-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="0077e-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0077e-128">-Confirm</span></span>
<span data-ttu-id="0077e-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0077e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0077e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0077e-130">-WhatIf</span></span>
<span data-ttu-id="0077e-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0077e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0077e-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0077e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0077e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0077e-133">CommonParameters</span></span>
<span data-ttu-id="0077e-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0077e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0077e-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0077e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0077e-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0077e-136">INPUTS</span></span>

### <span data-ttu-id="0077e-137">System.String</span><span class="sxs-lookup"><span data-stu-id="0077e-137">System.String</span></span>

### <span data-ttu-id="0077e-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="0077e-138">System.String[]</span></span>

## <span data-ttu-id="0077e-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0077e-139">OUTPUTS</span></span>

### <span data-ttu-id="0077e-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0077e-140">System.Boolean</span></span>

## <span data-ttu-id="0077e-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0077e-141">NOTES</span></span>
* <span data-ttu-id="0077e-142">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="0077e-142">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="0077e-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0077e-143">RELATED LINKS</span></span>

[<span data-ttu-id="0077e-144">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="0077e-144">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="0077e-145">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="0077e-145">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="0077e-146">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="0077e-146">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="0077e-147">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="0077e-147">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="0077e-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="0077e-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


