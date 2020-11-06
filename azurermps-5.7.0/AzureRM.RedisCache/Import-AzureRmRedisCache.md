---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/import-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
ms.openlocfilehash: ff7ac13080d3d5cb717cf7efbff322cabf83cc3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542391"
---
# <span data-ttu-id="c573e-101">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c573e-101">Import-AzureRmRedisCache</span></span>

## <span data-ttu-id="c573e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c573e-102">SYNOPSIS</span></span>
<span data-ttu-id="c573e-103">Importuje dane z obiektów BLOB do pamięci podręcznej platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="c573e-103">Imports data from blobs to Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c573e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c573e-104">SYNTAX</span></span>

```
Import-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c573e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c573e-105">DESCRIPTION</span></span>
<span data-ttu-id="c573e-106">Polecenie cmdlet **Import-AzureRmRedisCache** importuje dane ze obiektów BLOB do pamięci podręcznej platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="c573e-106">The **Import-AzureRmRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="c573e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c573e-107">EXAMPLES</span></span>

### <span data-ttu-id="c573e-108">Przykład 1. Importowanie danych</span><span class="sxs-lookup"><span data-stu-id="c573e-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="c573e-109">To polecenie importuje dane z obiektu blob określonego przez adres URL SAS do pamięci podręcznej platformy Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="c573e-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="c573e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c573e-110">PARAMETERS</span></span>

### <span data-ttu-id="c573e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c573e-111">-DefaultProfile</span></span>
<span data-ttu-id="c573e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c573e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c573e-113">-Files</span><span class="sxs-lookup"><span data-stu-id="c573e-113">-Files</span></span>
<span data-ttu-id="c573e-114">Określa adresy URL SAS obiektów blob, których zawartość jest importowana do pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="c573e-114">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="c573e-115">Adresy URL SAS można generować za pomocą następujących poleceń programu PowerShell:</span><span class="sxs-lookup"><span data-stu-id="c573e-115">You can generate the SAS URLs using the following PowerShell commands:</span></span>

<span data-ttu-id="c573e-116">$storageAccountContext = New-AzureStorageContext-StorageAccountName "storagename"-StorageAccountKey "Key"</span><span class="sxs-lookup"><span data-stu-id="c573e-116">$storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key"</span></span>

<span data-ttu-id="c573e-117">$sasKeyForBlob = New-AzureStorageBlobSASToken-ContainerName "-BLOB" blobname "-uprawnienie" rwdl "-StartTime ([System. DateTime]:: Now). Addminut (-15)-ExpiryTime ([System. DateTime]:: teraz). Addgodzin (5)-Context $storageAccountContext-FullUri</span><span class="sxs-lookup"><span data-stu-id="c573e-117">$sasKeyForBlob = New-AzureStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri</span></span>

<span data-ttu-id="c573e-118">Import-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-name "cacheName"-Files ($sasKeyForBlob)-Force</span><span class="sxs-lookup"><span data-stu-id="c573e-118">Import-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c573e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c573e-119">-Force</span></span>
<span data-ttu-id="c573e-120">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c573e-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c573e-121">-Format</span><span class="sxs-lookup"><span data-stu-id="c573e-121">-Format</span></span>
<span data-ttu-id="c573e-122">Określa format obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="c573e-122">Specifies the format of the blob.</span></span>
<span data-ttu-id="c573e-123">Obecnie RDB jest jedynym obsługiwanym formatem.</span><span class="sxs-lookup"><span data-stu-id="c573e-123">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="c573e-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c573e-124">-Name</span></span>
<span data-ttu-id="c573e-125">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="c573e-125">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="c573e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c573e-126">-PassThru</span></span>
<span data-ttu-id="c573e-127">Wskazuje, że to polecenie cmdlet zwraca wartość logiczną wskazującą, czy operacja kończy się pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="c573e-127">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="c573e-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="c573e-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c573e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c573e-129">-ResourceGroupName</span></span>
<span data-ttu-id="c573e-130">Określa nazwę grupy zasobów zawierającej pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="c573e-130">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="c573e-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c573e-131">-Confirm</span></span>
<span data-ttu-id="c573e-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c573e-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c573e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c573e-133">-WhatIf</span></span>
<span data-ttu-id="c573e-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c573e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c573e-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c573e-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c573e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c573e-136">CommonParameters</span></span>
<span data-ttu-id="c573e-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c573e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c573e-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c573e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c573e-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c573e-139">INPUTS</span></span>

### <span data-ttu-id="c573e-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c573e-140">None</span></span>
<span data-ttu-id="c573e-141">Możesz popotokować dane wejściowe tego polecenia cmdlet, korzystając z nazwy właściwości, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="c573e-141">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="c573e-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c573e-142">OUTPUTS</span></span>

### <span data-ttu-id="c573e-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c573e-143">None</span></span>

## <span data-ttu-id="c573e-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c573e-144">NOTES</span></span>
* <span data-ttu-id="c573e-145">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, aplikacji, witryna internetowa</span><span class="sxs-lookup"><span data-stu-id="c573e-145">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="c573e-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c573e-146">RELATED LINKS</span></span>

[<span data-ttu-id="c573e-147">Eksportowanie — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c573e-147">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="c573e-148">Nowe — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c573e-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="c573e-149">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c573e-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="c573e-150">Resetowanie — AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c573e-150">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="c573e-151">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c573e-151">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


