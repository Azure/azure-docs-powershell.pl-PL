---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: a5b5b1c761bb6e3c23a5dd5f0525d2d6627b3ab2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376350"
---
# <span data-ttu-id="f7bcc-101">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="f7bcc-101">Enable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="f7bcc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7bcc-102">SYNOPSIS</span></span>
<span data-ttu-id="f7bcc-103">Umożliwia włączanie zasad przywracania obiektu BLOB na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="f7bcc-103">Enables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="f7bcc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7bcc-104">SYNTAX</span></span>

### <span data-ttu-id="f7bcc-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f7bcc-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RestoreDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7bcc-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="f7bcc-106">AccountObject</span></span>
```
Enable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7bcc-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="f7bcc-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceId] <String> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7bcc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f7bcc-108">DESCRIPTION</span></span>
<span data-ttu-id="f7bcc-109">Polecenie cmdlet **enable-AzStorageBlobRestorePolicy** włącza zasady przywracania obiektów BLOB dla usługi Azure Storage BLOB.</span><span class="sxs-lookup"><span data-stu-id="f7bcc-109">The **Enable-AzStorageBlobRestorePolicy** cmdlet enables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="f7bcc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7bcc-110">EXAMPLES</span></span>

### <span data-ttu-id="f7bcc-111">Przykład 1: włączenie zasad przywracania obiektu BLOB dla usługi blob magazynu Azure na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="f7bcc-111">Example 1: Enables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
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

<span data-ttu-id="f7bcc-112">To polecenie najpierw włącz funkcję BLOB softdelete i changefeed, a następnie Włącz zasady przywracania obiektu BLOB, a wreszcie Sprawdź ustawienia w obszarze właściwości usługi BLOB.</span><span class="sxs-lookup"><span data-stu-id="f7bcc-112">This command first enable Blob softdelete and changefeed, then enables Blob Restore Policy, finally check the setting in Blob service properties.</span></span>
<span data-ttu-id="f7bcc-113">Usługa BLOB Service RestorePolicy. dni musi być mniejsza niż DeleteRetentionPolicy. dni.</span><span class="sxs-lookup"><span data-stu-id="f7bcc-113">The Blob service RestorePolicy.Days must be smaller than DeleteRetentionPolicy.Days.</span></span>
<span data-ttu-id="f7bcc-114">Przed włączeniem zasad przywracania obiektu BLOB muszą być włączone softdelete, a ChangeFeed.</span><span class="sxs-lookup"><span data-stu-id="f7bcc-114">Blob softdelete and ChangeFeed must be enabled before enable blob Restore Policy.</span></span>
<span data-ttu-id="f7bcc-115">Jeśli softdelete i Changefeed są po prostu włączone, może być konieczne odczekanie czasu, zanim serwer przeprowadzi to ustawienie, przed włączeniem zasad przywracania obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="f7bcc-115">If softdelete and Changefeed are just enabled, might need wait for some time for server to handle the setting, before enable Blob restore policy.</span></span>

## <span data-ttu-id="f7bcc-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7bcc-116">PARAMETERS</span></span>

### <span data-ttu-id="f7bcc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7bcc-117">-DefaultProfile</span></span>
<span data-ttu-id="f7bcc-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7bcc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7bcc-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7bcc-119">-PassThru</span></span>
<span data-ttu-id="f7bcc-120">Wyświetlanie właściwości serviceproperties</span><span class="sxs-lookup"><span data-stu-id="f7bcc-120">Display ServiceProperties</span></span>

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

### <span data-ttu-id="f7bcc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7bcc-121">-ResourceGroupName</span></span>
<span data-ttu-id="f7bcc-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f7bcc-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="f7bcc-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7bcc-123">-ResourceId</span></span>
<span data-ttu-id="f7bcc-124">Wprowadź identyfikator zasobu konta magazynu lub identyfikator zasobu właściwości usługi obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="f7bcc-124">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="f7bcc-125">-RestoreDays</span><span class="sxs-lookup"><span data-stu-id="f7bcc-125">-RestoreDays</span></span>
<span data-ttu-id="f7bcc-126">Umożliwia ustawienie liczby dni, w ciągu których obiekt BLOB może zostać przywrócony...</span><span class="sxs-lookup"><span data-stu-id="f7bcc-126">Sets the number of days for the blob can be restored..</span></span>

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

### <span data-ttu-id="f7bcc-127">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7bcc-127">-StorageAccount</span></span>
<span data-ttu-id="f7bcc-128">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="f7bcc-128">Storage account object</span></span>

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

### <span data-ttu-id="f7bcc-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f7bcc-129">-StorageAccountName</span></span>
<span data-ttu-id="f7bcc-130">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="f7bcc-130">Storage Account Name.</span></span>

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

### <span data-ttu-id="f7bcc-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f7bcc-131">-Confirm</span></span>
<span data-ttu-id="f7bcc-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7bcc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7bcc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7bcc-133">-WhatIf</span></span>
<span data-ttu-id="f7bcc-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7bcc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7bcc-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f7bcc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7bcc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7bcc-136">CommonParameters</span></span>
<span data-ttu-id="f7bcc-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7bcc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7bcc-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7bcc-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7bcc-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7bcc-139">INPUTS</span></span>

### <span data-ttu-id="f7bcc-140">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7bcc-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="f7bcc-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f7bcc-141">System.String</span></span>

## <span data-ttu-id="f7bcc-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7bcc-142">OUTPUTS</span></span>

### <span data-ttu-id="f7bcc-143">Microsoft. Azure. Commands. Management. Storage. models. PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="f7bcc-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="f7bcc-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7bcc-144">NOTES</span></span>

## <span data-ttu-id="f7bcc-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7bcc-145">RELATED LINKS</span></span>
