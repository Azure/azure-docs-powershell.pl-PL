---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: b1a570d2821606944d4afde21919dad8832ed380
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716736"
---
# <span data-ttu-id="f54f1-101">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f54f1-101">Get-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="f54f1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f54f1-102">SYNOPSIS</span></span>
<span data-ttu-id="f54f1-103">Pobiera szczegóły dotyczące pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f54f1-103">Gets the details of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f54f1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f54f1-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f54f1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f54f1-105">DESCRIPTION</span></span>
<span data-ttu-id="f54f1-106">Polecenie cmdlet **Get-AzureRmDataLakeStoreItem** pobiera szczegóły pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f54f1-106">The **Get-AzureRmDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f54f1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f54f1-107">EXAMPLES</span></span>

### <span data-ttu-id="f54f1-108">Przykład 1: uzyskiwanie szczegółowych informacji o pliku z usługi Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="f54f1-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="f54f1-109">To polecenie pobiera szczegóły pliku Test.csv z usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f54f1-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="f54f1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f54f1-110">PARAMETERS</span></span>

### <span data-ttu-id="f54f1-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="f54f1-111">-Account</span></span>
<span data-ttu-id="f54f1-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f54f1-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f54f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f54f1-113">-DefaultProfile</span></span>
<span data-ttu-id="f54f1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f54f1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f54f1-115">-Path</span><span class="sxs-lookup"><span data-stu-id="f54f1-115">-Path</span></span>
<span data-ttu-id="f54f1-116">Określa ścieżkę usługi Data Lake Store, z której należy uzyskać szczegóły elementu, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="f54f1-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="f54f1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f54f1-117">CommonParameters</span></span>
<span data-ttu-id="f54f1-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f54f1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f54f1-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f54f1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f54f1-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f54f1-120">INPUTS</span></span>

### <span data-ttu-id="f54f1-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f54f1-121">None</span></span>
<span data-ttu-id="f54f1-122">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f54f1-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f54f1-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f54f1-123">OUTPUTS</span></span>

### <span data-ttu-id="f54f1-124">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f54f1-124">DataLakeStoreItem</span></span>
<span data-ttu-id="f54f1-125">Plik lub folder w określonym podanej ścieżce.</span><span class="sxs-lookup"><span data-stu-id="f54f1-125">The file or folder at the path specified.</span></span>

## <span data-ttu-id="f54f1-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f54f1-126">NOTES</span></span>

## <span data-ttu-id="f54f1-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f54f1-127">RELATED LINKS</span></span>

[<span data-ttu-id="f54f1-128">Eksportowanie — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f54f1-128">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f54f1-129">Get-AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="f54f1-129">Get-AzureRmDataLakeStoreChildItem</span></span>](./Get-AzureRmDataLakeStoreChildItem.md)

[<span data-ttu-id="f54f1-130">Import — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f54f1-130">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f54f1-131">Dołącz do AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f54f1-131">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f54f1-132">Przenieś — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f54f1-132">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f54f1-133">Nowe — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f54f1-133">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f54f1-134">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f54f1-134">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f54f1-135">Test — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f54f1-135">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


