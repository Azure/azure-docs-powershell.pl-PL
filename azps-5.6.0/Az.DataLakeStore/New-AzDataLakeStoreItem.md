---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/new-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
ms.openlocfilehash: 46495d5a057de6c7cff21cdc09fe68d80e0c4da7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991425"
---
# <span data-ttu-id="e65ac-101">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e65ac-101">New-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="e65ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e65ac-102">SYNOPSIS</span></span>
<span data-ttu-id="e65ac-103">Tworzy nowy plik lub folder w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e65ac-103">Creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e65ac-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e65ac-104">SYNTAX</span></span>

```
New-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <Encoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e65ac-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e65ac-105">DESCRIPTION</span></span>
<span data-ttu-id="e65ac-106">Polecenie **cmdlet New-AzDataLakeStoreItem** tworzy nowy plik lub folder w magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e65ac-106">The **New-AzDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e65ac-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e65ac-107">EXAMPLES</span></span>

### <span data-ttu-id="e65ac-108">Przykład 1. Tworzenie nowego pliku i nowego folderu</span><span class="sxs-lookup"><span data-stu-id="e65ac-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="e65ac-109">Pierwsze polecenie tworzy plik NewFile.txt dla określonego konta.</span><span class="sxs-lookup"><span data-stu-id="e65ac-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="e65ac-110">Drugie polecenie tworzy folder NewFolder w folderze głównym.</span><span class="sxs-lookup"><span data-stu-id="e65ac-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="e65ac-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e65ac-111">PARAMETERS</span></span>

### <span data-ttu-id="e65ac-112">— Konto</span><span class="sxs-lookup"><span data-stu-id="e65ac-112">-Account</span></span>
<span data-ttu-id="e65ac-113">Określa nazwę konta sklepu Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e65ac-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="e65ac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e65ac-114">-DefaultProfile</span></span>
<span data-ttu-id="e65ac-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e65ac-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e65ac-116">— Kodowanie</span><span class="sxs-lookup"><span data-stu-id="e65ac-116">-Encoding</span></span>
<span data-ttu-id="e65ac-117">Określa kodowanie elementu do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="e65ac-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="e65ac-118">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e65ac-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e65ac-119">Nieznany</span><span class="sxs-lookup"><span data-stu-id="e65ac-119">Unknown</span></span>
- <span data-ttu-id="e65ac-120">Ciąg</span><span class="sxs-lookup"><span data-stu-id="e65ac-120">String</span></span>
- <span data-ttu-id="e65ac-121">Unicode</span><span class="sxs-lookup"><span data-stu-id="e65ac-121">Unicode</span></span>
- <span data-ttu-id="e65ac-122">Bajt</span><span class="sxs-lookup"><span data-stu-id="e65ac-122">Byte</span></span>
- <span data-ttu-id="e65ac-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="e65ac-123">BigEndianUnicode</span></span>
- <span data-ttu-id="e65ac-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="e65ac-124">UTF8</span></span>
- <span data-ttu-id="e65ac-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="e65ac-125">UTF7</span></span>
- <span data-ttu-id="e65ac-126">Ascii</span><span class="sxs-lookup"><span data-stu-id="e65ac-126">Ascii</span></span>
- <span data-ttu-id="e65ac-127">Domyślne</span><span class="sxs-lookup"><span data-stu-id="e65ac-127">Default</span></span>
- <span data-ttu-id="e65ac-128">Oem</span><span class="sxs-lookup"><span data-stu-id="e65ac-128">Oem</span></span>
- <span data-ttu-id="e65ac-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="e65ac-129">BigEndianUTF32</span></span>

```yaml
Type: System.Text.Encoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e65ac-130">- Folder</span><span class="sxs-lookup"><span data-stu-id="e65ac-130">-Folder</span></span>
<span data-ttu-id="e65ac-131">Wskazuje, że ta operacja powoduje utworzenie folderu.</span><span class="sxs-lookup"><span data-stu-id="e65ac-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="e65ac-132">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="e65ac-132">-Force</span></span>
<span data-ttu-id="e65ac-133">Oznacza, że ta operacja może zastąpić element docelowy, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="e65ac-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="e65ac-134">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="e65ac-134">-Path</span></span>
<span data-ttu-id="e65ac-135">Określa ścieżkę elementu do utworzenia w magazynie Data Lake Store, począwszy od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="e65ac-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="e65ac-136">— Wartość</span><span class="sxs-lookup"><span data-stu-id="e65ac-136">-Value</span></span>
<span data-ttu-id="e65ac-137">Określa zawartość do dodania do tworzyć elementu.</span><span class="sxs-lookup"><span data-stu-id="e65ac-137">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="e65ac-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e65ac-138">-Confirm</span></span>
<span data-ttu-id="e65ac-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e65ac-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e65ac-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e65ac-140">-WhatIf</span></span>
<span data-ttu-id="e65ac-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e65ac-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e65ac-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e65ac-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e65ac-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e65ac-143">CommonParameters</span></span>
<span data-ttu-id="e65ac-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e65ac-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e65ac-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e65ac-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e65ac-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e65ac-146">INPUTS</span></span>

### <span data-ttu-id="e65ac-147">System.String</span><span class="sxs-lookup"><span data-stu-id="e65ac-147">System.String</span></span>

### <span data-ttu-id="e65ac-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="e65ac-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="e65ac-149">System.Object</span><span class="sxs-lookup"><span data-stu-id="e65ac-149">System.Object</span></span>

### <span data-ttu-id="e65ac-150">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="e65ac-150">System.Text.Encoding</span></span>

### <span data-ttu-id="e65ac-151">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="e65ac-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e65ac-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e65ac-152">OUTPUTS</span></span>

### <span data-ttu-id="e65ac-153">System.String</span><span class="sxs-lookup"><span data-stu-id="e65ac-153">System.String</span></span>

## <span data-ttu-id="e65ac-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e65ac-154">NOTES</span></span>

## <span data-ttu-id="e65ac-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e65ac-155">RELATED LINKS</span></span>

[<span data-ttu-id="e65ac-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e65ac-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="e65ac-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e65ac-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="e65ac-158">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e65ac-158">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="e65ac-159">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e65ac-159">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="e65ac-160">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e65ac-160">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="e65ac-161">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e65ac-161">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


