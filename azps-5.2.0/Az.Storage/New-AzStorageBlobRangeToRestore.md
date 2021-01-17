---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324805"
---
# <span data-ttu-id="6fad2-101">New-AzStorageBlobRangeToRestore</span><span class="sxs-lookup"><span data-stu-id="6fad2-101">New-AzStorageBlobRangeToRestore</span></span>

## <span data-ttu-id="6fad2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6fad2-102">SYNOPSIS</span></span>
<span data-ttu-id="6fad2-103">Tworzy obiekt zakresu BLOB w celu przywrócenia konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="6fad2-103">Creates a Blob Range object to restores a Storage account.</span></span>

## <span data-ttu-id="6fad2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6fad2-104">SYNTAX</span></span>

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fad2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6fad2-105">DESCRIPTION</span></span>
<span data-ttu-id="6fad2-106">Polecenie cmdlet **New-AzStorageBlobRangeToRestore** tworzy obiekt Range obiektu BLOB, którego można użyć w funkcji Restore-AzStorageBlobRange.</span><span class="sxs-lookup"><span data-stu-id="6fad2-106">The **New-AzStorageBlobRangeToRestore** cmdlet creates a Blob range object, which can be used in Restore-AzStorageBlobRange.</span></span>

## <span data-ttu-id="6fad2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6fad2-107">EXAMPLES</span></span>

### <span data-ttu-id="6fad2-108">Przykład 1: Tworzenie zakresu obiektu BLOB do przywrócenia</span><span class="sxs-lookup"><span data-stu-id="6fad2-108">Example 1: Creates a blob range to restore</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

<span data-ttu-id="6fad2-109">To polecenie tworzy zakres obiektu BLOB do przywrócenia, który rozpoczyna się od container1/blob1 (dołączanie) i kończy się na container2/blob2 (Exclude).</span><span class="sxs-lookup"><span data-stu-id="6fad2-109">This command creates a blob range to restore, which starts at container1/blob1 (include), and ends at container2/blob2 (exclude).</span></span>

### <span data-ttu-id="6fad2-110">Przykład 2: tworzy zakres obiektu BLOB, który zostanie przywrócony z pierwszego obiektu BLOB w kolejności alfabetycznej, do określonego obiektu BLOB (Wyklucz)</span><span class="sxs-lookup"><span data-stu-id="6fad2-110">Example 2: Creates a blob range which will restore from first blob in alphabetical order, to a specific blob (exclude)</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

<span data-ttu-id="6fad2-111">To polecenie tworzy zakres obiektu BLOB, który zostanie przywrócony z pierwszego obiektu BLOB kolejności alfabetycznej do określonego obiektu BLOB container2/blob2 (Wyklucz).</span><span class="sxs-lookup"><span data-stu-id="6fad2-111">This command creates a blob range which will restore from first blob of alphabetical order, to a specific blob container2/blob2 (exclude)</span></span>

### <span data-ttu-id="6fad2-112">Przykład 3: tworzy zakres obiektu BLOB, który zostanie przywrócony z określonego obiektu BLOB (include), do ostatniego obiektu BLOB w kolejności alfabetycznej.</span><span class="sxs-lookup"><span data-stu-id="6fad2-112">Example 3: Creates a blob range which will restore from a specific blob (include), to the last blob in alphabetical order</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

<span data-ttu-id="6fad2-113">To polecenie tworzy zakres obiektu BLOB, który zostanie przywrócony z określonego obiektu BLOB container1/blob1 (include), do ostatniego obiektu BLOB w kolejności alfabetycznej.</span><span class="sxs-lookup"><span data-stu-id="6fad2-113">This command creates a blob range which will restore from a specific blob container1/blob1 (include), to the last blob in alphabetical order.</span></span>

### <span data-ttu-id="6fad2-114">Przykład 4: tworzy zakres BLOB, który przywraca wszystkie obiekty blob</span><span class="sxs-lookup"><span data-stu-id="6fad2-114">Example 4: Creates a blob range which will restore all blobs</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

<span data-ttu-id="6fad2-115">To polecenie tworzy zakres obiektu BLOB, w którym zostaną przywrócone wszystkie obiekty blob.</span><span class="sxs-lookup"><span data-stu-id="6fad2-115">This command creates a blob range which will restore all blobs.</span></span>

## <span data-ttu-id="6fad2-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6fad2-116">PARAMETERS</span></span>

### <span data-ttu-id="6fad2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fad2-117">-DefaultProfile</span></span>
<span data-ttu-id="6fad2-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6fad2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fad2-119">-EndRange</span><span class="sxs-lookup"><span data-stu-id="6fad2-119">-EndRange</span></span>
<span data-ttu-id="6fad2-120">Określ zakres końcowy przywracania obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="6fad2-120">Specify the blob restore End range.</span></span>
<span data-ttu-id="6fad2-121">Zakres końcowy zostanie wykluczony w obszarze Przywróć obiekty blob.</span><span class="sxs-lookup"><span data-stu-id="6fad2-121">End range will be excluded in restore blobs.</span></span>
<span data-ttu-id="6fad2-122">Ustaw ją jako pustą strng, aby przywrócić jej koniec.</span><span class="sxs-lookup"><span data-stu-id="6fad2-122">Set it as empty strng to restore to the end.</span></span>

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

### <span data-ttu-id="6fad2-123">-StartRange</span><span class="sxs-lookup"><span data-stu-id="6fad2-123">-StartRange</span></span>
<span data-ttu-id="6fad2-124">Określ zakres początkowy przywracania obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="6fad2-124">Specify the blob restore start range.</span></span>
<span data-ttu-id="6fad2-125">Zakres początkowy zostanie dołączony do funkcji Przywróć obiekty blob.</span><span class="sxs-lookup"><span data-stu-id="6fad2-125">Start range will be included in restore blobs.</span></span>
<span data-ttu-id="6fad2-126">Ustaw ją jako ciąg pusty, aby przywrócić z początku.</span><span class="sxs-lookup"><span data-stu-id="6fad2-126">Set it as empty string to restore from begining.</span></span>

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

### <span data-ttu-id="6fad2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fad2-127">CommonParameters</span></span>
<span data-ttu-id="6fad2-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fad2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fad2-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fad2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fad2-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fad2-130">INPUTS</span></span>

### <span data-ttu-id="6fad2-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6fad2-131">None</span></span>

## <span data-ttu-id="6fad2-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6fad2-132">OUTPUTS</span></span>

### <span data-ttu-id="6fad2-133">Microsoft. Azure. Commands. Management. Storage. models. PSBlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="6fad2-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span></span>

## <span data-ttu-id="6fad2-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6fad2-134">NOTES</span></span>

## <span data-ttu-id="6fad2-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6fad2-135">RELATED LINKS</span></span>
