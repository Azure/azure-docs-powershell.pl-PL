---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 3da97a14049671f8fff8bc03f7f32609f9b86984
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718224"
---
# <span data-ttu-id="a3122-101">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="a3122-101">Get-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="a3122-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a3122-102">SYNOPSIS</span></span>
<span data-ttu-id="a3122-103">Pobiera zawartość pliku w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a3122-103">Gets the contents of a file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3122-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a3122-104">SYNTAX</span></span>

### <span data-ttu-id="a3122-105">Podgląd zawartości pliku (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="a3122-105">Preview file content (Default)</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3122-106">Wyświetlanie podglądu wierszy pliku z poziomu nagłówka pliku</span><span class="sxs-lookup"><span data-stu-id="a3122-106">Preview file rows from the head of the file</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3122-107">Wyświetlanie podglądu wierszy plików od ogona pliku</span><span class="sxs-lookup"><span data-stu-id="a3122-107">Preview file rows from the tail of the file</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3122-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a3122-108">DESCRIPTION</span></span>
<span data-ttu-id="a3122-109">Polecenie cmdlet **Get-AzureRmDataLakeStoreItemContent** pobiera zawartość pliku w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a3122-109">The **Get-AzureRmDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="a3122-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a3122-110">EXAMPLES</span></span>

### <span data-ttu-id="a3122-111">Przykład 1. pobieranie zawartości pliku</span><span class="sxs-lookup"><span data-stu-id="a3122-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="a3122-112">To polecenie pobiera zawartość pliku MyFile.txt na koncie ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="a3122-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="a3122-113">Przykład 2: uzyskiwanie dwóch pierwszych wierszy pliku</span><span class="sxs-lookup"><span data-stu-id="a3122-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="a3122-114">To polecenie powoduje wyświetlenie dwóch pierwszych nowych wierszy rozdzielanych wierszami w pliku MyFile.txt na koncie ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="a3122-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="a3122-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a3122-115">PARAMETERS</span></span>

### <span data-ttu-id="a3122-116">— Konto</span><span class="sxs-lookup"><span data-stu-id="a3122-116">-Account</span></span>
<span data-ttu-id="a3122-117">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a3122-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="a3122-118">-Encoding</span><span class="sxs-lookup"><span data-stu-id="a3122-118">-Encoding</span></span>
<span data-ttu-id="a3122-119">Określa kodowanie elementu, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="a3122-119">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="a3122-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="a3122-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a3122-121">Wiadom</span><span class="sxs-lookup"><span data-stu-id="a3122-121">Unknown</span></span>
- <span data-ttu-id="a3122-122">Ciąg</span><span class="sxs-lookup"><span data-stu-id="a3122-122">String</span></span>
- <span data-ttu-id="a3122-123">Ze</span><span class="sxs-lookup"><span data-stu-id="a3122-123">Unicode</span></span>
- <span data-ttu-id="a3122-124">Jednobajtowe</span><span class="sxs-lookup"><span data-stu-id="a3122-124">Byte</span></span>
- <span data-ttu-id="a3122-125">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="a3122-125">BigEndianUnicode</span></span>
- <span data-ttu-id="a3122-126">UTF8</span><span class="sxs-lookup"><span data-stu-id="a3122-126">UTF8</span></span>
- <span data-ttu-id="a3122-127">UTF7</span><span class="sxs-lookup"><span data-stu-id="a3122-127">UTF7</span></span>
- <span data-ttu-id="a3122-128">Znaki</span><span class="sxs-lookup"><span data-stu-id="a3122-128">Ascii</span></span>
- <span data-ttu-id="a3122-129">Domyślne</span><span class="sxs-lookup"><span data-stu-id="a3122-129">Default</span></span>
- <span data-ttu-id="a3122-130">Equipment</span><span class="sxs-lookup"><span data-stu-id="a3122-130">Oem</span></span>
- <span data-ttu-id="a3122-131">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="a3122-131">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.PowerShell.Commands.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3122-132">-Force</span><span class="sxs-lookup"><span data-stu-id="a3122-132">-Force</span></span>
<span data-ttu-id="a3122-133">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a3122-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Preview file content
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3122-134">-Head</span><span class="sxs-lookup"><span data-stu-id="a3122-134">-Head</span></span>
<span data-ttu-id="a3122-135">Liczba wierszy (rozdzielanych wierszami) od początku pliku do wyświetlenia podglądu.</span><span class="sxs-lookup"><span data-stu-id="a3122-135">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="a3122-136">Jeśli nie zostanie napotkany żaden nowy wiersz w pierwszych 4 MB danych, zostaną zwrócone tylko te dane.</span><span class="sxs-lookup"><span data-stu-id="a3122-136">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Preview file rows from the head of the file
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3122-137">-Length</span><span class="sxs-lookup"><span data-stu-id="a3122-137">-Length</span></span>
<span data-ttu-id="a3122-138">Określa długość zawartości (w bajtach), którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="a3122-138">Specifies the length, in bytes, of the content to get.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Preview file content
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3122-139">-Przesunięcie</span><span class="sxs-lookup"><span data-stu-id="a3122-139">-Offset</span></span>
<span data-ttu-id="a3122-140">Określa liczbę bajtów, które należy pominąć w pliku przed uzyskaniem zawartości.</span><span class="sxs-lookup"><span data-stu-id="a3122-140">Specifies the number of bytes to skip in a file before getting content.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Preview file content
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3122-141">-Path</span><span class="sxs-lookup"><span data-stu-id="a3122-141">-Path</span></span>
<span data-ttu-id="a3122-142">Określa ścieżkę pliku Data Lake Store, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="a3122-142">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="a3122-143">-Koniec</span><span class="sxs-lookup"><span data-stu-id="a3122-143">-Tail</span></span>
<span data-ttu-id="a3122-144">Liczba wierszy (rozdzielanych wierszami) od końca pliku do wyświetlenia podglądu.</span><span class="sxs-lookup"><span data-stu-id="a3122-144">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="a3122-145">Jeśli nie zostanie napotkany żaden nowy wiersz w pierwszych 4 MB danych, zostaną zwrócone tylko te dane.</span><span class="sxs-lookup"><span data-stu-id="a3122-145">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Preview file rows from the tail of the file
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3122-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a3122-146">-Confirm</span></span>
<span data-ttu-id="a3122-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3122-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3122-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3122-148">-WhatIf</span></span>
<span data-ttu-id="a3122-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3122-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3122-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a3122-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3122-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3122-151">-DefaultProfile</span></span>
<span data-ttu-id="a3122-152">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3122-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3122-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3122-153">CommonParameters</span></span>
<span data-ttu-id="a3122-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3122-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3122-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3122-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3122-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3122-156">INPUTS</span></span>

## <span data-ttu-id="a3122-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a3122-157">OUTPUTS</span></span>

### <span data-ttu-id="a3122-158">Byte []</span><span class="sxs-lookup"><span data-stu-id="a3122-158">byte[]</span></span>
<span data-ttu-id="a3122-159">Bajtowa reprezentacja zawartości pliku w strumieniu bajtów została pobrana.</span><span class="sxs-lookup"><span data-stu-id="a3122-159">The byte stream representation of the file contents retrieved.</span></span>

### <span data-ttu-id="a3122-160">ciąg</span><span class="sxs-lookup"><span data-stu-id="a3122-160">string</span></span>
<span data-ttu-id="a3122-161">Reprezentacja ciągu (w określonym kodowaniu) pobranej zawartości pliku.</span><span class="sxs-lookup"><span data-stu-id="a3122-161">The string representation (in the specified encoding) of the file contents retrieved.</span></span>

## <span data-ttu-id="a3122-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a3122-162">NOTES</span></span>

## <span data-ttu-id="a3122-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3122-163">RELATED LINKS</span></span>

