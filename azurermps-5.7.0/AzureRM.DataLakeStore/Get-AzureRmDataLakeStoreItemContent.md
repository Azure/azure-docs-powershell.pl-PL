---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 28e314f5ac7306233c3e2a3619a1a332dd6f3314
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717007"
---
# <span data-ttu-id="59bed-101">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="59bed-101">Get-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="59bed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="59bed-102">SYNOPSIS</span></span>
<span data-ttu-id="59bed-103">Pobiera zawartość pliku w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="59bed-103">Gets the contents of a file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59bed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="59bed-104">SYNTAX</span></span>

### <span data-ttu-id="59bed-105">PreviewFileContent (domyślny)</span><span class="sxs-lookup"><span data-stu-id="59bed-105">PreviewFileContent (Default)</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59bed-106">PreviewFileRowsFromHead</span><span class="sxs-lookup"><span data-stu-id="59bed-106">PreviewFileRowsFromHead</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59bed-107">PreviewFileRowsFromTail</span><span class="sxs-lookup"><span data-stu-id="59bed-107">PreviewFileRowsFromTail</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59bed-108">Opis</span><span class="sxs-lookup"><span data-stu-id="59bed-108">DESCRIPTION</span></span>
<span data-ttu-id="59bed-109">Polecenie cmdlet **Get-AzureRmDataLakeStoreItemContent** pobiera zawartość pliku w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="59bed-109">The **Get-AzureRmDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="59bed-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="59bed-110">EXAMPLES</span></span>

### <span data-ttu-id="59bed-111">Przykład 1. pobieranie zawartości pliku</span><span class="sxs-lookup"><span data-stu-id="59bed-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="59bed-112">To polecenie pobiera zawartość pliku MyFile.txt na koncie ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="59bed-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="59bed-113">Przykład 2: uzyskiwanie dwóch pierwszych wierszy pliku</span><span class="sxs-lookup"><span data-stu-id="59bed-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="59bed-114">To polecenie powoduje wyświetlenie dwóch pierwszych nowych wierszy rozdzielanych wierszami w pliku MyFile.txt na koncie ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="59bed-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="59bed-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="59bed-115">PARAMETERS</span></span>

### <span data-ttu-id="59bed-116">— Konto</span><span class="sxs-lookup"><span data-stu-id="59bed-116">-Account</span></span>
<span data-ttu-id="59bed-117">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="59bed-117">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59bed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59bed-118">-DefaultProfile</span></span>
<span data-ttu-id="59bed-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="59bed-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bed-120">-Encoding</span><span class="sxs-lookup"><span data-stu-id="59bed-120">-Encoding</span></span>
<span data-ttu-id="59bed-121">Określa kodowanie elementu, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="59bed-121">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="59bed-122">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="59bed-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="59bed-123">Wiadom</span><span class="sxs-lookup"><span data-stu-id="59bed-123">Unknown</span></span>
- <span data-ttu-id="59bed-124">Ciąg</span><span class="sxs-lookup"><span data-stu-id="59bed-124">String</span></span>
- <span data-ttu-id="59bed-125">Ze</span><span class="sxs-lookup"><span data-stu-id="59bed-125">Unicode</span></span>
- <span data-ttu-id="59bed-126">Jednobajtowe</span><span class="sxs-lookup"><span data-stu-id="59bed-126">Byte</span></span>
- <span data-ttu-id="59bed-127">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="59bed-127">BigEndianUnicode</span></span>
- <span data-ttu-id="59bed-128">UTF8</span><span class="sxs-lookup"><span data-stu-id="59bed-128">UTF8</span></span>
- <span data-ttu-id="59bed-129">UTF7</span><span class="sxs-lookup"><span data-stu-id="59bed-129">UTF7</span></span>
- <span data-ttu-id="59bed-130">Znaki</span><span class="sxs-lookup"><span data-stu-id="59bed-130">Ascii</span></span>
- <span data-ttu-id="59bed-131">Domyślne</span><span class="sxs-lookup"><span data-stu-id="59bed-131">Default</span></span>
- <span data-ttu-id="59bed-132">Equipment</span><span class="sxs-lookup"><span data-stu-id="59bed-132">Oem</span></span>
- <span data-ttu-id="59bed-133">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="59bed-133">BigEndianUTF32</span></span>

```yaml
Type: FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59bed-134">-Force</span><span class="sxs-lookup"><span data-stu-id="59bed-134">-Force</span></span>
<span data-ttu-id="59bed-135">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="59bed-135">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PreviewFileContent
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59bed-136">-Head</span><span class="sxs-lookup"><span data-stu-id="59bed-136">-Head</span></span>
<span data-ttu-id="59bed-137">Liczba wierszy (rozdzielanych wierszami) od początku pliku do wyświetlenia podglądu.</span><span class="sxs-lookup"><span data-stu-id="59bed-137">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="59bed-138">Jeśli nie zostanie napotkany żaden nowy wiersz w pierwszych 4 MB danych, zostaną zwrócone tylko te dane.</span><span class="sxs-lookup"><span data-stu-id="59bed-138">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: Int32
Parameter Sets: PreviewFileRowsFromHead
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59bed-139">-Length</span><span class="sxs-lookup"><span data-stu-id="59bed-139">-Length</span></span>
<span data-ttu-id="59bed-140">Określa długość zawartości (w bajtach), którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="59bed-140">Specifies the length, in bytes, of the content to get.</span></span>

```yaml
Type: Int64
Parameter Sets: PreviewFileContent
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59bed-141">-Przesunięcie</span><span class="sxs-lookup"><span data-stu-id="59bed-141">-Offset</span></span>
<span data-ttu-id="59bed-142">Określa liczbę bajtów, które należy pominąć w pliku przed uzyskaniem zawartości.</span><span class="sxs-lookup"><span data-stu-id="59bed-142">Specifies the number of bytes to skip in a file before getting content.</span></span>

```yaml
Type: Int64
Parameter Sets: PreviewFileContent
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59bed-143">-Path</span><span class="sxs-lookup"><span data-stu-id="59bed-143">-Path</span></span>
<span data-ttu-id="59bed-144">Określa ścieżkę pliku Data Lake Store, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="59bed-144">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59bed-145">-Koniec</span><span class="sxs-lookup"><span data-stu-id="59bed-145">-Tail</span></span>
<span data-ttu-id="59bed-146">Liczba wierszy (rozdzielanych wierszami) od końca pliku do wyświetlenia podglądu.</span><span class="sxs-lookup"><span data-stu-id="59bed-146">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="59bed-147">Jeśli nie zostanie napotkany żaden nowy wiersz w pierwszych 4 MB danych, zostaną zwrócone tylko te dane.</span><span class="sxs-lookup"><span data-stu-id="59bed-147">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: Int32
Parameter Sets: PreviewFileRowsFromTail
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59bed-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="59bed-148">-Confirm</span></span>
<span data-ttu-id="59bed-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59bed-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bed-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59bed-150">-WhatIf</span></span>
<span data-ttu-id="59bed-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59bed-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59bed-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="59bed-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bed-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59bed-153">CommonParameters</span></span>
<span data-ttu-id="59bed-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59bed-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59bed-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59bed-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59bed-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59bed-156">INPUTS</span></span>

### <span data-ttu-id="59bed-157">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="59bed-157">None</span></span>
<span data-ttu-id="59bed-158">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="59bed-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="59bed-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="59bed-159">OUTPUTS</span></span>

### <span data-ttu-id="59bed-160">Byte []</span><span class="sxs-lookup"><span data-stu-id="59bed-160">byte[]</span></span>
<span data-ttu-id="59bed-161">Bajtowa reprezentacja zawartości pliku w strumieniu bajtów została pobrana.</span><span class="sxs-lookup"><span data-stu-id="59bed-161">The byte stream representation of the file contents retrieved.</span></span>

### <span data-ttu-id="59bed-162">ciąg</span><span class="sxs-lookup"><span data-stu-id="59bed-162">string</span></span>
<span data-ttu-id="59bed-163">Reprezentacja ciągu (w określonym kodowaniu) pobranej zawartości pliku.</span><span class="sxs-lookup"><span data-stu-id="59bed-163">The string representation (in the specified encoding) of the file contents retrieved.</span></span>

## <span data-ttu-id="59bed-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="59bed-164">NOTES</span></span>

## <span data-ttu-id="59bed-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59bed-165">RELATED LINKS</span></span>

