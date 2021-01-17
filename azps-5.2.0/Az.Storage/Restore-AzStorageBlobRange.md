---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azstorageblobrange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
ms.openlocfilehash: ee8a8bd6a12d3f4aa1dc1624d0dc5c11de972b11
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348397"
---
# <span data-ttu-id="205ee-101">Restore-AzStorageBlobRange</span><span class="sxs-lookup"><span data-stu-id="205ee-101">Restore-AzStorageBlobRange</span></span>

## <span data-ttu-id="205ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="205ee-102">SYNOPSIS</span></span>
<span data-ttu-id="205ee-103">Przywraca konto magazynu dla określonych zakresów obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="205ee-103">Restores a Storage account for specific blob ranges.</span></span>

## <span data-ttu-id="205ee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="205ee-104">SYNTAX</span></span>

### <span data-ttu-id="205ee-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="205ee-105">AccountName (Default)</span></span>
```
Restore-AzStorageBlobRange [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -TimeToRestore <DateTime> [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="205ee-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="205ee-106">AccountResourceId</span></span>
```
Restore-AzStorageBlobRange [-ResourceId] <String> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="205ee-107">AccountName</span><span class="sxs-lookup"><span data-stu-id="205ee-107">AccountObject</span></span>
```
Restore-AzStorageBlobRange -StorageAccount <PSStorageAccount> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="205ee-108">Opis</span><span class="sxs-lookup"><span data-stu-id="205ee-108">DESCRIPTION</span></span>
<span data-ttu-id="205ee-109">Polecenie cmdlet **Restore-AzStorageBlobRange** przywraca obiekty blob na koncie magazynu dla określonych zakresów BLOB.</span><span class="sxs-lookup"><span data-stu-id="205ee-109">The **Restore-AzStorageBlobRange** cmdlet restores blobs in a Storage account for specific blob ranges.</span></span>
<span data-ttu-id="205ee-110">Zakres początkowy jest dołączany, a zakres końcowy jest wykluczony w funkcji przywracania obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="205ee-110">The start range is included, and the end range is excluded in blob restore.</span></span>

## <span data-ttu-id="205ee-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="205ee-111">EXAMPLES</span></span>

### <span data-ttu-id="205ee-112">Przykład 1. Jeżeli zaczynam przywracać obiekty blob na koncie magazynu z określonymi zakresami BLOB</span><span class="sxs-lookup"><span data-stu-id="205ee-112">Example 1: Start restores blobs in a Storage account with specific blob ranges</span></span>
```powershell
PS C:\> $range1 = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
PS C:\> $range2 = New-AzStorageBlobRangeToRestore -StartRange container3/blob3 -EndRange container4/blob4
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddDays(-1) -BlobRestoreRange $range1,$range2

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                     
------     ---------                            ------------- ------------------------     ---------------------                     
InProgress 6ca55a8b-fca0-461a-8e4c-13927a9707e6               2020-02-10T13:58:44.6841810Z ["container1/blob1" -> "container2/blob2",...]

PS C:\> (Get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName -IncludeBlobRestoreStatus).BlobRestoreStatus 

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                     
------   ---------                            ------------- ------------------------     ---------------------                     
Complete 6ca55a8b-fca0-461a-8e4c-13927a9707e6               2020-02-10T13:58:44.6841810Z ["container1/blob1" -> "container2/blob2",...]
```

<span data-ttu-id="205ee-113">To polecenie najpierw tworzy 2 zakresy obiektów blob, a następnie zaczyna przywracać w ramach konta magazynu obiekty blob z 2 zakresami BLOB (1 dzień temu).</span><span class="sxs-lookup"><span data-stu-id="205ee-113">This command first creates 2 blob ranges, then start restores blobs in a Storage account with the 2 blob ranges from 1 day ago.</span></span> <span data-ttu-id="205ee-114">Użytkownik może użyć Get-AzStorageAccount, aby później śledzić stan przywracania.</span><span class="sxs-lookup"><span data-stu-id="205ee-114">User can use Get-AzStorageAccount to trace the restore status later.</span></span>

### <span data-ttu-id="205ee-115">Przykład 2: przywraca wszystkie obiekty blob na koncie magazynu w wewnętrznej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="205ee-115">Example 2: Restores all blobs in a Storage account in the backend</span></span>
```powershell
PS C:\> $job = Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddMinutes(-30) -WaitForComplete -asjob

PS C:\> $job | Wait-Job

PS C:\> $job.Output

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges
------   ---------                            ------------- ------------------------     ---------------------
Complete 0387953a-bbe6-4602-818d-e661581ee44b               2020-08-28T07:11:33.9843100Z ["" -> ""]
```

<span data-ttu-id="205ee-116">To polecenie przywraca wszystkie obiekty blob na koncie magazynu od 30 minut temu i poczekaj na zakończenie przywracania.</span><span class="sxs-lookup"><span data-stu-id="205ee-116">This command restores all blobs in a Storage account from 30 minutes ago, and wait for the restore complete.</span></span> <span data-ttu-id="205ee-117">Ponieważ polecenie Przywróć obiekty blob może zająć dużo czasu, uruchom je w parametrze wewnętrznej bazy danych with AsJob, a następnie poczekaj na ukończenie zadania i Wyświetl wynik.</span><span class="sxs-lookup"><span data-stu-id="205ee-117">Since restore blobs might take a long time, run it in the backend with -Asjob parameter, and then wait for the job complete and show the result.</span></span>

### <span data-ttu-id="205ee-118">Przykład 3: przywraca obiekty blob bezpośrednio przez wprowadzanie zakresów BLOB i poczekaj na zakończenie</span><span class="sxs-lookup"><span data-stu-id="205ee-118">Example 3: Restores blobs by input blob ranges directly, and wait for complete</span></span>
```powershell
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -WaitForComplete `
    -TimeToRestore (Get-Date).AddSeconds(-1) `
    -BlobRestoreRange @{StartRange="aaa/abc";EndRange="bbb/abc"},@{StartRange="bbb/acc";EndRange=""}
WARNING: Restore blob rang with Id 'd66d1d02-6e48-47ef-b516-0155dd8319c6' started. Restore blob ranges time to complete is dependent on the size of the restore.

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges   
------   ---------                            ------------- ------------------------     ---------------------   
Complete d66d1d02-6e48-47ef-b516-0155dd8319c6               2020-02-10T14:17:46.8189116Z ["aaa/abc" -> "bbb/abc",...]
```

<span data-ttu-id="205ee-119">To polecenie przywraca obiekty blob na koncie magazynu z przedziału od 1 dnia, przez wprowadzanie 2 zakresów obiektów BLOB bezpośrednio do Restore-AzStorageBlobRange polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="205ee-119">This command restores blobs in a Storage account from 1 day ago, by input 2 blob ranges directly to the Restore-AzStorageBlobRange cmdlet.</span></span> <span data-ttu-id="205ee-120">To polecenie będzie oczekiwać na zakończenie przywracania.</span><span class="sxs-lookup"><span data-stu-id="205ee-120">This command will wait for the restore complete.</span></span>

## <span data-ttu-id="205ee-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="205ee-121">PARAMETERS</span></span>

### <span data-ttu-id="205ee-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="205ee-122">-AsJob</span></span>
<span data-ttu-id="205ee-123">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="205ee-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="205ee-124">-BlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="205ee-124">-BlobRestoreRange</span></span>
<span data-ttu-id="205ee-125">Zakres obiektu BLOB do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="205ee-125">The blob range to Restore.</span></span>
<span data-ttu-id="205ee-126">Jeśli nie określono tego parametru, przywróci wszystkie obiekty blob.</span><span class="sxs-lookup"><span data-stu-id="205ee-126">If not specify this parameter, will restore all blobs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205ee-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="205ee-127">-DefaultProfile</span></span>
<span data-ttu-id="205ee-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="205ee-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="205ee-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="205ee-129">-ResourceGroupName</span></span>
<span data-ttu-id="205ee-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="205ee-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="205ee-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="205ee-131">-ResourceId</span></span>
<span data-ttu-id="205ee-132">Identyfikator zasobu konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="205ee-132">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="205ee-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="205ee-133">-StorageAccount</span></span>
<span data-ttu-id="205ee-134">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="205ee-134">Storage account object</span></span>

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

### <span data-ttu-id="205ee-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="205ee-135">-StorageAccountName</span></span>
<span data-ttu-id="205ee-136">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="205ee-136">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205ee-137">-TimeToRestore</span><span class="sxs-lookup"><span data-stu-id="205ee-137">-TimeToRestore</span></span>
<span data-ttu-id="205ee-138">Czas przywracania obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="205ee-138">The Time to Restore Blob.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205ee-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="205ee-139">-WaitForComplete</span></span>
<span data-ttu-id="205ee-140">Zaczekaj na zakończenie zadania przywracania</span><span class="sxs-lookup"><span data-stu-id="205ee-140">Wait for Restore task complete</span></span>

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

### <span data-ttu-id="205ee-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="205ee-141">-Confirm</span></span>
<span data-ttu-id="205ee-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="205ee-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="205ee-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="205ee-143">-WhatIf</span></span>
<span data-ttu-id="205ee-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="205ee-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="205ee-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="205ee-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="205ee-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="205ee-146">CommonParameters</span></span>
<span data-ttu-id="205ee-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="205ee-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="205ee-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="205ee-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="205ee-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="205ee-149">INPUTS</span></span>

### <span data-ttu-id="205ee-150">System. String</span><span class="sxs-lookup"><span data-stu-id="205ee-150">System.String</span></span>

### <span data-ttu-id="205ee-151">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="205ee-151">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="205ee-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="205ee-152">OUTPUTS</span></span>

### <span data-ttu-id="205ee-153">Microsoft. Azure. Commands. Management. Storage. models. PSBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="205ee-153">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreStatus</span></span>

## <span data-ttu-id="205ee-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="205ee-154">NOTES</span></span>

## <span data-ttu-id="205ee-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="205ee-155">RELATED LINKS</span></span>
