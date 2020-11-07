---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/test-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: bf754e335753efc5350d3c0979db9f0f7057f010
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718503"
---
# <span data-ttu-id="6aae2-101">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6aae2-101">Test-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="6aae2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6aae2-102">SYNOPSIS</span></span>
<span data-ttu-id="6aae2-103">Sprawdza istnienie pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6aae2-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6aae2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6aae2-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6aae2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6aae2-105">DESCRIPTION</span></span>
<span data-ttu-id="6aae2-106">Polecenie cmdlet **test-AzureRmDataLakeStoreItem** sprawdza istnienie pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6aae2-106">The **Test-AzureRmDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="6aae2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6aae2-107">EXAMPLES</span></span>

### <span data-ttu-id="6aae2-108">Przykład 1: testowanie pliku</span><span class="sxs-lookup"><span data-stu-id="6aae2-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="6aae2-109">To polecenie sprawdza, czy plik Test.csv istnieje na koncie usługi ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="6aae2-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="6aae2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6aae2-110">PARAMETERS</span></span>

### <span data-ttu-id="6aae2-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="6aae2-111">-Account</span></span>
<span data-ttu-id="6aae2-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6aae2-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="6aae2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aae2-113">-DefaultProfile</span></span>
<span data-ttu-id="6aae2-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6aae2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6aae2-115">-Path</span><span class="sxs-lookup"><span data-stu-id="6aae2-115">-Path</span></span>
<span data-ttu-id="6aae2-116">Określa ścieżkę elementu, który należy przetestować, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="6aae2-116">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="6aae2-117">-PathType</span><span class="sxs-lookup"><span data-stu-id="6aae2-117">-PathType</span></span>
<span data-ttu-id="6aae2-118">Określa typ testowanego elementu.</span><span class="sxs-lookup"><span data-stu-id="6aae2-118">Specifies the type of item to test.</span></span>
<span data-ttu-id="6aae2-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6aae2-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6aae2-120">Jakieś</span><span class="sxs-lookup"><span data-stu-id="6aae2-120">Any</span></span> 
- <span data-ttu-id="6aae2-121">Plik</span><span class="sxs-lookup"><span data-stu-id="6aae2-121">File</span></span> 
- <span data-ttu-id="6aae2-122">Folder</span><span class="sxs-lookup"><span data-stu-id="6aae2-122">Folder</span></span>

```yaml
Type: PathType
Parameter Sets: (All)
Aliases: 
Accepted values: Any, File, Folder

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aae2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aae2-123">CommonParameters</span></span>
<span data-ttu-id="6aae2-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aae2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aae2-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aae2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aae2-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6aae2-126">INPUTS</span></span>

### <span data-ttu-id="6aae2-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6aae2-127">None</span></span>
<span data-ttu-id="6aae2-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="6aae2-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6aae2-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6aae2-129">OUTPUTS</span></span>

### <span data-ttu-id="6aae2-130">logiczną</span><span class="sxs-lookup"><span data-stu-id="6aae2-130">bool</span></span>
<span data-ttu-id="6aae2-131">Prawda lub FAŁSZ wskazujący istnienie określonego pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="6aae2-131">True or false indicating the existence of the specified file or folder.</span></span>

## <span data-ttu-id="6aae2-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6aae2-132">NOTES</span></span>

## <span data-ttu-id="6aae2-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6aae2-133">RELATED LINKS</span></span>

[<span data-ttu-id="6aae2-134">Eksportowanie — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6aae2-134">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6aae2-135">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6aae2-135">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6aae2-136">Import — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6aae2-136">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6aae2-137">Dołącz do AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6aae2-137">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6aae2-138">Przenieś — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6aae2-138">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6aae2-139">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6aae2-139">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)


