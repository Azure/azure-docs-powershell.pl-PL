---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: 0f74ad9b146a0c5d2f2c65b7109fb57f56902834
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002593"
---
# <span data-ttu-id="e42dd-101">New-AzStorageBlobRangeToRestore</span><span class="sxs-lookup"><span data-stu-id="e42dd-101">New-AzStorageBlobRangeToRestore</span></span>

## <span data-ttu-id="e42dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e42dd-102">SYNOPSIS</span></span>
<span data-ttu-id="e42dd-103">Tworzy obiekt zakres obiektów blob w celu przywrócenia konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="e42dd-103">Creates a Blob Range object to restores a Storage account.</span></span>

## <span data-ttu-id="e42dd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e42dd-104">SYNTAX</span></span>

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e42dd-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e42dd-105">DESCRIPTION</span></span>
<span data-ttu-id="e42dd-106">Polecenie **cmdlet New-AzStorageBlobRangeToRestore** tworzy obiekt zakresu obiektów blob, który może być używany w przywróceniu azStorageBlobRange.</span><span class="sxs-lookup"><span data-stu-id="e42dd-106">The **New-AzStorageBlobRangeToRestore** cmdlet creates a Blob range object, which can be used in Restore-AzStorageBlobRange.</span></span>

## <span data-ttu-id="e42dd-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e42dd-107">EXAMPLES</span></span>

### <span data-ttu-id="e42dd-108">Przykład 1. Tworzy zakres obiektów blob do przywrócenia</span><span class="sxs-lookup"><span data-stu-id="e42dd-108">Example 1: Creates a blob range to restore</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

<span data-ttu-id="e42dd-109">To polecenie tworzy zakres obiektów blob do przywrócenia, który zaczyna się od container1/blob1 (include) i kończy się na kontenerze2/obiekcie blob2 (exclude).</span><span class="sxs-lookup"><span data-stu-id="e42dd-109">This command creates a blob range to restore, which starts at container1/blob1 (include), and ends at container2/blob2 (exclude).</span></span>

### <span data-ttu-id="e42dd-110">Przykład 2. Tworzy zakres obiektów blob, który przywróci pierwszy obiekt blob w kolejności alfabetycznej, do określonego obiektu blob (exclude)</span><span class="sxs-lookup"><span data-stu-id="e42dd-110">Example 2: Creates a blob range which will restore from first blob in alphabetical order, to a specific blob (exclude)</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

<span data-ttu-id="e42dd-111">To polecenie tworzy zakres obiektów blob, który przywraca z pierwszego obiektu blob w kolejności alfabetycznej do określonego kontenera obiektów blob2/blob2 (exclude)</span><span class="sxs-lookup"><span data-stu-id="e42dd-111">This command creates a blob range which will restore from first blob of alphabetical order, to a specific blob container2/blob2 (exclude)</span></span>

### <span data-ttu-id="e42dd-112">Przykład 3. Tworzy zakres obiektów blob, który przywróci określony obiekt blob (include) do ostatniego obiektu blob w kolejności alfabetycznej</span><span class="sxs-lookup"><span data-stu-id="e42dd-112">Example 3: Creates a blob range which will restore from a specific blob (include), to the last blob in alphabetical order</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

<span data-ttu-id="e42dd-113">To polecenie tworzy zakres obiektów blob, który zostanie przywrócony z określonego kontenera obiektów blob1/blob1 (include) do ostatniego obiektu blob w kolejności alfabetycznej.</span><span class="sxs-lookup"><span data-stu-id="e42dd-113">This command creates a blob range which will restore from a specific blob container1/blob1 (include), to the last blob in alphabetical order.</span></span>

### <span data-ttu-id="e42dd-114">Przykład 4. Tworzy zakres obiektów blob, co spowoduje przywrócenie wszystkich obiektów blob</span><span class="sxs-lookup"><span data-stu-id="e42dd-114">Example 4: Creates a blob range which will restore all blobs</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

<span data-ttu-id="e42dd-115">To polecenie tworzy zakres obiektów blob, co spowoduje przywrócenie wszystkich obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="e42dd-115">This command creates a blob range which will restore all blobs.</span></span>

## <span data-ttu-id="e42dd-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e42dd-116">PARAMETERS</span></span>

### <span data-ttu-id="e42dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e42dd-117">-DefaultProfile</span></span>
<span data-ttu-id="e42dd-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e42dd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e42dd-119">-EndRange</span><span class="sxs-lookup"><span data-stu-id="e42dd-119">-EndRange</span></span>
<span data-ttu-id="e42dd-120">Określ zakres końcowy przywracania obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="e42dd-120">Specify the blob restore End range.</span></span>
<span data-ttu-id="e42dd-121">Zakres końcowy zostanie wykluczony w przypadku obiektów blob przywracania.</span><span class="sxs-lookup"><span data-stu-id="e42dd-121">End range will be excluded in restore blobs.</span></span>
<span data-ttu-id="e42dd-122">Ustaw go jako pusty strng, aby przywrócić do końca.</span><span class="sxs-lookup"><span data-stu-id="e42dd-122">Set it as empty strng to restore to the end.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e42dd-123">-StartRange</span><span class="sxs-lookup"><span data-stu-id="e42dd-123">-StartRange</span></span>
<span data-ttu-id="e42dd-124">Określ zakres rozpoczęcia przywracania obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="e42dd-124">Specify the blob restore start range.</span></span>
<span data-ttu-id="e42dd-125">Zakres rozpoczęcia zostanie uwzględniony w obiektach blob przywracania.</span><span class="sxs-lookup"><span data-stu-id="e42dd-125">Start range will be included in restore blobs.</span></span>
<span data-ttu-id="e42dd-126">Ustaw go jako pusty ciąg, który będzie przywracany od początku.</span><span class="sxs-lookup"><span data-stu-id="e42dd-126">Set it as empty string to restore from begining.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e42dd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e42dd-127">CommonParameters</span></span>
<span data-ttu-id="e42dd-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e42dd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e42dd-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e42dd-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e42dd-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e42dd-130">INPUTS</span></span>

### <span data-ttu-id="e42dd-131">Brak</span><span class="sxs-lookup"><span data-stu-id="e42dd-131">None</span></span>

## <span data-ttu-id="e42dd-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e42dd-132">OUTPUTS</span></span>

### <span data-ttu-id="e42dd-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="e42dd-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span></span>

## <span data-ttu-id="e42dd-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e42dd-134">NOTES</span></span>

## <span data-ttu-id="e42dd-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e42dd-135">RELATED LINKS</span></span>
