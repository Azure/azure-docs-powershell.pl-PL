---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: a087c2f7cfd4358e137550aa2e916fa2200d2a2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551047"
---
# <span data-ttu-id="0327f-101">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0327f-101">New-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="0327f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0327f-102">SYNOPSIS</span></span>
<span data-ttu-id="0327f-103">Tworzy nowy plik lub folder w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0327f-103">Creates a new file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0327f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0327f-104">SYNTAX</span></span>

```
New-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0327f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0327f-105">DESCRIPTION</span></span>
<span data-ttu-id="0327f-106">Polecenie cmdlet **New-AzureRmDataLakeStoreItem** tworzy nowy plik lub folder w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0327f-106">The **New-AzureRmDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0327f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0327f-107">EXAMPLES</span></span>

### <span data-ttu-id="0327f-108">Przykład 1. Tworzenie nowego pliku i nowego folderu</span><span class="sxs-lookup"><span data-stu-id="0327f-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="0327f-109">Pierwsze polecenie tworzy plik NewFile.txt dla określonego konta.</span><span class="sxs-lookup"><span data-stu-id="0327f-109">The first command creates the file NewFile.txt for the specified account.</span></span>

<span data-ttu-id="0327f-110">Drugie polecenie utworzy folder NewFolder w folderze głównym.</span><span class="sxs-lookup"><span data-stu-id="0327f-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="0327f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0327f-111">PARAMETERS</span></span>

### <span data-ttu-id="0327f-112">— Konto</span><span class="sxs-lookup"><span data-stu-id="0327f-112">-Account</span></span>
<span data-ttu-id="0327f-113">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0327f-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="0327f-114">-Encoding</span><span class="sxs-lookup"><span data-stu-id="0327f-114">-Encoding</span></span>
<span data-ttu-id="0327f-115">Określa kodowanie elementu, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="0327f-115">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="0327f-116">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0327f-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0327f-117">Wiadom</span><span class="sxs-lookup"><span data-stu-id="0327f-117">Unknown</span></span>
- <span data-ttu-id="0327f-118">Ciąg</span><span class="sxs-lookup"><span data-stu-id="0327f-118">String</span></span>
- <span data-ttu-id="0327f-119">Ze</span><span class="sxs-lookup"><span data-stu-id="0327f-119">Unicode</span></span>
- <span data-ttu-id="0327f-120">Jednobajtowe</span><span class="sxs-lookup"><span data-stu-id="0327f-120">Byte</span></span>
- <span data-ttu-id="0327f-121">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="0327f-121">BigEndianUnicode</span></span>
- <span data-ttu-id="0327f-122">UTF8</span><span class="sxs-lookup"><span data-stu-id="0327f-122">UTF8</span></span>
- <span data-ttu-id="0327f-123">UTF7</span><span class="sxs-lookup"><span data-stu-id="0327f-123">UTF7</span></span>
- <span data-ttu-id="0327f-124">Znaki</span><span class="sxs-lookup"><span data-stu-id="0327f-124">Ascii</span></span>
- <span data-ttu-id="0327f-125">Domyślne</span><span class="sxs-lookup"><span data-stu-id="0327f-125">Default</span></span>
- <span data-ttu-id="0327f-126">Equipment</span><span class="sxs-lookup"><span data-stu-id="0327f-126">Oem</span></span>
- <span data-ttu-id="0327f-127">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="0327f-127">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.PowerShell.Commands.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0327f-128">-Folder</span><span class="sxs-lookup"><span data-stu-id="0327f-128">-Folder</span></span>
<span data-ttu-id="0327f-129">Wskazuje, że ta operacja powoduje utworzenie folderu.</span><span class="sxs-lookup"><span data-stu-id="0327f-129">Indicates that this operation creates a folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0327f-130">-Force</span><span class="sxs-lookup"><span data-stu-id="0327f-130">-Force</span></span>
<span data-ttu-id="0327f-131">Wskazuje, że ta operacja może zastąpić element docelowy, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="0327f-131">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0327f-132">-Path</span><span class="sxs-lookup"><span data-stu-id="0327f-132">-Path</span></span>
<span data-ttu-id="0327f-133">Określa ścieżkę elementu, który ma zostać utworzony, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="0327f-133">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="0327f-134">-Value</span><span class="sxs-lookup"><span data-stu-id="0327f-134">-Value</span></span>
<span data-ttu-id="0327f-135">Określa zawartość, którą należy dodać do tworzonego elementu.</span><span class="sxs-lookup"><span data-stu-id="0327f-135">Specifies the content to add to the item you create.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0327f-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0327f-136">-Confirm</span></span>
<span data-ttu-id="0327f-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0327f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0327f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0327f-138">-WhatIf</span></span>
<span data-ttu-id="0327f-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0327f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0327f-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0327f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0327f-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0327f-141">-DefaultProfile</span></span>
<span data-ttu-id="0327f-142">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0327f-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0327f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0327f-143">CommonParameters</span></span>
<span data-ttu-id="0327f-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0327f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0327f-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0327f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0327f-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0327f-146">INPUTS</span></span>

### <span data-ttu-id="0327f-147">Stream</span><span class="sxs-lookup"><span data-stu-id="0327f-147">Object</span></span>
<span data-ttu-id="0327f-148">Parametr "value" przyjmuje wartość typu "Object" z procesu</span><span class="sxs-lookup"><span data-stu-id="0327f-148">Parameter 'Value' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="0327f-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0327f-149">OUTPUTS</span></span>

### <span data-ttu-id="0327f-150">ciąg</span><span class="sxs-lookup"><span data-stu-id="0327f-150">string</span></span>
<span data-ttu-id="0327f-151">Pełna ścieżka do utworzonego pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="0327f-151">The full path to the created file or folder.</span></span>

## <span data-ttu-id="0327f-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0327f-152">NOTES</span></span>

## <span data-ttu-id="0327f-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0327f-153">RELATED LINKS</span></span>

[<span data-ttu-id="0327f-154">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0327f-154">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="0327f-155">Eksportowanie — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0327f-155">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="0327f-156">Import — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0327f-156">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="0327f-157">Nowe — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0327f-157">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="0327f-158">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0327f-158">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="0327f-159">Test — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0327f-159">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


