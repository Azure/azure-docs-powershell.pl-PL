---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/test-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: e9410c8bd63a123f275f6e644971870b998deea0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551271"
---
# <span data-ttu-id="cff5c-101">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cff5c-101">Test-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="cff5c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cff5c-102">SYNOPSIS</span></span>
<span data-ttu-id="cff5c-103">Sprawdza istnienie pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cff5c-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cff5c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cff5c-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cff5c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cff5c-105">DESCRIPTION</span></span>
<span data-ttu-id="cff5c-106">Polecenie cmdlet **test-AzureRmDataLakeStoreItem** sprawdza istnienie pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cff5c-106">The **Test-AzureRmDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="cff5c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cff5c-107">EXAMPLES</span></span>

### <span data-ttu-id="cff5c-108">Przykład 1: testowanie pliku</span><span class="sxs-lookup"><span data-stu-id="cff5c-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="cff5c-109">To polecenie sprawdza, czy plik Test.csv istnieje na koncie usługi ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="cff5c-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="cff5c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cff5c-110">PARAMETERS</span></span>

### <span data-ttu-id="cff5c-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="cff5c-111">-Account</span></span>
<span data-ttu-id="cff5c-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cff5c-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="cff5c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cff5c-113">-DefaultProfile</span></span>
<span data-ttu-id="cff5c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cff5c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cff5c-115">-Path</span><span class="sxs-lookup"><span data-stu-id="cff5c-115">-Path</span></span>
<span data-ttu-id="cff5c-116">Określa ścieżkę elementu, który należy przetestować, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="cff5c-116">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="cff5c-117">-PathType</span><span class="sxs-lookup"><span data-stu-id="cff5c-117">-PathType</span></span>
<span data-ttu-id="cff5c-118">Określa typ testowanego elementu.</span><span class="sxs-lookup"><span data-stu-id="cff5c-118">Specifies the type of item to test.</span></span>
<span data-ttu-id="cff5c-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="cff5c-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cff5c-120">Jakieś</span><span class="sxs-lookup"><span data-stu-id="cff5c-120">Any</span></span> 
- <span data-ttu-id="cff5c-121">Plik</span><span class="sxs-lookup"><span data-stu-id="cff5c-121">File</span></span> 
- <span data-ttu-id="cff5c-122">Folder</span><span class="sxs-lookup"><span data-stu-id="cff5c-122">Folder</span></span>

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

### <span data-ttu-id="cff5c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cff5c-123">CommonParameters</span></span>
<span data-ttu-id="cff5c-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cff5c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cff5c-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cff5c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cff5c-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cff5c-126">INPUTS</span></span>

### <span data-ttu-id="cff5c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="cff5c-127">System.String</span></span>

### <span data-ttu-id="cff5c-128">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="cff5c-128">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="cff5c-129">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreEnums + PathType</span><span class="sxs-lookup"><span data-stu-id="cff5c-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType</span></span>

## <span data-ttu-id="cff5c-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cff5c-130">OUTPUTS</span></span>

### <span data-ttu-id="cff5c-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cff5c-131">System.Boolean</span></span>

## <span data-ttu-id="cff5c-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cff5c-132">NOTES</span></span>

## <span data-ttu-id="cff5c-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cff5c-133">RELATED LINKS</span></span>

[<span data-ttu-id="cff5c-134">Eksportowanie — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cff5c-134">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="cff5c-135">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cff5c-135">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="cff5c-136">Import — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cff5c-136">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="cff5c-137">Dołącz do AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cff5c-137">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="cff5c-138">Przenieś — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cff5c-138">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="cff5c-139">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cff5c-139">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)


