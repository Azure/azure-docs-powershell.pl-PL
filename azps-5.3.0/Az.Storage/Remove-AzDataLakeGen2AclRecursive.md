---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: cb2c409ae2bbe7734c433de74ef4a21c368221e1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502713"
---
# <span data-ttu-id="63e4d-101">Remove-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="63e4d-101">Remove-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="63e4d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63e4d-102">SYNOPSIS</span></span>
<span data-ttu-id="63e4d-103">Usuń listę ACL rekursywnie w określonej ścieżce.</span><span class="sxs-lookup"><span data-stu-id="63e4d-103">Remove ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="63e4d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63e4d-104">SYNTAX</span></span>

```
Remove-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63e4d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="63e4d-105">DESCRIPTION</span></span>
<span data-ttu-id="63e4d-106">Polecenie cmdlet **Remove-AzDataLakeGen2AclRecursive** usuwa rekursywnie ACL z określonej ścieżki.</span><span class="sxs-lookup"><span data-stu-id="63e4d-106">The **Remove-AzDataLakeGen2AclRecursive** cmdlet removes ACL recursively on the specified path.</span></span> <span data-ttu-id="63e4d-107">Wpisy ACL w oryginalnej liście ACL, które mają takie same AccessControlType, DefaultScope i EntityId z wejściowymi wpisami ACL (nawet z innymi uprawnieniami) będzie LBE usunięte.</span><span class="sxs-lookup"><span data-stu-id="63e4d-107">The ACL entries in original ACL, which has same AccessControlType, DefaultScope and EntityId with input ACL entries (even with different permission) wil lbe removed.</span></span>

## <span data-ttu-id="63e4d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63e4d-108">EXAMPLES</span></span>

### <span data-ttu-id="63e4d-109">Przykład 1: Usuwanie listy ACL rekursywnie w katalogu głównym directiry systemu plików</span><span class="sxs-lookup"><span data-stu-id="63e4d-109">Example 1: Remove ACL recursively on a root directiry of filesystem</span></span>
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

<span data-ttu-id="63e4d-110">To polecenie po raz pierwszy tworzy obiekt ACL z 2 wpisami ACL, a następnie usuwa listę ACL rekursywnie w katalogu głównym systemu plików.</span><span class="sxs-lookup"><span data-stu-id="63e4d-110">This command first creates an ACL object with 2 acl entries, then removes ACL recursively on a root directory of a file system.</span></span>

### <span data-ttu-id="63e4d-111">Przykład 2: Usuwanie listy ACL rekursywnie w katalogu</span><span class="sxs-lookup"><span data-stu-id="63e4d-111">Example 2: Remove ACL recursively on a directory</span></span>
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

<span data-ttu-id="63e4d-112">To polecenie najpierw usuwa listę ACL rekursywnie w katalogu, a następnie można ją wznowić za pomocą ContinuationToken, gdy użytkownik naprawi uszkodzony plik.</span><span class="sxs-lookup"><span data-stu-id="63e4d-112">This command first removes ACL recursively on a directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="63e4d-113">Przykład 3: Usuwanie listy ACL rekursywnie według fragmentu</span><span class="sxs-lookup"><span data-stu-id="63e4d-113">Example 3: Remove ACL recursively chunk by chunk</span></span>
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

<span data-ttu-id="63e4d-114">Ten skrypt usunie listę ACL rescursively dla fragmentu katalogu, z rozmiarem fragmentu jako BatchSize \* MaxBatchCount.</span><span class="sxs-lookup"><span data-stu-id="63e4d-114">This script will remove ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="63e4d-115">Rozmiar fragmentu to 50000 w tym skrypcie.</span><span class="sxs-lookup"><span data-stu-id="63e4d-115">Chunk size is 50000 in this script.</span></span>

### <span data-ttu-id="63e4d-116">Przykład 4: Usuwanie listy ACL rekursywnie w katalogu i ContinueOnFailure, a następnie wznawianie od błędów o jednej</span><span class="sxs-lookup"><span data-stu-id="63e4d-116">Example 4: Remove ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
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

<span data-ttu-id="63e4d-117">To polecenie najpierw usuwa listę ACL rekursywnie do katalogu z ContinueOnFailure, a niektóre elementy nie powiodły się, a następnie wznowienie działania elementów, które nie powiodły się pojedynczo.</span><span class="sxs-lookup"><span data-stu-id="63e4d-117">This command first removes ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="63e4d-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63e4d-118">PARAMETERS</span></span>

### <span data-ttu-id="63e4d-119">-ACL</span><span class="sxs-lookup"><span data-stu-id="63e4d-119">-Acl</span></span>
<span data-ttu-id="63e4d-120">Lista kontroli dostępu POSIX, która umożliwia cykliczne ustawianie plików lub katalogów.</span><span class="sxs-lookup"><span data-stu-id="63e4d-120">The POSIX access control list to set recursively for the file or directory.</span></span>

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

### <span data-ttu-id="63e4d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63e4d-121">-AsJob</span></span>
<span data-ttu-id="63e4d-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="63e4d-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63e4d-123">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="63e4d-123">-BatchSize</span></span>
<span data-ttu-id="63e4d-124">Jeśli rozmiar zestawu danych przekracza wielkość partii, operacja zostanie podzielona na wiele żądań, aby można było śledzić postępy.</span><span class="sxs-lookup"><span data-stu-id="63e4d-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="63e4d-125">Rozmiar wsadu powinien mieścić się w zakresie od 1 do 2000.</span><span class="sxs-lookup"><span data-stu-id="63e4d-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="63e4d-126">Wartość domyślna to 2000.</span><span class="sxs-lookup"><span data-stu-id="63e4d-126">Default is 2000.</span></span>

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

### <span data-ttu-id="63e4d-127">-Context</span><span class="sxs-lookup"><span data-stu-id="63e4d-127">-Context</span></span>
<span data-ttu-id="63e4d-128">Obiekt kontekstu usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="63e4d-128">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="63e4d-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="63e4d-129">-ContinuationToken</span></span>
<span data-ttu-id="63e4d-130">Token kontynuacji.</span><span class="sxs-lookup"><span data-stu-id="63e4d-130">Continuation Token.</span></span>

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

### <span data-ttu-id="63e4d-131">-ContinueOnFailure</span><span class="sxs-lookup"><span data-stu-id="63e4d-131">-ContinueOnFailure</span></span>
<span data-ttu-id="63e4d-132">Ustaw ten parametr, aby ignorować błędy i kontynuować proceeing z operacją na innych podjednostkach katalogu.</span><span class="sxs-lookup"><span data-stu-id="63e4d-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="63e4d-133">Domyślna operacja zostanie wkrótce zakończona w przypadku napotkania błędów.</span><span class="sxs-lookup"><span data-stu-id="63e4d-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="63e4d-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63e4d-134">-DefaultProfile</span></span>
<span data-ttu-id="63e4d-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="63e4d-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63e4d-136">— System plików</span><span class="sxs-lookup"><span data-stu-id="63e4d-136">-FileSystem</span></span>
<span data-ttu-id="63e4d-137">Nazwa systemu plików</span><span class="sxs-lookup"><span data-stu-id="63e4d-137">FileSystem name</span></span>

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

### <span data-ttu-id="63e4d-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="63e4d-138">-MaxBatchCount</span></span>
<span data-ttu-id="63e4d-139">Maksymalna liczba partii, w których można wykonać operację kontroli dostępu pojedynczej zmiany.</span><span class="sxs-lookup"><span data-stu-id="63e4d-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="63e4d-140">Jeśli rozmiar zestawu danych przekracza MaxBatchCount mnożenie BatchSize, token kontynuacji będzie zwracany.</span><span class="sxs-lookup"><span data-stu-id="63e4d-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

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

### <span data-ttu-id="63e4d-141">-Path</span><span class="sxs-lookup"><span data-stu-id="63e4d-141">-Path</span></span>
<span data-ttu-id="63e4d-142">Ścieżka w określonym systemie plików, która rekursywnie zmienia dane ACL.</span><span class="sxs-lookup"><span data-stu-id="63e4d-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="63e4d-143">Może to być plik lub katalog.</span><span class="sxs-lookup"><span data-stu-id="63e4d-143">Can be a file or directory.</span></span>
<span data-ttu-id="63e4d-144">W formacie "Directory/file.txt" lub "directory1/Directory2/".</span><span class="sxs-lookup"><span data-stu-id="63e4d-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="63e4d-145">Pomiń Ustaw ten parametr, aby zmienić listę ACL rekursywnie z katalogu głównego systemu plików.</span><span class="sxs-lookup"><span data-stu-id="63e4d-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="63e4d-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="63e4d-146">-Confirm</span></span>
<span data-ttu-id="63e4d-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63e4d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63e4d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63e4d-148">-WhatIf</span></span>
<span data-ttu-id="63e4d-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63e4d-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63e4d-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="63e4d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63e4d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e4d-151">CommonParameters</span></span>
<span data-ttu-id="63e4d-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63e4d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e4d-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63e4d-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e4d-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63e4d-154">INPUTS</span></span>

### <span data-ttu-id="63e4d-155">System. String</span><span class="sxs-lookup"><span data-stu-id="63e4d-155">System.String</span></span>

### <span data-ttu-id="63e4d-156">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="63e4d-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="63e4d-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63e4d-157">OUTPUTS</span></span>

### <span data-ttu-id="63e4d-158">System. String</span><span class="sxs-lookup"><span data-stu-id="63e4d-158">System.String</span></span>

## <span data-ttu-id="63e4d-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63e4d-159">NOTES</span></span>

## <span data-ttu-id="63e4d-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63e4d-160">RELATED LINKS</span></span>
