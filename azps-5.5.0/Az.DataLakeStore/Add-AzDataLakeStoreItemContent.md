---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: 3cf411e75e2a3ec430f13354015d5b6e271c840c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194691"
---
# <span data-ttu-id="b7e0e-101">Add-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="b7e0e-101">Add-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="b7e0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7e0e-102">SYNOPSIS</span></span>
<span data-ttu-id="b7e0e-103">Dodaje zawartość do elementu w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b7e0e-103">Adds content to an item in a Data Lake Store.</span></span>

## <span data-ttu-id="b7e0e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b7e0e-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7e0e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b7e0e-105">DESCRIPTION</span></span>
<span data-ttu-id="b7e0e-106">Polecenie **cmdlet Add-AzDataLakeStoreItemContent** dodaje zawartość do elementu w sklepie Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b7e0e-106">The **Add-AzDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="b7e0e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b7e0e-107">EXAMPLES</span></span>

### <span data-ttu-id="b7e0e-108">Przykład 1. Dodawanie zawartości do pliku</span><span class="sxs-lookup"><span data-stu-id="b7e0e-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="b7e0e-109">To polecenie dodaje zawartość do pliku myFile.txt.</span><span class="sxs-lookup"><span data-stu-id="b7e0e-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="b7e0e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7e0e-110">PARAMETERS</span></span>

### <span data-ttu-id="b7e0e-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="b7e0e-111">-Account</span></span>
<span data-ttu-id="b7e0e-112">Określa nazwę konta sklepu Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b7e0e-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="b7e0e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7e0e-113">-DefaultProfile</span></span>
<span data-ttu-id="b7e0e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="b7e0e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7e0e-115">— Kodowanie</span><span class="sxs-lookup"><span data-stu-id="b7e0e-115">-Encoding</span></span>
<span data-ttu-id="b7e0e-116">Określa kodowanie elementu do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="b7e0e-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="b7e0e-117">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b7e0e-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7e0e-118">Nieznany</span><span class="sxs-lookup"><span data-stu-id="b7e0e-118">Unknown</span></span>
- <span data-ttu-id="b7e0e-119">Ciąg</span><span class="sxs-lookup"><span data-stu-id="b7e0e-119">String</span></span>
- <span data-ttu-id="b7e0e-120">Unicode</span><span class="sxs-lookup"><span data-stu-id="b7e0e-120">Unicode</span></span>
- <span data-ttu-id="b7e0e-121">Bajt</span><span class="sxs-lookup"><span data-stu-id="b7e0e-121">Byte</span></span>
- <span data-ttu-id="b7e0e-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="b7e0e-122">BigEndianUnicode</span></span>
- <span data-ttu-id="b7e0e-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="b7e0e-123">UTF8</span></span>
- <span data-ttu-id="b7e0e-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="b7e0e-124">UTF7</span></span>
- <span data-ttu-id="b7e0e-125">Ascii</span><span class="sxs-lookup"><span data-stu-id="b7e0e-125">Ascii</span></span>
- <span data-ttu-id="b7e0e-126">Domyślne</span><span class="sxs-lookup"><span data-stu-id="b7e0e-126">Default</span></span>
- <span data-ttu-id="b7e0e-127">Oem</span><span class="sxs-lookup"><span data-stu-id="b7e0e-127">Oem</span></span>
- <span data-ttu-id="b7e0e-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="b7e0e-128">BigEndianUTF32</span></span>

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

### <span data-ttu-id="b7e0e-129">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="b7e0e-129">-Path</span></span>
<span data-ttu-id="b7e0e-130">Określa ścieżkę sklepu Data Lake Store elementu do zmodyfikowania, począwszy od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="b7e0e-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="b7e0e-131">— Wartość</span><span class="sxs-lookup"><span data-stu-id="b7e0e-131">-Value</span></span>
<span data-ttu-id="b7e0e-132">Określa zawartość do dodania do elementu.</span><span class="sxs-lookup"><span data-stu-id="b7e0e-132">Specifies the content to add to the item.</span></span>

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

### <span data-ttu-id="b7e0e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7e0e-133">CommonParameters</span></span>
<span data-ttu-id="b7e0e-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7e0e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7e0e-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7e0e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7e0e-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7e0e-136">INPUTS</span></span>

### <span data-ttu-id="b7e0e-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b7e0e-137">System.String</span></span>

### <span data-ttu-id="b7e0e-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="b7e0e-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="b7e0e-139">System.Object</span><span class="sxs-lookup"><span data-stu-id="b7e0e-139">System.Object</span></span>

### <span data-ttu-id="b7e0e-140">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="b7e0e-140">System.Text.Encoding</span></span>

## <span data-ttu-id="b7e0e-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7e0e-141">OUTPUTS</span></span>

### <span data-ttu-id="b7e0e-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b7e0e-142">System.Boolean</span></span>

## <span data-ttu-id="b7e0e-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b7e0e-143">NOTES</span></span>

## <span data-ttu-id="b7e0e-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7e0e-144">RELATED LINKS</span></span>

[<span data-ttu-id="b7e0e-145">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="b7e0e-145">Get-AzDataLakeStoreItemContent</span></span>](./Get-AzDataLakeStoreItemContent.md)


