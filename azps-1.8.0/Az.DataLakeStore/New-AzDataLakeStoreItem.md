---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
ms.openlocfilehash: 222df24f2d3db296ce116e49da8baeb3e22ec699
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868516"
---
# <span data-ttu-id="f8663-101">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f8663-101">New-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="f8663-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8663-102">SYNOPSIS</span></span>
<span data-ttu-id="f8663-103">Tworzy nowy plik lub folder w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f8663-103">Creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f8663-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8663-104">SYNTAX</span></span>

```
New-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <Encoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8663-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f8663-105">DESCRIPTION</span></span>
<span data-ttu-id="f8663-106">Polecenie cmdlet **New-AzDataLakeStoreItem** tworzy nowy plik lub folder w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f8663-106">The **New-AzDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f8663-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8663-107">EXAMPLES</span></span>

### <span data-ttu-id="f8663-108">Przykład 1. Tworzenie nowego pliku i nowego folderu</span><span class="sxs-lookup"><span data-stu-id="f8663-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="f8663-109">Pierwsze polecenie tworzy plik NewFile.txt dla określonego konta.</span><span class="sxs-lookup"><span data-stu-id="f8663-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="f8663-110">Drugie polecenie utworzy folder NewFolder w folderze głównym.</span><span class="sxs-lookup"><span data-stu-id="f8663-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="f8663-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8663-111">PARAMETERS</span></span>

### <span data-ttu-id="f8663-112">— Konto</span><span class="sxs-lookup"><span data-stu-id="f8663-112">-Account</span></span>
<span data-ttu-id="f8663-113">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f8663-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f8663-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8663-114">-DefaultProfile</span></span>
<span data-ttu-id="f8663-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f8663-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8663-116">-Encoding</span><span class="sxs-lookup"><span data-stu-id="f8663-116">-Encoding</span></span>
<span data-ttu-id="f8663-117">Określa kodowanie elementu, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="f8663-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="f8663-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f8663-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f8663-119">Wiadom</span><span class="sxs-lookup"><span data-stu-id="f8663-119">Unknown</span></span>
- <span data-ttu-id="f8663-120">Ciąg</span><span class="sxs-lookup"><span data-stu-id="f8663-120">String</span></span>
- <span data-ttu-id="f8663-121">Ze</span><span class="sxs-lookup"><span data-stu-id="f8663-121">Unicode</span></span>
- <span data-ttu-id="f8663-122">Jednobajtowe</span><span class="sxs-lookup"><span data-stu-id="f8663-122">Byte</span></span>
- <span data-ttu-id="f8663-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="f8663-123">BigEndianUnicode</span></span>
- <span data-ttu-id="f8663-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="f8663-124">UTF8</span></span>
- <span data-ttu-id="f8663-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="f8663-125">UTF7</span></span>
- <span data-ttu-id="f8663-126">Znaki</span><span class="sxs-lookup"><span data-stu-id="f8663-126">Ascii</span></span>
- <span data-ttu-id="f8663-127">Domyślne</span><span class="sxs-lookup"><span data-stu-id="f8663-127">Default</span></span>
- <span data-ttu-id="f8663-128">Equipment</span><span class="sxs-lookup"><span data-stu-id="f8663-128">Oem</span></span>
- <span data-ttu-id="f8663-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="f8663-129">BigEndianUTF32</span></span>

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

### <span data-ttu-id="f8663-130">-Folder</span><span class="sxs-lookup"><span data-stu-id="f8663-130">-Folder</span></span>
<span data-ttu-id="f8663-131">Wskazuje, że ta operacja powoduje utworzenie folderu.</span><span class="sxs-lookup"><span data-stu-id="f8663-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="f8663-132">-Force</span><span class="sxs-lookup"><span data-stu-id="f8663-132">-Force</span></span>
<span data-ttu-id="f8663-133">Wskazuje, że ta operacja może zastąpić element docelowy, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="f8663-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="f8663-134">-Path</span><span class="sxs-lookup"><span data-stu-id="f8663-134">-Path</span></span>
<span data-ttu-id="f8663-135">Określa ścieżkę elementu, który ma zostać utworzony, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="f8663-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="f8663-136">-Value</span><span class="sxs-lookup"><span data-stu-id="f8663-136">-Value</span></span>
<span data-ttu-id="f8663-137">Określa zawartość, którą należy dodać do tworzonego elementu.</span><span class="sxs-lookup"><span data-stu-id="f8663-137">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="f8663-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f8663-138">-Confirm</span></span>
<span data-ttu-id="f8663-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8663-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8663-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8663-140">-WhatIf</span></span>
<span data-ttu-id="f8663-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8663-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8663-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f8663-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8663-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8663-143">CommonParameters</span></span>
<span data-ttu-id="f8663-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8663-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8663-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8663-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8663-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8663-146">INPUTS</span></span>

### <span data-ttu-id="f8663-147">System. String</span><span class="sxs-lookup"><span data-stu-id="f8663-147">System.String</span></span>

### <span data-ttu-id="f8663-148">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="f8663-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="f8663-149">System. Object</span><span class="sxs-lookup"><span data-stu-id="f8663-149">System.Object</span></span>

### <span data-ttu-id="f8663-150">System. Text. Encoding</span><span class="sxs-lookup"><span data-stu-id="f8663-150">System.Text.Encoding</span></span>

### <span data-ttu-id="f8663-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f8663-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f8663-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8663-152">OUTPUTS</span></span>

### <span data-ttu-id="f8663-153">System. String</span><span class="sxs-lookup"><span data-stu-id="f8663-153">System.String</span></span>

## <span data-ttu-id="f8663-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8663-154">NOTES</span></span>

## <span data-ttu-id="f8663-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8663-155">RELATED LINKS</span></span>

[<span data-ttu-id="f8663-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f8663-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="f8663-157">Eksportowanie — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f8663-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="f8663-158">Import — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f8663-158">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="f8663-159">Nowe — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f8663-159">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="f8663-160">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f8663-160">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="f8663-161">Test — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f8663-161">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


