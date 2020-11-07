---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: f272d7c57a1543f916d828d6324dd23f5780ccad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717126"
---
# <span data-ttu-id="f2756-101">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="f2756-101">Add-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="f2756-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f2756-102">SYNOPSIS</span></span>
<span data-ttu-id="f2756-103">Dodawanie zawartości do elementu w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f2756-103">Adds content to an item in a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2756-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f2756-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2756-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f2756-105">DESCRIPTION</span></span>
<span data-ttu-id="f2756-106">Polecenie cmdlet **Add-AzureRmDataLakeStoreItemContent** umożliwia dodanie zawartości do elementu w usłudze Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f2756-106">The **Add-AzureRmDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="f2756-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f2756-107">EXAMPLES</span></span>

### <span data-ttu-id="f2756-108">Przykład 1. Dodawanie zawartości do pliku</span><span class="sxs-lookup"><span data-stu-id="f2756-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzureRmDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="f2756-109">To polecenie umożliwia dodanie zawartości do pliku myFile.txt.</span><span class="sxs-lookup"><span data-stu-id="f2756-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="f2756-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f2756-110">PARAMETERS</span></span>

### <span data-ttu-id="f2756-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="f2756-111">-Account</span></span>
<span data-ttu-id="f2756-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f2756-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f2756-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2756-113">-DefaultProfile</span></span>
<span data-ttu-id="f2756-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f2756-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2756-115">-Encoding</span><span class="sxs-lookup"><span data-stu-id="f2756-115">-Encoding</span></span>
<span data-ttu-id="f2756-116">Określa kodowanie elementu, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="f2756-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="f2756-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f2756-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f2756-118">Wiadom</span><span class="sxs-lookup"><span data-stu-id="f2756-118">Unknown</span></span>
- <span data-ttu-id="f2756-119">Ciąg</span><span class="sxs-lookup"><span data-stu-id="f2756-119">String</span></span>
- <span data-ttu-id="f2756-120">Ze</span><span class="sxs-lookup"><span data-stu-id="f2756-120">Unicode</span></span>
- <span data-ttu-id="f2756-121">Jednobajtowe</span><span class="sxs-lookup"><span data-stu-id="f2756-121">Byte</span></span>
- <span data-ttu-id="f2756-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="f2756-122">BigEndianUnicode</span></span>
- <span data-ttu-id="f2756-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="f2756-123">UTF8</span></span>
- <span data-ttu-id="f2756-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="f2756-124">UTF7</span></span>
- <span data-ttu-id="f2756-125">Znaki</span><span class="sxs-lookup"><span data-stu-id="f2756-125">Ascii</span></span>
- <span data-ttu-id="f2756-126">Domyślne</span><span class="sxs-lookup"><span data-stu-id="f2756-126">Default</span></span>
- <span data-ttu-id="f2756-127">Equipment</span><span class="sxs-lookup"><span data-stu-id="f2756-127">Oem</span></span>
- <span data-ttu-id="f2756-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="f2756-128">BigEndianUTF32</span></span>

```yaml
Type: FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2756-129">-Path</span><span class="sxs-lookup"><span data-stu-id="f2756-129">-Path</span></span>
<span data-ttu-id="f2756-130">Określa ścieżkę elementu, który należy zmodyfikować, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="f2756-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="f2756-131">-Value</span><span class="sxs-lookup"><span data-stu-id="f2756-131">-Value</span></span>
<span data-ttu-id="f2756-132">Określa zawartość, którą należy dodać do elementu.</span><span class="sxs-lookup"><span data-stu-id="f2756-132">Specifies the content to add to the item.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2756-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2756-133">CommonParameters</span></span>
<span data-ttu-id="f2756-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2756-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2756-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2756-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2756-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2756-136">INPUTS</span></span>

### <span data-ttu-id="f2756-137">Stream</span><span class="sxs-lookup"><span data-stu-id="f2756-137">Object</span></span>
<span data-ttu-id="f2756-138">Parametr "value" przyjmuje wartość typu "Object" z procesu</span><span class="sxs-lookup"><span data-stu-id="f2756-138">Parameter 'Value' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="f2756-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f2756-139">OUTPUTS</span></span>

### <span data-ttu-id="f2756-140">logiczną</span><span class="sxs-lookup"><span data-stu-id="f2756-140">bool</span></span>
<span data-ttu-id="f2756-141">Zwraca wartość prawda w przypadku sukcesu.</span><span class="sxs-lookup"><span data-stu-id="f2756-141">Returns true on success.</span></span>

## <span data-ttu-id="f2756-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f2756-142">NOTES</span></span>

## <span data-ttu-id="f2756-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2756-143">RELATED LINKS</span></span>

[<span data-ttu-id="f2756-144">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="f2756-144">Get-AzureRmDataLakeStoreItemContent</span></span>](./Get-AzureRmDataLakeStoreItemContent.md)

