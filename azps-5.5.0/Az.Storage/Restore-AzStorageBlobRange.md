---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azstorageblobrange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
ms.openlocfilehash: ee8a8bd6a12d3f4aa1dc1624d0dc5c11de972b11
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190730"
---
# <span data-ttu-id="62978-101">Restore-AzStorageBlobRange</span><span class="sxs-lookup"><span data-stu-id="62978-101">Restore-AzStorageBlobRange</span></span>

## <span data-ttu-id="62978-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62978-102">SYNOPSIS</span></span>
<span data-ttu-id="62978-103">Przywraca konto magazynu dla określonych zakresów obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="62978-103">Restores a Storage account for specific blob ranges.</span></span>

## <span data-ttu-id="62978-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="62978-104">SYNTAX</span></span>

### <span data-ttu-id="62978-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="62978-105">AccountName (Default)</span></span>
```
Restore-AzStorageBlobRange [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -TimeToRestore <DateTime> [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62978-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="62978-106">AccountResourceId</span></span>
```
Restore-AzStorageBlobRange [-ResourceId] <String> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62978-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="62978-107">AccountObject</span></span>
```
Restore-AzStorageBlobRange -StorageAccount <PSStorageAccount> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62978-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="62978-108">DESCRIPTION</span></span>
<span data-ttu-id="62978-109">Polecenie **cmdlet Restore-AzStorageBlobRange** przywraca obiekty blob na koncie magazynu dla określonych zakresów obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="62978-109">The **Restore-AzStorageBlobRange** cmdlet restores blobs in a Storage account for specific blob ranges.</span></span>
<span data-ttu-id="62978-110">Zakres rozpoczęcia zostanie uwzględniony, a zakres końcowy zostanie wykluczony podczas przywracania obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="62978-110">The start range is included, and the end range is excluded in blob restore.</span></span>

## <span data-ttu-id="62978-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="62978-111">EXAMPLES</span></span>

### <span data-ttu-id="62978-112">Przykład 1. Rozpoczęcie przywracania obiektów blob na koncie magazynu z określonymi zakresami obiektów blob</span><span class="sxs-lookup"><span data-stu-id="62978-112">Example 1: Start restores blobs in a Storage account with specific blob ranges</span></span>
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

<span data-ttu-id="62978-113">To polecenie najpierw tworzy 2 zakresy obiektów blob, a następnie rozpoczyna przywracanie obiektów blob na koncie magazynu z 2 zakresami obiektów blob z 1 dnia temu.</span><span class="sxs-lookup"><span data-stu-id="62978-113">This command first creates 2 blob ranges, then start restores blobs in a Storage account with the 2 blob ranges from 1 day ago.</span></span> <span data-ttu-id="62978-114">Użytkownik może później użyć Get-AzStorageAccount, aby prześledzić stan przywracania.</span><span class="sxs-lookup"><span data-stu-id="62978-114">User can use Get-AzStorageAccount to trace the restore status later.</span></span>

### <span data-ttu-id="62978-115">Przykład 2. Przywracanie wszystkich obiektów blob na koncie magazynu w zaplecza</span><span class="sxs-lookup"><span data-stu-id="62978-115">Example 2: Restores all blobs in a Storage account in the backend</span></span>
```powershell
PS C:\> $job = Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddMinutes(-30) -WaitForComplete -asjob

PS C:\> $job | Wait-Job

PS C:\> $job.Output

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges
------   ---------                            ------------- ------------------------     ---------------------
Complete 0387953a-bbe6-4602-818d-e661581ee44b               2020-08-28T07:11:33.9843100Z ["" -> ""]
```

<span data-ttu-id="62978-116">To polecenie przywraca wszystkie obiekty blob na koncie magazynu z 30 minut temu i czeka na ukończenie przywracania.</span><span class="sxs-lookup"><span data-stu-id="62978-116">This command restores all blobs in a Storage account from 30 minutes ago, and wait for the restore complete.</span></span> <span data-ttu-id="62978-117">Ponieważ przywracanie obiektów blob może zająć dużo czasu, należy uruchomić ją w zaplecza z parametrem -Asjob, a następnie zaczekać na ukończenie zadania i wyświetlić wynik.</span><span class="sxs-lookup"><span data-stu-id="62978-117">Since restore blobs might take a long time, run it in the backend with -Asjob parameter, and then wait for the job complete and show the result.</span></span>

### <span data-ttu-id="62978-118">Przykład 3. Przywracanie obiektów blob przez zakresy wejściowych obiektów blob bezpośrednio i oczekiwanie na ukończenie</span><span class="sxs-lookup"><span data-stu-id="62978-118">Example 3: Restores blobs by input blob ranges directly, and wait for complete</span></span>
```powershell
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -WaitForComplete `
    -TimeToRestore (Get-Date).AddSeconds(-1) `
    -BlobRestoreRange @{StartRange="aaa/abc";EndRange="bbb/abc"},@{StartRange="bbb/acc";EndRange=""}
WARNING: Restore blob rang with Id 'd66d1d02-6e48-47ef-b516-0155dd8319c6' started. Restore blob ranges time to complete is dependent on the size of the restore.

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges   
------   ---------                            ------------- ------------------------     ---------------------   
Complete d66d1d02-6e48-47ef-b516-0155dd8319c6               2020-02-10T14:17:46.8189116Z ["aaa/abc" -> "bbb/abc",...]
```

<span data-ttu-id="62978-119">To polecenie przywraca obiekty blob na koncie magazynu z 1 dnia temu przez wprowadzenie 2 zakresów obiektów blob bezpośrednio do Restore-AzStorageBlobRange cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62978-119">This command restores blobs in a Storage account from 1 day ago, by input 2 blob ranges directly to the Restore-AzStorageBlobRange cmdlet.</span></span> <span data-ttu-id="62978-120">To polecenie będzie czekać na ukończenie przywracania.</span><span class="sxs-lookup"><span data-stu-id="62978-120">This command will wait for the restore complete.</span></span>

## <span data-ttu-id="62978-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62978-121">PARAMETERS</span></span>

### <span data-ttu-id="62978-122">— AsJob</span><span class="sxs-lookup"><span data-stu-id="62978-122">-AsJob</span></span>
<span data-ttu-id="62978-123">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="62978-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62978-124">-BlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="62978-124">-BlobRestoreRange</span></span>
<span data-ttu-id="62978-125">Zakres obiektów blob do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="62978-125">The blob range to Restore.</span></span>
<span data-ttu-id="62978-126">Jeśli nie określisz tego parametru, przywróci wszystkie obiekty blob.</span><span class="sxs-lookup"><span data-stu-id="62978-126">If not specify this parameter, will restore all blobs.</span></span>

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

### <span data-ttu-id="62978-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62978-127">-DefaultProfile</span></span>
<span data-ttu-id="62978-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="62978-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62978-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62978-129">-ResourceGroupName</span></span>
<span data-ttu-id="62978-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="62978-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="62978-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62978-131">-ResourceId</span></span>
<span data-ttu-id="62978-132">Identyfikator zasobu konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="62978-132">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="62978-133">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="62978-133">-StorageAccount</span></span>
<span data-ttu-id="62978-134">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="62978-134">Storage account object</span></span>

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

### <span data-ttu-id="62978-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="62978-135">-StorageAccountName</span></span>
<span data-ttu-id="62978-136">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="62978-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="62978-137">-TimeToRestore</span><span class="sxs-lookup"><span data-stu-id="62978-137">-TimeToRestore</span></span>
<span data-ttu-id="62978-138">Czas na przywrócenie obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="62978-138">The Time to Restore Blob.</span></span>

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

### <span data-ttu-id="62978-139">- WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="62978-139">-WaitForComplete</span></span>
<span data-ttu-id="62978-140">Oczekiwanie na ukończenie zadania przywracania</span><span class="sxs-lookup"><span data-stu-id="62978-140">Wait for Restore task complete</span></span>

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

### <span data-ttu-id="62978-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="62978-141">-Confirm</span></span>
<span data-ttu-id="62978-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="62978-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62978-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62978-143">-WhatIf</span></span>
<span data-ttu-id="62978-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62978-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62978-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="62978-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62978-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62978-146">CommonParameters</span></span>
<span data-ttu-id="62978-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62978-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62978-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62978-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62978-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62978-149">INPUTS</span></span>

### <span data-ttu-id="62978-150">System.String</span><span class="sxs-lookup"><span data-stu-id="62978-150">System.String</span></span>

### <span data-ttu-id="62978-151">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="62978-151">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="62978-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62978-152">OUTPUTS</span></span>

### <span data-ttu-id="62978-153">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="62978-153">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreStatus</span></span>

## <span data-ttu-id="62978-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="62978-154">NOTES</span></span>

## <span data-ttu-id="62978-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62978-155">RELATED LINKS</span></span>
