---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/enable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: cd3a8b12b6dbd6aec6dbc157aa3ff4d4ce398002
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973345"
---
# <span data-ttu-id="51907-101">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="51907-101">Enable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="51907-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51907-102">SYNOPSIS</span></span>
<span data-ttu-id="51907-103">Włącza zasady przywracania obiektów blob na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="51907-103">Enables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="51907-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="51907-104">SYNTAX</span></span>

### <span data-ttu-id="51907-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="51907-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RestoreDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51907-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="51907-106">AccountObject</span></span>
```
Enable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51907-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="51907-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceId] <String> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51907-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="51907-108">DESCRIPTION</span></span>
<span data-ttu-id="51907-109">Polecenie **cmdlet Enable-azStorageBlobRestorePolicy** włącza zasady przywracania obiektów blob dla usługi obiektów blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="51907-109">The **Enable-AzStorageBlobRestorePolicy** cmdlet enables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="51907-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="51907-110">EXAMPLES</span></span>

### <span data-ttu-id="51907-111">Przykład 1. Włączenie zasad przywracania obiektów blob dla usługi obiektów blob magazynu platformy Azure na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="51907-111">Example 1: Enables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" $accountName -RetentionDays 5

PS C:\> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -EnableChangeFeed $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegoup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : True
DeleteRetentionPolicy.Days    : 5
RestorePolicy.Enabled         : False
RestorePolicy.Days            : 
RestorePolicy.MinRestoreTime  : 
ChangeFeed                    : True
IsVersioningEnabled           : True

PS C:\> Enable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -RestoreDays 4

PS C:\> Get-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegoup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : True
DeleteRetentionPolicy.Days    : 5
RestorePolicy.Enabled         : True
RestorePolicy.Days            : 4
RestorePolicy.MinRestoreTime  : 8/28/2020 6:00:59 AM
ChangeFeed                    : True
IsVersioningEnabled           : True
```

<span data-ttu-id="51907-112">To polecenie najpierw włącza właściwości softdelete i changefeed obiektów blob, a następnie włącza zasady przywracania obiektów blob, a na koniec sprawdza ustawienie we właściwościach usługi obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="51907-112">This command first enable Blob softdelete and changefeed, then enables Blob Restore Policy, finally check the setting in Blob service properties.</span></span>
<span data-ttu-id="51907-113">The Blob service RestorePolicy.Days must be smaller than DeleteRetentionPolicy.Days.</span><span class="sxs-lookup"><span data-stu-id="51907-113">The Blob service RestorePolicy.Days must be smaller than DeleteRetentionPolicy.Days.</span></span>
<span data-ttu-id="51907-114">Przed włączeniem zasad przywracania obiektów blob należy włączyć program Softdelete i ChangeFeed.</span><span class="sxs-lookup"><span data-stu-id="51907-114">Blob softdelete and ChangeFeed must be enabled before enable blob Restore Policy.</span></span>
<span data-ttu-id="51907-115">Jeśli ustawienia softdelete i Changefeed są właśnie włączone, może być konieczne zaczekanie przez pewien czas na obsługę ustawienia przez serwer, zanim zasady przywracania obiektów blob zostaną włączone.</span><span class="sxs-lookup"><span data-stu-id="51907-115">If softdelete and Changefeed are just enabled, might need wait for some time for server to handle the setting, before enable Blob restore policy.</span></span>

## <span data-ttu-id="51907-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51907-116">PARAMETERS</span></span>

### <span data-ttu-id="51907-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51907-117">-DefaultProfile</span></span>
<span data-ttu-id="51907-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="51907-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51907-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51907-119">-PassThru</span></span>
<span data-ttu-id="51907-120">Wyświetl właściwości usługi</span><span class="sxs-lookup"><span data-stu-id="51907-120">Display ServiceProperties</span></span>

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

### <span data-ttu-id="51907-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51907-121">-ResourceGroupName</span></span>
<span data-ttu-id="51907-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="51907-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51907-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51907-123">-ResourceId</span></span>
<span data-ttu-id="51907-124">Wprowadź identyfikator zasobu konta magazynu lub identyfikator zasobu właściwości usługi obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="51907-124">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51907-125">-RestoreDays</span><span class="sxs-lookup"><span data-stu-id="51907-125">-RestoreDays</span></span>
<span data-ttu-id="51907-126">Ustawia liczbę dni, przez które można przywrócić obiekt blob.</span><span class="sxs-lookup"><span data-stu-id="51907-126">Sets the number of days for the blob can be restored..</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51907-127">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="51907-127">-StorageAccount</span></span>
<span data-ttu-id="51907-128">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="51907-128">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51907-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="51907-129">-StorageAccountName</span></span>
<span data-ttu-id="51907-130">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="51907-130">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51907-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="51907-131">-Confirm</span></span>
<span data-ttu-id="51907-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="51907-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51907-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51907-133">-WhatIf</span></span>
<span data-ttu-id="51907-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51907-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51907-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="51907-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51907-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51907-136">CommonParameters</span></span>
<span data-ttu-id="51907-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51907-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51907-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51907-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51907-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51907-139">INPUTS</span></span>

### <span data-ttu-id="51907-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="51907-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="51907-141">System.String</span><span class="sxs-lookup"><span data-stu-id="51907-141">System.String</span></span>

## <span data-ttu-id="51907-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51907-142">OUTPUTS</span></span>

### <span data-ttu-id="51907-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="51907-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="51907-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="51907-144">NOTES</span></span>

## <span data-ttu-id="51907-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51907-145">RELATED LINKS</span></span>
