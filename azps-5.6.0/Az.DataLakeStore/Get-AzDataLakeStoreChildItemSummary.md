---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorechilditemsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
ms.openlocfilehash: d83e07e207c2b0e3a03c745abc874814378e5ee4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957290"
---
# <span data-ttu-id="e8dd2-101">Get-AzDataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="e8dd2-101">Get-AzDataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="e8dd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8dd2-102">SYNOPSIS</span></span>
<span data-ttu-id="e8dd2-103">Pobiera podsumowanie całkowitego rozmiaru plików i katalogów zawartych w określonej ścieżce.</span><span class="sxs-lookup"><span data-stu-id="e8dd2-103">Gets the summary of total size, files and directories contained in the path specified</span></span>

## <span data-ttu-id="e8dd2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e8dd2-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItemSummary [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8dd2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e8dd2-105">DESCRIPTION</span></span>
<span data-ttu-id="e8dd2-106">**Get-AzDataLakeStoreChildItemSummary** pobiera podsumowanie zawartości dla danej ścieżki.</span><span class="sxs-lookup"><span data-stu-id="e8dd2-106">The **Get-AzDataLakeStoreChildItemSummary** retrieves the content summary for a given path.</span></span> <span data-ttu-id="e8dd2-107">Rekurencyjnie oblicza całkowitą liczbę plików, katalogów i całkowity rozmiar wszystkich plików w danej ścieżce.</span><span class="sxs-lookup"><span data-stu-id="e8dd2-107">It recursively computes total number of files, directories and total size of all the files under the given path.</span></span>

## <span data-ttu-id="e8dd2-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e8dd2-108">EXAMPLES</span></span>

### <span data-ttu-id="e8dd2-109">Przykład 1. Uzyskiwanie podsumowania zawartości folderu</span><span class="sxs-lookup"><span data-stu-id="e8dd2-109">Example 1: Get the content summary of a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreChildItemSummary -Account ContosoADL -Path /a -Concurrency 128
```

<span data-ttu-id="e8dd2-110">Lista zawiera łączną liczbę katalogów, plików i ich rozmiaru zawartych w obszarze /a.</span><span class="sxs-lookup"><span data-stu-id="e8dd2-110">It lists number of total directories, files and their size contained under /a.</span></span>

## <span data-ttu-id="e8dd2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8dd2-111">PARAMETERS</span></span>

### <span data-ttu-id="e8dd2-112">— Konto</span><span class="sxs-lookup"><span data-stu-id="e8dd2-112">-Account</span></span>
<span data-ttu-id="e8dd2-113">Konto magazynu Data Lake Store w celu wykonania operacji systemu plików w</span><span class="sxs-lookup"><span data-stu-id="e8dd2-113">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="e8dd2-114">— współbieżność</span><span class="sxs-lookup"><span data-stu-id="e8dd2-114">-Concurrency</span></span>
<span data-ttu-id="e8dd2-115">Wskazuje liczbę plików/katalogów przetwarzanych równolegle.</span><span class="sxs-lookup"><span data-stu-id="e8dd2-115">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="e8dd2-116">Wartość domyślna zostanie obliczona według najlepszych starań, na podstawie specyfikacji systemu.</span><span class="sxs-lookup"><span data-stu-id="e8dd2-116">Default will be computed as a best effort based on system specification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8dd2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8dd2-117">-DefaultProfile</span></span>
<span data-ttu-id="e8dd2-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8dd2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8dd2-119">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="e8dd2-119">-Path</span></span>
<span data-ttu-id="e8dd2-120">Ścieżka na określonym koncie data lake, które ma zostać pobrane.</span><span class="sxs-lookup"><span data-stu-id="e8dd2-120">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="e8dd2-121">Może to być plik lub folder W formacie "/folder/file.txt", gdzie pierwszy "/" po systemie DNS wskazuje katalog główny systemu plików.</span><span class="sxs-lookup"><span data-stu-id="e8dd2-121">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8dd2-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e8dd2-122">-Confirm</span></span>
<span data-ttu-id="e8dd2-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e8dd2-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8dd2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8dd2-124">-WhatIf</span></span>
<span data-ttu-id="e8dd2-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8dd2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8dd2-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e8dd2-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8dd2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8dd2-127">CommonParameters</span></span>
<span data-ttu-id="e8dd2-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8dd2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8dd2-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8dd2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8dd2-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8dd2-130">INPUTS</span></span>

### <span data-ttu-id="e8dd2-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e8dd2-131">System.String</span></span>

### <span data-ttu-id="e8dd2-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="e8dd2-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="e8dd2-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e8dd2-133">System.Int32</span></span>

## <span data-ttu-id="e8dd2-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8dd2-134">OUTPUTS</span></span>

### <span data-ttu-id="e8dd2-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="e8dd2-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="e8dd2-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e8dd2-136">NOTES</span></span>

## <span data-ttu-id="e8dd2-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8dd2-137">RELATED LINKS</span></span>
