---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: 80b1816dff686db7e84bf876fd74f9642389b42f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232930"
---
# <span data-ttu-id="c148d-101">Update-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="c148d-101">Update-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="c148d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c148d-102">SYNOPSIS</span></span>
<span data-ttu-id="c148d-103">Aktualizuj listę ACL rekursywnie w określonej ścieżce.</span><span class="sxs-lookup"><span data-stu-id="c148d-103">Update ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="c148d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c148d-104">SYNTAX</span></span>

```
Update-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c148d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c148d-105">DESCRIPTION</span></span>
<span data-ttu-id="c148d-106">Polecenie cmdlet **Update-AzDataLakeGen2AclRecursive** umożliwia cykliczne aktualizowanie listy ACL w określonej ścieżce.</span><span class="sxs-lookup"><span data-stu-id="c148d-106">The **Update-AzDataLakeGen2AclRecursive** cmdlet updates ACL recursively on the specified path.</span></span> <span data-ttu-id="c148d-107">Wejściowa lista ACL zostanie scalona z pierwotną LISTą ACL: Jeśli wpis ACL ma taką samą AccessControlType/EntityId/DefaultScope, uprawnienie "Aktualizowanie"; w innym przypadku Dodaj nowy wpis listy ACL.</span><span class="sxs-lookup"><span data-stu-id="c148d-107">The input ACL will merge the the original ACL: If ACL entry with same AccessControlType/EntityId/DefaultScope exist, update permission; else add a new ACL entry.</span></span>

## <span data-ttu-id="c148d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c148d-108">EXAMPLES</span></span>

### <span data-ttu-id="c148d-109">Przykład 1: aktualizowanie listy ACL rekursywnie w katalogu głównym directiry systemu plików</span><span class="sxs-lookup"><span data-stu-id="c148d-109">Example 1: Update ACL recursively on a root directiry of filesystem</span></span>
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\> Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl -Context $ctx

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 7
TotalFilesSuccessfulCount       : 5
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="c148d-110">To polecenie najpierw tworzy obiekt ACL z trzema wpisami ACL, a następnie aktualizuje rekursywnie listę ACL w katalogu głównym systemu plików.</span><span class="sxs-lookup"><span data-stu-id="c148d-110">This command first creates an ACL object with 3 acl entries, then updates ACL recursively on a root directory of a file system.</span></span>

### <span data-ttu-id="c148d-111">Przykład 2: aktualizowanie listy ACL rekursywnie w katalogu i wznawianie działania po błędzie z usługą ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="c148d-111">Example 2: Update ACL recursively on a directory, and resume from failure with ContinuationToken</span></span>
```
PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -Context $ctx

PS C:\> $result

FailedEntries                   : {dir1/dir2/file4}
TotalDirectoriesSuccessfulCount : 500
TotalFilesSuccessfulCount       : 2500
TotalFailureCount               : 1
ContinuationToken               : VBaHi5TfyO2ai1wYTRhIL2FjbGNibjA2c3RmATAxRDVEN0UzRENFQzZCRTAvYWRsc3Rlc3QyATAxRDY2M0ZCQTZBN0JGQTkvZGlyMC9kaXIxL2ZpbGUzFgAAAA==

PS C:\> $result.FailedEntries

Name            IsDirectory ErrorMessage                                                                   
----            ----------- ------------                                                                   
dir0/dir2/file4       False This request is not authorized to perform this operation using this permission.

# user need fix the failed item , then can resume with ContinuationToken

PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinuationToken $result.ContinuationToken -Context $ctx

PS C:\> $result

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 1000
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="c148d-112">To polecenie po raz pierwszy zaktualizowała listę ACL do katalogu i nie powiodło się, a następnie wznowić pracę z usługą ContinuationToken po usunięciu nieudanego pliku przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c148d-112">This command first updateds ACL recursively to a directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="c148d-113">Przykład 3: aktualizowanie listy ACL rekursywnie fragmentu według fragmentu</span><span class="sxs-lookup"><span data-stu-id="c148d-113">Example 3: Update ACL recursively chunk by chunk</span></span>
```
$ContinueOnFailure = $true # Set it to $false if want to terminate the operation quickly on encountering failures
$token = $null
$TotalDirectoriesSuccess = 0
$TotalFilesSuccess = 0
$totalFailure = 0
$FailedEntries = New-Object System.Collections.Generic.List[System.Object]
do
{
    
    if ($ContinueOnFailure)
    {
        $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 100 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx -ContinueOnFailure
    }
    else
    {
        $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 100 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx
    }

    # echo $result
    $TotalFilesSuccess += $result.TotalFilesSuccessfulCount
    $TotalDirectoriesSuccess += $result.TotalDirectoriesSuccessfulCount
    $totalFailure += $result.TotalFailureCount
    $FailedEntries += $result.FailedEntries
    $token = $result.ContinuationToken
}while (($token -ne $null) -and (($ContinueOnFailure) -or ($result.TotalFailureCount -eq 0)))
echo ""
echo "[Result Summary]"
echo "TotalDirectoriesSuccessfulCount: `t$($TotalDirectoriesSuccess)"
echo "TotalFilesSuccessfulCount: `t`t`t$($TotalFilesSuccess)"
echo "TotalFailureCount: `t`t`t`t`t$($totalFailure)"
echo "ContinuationToken: `t`t`t`t`t$($token)"
echo "FailedEntries:"$($FailedEntries | ft)
```

<span data-ttu-id="c148d-114">Ten skrypt zaktualizuje rescursively ACL katalogu według fragmentów, z rozmiarem fragmentu jako BatchSize \* MaxBatchCount.</span><span class="sxs-lookup"><span data-stu-id="c148d-114">This script will update ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="c148d-115">Rozmiar fragmentu to 5000 w tym skrypcie.</span><span class="sxs-lookup"><span data-stu-id="c148d-115">Chunk size is 5000 in this script.</span></span>

### <span data-ttu-id="c148d-116">Przykład 4: aktualizowanie listy ACL rekursywnie w katalogu i ContinueOnFailure, a następnie wznawianie od błędów o jednej</span><span class="sxs-lookup"><span data-stu-id="c148d-116">Example 4: Update ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
```
PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinueOnFailure -Context $ctx

PS C:\> $result

FailedEntries                   : {dir0/dir1/file1, dir0/dir2/file4}
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 500
TotalFailureCount               : 2
ContinuationToken               : VBaHi5TfyO2ai1wYTRhIL2FjbGNibjA2c3RmATAxRDVEN0UzRENFQzZCRTAvYWRsc3Rlc3QyATAxRDY2M0ZCQTZBN0JGQTkvZGlyMC9kaXIxL2ZpbGUzFgAAAA==

PS C:\> $result.FailedEntries

Name            IsDirectory ErrorMessage                                                                   
----            ----------- ------------                                                                   
dir0/dir1/file1       False This request is not authorized to perform this operation using this permission.
dir0/dir2/file4       False This request is not authorized to perform this operation using this permission.

# user need fix the failed item , then can resume with ContinuationToken

PS C:\> foreach ($path in $result.FailedEntries.Name)
        {
            # user code to fix failed entry in $path
            
            #set ACL again
            Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path $path -Acl $acl -Context $ctx
        }
```

<span data-ttu-id="c148d-117">To polecenie po raz pierwszy zaktualizowała listę ACL do katalogu z ContinueOnFailure, a niektóre elementy nie powiodły się, a następnie wznowić działanie nieuszkodzonych elementów o jednej osobie.</span><span class="sxs-lookup"><span data-stu-id="c148d-117">This command first updateds ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="c148d-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c148d-118">PARAMETERS</span></span>

### <span data-ttu-id="c148d-119">-ACL</span><span class="sxs-lookup"><span data-stu-id="c148d-119">-Acl</span></span>
<span data-ttu-id="c148d-120">Lista kontroli dostępu POSIX, która umożliwia cykliczne ustawianie plików lub katalogów.</span><span class="sxs-lookup"><span data-stu-id="c148d-120">The POSIX access control list to set recursively for the file or directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c148d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c148d-121">-AsJob</span></span>
<span data-ttu-id="c148d-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c148d-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c148d-123">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="c148d-123">-BatchSize</span></span>
<span data-ttu-id="c148d-124">Jeśli rozmiar zestawu danych przekracza wielkość partii, operacja zostanie podzielona na wiele żądań, aby można było śledzić postępy.</span><span class="sxs-lookup"><span data-stu-id="c148d-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="c148d-125">Rozmiar wsadu powinien mieścić się w zakresie od 1 do 2000.</span><span class="sxs-lookup"><span data-stu-id="c148d-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="c148d-126">Wartość domyślna to 2000.</span><span class="sxs-lookup"><span data-stu-id="c148d-126">Default is 2000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c148d-127">-Context</span><span class="sxs-lookup"><span data-stu-id="c148d-127">-Context</span></span>
<span data-ttu-id="c148d-128">Obiekt kontekstu usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="c148d-128">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c148d-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="c148d-129">-ContinuationToken</span></span>
<span data-ttu-id="c148d-130">Token kontynuacji.</span><span class="sxs-lookup"><span data-stu-id="c148d-130">Continuation Token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c148d-131">-ContinueOnFailure</span><span class="sxs-lookup"><span data-stu-id="c148d-131">-ContinueOnFailure</span></span>
<span data-ttu-id="c148d-132">Ustaw ten parametr, aby ignorować błędy i kontynuować proceeing z operacją na innych podjednostkach katalogu.</span><span class="sxs-lookup"><span data-stu-id="c148d-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="c148d-133">Domyślna operacja zostanie wkrótce zakończona w przypadku napotkania błędów.</span><span class="sxs-lookup"><span data-stu-id="c148d-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="c148d-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c148d-134">-DefaultProfile</span></span>
<span data-ttu-id="c148d-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c148d-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c148d-136">— System plików</span><span class="sxs-lookup"><span data-stu-id="c148d-136">-FileSystem</span></span>
<span data-ttu-id="c148d-137">Nazwa systemu plików</span><span class="sxs-lookup"><span data-stu-id="c148d-137">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c148d-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="c148d-138">-MaxBatchCount</span></span>
<span data-ttu-id="c148d-139">Maksymalna liczba partii, w których można wykonać operację kontroli dostępu pojedynczej zmiany.</span><span class="sxs-lookup"><span data-stu-id="c148d-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="c148d-140">Jeśli rozmiar zestawu danych przekracza MaxBatchCount mnożenie BatchSize, token kontynuacji będzie zwracany.</span><span class="sxs-lookup"><span data-stu-id="c148d-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c148d-141">-Path</span><span class="sxs-lookup"><span data-stu-id="c148d-141">-Path</span></span>
<span data-ttu-id="c148d-142">Ścieżka w określonym systemie plików, która rekursywnie zmienia dane ACL.</span><span class="sxs-lookup"><span data-stu-id="c148d-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="c148d-143">Może to być plik lub katalog.</span><span class="sxs-lookup"><span data-stu-id="c148d-143">Can be a file or directory.</span></span>
<span data-ttu-id="c148d-144">W formacie "Directory/file.txt" lub "directory1/Directory2/".</span><span class="sxs-lookup"><span data-stu-id="c148d-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="c148d-145">Pomiń Ustaw ten parametr, aby zmienić listę ACL rekursywnie z katalogu głównego systemu plików.</span><span class="sxs-lookup"><span data-stu-id="c148d-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c148d-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c148d-146">-Confirm</span></span>
<span data-ttu-id="c148d-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c148d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c148d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c148d-148">-WhatIf</span></span>
<span data-ttu-id="c148d-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c148d-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c148d-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c148d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c148d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c148d-151">CommonParameters</span></span>
<span data-ttu-id="c148d-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c148d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c148d-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c148d-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c148d-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c148d-154">INPUTS</span></span>

### <span data-ttu-id="c148d-155">System. String</span><span class="sxs-lookup"><span data-stu-id="c148d-155">System.String</span></span>

### <span data-ttu-id="c148d-156">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c148d-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c148d-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c148d-157">OUTPUTS</span></span>

### <span data-ttu-id="c148d-158">System. String</span><span class="sxs-lookup"><span data-stu-id="c148d-158">System.String</span></span>

## <span data-ttu-id="c148d-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c148d-159">NOTES</span></span>

## <span data-ttu-id="c148d-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c148d-160">RELATED LINKS</span></span>
