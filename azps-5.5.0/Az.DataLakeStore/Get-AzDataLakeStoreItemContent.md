---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
ms.openlocfilehash: e5aaff4f915143e2e7695c9f650aed6fb01ba389
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196570"
---
# <span data-ttu-id="49eb1-101">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="49eb1-101">Get-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="49eb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49eb1-102">SYNOPSIS</span></span>
<span data-ttu-id="49eb1-103">Pobiera zawartość pliku w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="49eb1-103">Gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="49eb1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="49eb1-104">SYNTAX</span></span>

### <span data-ttu-id="49eb1-105">PreviewFileContent (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="49eb1-105">PreviewFileContent (Default)</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <Encoding>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49eb1-106">PreviewFileRowsFromHead</span><span class="sxs-lookup"><span data-stu-id="49eb1-106">PreviewFileRowsFromHead</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49eb1-107">PreviewFileRowsFromTail</span><span class="sxs-lookup"><span data-stu-id="49eb1-107">PreviewFileRowsFromTail</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49eb1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="49eb1-108">DESCRIPTION</span></span>
<span data-ttu-id="49eb1-109">Polecenie **cmdlet Get-AzDataLakeStoreItemContent** pobiera zawartość pliku w magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="49eb1-109">The **Get-AzDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="49eb1-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="49eb1-110">EXAMPLES</span></span>

### <span data-ttu-id="49eb1-111">Przykład 1. Uzyskiwanie zawartości pliku</span><span class="sxs-lookup"><span data-stu-id="49eb1-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="49eb1-112">To polecenie pobiera zawartość pliku MyFile.txt na koncie ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="49eb1-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="49eb1-113">Przykład 2. Uzyskiwanie pierwszych dwóch wierszy pliku</span><span class="sxs-lookup"><span data-stu-id="49eb1-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="49eb1-114">To polecenie pobiera dwa pierwsze nowe wiersze rozdzielone wierszami w pliku, MyFile.txt na koncie ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="49eb1-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="49eb1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49eb1-115">PARAMETERS</span></span>

### <span data-ttu-id="49eb1-116">— Konto</span><span class="sxs-lookup"><span data-stu-id="49eb1-116">-Account</span></span>
<span data-ttu-id="49eb1-117">Określa nazwę konta sklepu Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="49eb1-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="49eb1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49eb1-118">-DefaultProfile</span></span>
<span data-ttu-id="49eb1-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="49eb1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49eb1-120">— Kodowanie</span><span class="sxs-lookup"><span data-stu-id="49eb1-120">-Encoding</span></span>
<span data-ttu-id="49eb1-121">Określa kodowanie elementu do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="49eb1-121">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="49eb1-122">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="49eb1-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="49eb1-123">Nieznany</span><span class="sxs-lookup"><span data-stu-id="49eb1-123">Unknown</span></span>
- <span data-ttu-id="49eb1-124">Ciąg</span><span class="sxs-lookup"><span data-stu-id="49eb1-124">String</span></span>
- <span data-ttu-id="49eb1-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="49eb1-125">Unicode</span></span>
- <span data-ttu-id="49eb1-126">Bajt</span><span class="sxs-lookup"><span data-stu-id="49eb1-126">Byte</span></span>
- <span data-ttu-id="49eb1-127">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="49eb1-127">BigEndianUnicode</span></span>
- <span data-ttu-id="49eb1-128">UTF8</span><span class="sxs-lookup"><span data-stu-id="49eb1-128">UTF8</span></span>
- <span data-ttu-id="49eb1-129">UTF7</span><span class="sxs-lookup"><span data-stu-id="49eb1-129">UTF7</span></span>
- <span data-ttu-id="49eb1-130">Ascii</span><span class="sxs-lookup"><span data-stu-id="49eb1-130">Ascii</span></span>
- <span data-ttu-id="49eb1-131">Domyślne</span><span class="sxs-lookup"><span data-stu-id="49eb1-131">Default</span></span>
- <span data-ttu-id="49eb1-132">Oem</span><span class="sxs-lookup"><span data-stu-id="49eb1-132">Oem</span></span>
- <span data-ttu-id="49eb1-133">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="49eb1-133">BigEndianUTF32</span></span>

```yaml
Type: System.Text.Encoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49eb1-134">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="49eb1-134">-Force</span></span>
<span data-ttu-id="49eb1-135">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="49eb1-135">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49eb1-136">— Head</span><span class="sxs-lookup"><span data-stu-id="49eb1-136">-Head</span></span>
<span data-ttu-id="49eb1-137">Liczba wierszy (rozdzielanych nowymi wierszami) od początku pliku do podglądu.</span><span class="sxs-lookup"><span data-stu-id="49eb1-137">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="49eb1-138">Jeśli w pierwszych 4 mb danych nie zostanie napotkany żaden nowy wiersz, zostaną zwrócone tylko te dane.</span><span class="sxs-lookup"><span data-stu-id="49eb1-138">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: PreviewFileRowsFromHead
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49eb1-139">-Length</span><span class="sxs-lookup"><span data-stu-id="49eb1-139">-Length</span></span>
<span data-ttu-id="49eb1-140">Określa w bajtach długość zawartości, która ma być uzyskaja.</span><span class="sxs-lookup"><span data-stu-id="49eb1-140">Specifies the length, in bytes, of the content to get.</span></span>

```yaml
Type: System.Int64
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49eb1-141">— Przesunięcie</span><span class="sxs-lookup"><span data-stu-id="49eb1-141">-Offset</span></span>
<span data-ttu-id="49eb1-142">Określa liczbę bajtów, które mają być pomijane w pliku przed uzyskaniem zawartości.</span><span class="sxs-lookup"><span data-stu-id="49eb1-142">Specifies the number of bytes to skip in a file before getting content.</span></span>

```yaml
Type: System.Int64
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49eb1-143">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="49eb1-143">-Path</span></span>
<span data-ttu-id="49eb1-144">Określa ścieżkę pliku do magazynu data lake, zaczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="49eb1-144">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="49eb1-145">- Tail</span><span class="sxs-lookup"><span data-stu-id="49eb1-145">-Tail</span></span>
<span data-ttu-id="49eb1-146">Liczba wierszy (rozdzielanych nowymi wierszami) od końca pliku do podglądu.</span><span class="sxs-lookup"><span data-stu-id="49eb1-146">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="49eb1-147">Jeśli w pierwszych 4 mb danych nie zostanie napotkany żaden nowy wiersz, zostaną zwrócone tylko te dane.</span><span class="sxs-lookup"><span data-stu-id="49eb1-147">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: PreviewFileRowsFromTail
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49eb1-148">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49eb1-148">-Confirm</span></span>
<span data-ttu-id="49eb1-149">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="49eb1-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49eb1-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49eb1-150">-WhatIf</span></span>
<span data-ttu-id="49eb1-151">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49eb1-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49eb1-152">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="49eb1-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49eb1-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49eb1-153">CommonParameters</span></span>
<span data-ttu-id="49eb1-154">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49eb1-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49eb1-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49eb1-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49eb1-156">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49eb1-156">INPUTS</span></span>

### <span data-ttu-id="49eb1-157">System.String</span><span class="sxs-lookup"><span data-stu-id="49eb1-157">System.String</span></span>

### <span data-ttu-id="49eb1-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="49eb1-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="49eb1-159">System.Int32</span><span class="sxs-lookup"><span data-stu-id="49eb1-159">System.Int32</span></span>

### <span data-ttu-id="49eb1-160">System.Int64</span><span class="sxs-lookup"><span data-stu-id="49eb1-160">System.Int64</span></span>

### <span data-ttu-id="49eb1-161">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="49eb1-161">System.Text.Encoding</span></span>

### <span data-ttu-id="49eb1-162">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="49eb1-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="49eb1-163">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49eb1-163">OUTPUTS</span></span>

### <span data-ttu-id="49eb1-164">System.Byte</span><span class="sxs-lookup"><span data-stu-id="49eb1-164">System.Byte</span></span>

### <span data-ttu-id="49eb1-165">System.String</span><span class="sxs-lookup"><span data-stu-id="49eb1-165">System.String</span></span>

## <span data-ttu-id="49eb1-166">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="49eb1-166">NOTES</span></span>

## <span data-ttu-id="49eb1-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49eb1-167">RELATED LINKS</span></span>
