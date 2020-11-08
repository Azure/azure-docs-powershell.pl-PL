---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: 3cf411e75e2a3ec430f13354015d5b6e271c840c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049487"
---
# <span data-ttu-id="d359d-101">Add-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="d359d-101">Add-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="d359d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d359d-102">SYNOPSIS</span></span>
<span data-ttu-id="d359d-103">Dodawanie zawartości do elementu w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d359d-103">Adds content to an item in a Data Lake Store.</span></span>

## <span data-ttu-id="d359d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d359d-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d359d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d359d-105">DESCRIPTION</span></span>
<span data-ttu-id="d359d-106">Polecenie cmdlet **Add-AzDataLakeStoreItemContent** umożliwia dodanie zawartości do elementu w usłudze Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d359d-106">The **Add-AzDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="d359d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d359d-107">EXAMPLES</span></span>

### <span data-ttu-id="d359d-108">Przykład 1. Dodawanie zawartości do pliku</span><span class="sxs-lookup"><span data-stu-id="d359d-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="d359d-109">To polecenie umożliwia dodanie zawartości do pliku myFile.txt.</span><span class="sxs-lookup"><span data-stu-id="d359d-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="d359d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d359d-110">PARAMETERS</span></span>

### <span data-ttu-id="d359d-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="d359d-111">-Account</span></span>
<span data-ttu-id="d359d-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d359d-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d359d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d359d-113">-DefaultProfile</span></span>
<span data-ttu-id="d359d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d359d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d359d-115">-Encoding</span><span class="sxs-lookup"><span data-stu-id="d359d-115">-Encoding</span></span>
<span data-ttu-id="d359d-116">Określa kodowanie elementu, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="d359d-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="d359d-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d359d-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d359d-118">Wiadom</span><span class="sxs-lookup"><span data-stu-id="d359d-118">Unknown</span></span>
- <span data-ttu-id="d359d-119">Ciąg</span><span class="sxs-lookup"><span data-stu-id="d359d-119">String</span></span>
- <span data-ttu-id="d359d-120">Ze</span><span class="sxs-lookup"><span data-stu-id="d359d-120">Unicode</span></span>
- <span data-ttu-id="d359d-121">Jednobajtowe</span><span class="sxs-lookup"><span data-stu-id="d359d-121">Byte</span></span>
- <span data-ttu-id="d359d-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="d359d-122">BigEndianUnicode</span></span>
- <span data-ttu-id="d359d-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="d359d-123">UTF8</span></span>
- <span data-ttu-id="d359d-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="d359d-124">UTF7</span></span>
- <span data-ttu-id="d359d-125">Znaki</span><span class="sxs-lookup"><span data-stu-id="d359d-125">Ascii</span></span>
- <span data-ttu-id="d359d-126">Domyślne</span><span class="sxs-lookup"><span data-stu-id="d359d-126">Default</span></span>
- <span data-ttu-id="d359d-127">Equipment</span><span class="sxs-lookup"><span data-stu-id="d359d-127">Oem</span></span>
- <span data-ttu-id="d359d-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="d359d-128">BigEndianUTF32</span></span>

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

### <span data-ttu-id="d359d-129">-Path</span><span class="sxs-lookup"><span data-stu-id="d359d-129">-Path</span></span>
<span data-ttu-id="d359d-130">Określa ścieżkę elementu, który należy zmodyfikować, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="d359d-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d359d-131">-Value</span><span class="sxs-lookup"><span data-stu-id="d359d-131">-Value</span></span>
<span data-ttu-id="d359d-132">Określa zawartość, którą należy dodać do elementu.</span><span class="sxs-lookup"><span data-stu-id="d359d-132">Specifies the content to add to the item.</span></span>

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

### <span data-ttu-id="d359d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d359d-133">CommonParameters</span></span>
<span data-ttu-id="d359d-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d359d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d359d-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d359d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d359d-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d359d-136">INPUTS</span></span>

### <span data-ttu-id="d359d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d359d-137">System.String</span></span>

### <span data-ttu-id="d359d-138">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d359d-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="d359d-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="d359d-139">System.Object</span></span>

### <span data-ttu-id="d359d-140">System. Text. Encoding</span><span class="sxs-lookup"><span data-stu-id="d359d-140">System.Text.Encoding</span></span>

## <span data-ttu-id="d359d-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d359d-141">OUTPUTS</span></span>

### <span data-ttu-id="d359d-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d359d-142">System.Boolean</span></span>

## <span data-ttu-id="d359d-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d359d-143">NOTES</span></span>

## <span data-ttu-id="d359d-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d359d-144">RELATED LINKS</span></span>

[<span data-ttu-id="d359d-145">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="d359d-145">Get-AzDataLakeStoreItemContent</span></span>](./Get-AzDataLakeStoreItemContent.md)


