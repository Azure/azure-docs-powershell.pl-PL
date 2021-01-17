---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: 1d2a4bc1dd9dab05e56f8b69c92d98985cf98e15
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348373"
---
# <span data-ttu-id="223fe-101">Set-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="223fe-101">Set-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="223fe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="223fe-102">SYNOPSIS</span></span>
<span data-ttu-id="223fe-103">Ustawianie listy ACL rekursywnie w określonej ścieżce.</span><span class="sxs-lookup"><span data-stu-id="223fe-103">Set ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="223fe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="223fe-104">SYNTAX</span></span>

```
Set-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="223fe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="223fe-105">DESCRIPTION</span></span>
<span data-ttu-id="223fe-106">Polecenie cmdlet **Set-AzDataLakeGen2AclRecursive** ustawia rekursywnie listę ACL w określonej ścieżce.</span><span class="sxs-lookup"><span data-stu-id="223fe-106">The **Set-AzDataLakeGen2AclRecursive** cmdlet sets ACL recursively on the specified path.</span></span> <span data-ttu-id="223fe-107">Wejściowa lista ACL zastąpi całkowicie pierwotną listę ACL.</span><span class="sxs-lookup"><span data-stu-id="223fe-107">The input ACL will replace original ACL completely.</span></span>

## <span data-ttu-id="223fe-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="223fe-108">EXAMPLES</span></span>

### <span data-ttu-id="223fe-109">Przykład 1: ustawianie listy ACL rekursywnie w directiry</span><span class="sxs-lookup"><span data-stu-id="223fe-109">Example 1: Set ACL recursively on a directiry</span></span>
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\> Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -Context $ctx

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 7
TotalFilesSuccessfulCount       : 5
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="223fe-110">To polecenie najpierw tworzy obiekt ACL z trzema wpisami ACL, a następnie ustawia rekursywnie listę ACL w katalogu.</span><span class="sxs-lookup"><span data-stu-id="223fe-110">This command first creates an ACL object with 3 acl entries, then sets ACL recursively on a directory.</span></span>

### <span data-ttu-id="223fe-111">Przykład 2: ustawianie listy ACL rekursywnie na głównym directiry systemu plików</span><span class="sxs-lookup"><span data-stu-id="223fe-111">Example 2: Set ACL recursively on a root directiry of filesystem</span></span>
```
PS C:\> $result = Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl  -Context $ctx

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

PS C:\> $result = Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl -ContinuationToken $result.ContinuationToken -Context $ctx

PS C:\> $result

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 1000
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="223fe-112">To polecenie najpierw ustawia listę ACL rekursywnie w katalogu głównym i nie powiodło się, a następnie wznawia pracę z ContinuationToken po usunięciu nieudanego pliku przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="223fe-112">This command first sets ACL recursively to a root directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="223fe-113">Przykład 3: ustawianie listy ACL rekursywnie według fragmentu</span><span class="sxs-lookup"><span data-stu-id="223fe-113">Example 3: Set ACL recursively chunk by chunk</span></span>
```
$token = $null
$TotalDirectoriesSuccess = 0
$TotalFilesSuccess = 0
$totalFailure = 0
$FailedEntries = New-Object System.Collections.Generic.List[System.Object]
do
{
    $result = Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 100 -MaxBatchCount 2 -ContinuationToken $token -Context $ctx

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

<span data-ttu-id="223fe-114">Ten skrypt ustawia listę ACL rescursively dla fragmentu katalogu, z rozmiarem fragmentu jako BatchSize \* MaxBatchCount.</span><span class="sxs-lookup"><span data-stu-id="223fe-114">This script sets ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="223fe-115">Rozmiar fragmentu to 200 w tym skrypcie.</span><span class="sxs-lookup"><span data-stu-id="223fe-115">Chunk size is 200 in this script.</span></span>

### <span data-ttu-id="223fe-116">Przykład 4: ustawianie listy ACL w katalogu i ContinueOnFailure, a następnie wznawianie od błędów o jednej</span><span class="sxs-lookup"><span data-stu-id="223fe-116">Example 4: Set ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
```
PS C:\> $result = Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinueOnFailure -Context $ctx

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

<span data-ttu-id="223fe-117">To polecenie najpierw ustawia listę ACL rekursywnie w katalogu zawierającym ContinueOnFailure, a niektóre elementy nie powiodły się, a następnie wznowić działanie elementów, które nie powiodły się pojedynczo.</span><span class="sxs-lookup"><span data-stu-id="223fe-117">This command first sets ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="223fe-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="223fe-118">PARAMETERS</span></span>

### <span data-ttu-id="223fe-119">-ACL</span><span class="sxs-lookup"><span data-stu-id="223fe-119">-Acl</span></span>
<span data-ttu-id="223fe-120">Lista kontroli dostępu POSIX, która umożliwia cykliczne ustawianie plików lub katalogów.</span><span class="sxs-lookup"><span data-stu-id="223fe-120">The POSIX access control list to set recursively for the file or directory.</span></span>

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

### <span data-ttu-id="223fe-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="223fe-121">-AsJob</span></span>
<span data-ttu-id="223fe-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="223fe-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="223fe-123">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="223fe-123">-BatchSize</span></span>
<span data-ttu-id="223fe-124">Jeśli rozmiar zestawu danych przekracza wielkość partii, operacja zostanie podzielona na wiele żądań, aby można było śledzić postępy.</span><span class="sxs-lookup"><span data-stu-id="223fe-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="223fe-125">Rozmiar wsadu powinien mieścić się w zakresie od 1 do 2000.</span><span class="sxs-lookup"><span data-stu-id="223fe-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="223fe-126">Wartość domyślna to 2000.</span><span class="sxs-lookup"><span data-stu-id="223fe-126">Default is 2000.</span></span>

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

### <span data-ttu-id="223fe-127">-Context</span><span class="sxs-lookup"><span data-stu-id="223fe-127">-Context</span></span>
<span data-ttu-id="223fe-128">Obiekt kontekstu usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="223fe-128">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="223fe-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="223fe-129">-ContinuationToken</span></span>
<span data-ttu-id="223fe-130">Token kontynuacji.</span><span class="sxs-lookup"><span data-stu-id="223fe-130">Continuation Token.</span></span>

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

### <span data-ttu-id="223fe-131">-ContinueOnFailure</span><span class="sxs-lookup"><span data-stu-id="223fe-131">-ContinueOnFailure</span></span>
<span data-ttu-id="223fe-132">Ustaw ten parametr, aby ignorować błędy i kontynuować proceeing z operacją na innych podjednostkach katalogu.</span><span class="sxs-lookup"><span data-stu-id="223fe-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="223fe-133">Domyślna operacja zostanie wkrótce zakończona w przypadku napotkania błędów.</span><span class="sxs-lookup"><span data-stu-id="223fe-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="223fe-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="223fe-134">-DefaultProfile</span></span>
<span data-ttu-id="223fe-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="223fe-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="223fe-136">— System plików</span><span class="sxs-lookup"><span data-stu-id="223fe-136">-FileSystem</span></span>
<span data-ttu-id="223fe-137">Nazwa systemu plików</span><span class="sxs-lookup"><span data-stu-id="223fe-137">FileSystem name</span></span>

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

### <span data-ttu-id="223fe-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="223fe-138">-MaxBatchCount</span></span>
<span data-ttu-id="223fe-139">Maksymalna liczba partii, w których można wykonać operację kontroli dostępu pojedynczej zmiany.</span><span class="sxs-lookup"><span data-stu-id="223fe-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="223fe-140">Jeśli rozmiar zestawu danych przekracza MaxBatchCount mnożenie BatchSize, token kontynuacji będzie zwracany.</span><span class="sxs-lookup"><span data-stu-id="223fe-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

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

### <span data-ttu-id="223fe-141">-Path</span><span class="sxs-lookup"><span data-stu-id="223fe-141">-Path</span></span>
<span data-ttu-id="223fe-142">Ścieżka w określonym systemie plików, która rekursywnie zmienia dane ACL.</span><span class="sxs-lookup"><span data-stu-id="223fe-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="223fe-143">Może to być plik lub katalog.</span><span class="sxs-lookup"><span data-stu-id="223fe-143">Can be a file or directory.</span></span>
<span data-ttu-id="223fe-144">W formacie "Directory/file.txt" lub "directory1/Directory2/".</span><span class="sxs-lookup"><span data-stu-id="223fe-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="223fe-145">Pomiń Ustaw ten parametr, aby zmienić listę ACL rekursywnie z katalogu głównego systemu plików.</span><span class="sxs-lookup"><span data-stu-id="223fe-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="223fe-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="223fe-146">-Confirm</span></span>
<span data-ttu-id="223fe-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="223fe-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="223fe-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="223fe-148">-WhatIf</span></span>
<span data-ttu-id="223fe-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="223fe-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="223fe-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="223fe-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="223fe-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="223fe-151">CommonParameters</span></span>
<span data-ttu-id="223fe-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="223fe-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="223fe-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="223fe-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="223fe-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="223fe-154">INPUTS</span></span>

### <span data-ttu-id="223fe-155">System. String</span><span class="sxs-lookup"><span data-stu-id="223fe-155">System.String</span></span>

### <span data-ttu-id="223fe-156">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="223fe-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="223fe-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="223fe-157">OUTPUTS</span></span>

### <span data-ttu-id="223fe-158">System. String</span><span class="sxs-lookup"><span data-stu-id="223fe-158">System.String</span></span>

## <span data-ttu-id="223fe-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="223fe-159">NOTES</span></span>

## <span data-ttu-id="223fe-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="223fe-160">RELATED LINKS</span></span>
