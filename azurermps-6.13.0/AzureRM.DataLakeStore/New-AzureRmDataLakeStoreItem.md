---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/new-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 2e50135762826661e82f499f2aec48c67d00c648
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524466"
---
# <span data-ttu-id="03ade-101">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="03ade-101">New-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="03ade-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03ade-102">SYNOPSIS</span></span>
<span data-ttu-id="03ade-103">Tworzy nowy plik lub folder w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="03ade-103">Creates a new file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03ade-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03ade-104">SYNTAX</span></span>

```
New-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03ade-105">Opis</span><span class="sxs-lookup"><span data-stu-id="03ade-105">DESCRIPTION</span></span>
<span data-ttu-id="03ade-106">Polecenie cmdlet **New-AzureRmDataLakeStoreItem** tworzy nowy plik lub folder w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="03ade-106">The **New-AzureRmDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="03ade-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03ade-107">EXAMPLES</span></span>

### <span data-ttu-id="03ade-108">Przykład 1. Tworzenie nowego pliku i nowego folderu</span><span class="sxs-lookup"><span data-stu-id="03ade-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="03ade-109">Pierwsze polecenie tworzy plik NewFile.txt dla określonego konta.</span><span class="sxs-lookup"><span data-stu-id="03ade-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="03ade-110">Drugie polecenie utworzy folder NewFolder w folderze głównym.</span><span class="sxs-lookup"><span data-stu-id="03ade-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="03ade-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03ade-111">PARAMETERS</span></span>

### <span data-ttu-id="03ade-112">— Konto</span><span class="sxs-lookup"><span data-stu-id="03ade-112">-Account</span></span>
<span data-ttu-id="03ade-113">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="03ade-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="03ade-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03ade-114">-DefaultProfile</span></span>
<span data-ttu-id="03ade-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="03ade-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03ade-116">-Encoding</span><span class="sxs-lookup"><span data-stu-id="03ade-116">-Encoding</span></span>
<span data-ttu-id="03ade-117">Określa kodowanie elementu, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="03ade-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="03ade-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="03ade-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="03ade-119">Wiadom</span><span class="sxs-lookup"><span data-stu-id="03ade-119">Unknown</span></span>
- <span data-ttu-id="03ade-120">Ciąg</span><span class="sxs-lookup"><span data-stu-id="03ade-120">String</span></span>
- <span data-ttu-id="03ade-121">Ze</span><span class="sxs-lookup"><span data-stu-id="03ade-121">Unicode</span></span>
- <span data-ttu-id="03ade-122">Jednobajtowe</span><span class="sxs-lookup"><span data-stu-id="03ade-122">Byte</span></span>
- <span data-ttu-id="03ade-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="03ade-123">BigEndianUnicode</span></span>
- <span data-ttu-id="03ade-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="03ade-124">UTF8</span></span>
- <span data-ttu-id="03ade-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="03ade-125">UTF7</span></span>
- <span data-ttu-id="03ade-126">Znaki</span><span class="sxs-lookup"><span data-stu-id="03ade-126">Ascii</span></span>
- <span data-ttu-id="03ade-127">Domyślne</span><span class="sxs-lookup"><span data-stu-id="03ade-127">Default</span></span>
- <span data-ttu-id="03ade-128">Equipment</span><span class="sxs-lookup"><span data-stu-id="03ade-128">Oem</span></span>
- <span data-ttu-id="03ade-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="03ade-129">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ade-130">-Folder</span><span class="sxs-lookup"><span data-stu-id="03ade-130">-Folder</span></span>
<span data-ttu-id="03ade-131">Wskazuje, że ta operacja powoduje utworzenie folderu.</span><span class="sxs-lookup"><span data-stu-id="03ade-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="03ade-132">-Force</span><span class="sxs-lookup"><span data-stu-id="03ade-132">-Force</span></span>
<span data-ttu-id="03ade-133">Wskazuje, że ta operacja może zastąpić element docelowy, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="03ade-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="03ade-134">-Path</span><span class="sxs-lookup"><span data-stu-id="03ade-134">-Path</span></span>
<span data-ttu-id="03ade-135">Określa ścieżkę elementu, który ma zostać utworzony, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="03ade-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="03ade-136">-Value</span><span class="sxs-lookup"><span data-stu-id="03ade-136">-Value</span></span>
<span data-ttu-id="03ade-137">Określa zawartość, którą należy dodać do tworzonego elementu.</span><span class="sxs-lookup"><span data-stu-id="03ade-137">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="03ade-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="03ade-138">-Confirm</span></span>
<span data-ttu-id="03ade-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03ade-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03ade-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03ade-140">-WhatIf</span></span>
<span data-ttu-id="03ade-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03ade-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03ade-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="03ade-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03ade-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03ade-143">CommonParameters</span></span>
<span data-ttu-id="03ade-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03ade-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03ade-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03ade-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03ade-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03ade-146">INPUTS</span></span>

### <span data-ttu-id="03ade-147">System. String</span><span class="sxs-lookup"><span data-stu-id="03ade-147">System.String</span></span>

### <span data-ttu-id="03ade-148">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="03ade-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="03ade-149">System. Object</span><span class="sxs-lookup"><span data-stu-id="03ade-149">System.Object</span></span>

### <span data-ttu-id="03ade-150">Microsoft. Azure. Commands. DataLakeStore. models. FileSystemCmdletProviderEncoding</span><span class="sxs-lookup"><span data-stu-id="03ade-150">Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding</span></span>

### <span data-ttu-id="03ade-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="03ade-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="03ade-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03ade-152">OUTPUTS</span></span>

### <span data-ttu-id="03ade-153">System. String</span><span class="sxs-lookup"><span data-stu-id="03ade-153">System.String</span></span>
<span data-ttu-id="03ade-154">Pełna ścieżka do utworzonego pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="03ade-154">The full path to the created file or folder.</span></span>

## <span data-ttu-id="03ade-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03ade-155">NOTES</span></span>

## <span data-ttu-id="03ade-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03ade-156">RELATED LINKS</span></span>

[<span data-ttu-id="03ade-157">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="03ade-157">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="03ade-158">Eksportowanie — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="03ade-158">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="03ade-159">Import — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="03ade-159">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="03ade-160">Nowe — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="03ade-160">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="03ade-161">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="03ade-161">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="03ade-162">Test — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="03ade-162">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


