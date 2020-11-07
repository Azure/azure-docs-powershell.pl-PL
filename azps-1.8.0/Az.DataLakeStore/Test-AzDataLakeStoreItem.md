---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
ms.openlocfilehash: c79e8c225fbbc901d9c39eed85d795cf27d6d1d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710010"
---
# <span data-ttu-id="e6090-101">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e6090-101">Test-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="e6090-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e6090-102">SYNOPSIS</span></span>
<span data-ttu-id="e6090-103">Sprawdza istnienie pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e6090-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e6090-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e6090-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6090-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e6090-105">DESCRIPTION</span></span>
<span data-ttu-id="e6090-106">Polecenie cmdlet **test-AzDataLakeStoreItem** sprawdza istnienie pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e6090-106">The **Test-AzDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e6090-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e6090-107">EXAMPLES</span></span>

### <span data-ttu-id="e6090-108">Przykład 1: testowanie pliku</span><span class="sxs-lookup"><span data-stu-id="e6090-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="e6090-109">To polecenie sprawdza, czy plik Test.csv istnieje na koncie usługi ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="e6090-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="e6090-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e6090-110">PARAMETERS</span></span>

### <span data-ttu-id="e6090-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="e6090-111">-Account</span></span>
<span data-ttu-id="e6090-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e6090-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="e6090-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6090-113">-DefaultProfile</span></span>
<span data-ttu-id="e6090-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e6090-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6090-115">-Path</span><span class="sxs-lookup"><span data-stu-id="e6090-115">-Path</span></span>
<span data-ttu-id="e6090-116">Określa ścieżkę elementu, który należy przetestować, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="e6090-116">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="e6090-117">-PathType</span><span class="sxs-lookup"><span data-stu-id="e6090-117">-PathType</span></span>
<span data-ttu-id="e6090-118">Określa typ testowanego elementu.</span><span class="sxs-lookup"><span data-stu-id="e6090-118">Specifies the type of item to test.</span></span>
<span data-ttu-id="e6090-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e6090-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e6090-120">Jakieś</span><span class="sxs-lookup"><span data-stu-id="e6090-120">Any</span></span> 
- <span data-ttu-id="e6090-121">Plik</span><span class="sxs-lookup"><span data-stu-id="e6090-121">File</span></span> 
- <span data-ttu-id="e6090-122">Folder</span><span class="sxs-lookup"><span data-stu-id="e6090-122">Folder</span></span>

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

### <span data-ttu-id="e6090-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6090-123">CommonParameters</span></span>
<span data-ttu-id="e6090-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6090-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6090-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6090-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6090-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6090-126">INPUTS</span></span>

### <span data-ttu-id="e6090-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e6090-127">System.String</span></span>

### <span data-ttu-id="e6090-128">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="e6090-128">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="e6090-129">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreEnums + PathType</span><span class="sxs-lookup"><span data-stu-id="e6090-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType</span></span>

## <span data-ttu-id="e6090-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e6090-130">OUTPUTS</span></span>

### <span data-ttu-id="e6090-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e6090-131">System.Boolean</span></span>

## <span data-ttu-id="e6090-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e6090-132">NOTES</span></span>

## <span data-ttu-id="e6090-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6090-133">RELATED LINKS</span></span>

[<span data-ttu-id="e6090-134">Eksportowanie — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e6090-134">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="e6090-135">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e6090-135">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="e6090-136">Import — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e6090-136">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="e6090-137">Dołącz do AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e6090-137">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="e6090-138">Przenieś — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e6090-138">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="e6090-139">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e6090-139">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)


