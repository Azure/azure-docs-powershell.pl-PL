---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/new-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 2dc2d18fc0bc09fd7e9477115f4212aeb2452bbb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526845"
---
# <span data-ttu-id="2b32d-101">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2b32d-101">New-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="2b32d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b32d-102">SYNOPSIS</span></span>
<span data-ttu-id="2b32d-103">Tworzy nowy plik lub folder w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2b32d-103">Creates a new file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b32d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b32d-104">SYNTAX</span></span>

```
New-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b32d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2b32d-105">DESCRIPTION</span></span>
<span data-ttu-id="2b32d-106">Polecenie cmdlet **New-AzureRmDataLakeStoreItem** tworzy nowy plik lub folder w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2b32d-106">The **New-AzureRmDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="2b32d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b32d-107">EXAMPLES</span></span>

### <span data-ttu-id="2b32d-108">Przykład 1. Tworzenie nowego pliku i nowego folderu</span><span class="sxs-lookup"><span data-stu-id="2b32d-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="2b32d-109">Pierwsze polecenie tworzy plik NewFile.txt dla określonego konta.</span><span class="sxs-lookup"><span data-stu-id="2b32d-109">The first command creates the file NewFile.txt for the specified account.</span></span>

<span data-ttu-id="2b32d-110">Drugie polecenie utworzy folder NewFolder w folderze głównym.</span><span class="sxs-lookup"><span data-stu-id="2b32d-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="2b32d-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b32d-111">PARAMETERS</span></span>

### <span data-ttu-id="2b32d-112">— Konto</span><span class="sxs-lookup"><span data-stu-id="2b32d-112">-Account</span></span>
<span data-ttu-id="2b32d-113">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2b32d-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="2b32d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b32d-114">-DefaultProfile</span></span>
<span data-ttu-id="2b32d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b32d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b32d-116">-Encoding</span><span class="sxs-lookup"><span data-stu-id="2b32d-116">-Encoding</span></span>
<span data-ttu-id="2b32d-117">Określa kodowanie elementu, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="2b32d-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="2b32d-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2b32d-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2b32d-119">Wiadom</span><span class="sxs-lookup"><span data-stu-id="2b32d-119">Unknown</span></span>
- <span data-ttu-id="2b32d-120">Ciąg</span><span class="sxs-lookup"><span data-stu-id="2b32d-120">String</span></span>
- <span data-ttu-id="2b32d-121">Ze</span><span class="sxs-lookup"><span data-stu-id="2b32d-121">Unicode</span></span>
- <span data-ttu-id="2b32d-122">Jednobajtowe</span><span class="sxs-lookup"><span data-stu-id="2b32d-122">Byte</span></span>
- <span data-ttu-id="2b32d-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="2b32d-123">BigEndianUnicode</span></span>
- <span data-ttu-id="2b32d-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="2b32d-124">UTF8</span></span>
- <span data-ttu-id="2b32d-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="2b32d-125">UTF7</span></span>
- <span data-ttu-id="2b32d-126">Znaki</span><span class="sxs-lookup"><span data-stu-id="2b32d-126">Ascii</span></span>
- <span data-ttu-id="2b32d-127">Domyślne</span><span class="sxs-lookup"><span data-stu-id="2b32d-127">Default</span></span>
- <span data-ttu-id="2b32d-128">Equipment</span><span class="sxs-lookup"><span data-stu-id="2b32d-128">Oem</span></span>
- <span data-ttu-id="2b32d-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="2b32d-129">BigEndianUTF32</span></span>

```yaml
Type: FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b32d-130">-Folder</span><span class="sxs-lookup"><span data-stu-id="2b32d-130">-Folder</span></span>
<span data-ttu-id="2b32d-131">Wskazuje, że ta operacja powoduje utworzenie folderu.</span><span class="sxs-lookup"><span data-stu-id="2b32d-131">Indicates that this operation creates a folder.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b32d-132">-Force</span><span class="sxs-lookup"><span data-stu-id="2b32d-132">-Force</span></span>
<span data-ttu-id="2b32d-133">Wskazuje, że ta operacja może zastąpić element docelowy, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="2b32d-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b32d-134">-Path</span><span class="sxs-lookup"><span data-stu-id="2b32d-134">-Path</span></span>
<span data-ttu-id="2b32d-135">Określa ścieżkę elementu, który ma zostać utworzony, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="2b32d-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="2b32d-136">-Value</span><span class="sxs-lookup"><span data-stu-id="2b32d-136">-Value</span></span>
<span data-ttu-id="2b32d-137">Określa zawartość, którą należy dodać do tworzonego elementu.</span><span class="sxs-lookup"><span data-stu-id="2b32d-137">Specifies the content to add to the item you create.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b32d-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2b32d-138">-Confirm</span></span>
<span data-ttu-id="2b32d-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b32d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b32d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b32d-140">-WhatIf</span></span>
<span data-ttu-id="2b32d-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b32d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b32d-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2b32d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b32d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b32d-143">CommonParameters</span></span>
<span data-ttu-id="2b32d-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b32d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b32d-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b32d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b32d-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b32d-146">INPUTS</span></span>

### <span data-ttu-id="2b32d-147">Stream</span><span class="sxs-lookup"><span data-stu-id="2b32d-147">Object</span></span>
<span data-ttu-id="2b32d-148">Parametr "value" przyjmuje wartość typu "Object" z procesu</span><span class="sxs-lookup"><span data-stu-id="2b32d-148">Parameter 'Value' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="2b32d-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b32d-149">OUTPUTS</span></span>

### <span data-ttu-id="2b32d-150">ciąg</span><span class="sxs-lookup"><span data-stu-id="2b32d-150">string</span></span>
<span data-ttu-id="2b32d-151">Pełna ścieżka do utworzonego pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="2b32d-151">The full path to the created file or folder.</span></span>

## <span data-ttu-id="2b32d-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b32d-152">NOTES</span></span>

## <span data-ttu-id="2b32d-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b32d-153">RELATED LINKS</span></span>

[<span data-ttu-id="2b32d-154">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2b32d-154">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2b32d-155">Eksportowanie — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2b32d-155">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2b32d-156">Import — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2b32d-156">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2b32d-157">Nowe — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2b32d-157">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2b32d-158">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2b32d-158">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2b32d-159">Test — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2b32d-159">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


