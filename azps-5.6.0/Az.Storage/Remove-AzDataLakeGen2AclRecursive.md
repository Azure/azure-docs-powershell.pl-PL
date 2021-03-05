---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: db999e2cf473fc62a2c8463e8e08ab8c46bc6ac1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970170"
---
# <span data-ttu-id="ac9e8-101">Remove-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="ac9e8-101">Remove-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="ac9e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac9e8-102">SYNOPSIS</span></span>
<span data-ttu-id="ac9e8-103">Usuwanie listy ACL cyklicznie na określonej ścieżce.</span><span class="sxs-lookup"><span data-stu-id="ac9e8-103">Remove ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="ac9e8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ac9e8-104">SYNTAX</span></span>

```
Remove-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ac9e8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ac9e8-105">DESCRIPTION</span></span>
<span data-ttu-id="ac9e8-106">Polecenie **cmdlet Remove-AzDataLakeGen2AclRecursive** powoduje ponowne usunięcie listy ACL na określonej ścieżce.</span><span class="sxs-lookup"><span data-stu-id="ac9e8-106">The **Remove-AzDataLakeGen2AclRecursive** cmdlet removes ACL recursively on the specified path.</span></span> <span data-ttu-id="ac9e8-107">Wpisy ACL w oryginalnej licencji ACL, która ma takie same pozycje AccessControlType, DefaultScope i EntityId z usuniętymi wpisami ACL wejściowymi (nawet z innymi uprawnieniami) wil lbe.</span><span class="sxs-lookup"><span data-stu-id="ac9e8-107">The ACL entries in original ACL, which has same AccessControlType, DefaultScope and EntityId with input ACL entries (even with different permission) wil lbe removed.</span></span>

## <span data-ttu-id="ac9e8-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ac9e8-108">EXAMPLES</span></span>

### <span data-ttu-id="ac9e8-109">Przykład 1. Ponowne usuwanie listy ACL z katalogu głównego systemu plików</span><span class="sxs-lookup"><span data-stu-id="ac9e8-109">Example 1: Remove ACL recursively on a root directiry of filesystem</span></span>
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -InputObject $acl
PS C:\> Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl -Context $ctx
WARNING: To find the ACL Entry to remove, will only compare AccessControlType, DefaultScope and EntityId, will omit Permission.

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 7
TotalFilesSuccessfulCount       : 5
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="ac9e8-110">To polecenie najpierw tworzy obiekt ACL z 2 wpisami acl, a następnie rekurencyjnie usuwa pozycję ACL z katalogu głównego systemu plików.</span><span class="sxs-lookup"><span data-stu-id="ac9e8-110">This command first creates an ACL object with 2 acl entries, then removes ACL recursively on a root directory of a file system.</span></span>

### <span data-ttu-id="ac9e8-111">Przykład 2. Ponowne usuwanie listy ACL z katalogu</span><span class="sxs-lookup"><span data-stu-id="ac9e8-111">Example 2: Remove ACL recursively on a directory</span></span>
```
PS C:\> $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -Context $ctx
WARNING: To find the ACL Entry to remove, will only compare AccessControlType, DefaultScope and EntityId, will omit Permission.

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

PS C:\> $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinuationToken $result.ContinuationToken -Context $ctx
WARNING: To find the ACL Entry to remove, will only compare AccessControlType, DefaultScope and EntityId, will omit Permission.

PS C:\> $result

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 1000
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="ac9e8-112">To polecenie najpierw usuwa reckurencyjnie ACL z katalogu i nie powiodło się, a następnie wznów z ciągiem ContinuationToken po naprawieniu przez użytkownika pliku, który zakończył się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="ac9e8-112">This command first removes ACL recursively on a directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="ac9e8-113">Przykład 3. Usuwanie ponownego fragmentu listy ACL według fragmentu</span><span class="sxs-lookup"><span data-stu-id="ac9e8-113">Example 3: Remove ACL recursively chunk by chunk</span></span>
```
$token = $null
$TotalDirectoriesSuccess = 0
$TotalFilesSuccess = 0
$totalFailure = 0
$FailedEntries = New-Object System.Collections.Generic.List[System.Object]
do
{
    $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 1000 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx

    # echo $result
    $TotalFilesSuccess += $result.TotalFilesSuccessfulCount
    $TotalDirectoriesSuccess += $result.TotalDirectoriesSuccessfulCount
    $totalFailure += $result.TotalFailureCount
    $FailedEntries += $result.FailedEntries
    $token = $result.ContinuationToken
}while (($token -ne $null) -and ($result.TotalFailureCount -eq 0))
echo ""
echo "[Result Summary]"
echo "TotalDirectoriesSuccessfulCount: `t$($TotalDirectoriesSuccess)"
echo "TotalFilesSuccessfulCount: `t`t`t$($TotalFilesSuccess)"
echo "TotalFailureCount: `t`t`t`t`t$($totalFailure)"
echo "ContinuationToken: `t`t`t`t`t$($token)"
echo "FailedEntries:"$($FailedEntries | ft)
```

<span data-ttu-id="ac9e8-114">Ten skrypt spowoduje ponowne usunięcie listy ACL w fragcie katalogu według fragmentu, z rozmiarem fragmentu w rozmiarze BatchSize \* MaxBatchCount.</span><span class="sxs-lookup"><span data-stu-id="ac9e8-114">This script will remove ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="ac9e8-115">W tym skrypcie rozmiar fragmentu wynosi 50 000.</span><span class="sxs-lookup"><span data-stu-id="ac9e8-115">Chunk size is 50000 in this script.</span></span>

### <span data-ttu-id="ac9e8-116">Przykład 4. Ponowne usuwanie listy ACL z katalogu i powtarzanie się po awarii</span><span class="sxs-lookup"><span data-stu-id="ac9e8-116">Example 4: Remove ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
```
PS C:\> $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinueOnFailure -Context $ctx

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
            Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path $path -Acl $acl -Context $ctx
        }
```

<span data-ttu-id="ac9e8-117">To polecenie najpierw usuwa cyklicznie listy ACL do katalogu z ciągiem ContinueOnFailure, a niektóre elementy nie powiodły się, a następnie wznawiaj elementy, które zakończyły się niepowodzeniem, jeden po drugie.</span><span class="sxs-lookup"><span data-stu-id="ac9e8-117">This command first removes ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="ac9e8-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac9e8-118">PARAMETERS</span></span>

### <span data-ttu-id="ac9e8-119">-Acl</span><span class="sxs-lookup"><span data-stu-id="ac9e8-119">-Acl</span></span>
<span data-ttu-id="ac9e8-120">Lista kontroli dostępu POSIX, która umożliwia cykliczne ustawianie pliku lub katalogu.</span><span class="sxs-lookup"><span data-stu-id="ac9e8-120">The POSIX access control list to set recursively for the file or directory.</span></span>

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

### <span data-ttu-id="ac9e8-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ac9e8-121">-AsJob</span></span>
<span data-ttu-id="ac9e8-122">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ac9e8-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ac9e8-123">- BatchSize</span><span class="sxs-lookup"><span data-stu-id="ac9e8-123">-BatchSize</span></span>
<span data-ttu-id="ac9e8-124">Jeśli rozmiar zestawu danych przekracza rozmiar partii, operacja zostanie podzielona na wiele żądań, dzięki czemu będzie można śledzić postęp.</span><span class="sxs-lookup"><span data-stu-id="ac9e8-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="ac9e8-125">Rozmiar partii powinien być między 1 a 2000.</span><span class="sxs-lookup"><span data-stu-id="ac9e8-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="ac9e8-126">Wartość domyślna to 2000.</span><span class="sxs-lookup"><span data-stu-id="ac9e8-126">Default is 2000.</span></span>

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

### <span data-ttu-id="ac9e8-127">— kontekst</span><span class="sxs-lookup"><span data-stu-id="ac9e8-127">-Context</span></span>
<span data-ttu-id="ac9e8-128">Obiekt kontekstowy magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ac9e8-128">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="ac9e8-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="ac9e8-129">-ContinuationToken</span></span>
<span data-ttu-id="ac9e8-130">Token kontynuacji.</span><span class="sxs-lookup"><span data-stu-id="ac9e8-130">Continuation Token.</span></span>

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

### <span data-ttu-id="ac9e8-131">-ContinueOnFailure</span><span class="sxs-lookup"><span data-stu-id="ac9e8-131">-ContinueOnFailure</span></span>
<span data-ttu-id="ac9e8-132">Ustaw ten parametr tak, aby ignorował błędy i kontynuuj proceeing wraz z operacją w innych podencji katalogu.</span><span class="sxs-lookup"><span data-stu-id="ac9e8-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="ac9e8-133">Domyślna operacja zakończy się szybko po napotkaniu błędów.</span><span class="sxs-lookup"><span data-stu-id="ac9e8-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="ac9e8-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac9e8-134">-DefaultProfile</span></span>
<span data-ttu-id="ac9e8-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ac9e8-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac9e8-136">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="ac9e8-136">-FileSystem</span></span>
<span data-ttu-id="ac9e8-137">Nazwa systemu plików</span><span class="sxs-lookup"><span data-stu-id="ac9e8-137">FileSystem name</span></span>

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

### <span data-ttu-id="ac9e8-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="ac9e8-138">-MaxBatchCount</span></span>
<span data-ttu-id="ac9e8-139">Maksymalna liczba partii, w których można wykonać operację kontroli dostępu z jedną zmianą.</span><span class="sxs-lookup"><span data-stu-id="ac9e8-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="ac9e8-140">Jeśli rozmiar zestawu danych przekracza wartość MaxBatchCount, pomnóż wartość BatchSize, zwrócony zostanie token kontynuacji.</span><span class="sxs-lookup"><span data-stu-id="ac9e8-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

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

### <span data-ttu-id="ac9e8-141">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="ac9e8-141">-Path</span></span>
<span data-ttu-id="ac9e8-142">Ścieżka w określonym systemie plików, która ma rekurencyjnie zmieniać wartość Acl.</span><span class="sxs-lookup"><span data-stu-id="ac9e8-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="ac9e8-143">Może być plikiem lub katalogiem.</span><span class="sxs-lookup"><span data-stu-id="ac9e8-143">Can be a file or directory.</span></span>
<span data-ttu-id="ac9e8-144">W formacie "katalog/file.txt" lub "katalog1/katalog2/".</span><span class="sxs-lookup"><span data-stu-id="ac9e8-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="ac9e8-145">Pomiń ten parametr, aby zmienić wartość Acl rekurencyjnie z katalogu głównego systemu plików.</span><span class="sxs-lookup"><span data-stu-id="ac9e8-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="ac9e8-146">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ac9e8-146">-Confirm</span></span>
<span data-ttu-id="ac9e8-147">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ac9e8-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac9e8-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac9e8-148">-WhatIf</span></span>
<span data-ttu-id="ac9e8-149">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac9e8-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac9e8-150">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ac9e8-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac9e8-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac9e8-151">CommonParameters</span></span>
<span data-ttu-id="ac9e8-152">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac9e8-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac9e8-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac9e8-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac9e8-154">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac9e8-154">INPUTS</span></span>

### <span data-ttu-id="ac9e8-155">System.String</span><span class="sxs-lookup"><span data-stu-id="ac9e8-155">System.String</span></span>

### <span data-ttu-id="ac9e8-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ac9e8-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ac9e8-157">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac9e8-157">OUTPUTS</span></span>

### <span data-ttu-id="ac9e8-158">System.String</span><span class="sxs-lookup"><span data-stu-id="ac9e8-158">System.String</span></span>

## <span data-ttu-id="ac9e8-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ac9e8-159">NOTES</span></span>

## <span data-ttu-id="ac9e8-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac9e8-160">RELATED LINKS</span></span>
