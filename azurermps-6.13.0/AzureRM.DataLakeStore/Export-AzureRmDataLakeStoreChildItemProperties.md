---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azureatalakestorechilditemproperties
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreChildItemProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreChildItemProperties.md
ms.openlocfilehash: faaf8a0c614a1243a3e3812cd0b6e1202cc7e75b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548723"
---
# <span data-ttu-id="80fe4-101">Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="80fe4-101">Export-AzureRmDataLakeStoreChildItemProperties</span></span>

## <span data-ttu-id="80fe4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="80fe4-102">SYNOPSIS</span></span>
<span data-ttu-id="80fe4-103">Eksportuje właściwości (użycie dysku i listę ACL) dla całego drzewa z określonej ścieżki do ścieżki ouput.</span><span class="sxs-lookup"><span data-stu-id="80fe4-103">Exports the properties (Disk usage and Acl) for the entire tree from the specified path to a ouput path</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80fe4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="80fe4-104">SYNTAX</span></span>

### <span data-ttu-id="80fe4-105">GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="80fe4-105">GetDiskUsage</span></span>
```
Export-AzureRmDataLakeStoreChildItemProperties [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80fe4-106">GetAllProperties</span><span class="sxs-lookup"><span data-stu-id="80fe4-106">GetAllProperties</span></span>
```
Export-AzureRmDataLakeStoreChildItemProperties [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-GetAcl] [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80fe4-107">GetAclDump</span><span class="sxs-lookup"><span data-stu-id="80fe4-107">GetAclDump</span></span>
```
Export-AzureRmDataLakeStoreChildItemProperties [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>] [-GetAcl]
 [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="80fe4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="80fe4-108">DESCRIPTION</span></span>
<span data-ttu-id="80fe4-109">Element **Export-AzureRmDataLakeStoreChildItemProperties** jest wykorzystywany do raportowania ADLS użycia miejsca na dysku lub/lub listy ACL dla danego katalogu, a jego podkatalogi i pliki.</span><span class="sxs-lookup"><span data-stu-id="80fe4-109">The **Export-AzureRmDataLakeStoreChildItemProperties** is used to report the ADLS space usage or/and ACL usage for the given directory and it's sub directories and files.</span></span>

## <span data-ttu-id="80fe4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="80fe4-110">EXAMPLES</span></span>

### <span data-ttu-id="80fe4-111">Przykład 1: uzyskiwanie użycia dysku i listy ACL dla wszystkich podkatalogów i plików</span><span class="sxs-lookup"><span data-stu-id="80fe4-111">Example 1: Get the disk usage and ACL usage for all subdirectories and files</span></span>
```
PS C:\> Export-AzureRmDataLakeStoreChildItemProperties -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -GetDiskUsage -IncludeFile
```

<span data-ttu-id="80fe4-112">Uzyskiwanie użycia dysku i listy ACL dla wszystkich podkatalogów i plików w obszarze/a.</span><span class="sxs-lookup"><span data-stu-id="80fe4-112">Get the disk usage and ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="80fe4-113">IncludeFile gwarantuje, że użycie jest zgłaszane również dla plików</span><span class="sxs-lookup"><span data-stu-id="80fe4-113">IncludeFile ensures the usage is reported for files also</span></span>

### <span data-ttu-id="80fe4-114">Przykład 2: uzyskiwanie użycia listy ACL dla wszystkich podkatalogów i plików ze spójnym ukrytym listą ACL</span><span class="sxs-lookup"><span data-stu-id="80fe4-114">Example 2: Get the ACL usage for all subdirectories and files with the consistent ACL hidden</span></span>
```
PS C:\> $fullAcl="user:contoso-userid:--x|user::rwx|other::---|group::rwx"
PS C:\> $newFullAcl = $fullAcl.Split("{|}");
PS C:\> Set-AzureRmDataLakeStoreItemAcl -Account ContosoADL -Path /a -Acl $newFullAcl -Recurse -Debug

PS C:\> Export-AzureRmDataLakeStoreChildItemProperties -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -HideConsistentAcl -IncludeFile
```

<span data-ttu-id="80fe4-115">Uzyskiwanie użycia listy ACL dla wszystkich podkatalogów i plików w obszarze/a.</span><span class="sxs-lookup"><span data-stu-id="80fe4-115">Get the ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="80fe4-116">IncludeFile gwarantuje, że użycie jest zgłaszane również dla plików.</span><span class="sxs-lookup"><span data-stu-id="80fe4-116">IncludeFile ensures the usage is reported for files also.</span></span> <span data-ttu-id="80fe4-117">W HideconsistentAcl w tym przypadku zostanie wyświetlona lista ACL:/a, a nie jej dzieci, ponieważ wszystkie elementy podrzędne mają tę samą listę ACL co/a.</span><span class="sxs-lookup"><span data-stu-id="80fe4-117">HideconsistentAcl in this case will show the Acl of /a, not it's children since all of the children has same acl as /a.</span></span> <span data-ttu-id="80fe4-118">Ta flaga powoduje pominięcie ouput ACL w poddrzewie, jeśli wszystkie listy ACL są takie same jak w katalogu głównym.</span><span class="sxs-lookup"><span data-stu-id="80fe4-118">This flag skips the acl ouput of subtree if all it's acls are same as the root.</span></span>

## <span data-ttu-id="80fe4-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="80fe4-119">PARAMETERS</span></span>

### <span data-ttu-id="80fe4-120">— Konto</span><span class="sxs-lookup"><span data-stu-id="80fe4-120">-Account</span></span>
<span data-ttu-id="80fe4-121">Konto usługi Data Lake Store do wykonywania operacji na systemie plików</span><span class="sxs-lookup"><span data-stu-id="80fe4-121">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="80fe4-122">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="80fe4-122">-Concurrency</span></span>
<span data-ttu-id="80fe4-123">Wskazuje liczbę plików/katalogów przetworzonych równolegle.</span><span class="sxs-lookup"><span data-stu-id="80fe4-123">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="80fe4-124">Wartość domyślna będzie obliczana jako Najlepsza nakład pracy na podstawie specyfikacji systemu.</span><span class="sxs-lookup"><span data-stu-id="80fe4-124">Default will be computed as a best effort based on system specification.</span></span>

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

### <span data-ttu-id="80fe4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80fe4-125">-DefaultProfile</span></span>
<span data-ttu-id="80fe4-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="80fe4-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80fe4-127">-GetAcl</span><span class="sxs-lookup"><span data-stu-id="80fe4-127">-GetAcl</span></span>
<span data-ttu-id="80fe4-128">Pobiera listę ACL rozpoczynającą się od ścieżki katalogu głównego</span><span class="sxs-lookup"><span data-stu-id="80fe4-128">Retrieves the acl starting from the root path</span></span>

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

### <span data-ttu-id="80fe4-129">-GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="80fe4-129">-GetDiskUsage</span></span>
<span data-ttu-id="80fe4-130">Pobiera użycie dysku od ścieżki katalogu głównego.</span><span class="sxs-lookup"><span data-stu-id="80fe4-130">Retrieves the disk usage starting from the root path</span></span>

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

### <span data-ttu-id="80fe4-131">-HideConsistentAcl</span><span class="sxs-lookup"><span data-stu-id="80fe4-131">-HideConsistentAcl</span></span>
<span data-ttu-id="80fe4-132">Nie pokazuj poddrzewa katalogu, jeśli listy ACL są takie same w całym poddrzewie.</span><span class="sxs-lookup"><span data-stu-id="80fe4-132">Do not show directory subtree if the ACLs are the same throughout the entire subtree.</span></span> <span data-ttu-id="80fe4-133">Ułatwia to wyświetlanie tylko ścieżek, których listy ACL są różne. Jeśli na przykład wszystkie pliki i foldery w obszarze/a/b są takie same, nie wyświetlaj/a/b subtreeunder, a po prostu/a/b o wartości "prawda" w spójnym zbiorze danych listy kontroli dostępu columnCannot można ustawić, że IncludeFiles nie jest ustawiona, ponieważ nie można określić listy ACL dla tych plików.</span><span class="sxs-lookup"><span data-stu-id="80fe4-133">This makes it easier to see only the paths up to which the ACLs differ.For example if all files and folders under /a/b are the same, do not show the subtreeunder /a/b, and just output /a/b with 'True' in the Consistent ACL columnCannot be set if IncludeFiles is not set, because consistent Acl cannot be determined without retrieving acls for the files.</span></span>

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

### <span data-ttu-id="80fe4-134">-IncludeFile</span><span class="sxs-lookup"><span data-stu-id="80fe4-134">-IncludeFile</span></span>
<span data-ttu-id="80fe4-135">Pokaż statystykę na poziomie pliku (domyślnie wyświetlane są tylko informacje na poziomie katalogu)</span><span class="sxs-lookup"><span data-stu-id="80fe4-135">Show stats at file level (default is to show directory-level info only)</span></span>

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

### <span data-ttu-id="80fe4-136">-MaximumDepth</span><span class="sxs-lookup"><span data-stu-id="80fe4-136">-MaximumDepth</span></span>
<span data-ttu-id="80fe4-137">Maksymalna głębokość katalogu głównego, do którego są wyświetlane użycie dysku lub lista ACL</span><span class="sxs-lookup"><span data-stu-id="80fe4-137">Maximum depth from the root directory till which disk usage or acl is displayed</span></span>

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

### <span data-ttu-id="80fe4-138">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="80fe4-138">-OutputPath</span></span>
<span data-ttu-id="80fe4-139">Ścieżka do pliku wyjściowego.</span><span class="sxs-lookup"><span data-stu-id="80fe4-139">Path to output file.</span></span> <span data-ttu-id="80fe4-140">Może to być ścieżka lokalna lub ADL.</span><span class="sxs-lookup"><span data-stu-id="80fe4-140">Can be a Local path or Adl Path.</span></span> <span data-ttu-id="80fe4-141">Domyślnie jest to ustawienie lokalne.</span><span class="sxs-lookup"><span data-stu-id="80fe4-141">By default it is local.</span></span> <span data-ttu-id="80fe4-142">Jeśli SaveToAdl jest pecified, jest to ADL ścieżka na tym samym koncie</span><span class="sxs-lookup"><span data-stu-id="80fe4-142">If SaveToAdl is pecified then it is an ADL path in the same account</span></span>

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

### <span data-ttu-id="80fe4-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80fe4-143">-PassThru</span></span>
<span data-ttu-id="80fe4-144">Wskazuje, że należy zwrócić odpowiedź logiczną wskazującą wynik operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="80fe4-144">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="80fe4-145">-Path</span><span class="sxs-lookup"><span data-stu-id="80fe4-145">-Path</span></span>
<span data-ttu-id="80fe4-146">Ścieżka na określonym koncie Data Lake, które powinno być pobrane.</span><span class="sxs-lookup"><span data-stu-id="80fe4-146">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="80fe4-147">Może to być plik lub folder w formacie "/folder/file.txt", gdzie pierwszy znak "/" po systemie DNS wskazuje katalog główny systemu plików.</span><span class="sxs-lookup"><span data-stu-id="80fe4-147">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

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

### <span data-ttu-id="80fe4-148">-SaveToAdl</span><span class="sxs-lookup"><span data-stu-id="80fe4-148">-SaveToAdl</span></span>
<span data-ttu-id="80fe4-149">Jeśli przekazano, następnie zapisze plik zrzutu w ADL.</span><span class="sxs-lookup"><span data-stu-id="80fe4-149">If passed then saves the dump file to ADL.</span></span>
<span data-ttu-id="80fe4-150">W takim przypadku będzie DumpFile jest ścieżką ADL</span><span class="sxs-lookup"><span data-stu-id="80fe4-150">The DumpFile wil be a ADL path in that case</span></span>

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

### <span data-ttu-id="80fe4-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="80fe4-151">-Confirm</span></span>
<span data-ttu-id="80fe4-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80fe4-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80fe4-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80fe4-153">-WhatIf</span></span>
<span data-ttu-id="80fe4-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80fe4-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80fe4-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="80fe4-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80fe4-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80fe4-156">CommonParameters</span></span>
<span data-ttu-id="80fe4-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80fe4-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80fe4-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80fe4-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80fe4-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80fe4-159">INPUTS</span></span>

### <span data-ttu-id="80fe4-160">System. String</span><span class="sxs-lookup"><span data-stu-id="80fe4-160">System.String</span></span>

### <span data-ttu-id="80fe4-161">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="80fe4-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="80fe4-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="80fe4-162">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="80fe4-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="80fe4-163">System.Int32</span></span>

## <span data-ttu-id="80fe4-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="80fe4-164">OUTPUTS</span></span>

### <span data-ttu-id="80fe4-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="80fe4-165">System.Boolean</span></span>

## <span data-ttu-id="80fe4-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="80fe4-166">NOTES</span></span>

## <span data-ttu-id="80fe4-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80fe4-167">RELATED LINKS</span></span>
