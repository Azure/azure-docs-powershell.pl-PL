---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: a5087c3c2d2354eb33ab9777687d43f56f3eb42c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549215"
---
# <span data-ttu-id="745dc-101">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="745dc-101">Test-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="745dc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="745dc-102">SYNOPSIS</span></span>
<span data-ttu-id="745dc-103">Sprawdza istnienie pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="745dc-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="745dc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="745dc-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="745dc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="745dc-105">DESCRIPTION</span></span>
<span data-ttu-id="745dc-106">Polecenie cmdlet **test-AzureRmDataLakeStoreItem** sprawdza istnienie pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="745dc-106">The **Test-AzureRmDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="745dc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="745dc-107">EXAMPLES</span></span>

### <span data-ttu-id="745dc-108">Przykład 1: testowanie pliku</span><span class="sxs-lookup"><span data-stu-id="745dc-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="745dc-109">To polecenie sprawdza, czy plik Test.csv istnieje na koncie usługi ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="745dc-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="745dc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="745dc-110">PARAMETERS</span></span>

### <span data-ttu-id="745dc-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="745dc-111">-Account</span></span>
<span data-ttu-id="745dc-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="745dc-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="745dc-113">-Path</span><span class="sxs-lookup"><span data-stu-id="745dc-113">-Path</span></span>
<span data-ttu-id="745dc-114">Określa ścieżkę elementu, który należy przetestować, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="745dc-114">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="745dc-115">-PathType</span><span class="sxs-lookup"><span data-stu-id="745dc-115">-PathType</span></span>
<span data-ttu-id="745dc-116">Określa typ testowanego elementu.</span><span class="sxs-lookup"><span data-stu-id="745dc-116">Specifies the type of item to test.</span></span>
<span data-ttu-id="745dc-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="745dc-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="745dc-118">Jakieś</span><span class="sxs-lookup"><span data-stu-id="745dc-118">Any</span></span> 
- <span data-ttu-id="745dc-119">Plik</span><span class="sxs-lookup"><span data-stu-id="745dc-119">File</span></span> 
- <span data-ttu-id="745dc-120">Folder</span><span class="sxs-lookup"><span data-stu-id="745dc-120">Folder</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType
Parameter Sets: (All)
Aliases: 
Accepted values: Any, File, Folder

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="745dc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="745dc-121">-DefaultProfile</span></span>
<span data-ttu-id="745dc-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="745dc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="745dc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="745dc-123">CommonParameters</span></span>
<span data-ttu-id="745dc-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="745dc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="745dc-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="745dc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="745dc-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="745dc-126">INPUTS</span></span>

## <span data-ttu-id="745dc-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="745dc-127">OUTPUTS</span></span>

### <span data-ttu-id="745dc-128">logiczną</span><span class="sxs-lookup"><span data-stu-id="745dc-128">bool</span></span>
<span data-ttu-id="745dc-129">Prawda lub FAŁSZ wskazujący istnienie określonego pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="745dc-129">True or false indicating the existence of the specified file or folder.</span></span>

## <span data-ttu-id="745dc-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="745dc-130">NOTES</span></span>

## <span data-ttu-id="745dc-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="745dc-131">RELATED LINKS</span></span>

[<span data-ttu-id="745dc-132">Eksportowanie — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="745dc-132">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="745dc-133">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="745dc-133">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="745dc-134">Import — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="745dc-134">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="745dc-135">Dołącz do AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="745dc-135">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="745dc-136">Przenieś — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="745dc-136">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="745dc-137">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="745dc-137">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)


