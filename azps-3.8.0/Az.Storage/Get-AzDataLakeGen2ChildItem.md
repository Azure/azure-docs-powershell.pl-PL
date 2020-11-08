---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2childitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
ms.openlocfilehash: 9160eabf2492969ad7fa3916791854abd4ef6c44
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051269"
---
# <span data-ttu-id="1f9ba-101">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="1f9ba-101">Get-AzDataLakeGen2ChildItem</span></span>

## <span data-ttu-id="1f9ba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1f9ba-102">SYNOPSIS</span></span>
<span data-ttu-id="1f9ba-103">Wyświetla katalogi podrzędne i pliki z katalogu lub katalogu głównego systemu plików.</span><span class="sxs-lookup"><span data-stu-id="1f9ba-103">Lists sub directorys and files from a directory or filesystem root.</span></span>

## <span data-ttu-id="1f9ba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1f9ba-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2ChildItem [-FileSystem] <String> [[-Path] <String>] [-FetchProperty] [-Recurse]
 [-MaxCount <Int32>] [-ContinuationToken <String>] [-AsJob] [-OutputUserPrincipalName]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f9ba-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1f9ba-105">DESCRIPTION</span></span>
<span data-ttu-id="1f9ba-106">Polecenie cmdlet **Get-AzDataLakeGen2ChildItem** zawiera listę podkatalogów i plików w katalogu lub systemie plików na koncie usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="1f9ba-106">The **Get-AzDataLakeGen2ChildItem** cmdlet lists sub directorys and files in a directory or Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="1f9ba-107">To polecenie cmdlet działa tylko wtedy, gdy dla konta magazynu jest włączone hierarchiczne obszary nazw.</span><span class="sxs-lookup"><span data-stu-id="1f9ba-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="1f9ba-108">Ten rodzaj konta można utworzyć, uruchamiając polecenie cmdlet "New-AzStorageAccount" z opcją "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="1f9ba-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="1f9ba-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1f9ba-109">EXAMPLES</span></span>

### <span data-ttu-id="1f9ba-110">Przykład 1: wyświetlanie bezpośrednich podelementów z systemu plików</span><span class="sxs-lookup"><span data-stu-id="1f9ba-110">Example 1: List the direct sub items from a Filesystem</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxr-x---    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxr-x---    $superuser           $superuser
```

<span data-ttu-id="1f9ba-111">To polecenie umożliwia wyświetlenie listy bezpośrednich elementów podrzędnych z systemu plików</span><span class="sxs-lookup"><span data-stu-id="1f9ba-111">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="1f9ba-112">Przykład 2: Lista rekurencyjna z katalogu i właściwości pobierania/lista ACL</span><span class="sxs-lookup"><span data-stu-id="1f9ba-112">Example 2: List recursively from a directory, and fetch Properties/ACL</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Path "dir1/" -Recurse -FetchProperty

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwx---rwx    $superuser           $superuser          
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser           
dir1/testfile_1K_0   False        1024            2020-03-23 09:29:21Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="1f9ba-113">To polecenie umożliwia wyświetlenie listy bezpośrednich elementów podrzędnych z systemu plików</span><span class="sxs-lookup"><span data-stu-id="1f9ba-113">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="1f9ba-114">Przykład 3: porekurencyjnie elementy listy z systemu plików w wielu partiach</span><span class="sxs-lookup"><span data-stu-id="1f9ba-114">Example 3: List items recursively from a Filesystem in multiple batches</span></span>
```
PS C:\> $MaxReturn = 10000
PS C:\> $FileSystemName = "filesystem1"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $items = Get-AzDataLakeGen2ChildItem -FileSystem $FileSystemName -Recurse -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $items.Count
     if($items.Length -le 0) { Break;}
     $Token = $items[$items.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total items in Filesystem $FileSystemName"
```

<span data-ttu-id="1f9ba-115">W tym przykładzie użyto parametrów *MaxCount* i *ContinuationToken* , aby porekurencyjnie wyświetlić elementy z systemu plików w wielu partiach.</span><span class="sxs-lookup"><span data-stu-id="1f9ba-115">This example uses the *MaxCount* and *ContinuationToken* parameters to list items recursively from a Filesystem in multiple batches.</span></span>
<span data-ttu-id="1f9ba-116">Pierwsze cztery polecenia umożliwiają przypisanie wartości do zmiennych w przykładzie.</span><span class="sxs-lookup"><span data-stu-id="1f9ba-116">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="1f9ba-117">Piąte polecenie **określa instrukcję do wykonania,** która używa polecenia cmdlet **Get-AzDataLakeGen2ChildItem** w celu wylistowania elementów.</span><span class="sxs-lookup"><span data-stu-id="1f9ba-117">The fifth command specifies a **Do-While** statement that uses the **Get-AzDataLakeGen2ChildItem** cmdlet to list items.</span></span>
<span data-ttu-id="1f9ba-118">Instrukcja zawiera token kontynuacji przechowywany w zmiennej $Token.</span><span class="sxs-lookup"><span data-stu-id="1f9ba-118">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="1f9ba-119">$Token zmienia się w trakcie uruchamiania pętli.</span><span class="sxs-lookup"><span data-stu-id="1f9ba-119">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="1f9ba-120">W poleceniu ostatnim użyto polecenia **echo** do wyświetlenia sumy.</span><span class="sxs-lookup"><span data-stu-id="1f9ba-120">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="1f9ba-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1f9ba-121">PARAMETERS</span></span>

### <span data-ttu-id="1f9ba-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f9ba-122">-AsJob</span></span>
<span data-ttu-id="1f9ba-123">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1f9ba-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f9ba-124">-Context</span><span class="sxs-lookup"><span data-stu-id="1f9ba-124">-Context</span></span>
<span data-ttu-id="1f9ba-125">Obiekt kontekstu usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="1f9ba-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="1f9ba-126">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="1f9ba-126">-ContinuationToken</span></span>
<span data-ttu-id="1f9ba-127">Token kontynuacji.</span><span class="sxs-lookup"><span data-stu-id="1f9ba-127">Continuation Token.</span></span>

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

### <span data-ttu-id="1f9ba-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f9ba-128">-DefaultProfile</span></span>
<span data-ttu-id="1f9ba-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f9ba-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f9ba-130">-FetchProperty</span><span class="sxs-lookup"><span data-stu-id="1f9ba-130">-FetchProperty</span></span>
<span data-ttu-id="1f9ba-131">Pobierz właściwości elementu datalake i listę ACL.</span><span class="sxs-lookup"><span data-stu-id="1f9ba-131">Fetch the datalake item properties and ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: FetchPermission

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f9ba-132">— System plików</span><span class="sxs-lookup"><span data-stu-id="1f9ba-132">-FileSystem</span></span>
<span data-ttu-id="1f9ba-133">Nazwa systemu plików</span><span class="sxs-lookup"><span data-stu-id="1f9ba-133">FileSystem name</span></span>

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

### <span data-ttu-id="1f9ba-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="1f9ba-134">-MaxCount</span></span>
<span data-ttu-id="1f9ba-135">Maksymalna liczba obiektów blob, które mogą zostać zwrócone.</span><span class="sxs-lookup"><span data-stu-id="1f9ba-135">The max count of the blobs that can return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f9ba-136">-OutputUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="1f9ba-136">-OutputUserPrincipalName</span></span>
<span data-ttu-id="1f9ba-137">Jeśli speicify ten parametr, wartości tożsamości użytkowników zwrócone w polach właściciel i Grupa każdego wpisu listy zostaną przekształcone w identyfikatorach obiektów usługi Azure Active Directory na główne nazwy użytkowników.</span><span class="sxs-lookup"><span data-stu-id="1f9ba-137">If speicify this parameter, the user identity values returned in the owner and group fields of each list entry will be transformed from Azure Active Directory Object IDs to User Principal Names.</span></span> <span data-ttu-id="1f9ba-138">Jeśli nie speicify tego parametru, wartości zostaną zwrócone jako identyfikatory obiektów usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1f9ba-138">If not speicify this parameter, the values will be returned as Azure Active Directory Object IDs.</span></span> <span data-ttu-id="1f9ba-139">Pamiętaj, że identyfikatory obiektów grupy i aplikacji nie są tłumaczone, ponieważ nie mają unikatowych przyjaznych nazw.</span><span class="sxs-lookup"><span data-stu-id="1f9ba-139">Note that group and application Object IDs are not translated because they do not have unique friendly names.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f9ba-140">-Path</span><span class="sxs-lookup"><span data-stu-id="1f9ba-140">-Path</span></span>
<span data-ttu-id="1f9ba-141">Ścieżka w określonym systemie plików, który ma zostać pobrany.</span><span class="sxs-lookup"><span data-stu-id="1f9ba-141">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="1f9ba-142">Powinien być katalogiem w formacie "directory1/Directory2/".</span><span class="sxs-lookup"><span data-stu-id="1f9ba-142">Should be a directory, in the format 'directory1/directory2/'.</span></span>

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

### <span data-ttu-id="1f9ba-143">-Rekursywowanie</span><span class="sxs-lookup"><span data-stu-id="1f9ba-143">-Recurse</span></span>
<span data-ttu-id="1f9ba-144">Wskazuje, czy będzie cyklicznie pobierać element podrzędny.</span><span class="sxs-lookup"><span data-stu-id="1f9ba-144">Indicates if will recursively get the Child Item.</span></span>
<span data-ttu-id="1f9ba-145">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="1f9ba-145">The default is false.</span></span>

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

### <span data-ttu-id="1f9ba-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f9ba-146">CommonParameters</span></span>
<span data-ttu-id="1f9ba-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f9ba-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f9ba-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f9ba-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f9ba-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f9ba-149">INPUTS</span></span>

### <span data-ttu-id="1f9ba-150">System. String</span><span class="sxs-lookup"><span data-stu-id="1f9ba-150">System.String</span></span>

### <span data-ttu-id="1f9ba-151">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1f9ba-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1f9ba-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1f9ba-152">OUTPUTS</span></span>

### <span data-ttu-id="1f9ba-153">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="1f9ba-153">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="1f9ba-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1f9ba-154">NOTES</span></span>

## <span data-ttu-id="1f9ba-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f9ba-155">RELATED LINKS</span></span>
