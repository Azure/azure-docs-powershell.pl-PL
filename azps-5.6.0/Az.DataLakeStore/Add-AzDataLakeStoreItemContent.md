---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: aa2fe76f221ce412c0e47f7a43b1dba551131f45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994393"
---
# <span data-ttu-id="6b164-101">Add-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="6b164-101">Add-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="6b164-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b164-102">SYNOPSIS</span></span>
<span data-ttu-id="6b164-103">Dodaje zawartość do elementu w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6b164-103">Adds content to an item in a Data Lake Store.</span></span>

## <span data-ttu-id="6b164-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6b164-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b164-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6b164-105">DESCRIPTION</span></span>
<span data-ttu-id="6b164-106">Polecenie **cmdlet Add-AzDataLakeStoreItemContent** dodaje zawartość do elementu w sklepie Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6b164-106">The **Add-AzDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="6b164-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6b164-107">EXAMPLES</span></span>

### <span data-ttu-id="6b164-108">Przykład 1. Dodawanie zawartości do pliku</span><span class="sxs-lookup"><span data-stu-id="6b164-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="6b164-109">To polecenie dodaje zawartość do pliku myFile.txt.</span><span class="sxs-lookup"><span data-stu-id="6b164-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="6b164-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b164-110">PARAMETERS</span></span>

### <span data-ttu-id="6b164-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="6b164-111">-Account</span></span>
<span data-ttu-id="6b164-112">Określa nazwę konta sklepu Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6b164-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="6b164-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b164-113">-DefaultProfile</span></span>
<span data-ttu-id="6b164-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="6b164-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b164-115">— Kodowanie</span><span class="sxs-lookup"><span data-stu-id="6b164-115">-Encoding</span></span>
<span data-ttu-id="6b164-116">Określa kodowanie elementu do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="6b164-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="6b164-117">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6b164-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6b164-118">Nieznany</span><span class="sxs-lookup"><span data-stu-id="6b164-118">Unknown</span></span>
- <span data-ttu-id="6b164-119">Ciąg</span><span class="sxs-lookup"><span data-stu-id="6b164-119">String</span></span>
- <span data-ttu-id="6b164-120">Unicode</span><span class="sxs-lookup"><span data-stu-id="6b164-120">Unicode</span></span>
- <span data-ttu-id="6b164-121">Bajt</span><span class="sxs-lookup"><span data-stu-id="6b164-121">Byte</span></span>
- <span data-ttu-id="6b164-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="6b164-122">BigEndianUnicode</span></span>
- <span data-ttu-id="6b164-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="6b164-123">UTF8</span></span>
- <span data-ttu-id="6b164-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="6b164-124">UTF7</span></span>
- <span data-ttu-id="6b164-125">Ascii</span><span class="sxs-lookup"><span data-stu-id="6b164-125">Ascii</span></span>
- <span data-ttu-id="6b164-126">Domyślne</span><span class="sxs-lookup"><span data-stu-id="6b164-126">Default</span></span>
- <span data-ttu-id="6b164-127">Oem</span><span class="sxs-lookup"><span data-stu-id="6b164-127">Oem</span></span>
- <span data-ttu-id="6b164-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="6b164-128">BigEndianUTF32</span></span>

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

### <span data-ttu-id="6b164-129">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="6b164-129">-Path</span></span>
<span data-ttu-id="6b164-130">Określa ścieżkę elementu do zmodyfikowania w sklepie Data Lake Store, zaczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="6b164-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="6b164-131">— Wartość</span><span class="sxs-lookup"><span data-stu-id="6b164-131">-Value</span></span>
<span data-ttu-id="6b164-132">Określa zawartość do dodania do elementu.</span><span class="sxs-lookup"><span data-stu-id="6b164-132">Specifies the content to add to the item.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b164-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b164-133">CommonParameters</span></span>
<span data-ttu-id="6b164-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b164-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b164-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b164-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b164-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b164-136">INPUTS</span></span>

### <span data-ttu-id="6b164-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6b164-137">System.String</span></span>

### <span data-ttu-id="6b164-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="6b164-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="6b164-139">System.Object</span><span class="sxs-lookup"><span data-stu-id="6b164-139">System.Object</span></span>

### <span data-ttu-id="6b164-140">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="6b164-140">System.Text.Encoding</span></span>

## <span data-ttu-id="6b164-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b164-141">OUTPUTS</span></span>

### <span data-ttu-id="6b164-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6b164-142">System.Boolean</span></span>

## <span data-ttu-id="6b164-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6b164-143">NOTES</span></span>

## <span data-ttu-id="6b164-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b164-144">RELATED LINKS</span></span>

[<span data-ttu-id="6b164-145">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="6b164-145">Get-AzDataLakeStoreItemContent</span></span>](./Get-AzDataLakeStoreItemContent.md)


