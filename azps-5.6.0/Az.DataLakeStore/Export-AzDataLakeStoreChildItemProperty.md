---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/export-azdatalakestorechilditemproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
ms.openlocfilehash: 0f43c372901dbfd571343584f0ca8479d5b7081e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013665"
---
# <span data-ttu-id="a73c9-101">Export-AzDataLakeStoreChildItemProperty</span><span class="sxs-lookup"><span data-stu-id="a73c9-101">Export-AzDataLakeStoreChildItemProperty</span></span>

## <span data-ttu-id="a73c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a73c9-102">SYNOPSIS</span></span>
<span data-ttu-id="a73c9-103">Eksportuje właściwości (Użycie dysku i Acl) dla całego drzewa z określonej ścieżki do ścieżki wyjściowej.</span><span class="sxs-lookup"><span data-stu-id="a73c9-103">Exports the properties (Disk usage and Acl) for the entire tree from the specified path to a output path</span></span>

## <span data-ttu-id="a73c9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a73c9-104">SYNTAX</span></span>

### <span data-ttu-id="a73c9-105">Get JednakowyUsage</span><span class="sxs-lookup"><span data-stu-id="a73c9-105">GetDiskUsage</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a73c9-106">GetAllProperties</span><span class="sxs-lookup"><span data-stu-id="a73c9-106">GetAllProperties</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-GetAcl] [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a73c9-107">GetAclDump</span><span class="sxs-lookup"><span data-stu-id="a73c9-107">GetAclDump</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>] [-GetAcl]
 [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a73c9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a73c9-108">DESCRIPTION</span></span>
<span data-ttu-id="a73c9-109">**Eksport-AzDataLakeStoreChildItemProperty** służy do zgłaszania użycia miejsca w usłudze ADLS lub/i ACL dla danego katalogu oraz jest to podkategorie i pliki.</span><span class="sxs-lookup"><span data-stu-id="a73c9-109">The **Export-AzDataLakeStoreChildItemProperty** is used to report the ADLS space usage or/and ACL usage for the given directory and it's sub directories and files.</span></span>

## <span data-ttu-id="a73c9-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a73c9-110">EXAMPLES</span></span>

### <span data-ttu-id="a73c9-111">Przykład 1. Uzyskiwanie użycia dysku i użycia listy ACL dla wszystkich podkategorie i plików</span><span class="sxs-lookup"><span data-stu-id="a73c9-111">Example 1: Get the disk usage and ACL usage for all subdirectories and files</span></span>
```
PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -GetDiskUsage -IncludeFile
```

<span data-ttu-id="a73c9-112">Uzyskaj informacje o użyciu dysku i ACL dla wszystkich podkategorie i plików w obszarze /a.</span><span class="sxs-lookup"><span data-stu-id="a73c9-112">Get the disk usage and ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="a73c9-113">IncludeFile zapewnia, że użycie plików jest również zgłaszane</span><span class="sxs-lookup"><span data-stu-id="a73c9-113">IncludeFile ensures the usage is reported for files also</span></span>

### <span data-ttu-id="a73c9-114">Przykład 2. Uzyskiwanie użycia listy ACL dla wszystkich podkategorie i plików ze spójnym ukrytym listą ACL</span><span class="sxs-lookup"><span data-stu-id="a73c9-114">Example 2: Get the ACL usage for all subdirectories and files with the consistent ACL hidden</span></span>
```
PS C:\> $fullAcl="user:contoso-userid:--x|user::rwx|other::---|group::rwx"
PS C:\> $newFullAcl = $fullAcl.Split("{|}");
PS C:\> Set-AzDataLakeStoreItemAcl -Account ContosoADL -Path /a -Acl $newFullAcl -Recurse -Debug

PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -HideConsistentAcl -IncludeFile
```

<span data-ttu-id="a73c9-115">Uzyskaj użycie listy ACL dla wszystkich podkategori i plików w obszarze /a.</span><span class="sxs-lookup"><span data-stu-id="a73c9-115">Get the ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="a73c9-116">Użycie funkcji IncludeFile jest również zgłaszane w przypadku plików.</span><span class="sxs-lookup"><span data-stu-id="a73c9-116">IncludeFile ensures the usage is reported for files also.</span></span> <span data-ttu-id="a73c9-117">HideconsistentAcl w tym przypadku będzie pokazywać acl /a, a nie dzieci, ponieważ wszystkie dzieci mają taką samą acl jak /a.</span><span class="sxs-lookup"><span data-stu-id="a73c9-117">HideconsistentAcl in this case will show the Acl of /a, not it's children since all of the children has same acl as /a.</span></span> <span data-ttu-id="a73c9-118">Ta flaga pomija wynik acl drzew podrzędnych, jeśli wszystkie jej listy są takie same jak w katalogu głównym.</span><span class="sxs-lookup"><span data-stu-id="a73c9-118">This flag skips the acl output of subtree if all it's acls are same as the root.</span></span>

## <span data-ttu-id="a73c9-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a73c9-119">PARAMETERS</span></span>

### <span data-ttu-id="a73c9-120">— Konto</span><span class="sxs-lookup"><span data-stu-id="a73c9-120">-Account</span></span>
<span data-ttu-id="a73c9-121">Konto magazynu Data Lake Store w celu wykonania operacji systemu plików w</span><span class="sxs-lookup"><span data-stu-id="a73c9-121">The Data Lake Store account to execute the filesystem operation in</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73c9-122">— współbieżność</span><span class="sxs-lookup"><span data-stu-id="a73c9-122">-Concurrency</span></span>
<span data-ttu-id="a73c9-123">Wskazuje liczbę plików/katalogów przetwarzanych równolegle.</span><span class="sxs-lookup"><span data-stu-id="a73c9-123">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="a73c9-124">Wartość domyślna zostanie obliczona według najlepszych starań, na podstawie specyfikacji systemu.</span><span class="sxs-lookup"><span data-stu-id="a73c9-124">Default will be computed as a best effort based on system specification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73c9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a73c9-125">-DefaultProfile</span></span>
<span data-ttu-id="a73c9-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a73c9-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a73c9-127">-GetAcl</span><span class="sxs-lookup"><span data-stu-id="a73c9-127">-GetAcl</span></span>
<span data-ttu-id="a73c9-128">Pobiera acl, rozpoczynając od ścieżki głównej</span><span class="sxs-lookup"><span data-stu-id="a73c9-128">Retrieves the acl starting from the root path</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73c9-129">-Get InformacjeUsage</span><span class="sxs-lookup"><span data-stu-id="a73c9-129">-GetDiskUsage</span></span>
<span data-ttu-id="a73c9-130">Pobiera użycie dysku od ścieżki głównej.</span><span class="sxs-lookup"><span data-stu-id="a73c9-130">Retrieves the disk usage starting from the root path</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetDiskUsage, GetAllProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73c9-131">-HideConsistentAcl</span><span class="sxs-lookup"><span data-stu-id="a73c9-131">-HideConsistentAcl</span></span>
<span data-ttu-id="a73c9-132">Nie pokazuj drzew podrzędnego katalogu, jeśli adresy ACL są takie same w całym drzewie podrzędnym.</span><span class="sxs-lookup"><span data-stu-id="a73c9-132">Do not show directory subtree if the ACLs are the same throughout the entire subtree.</span></span> <span data-ttu-id="a73c9-133">Dzięki temu łatwiej będzie zobaczyć tylko ścieżki, do których różnią się ACL. Jeśli na przykład wszystkie pliki i foldery w obszarze /a/b są takie same, nie są wyświetlane podczerwone /a/b, a jedynie dane wyjściowe /a/b z wartością "True" w kolumnie Spójna kolumna ACLCannot nie można ustawić, jeśli wartość IncludeFiles nie jest ustawiona, ponieważ spójnego pola Acl nie można ustalić bez pobierania wartości acl dla plików.</span><span class="sxs-lookup"><span data-stu-id="a73c9-133">This makes it easier to see only the paths up to which the ACLs differ.For example if all files and folders under /a/b are the same, do not show the subtreeunder /a/b, and just output /a/b with 'True' in the Consistent ACL columnCannot be set if IncludeFiles is not set, because consistent Acl cannot be determined without retrieving acls for the files.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73c9-134">-IncludeFile</span><span class="sxs-lookup"><span data-stu-id="a73c9-134">-IncludeFile</span></span>
<span data-ttu-id="a73c9-135">Pokaż statystykę na poziomie pliku (domyślnie są wyświetlane tylko informacje na poziomie katalogu)</span><span class="sxs-lookup"><span data-stu-id="a73c9-135">Show stats at file level (default is to show directory-level info only)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73c9-136">-MaximumDepth</span><span class="sxs-lookup"><span data-stu-id="a73c9-136">-MaximumDepth</span></span>
<span data-ttu-id="a73c9-137">Maksymalna głębokość z katalogu głównego do czasu wyświetlania użycia dysku lub listy</span><span class="sxs-lookup"><span data-stu-id="a73c9-137">Maximum depth from the root directory till which disk usage or acl is displayed</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73c9-138">- OutputPath</span><span class="sxs-lookup"><span data-stu-id="a73c9-138">-OutputPath</span></span>
<span data-ttu-id="a73c9-139">Ścieżka do pliku wyjściowego.</span><span class="sxs-lookup"><span data-stu-id="a73c9-139">Path to output file.</span></span> <span data-ttu-id="a73c9-140">Może być ścieżką lokalną lub ścieżką ADL.</span><span class="sxs-lookup"><span data-stu-id="a73c9-140">Can be a Local path or Adl Path.</span></span> <span data-ttu-id="a73c9-141">Domyślnie jest to ustawienie lokalne.</span><span class="sxs-lookup"><span data-stu-id="a73c9-141">By default it is local.</span></span> <span data-ttu-id="a73c9-142">Jeśli jest określony zapis SaveToAdl, jest to ścieżka ADL na tym samym koncie</span><span class="sxs-lookup"><span data-stu-id="a73c9-142">If SaveToAdl is specified then it is an ADL path in the same account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73c9-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a73c9-143">-PassThru</span></span>
<span data-ttu-id="a73c9-144">Wskazuje, że powinna zostać zwrócona odpowiedź logiczna wskazująca wynik operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="a73c9-144">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73c9-145">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="a73c9-145">-Path</span></span>
<span data-ttu-id="a73c9-146">Ścieżka na określonym koncie data lake, które ma zostać pobrane.</span><span class="sxs-lookup"><span data-stu-id="a73c9-146">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="a73c9-147">Może to być plik lub folder W formacie "/folder/file.txt", gdzie pierwszy "/" po systemie DNS wskazuje katalog główny systemu plików.</span><span class="sxs-lookup"><span data-stu-id="a73c9-147">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73c9-148">-SaveToAdl</span><span class="sxs-lookup"><span data-stu-id="a73c9-148">-SaveToAdl</span></span>
<span data-ttu-id="a73c9-149">Jeśli pomyślnie to zda, zapisze plik zrzutu w pliku ADL.</span><span class="sxs-lookup"><span data-stu-id="a73c9-149">If passed then saves the dump file to ADL.</span></span>
<span data-ttu-id="a73c9-150">W takim przypadku plik Pochwowy może być ścieżką ADL</span><span class="sxs-lookup"><span data-stu-id="a73c9-150">The DumpFile wil be a ADL path in that case</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73c9-151">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a73c9-151">-Confirm</span></span>
<span data-ttu-id="a73c9-152">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a73c9-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a73c9-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a73c9-153">-WhatIf</span></span>
<span data-ttu-id="a73c9-154">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a73c9-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a73c9-155">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a73c9-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a73c9-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a73c9-156">CommonParameters</span></span>
<span data-ttu-id="a73c9-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a73c9-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a73c9-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a73c9-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a73c9-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a73c9-159">INPUTS</span></span>

### <span data-ttu-id="a73c9-160">System.String</span><span class="sxs-lookup"><span data-stu-id="a73c9-160">System.String</span></span>

### <span data-ttu-id="a73c9-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="a73c9-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="a73c9-162">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="a73c9-162">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a73c9-163">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a73c9-163">System.Int32</span></span>

## <span data-ttu-id="a73c9-164">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a73c9-164">OUTPUTS</span></span>

### <span data-ttu-id="a73c9-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a73c9-165">System.Boolean</span></span>

## <span data-ttu-id="a73c9-166">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a73c9-166">NOTES</span></span>

## <span data-ttu-id="a73c9-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a73c9-167">RELATED LINKS</span></span>
