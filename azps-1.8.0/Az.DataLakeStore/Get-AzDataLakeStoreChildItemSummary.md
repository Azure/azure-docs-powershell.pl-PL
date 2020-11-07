---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorechilditemsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
ms.openlocfilehash: 76490987a6a4d016a1d07b29cd69484305ddf849
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868551"
---
# <span data-ttu-id="4d992-101">Get-AzDataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="4d992-101">Get-AzDataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="4d992-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d992-102">SYNOPSIS</span></span>
<span data-ttu-id="4d992-103">Pobiera podsumowanie całkowitego rozmiaru, plików i katalogów znajdujących się w określonej ścieżce.</span><span class="sxs-lookup"><span data-stu-id="4d992-103">Gets the summary of total size, files and directories contained in the path specified</span></span>

## <span data-ttu-id="4d992-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d992-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItemSummary [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d992-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4d992-105">DESCRIPTION</span></span>
<span data-ttu-id="4d992-106">**Element get-AzDataLakeStoreChildItemSummary** pobiera podsumowanie zawartości dla danej ścieżki.</span><span class="sxs-lookup"><span data-stu-id="4d992-106">The **Get-AzDataLakeStoreChildItemSummary** retrieves the content summary for a given path.</span></span> <span data-ttu-id="4d992-107">Rekurencyjnie oblicza całkowitą liczbę plików, katalogów i całkowity rozmiar wszystkich plików pod daną ścieżką.</span><span class="sxs-lookup"><span data-stu-id="4d992-107">It recursively computes total number of files, directories and total size of all the files under the given path.</span></span>

## <span data-ttu-id="4d992-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d992-108">EXAMPLES</span></span>

### <span data-ttu-id="4d992-109">Przykład 1. Pobieranie podsumowania zawartości folderu</span><span class="sxs-lookup"><span data-stu-id="4d992-109">Example 1: Get the content summary of a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreChildItemSummary -Account ContosoADL -Path /a -Concurrency 128
```

<span data-ttu-id="4d992-110">Zawiera ona liczbę wszystkich katalogów, plików i ich rozmiar w obszarze/a.</span><span class="sxs-lookup"><span data-stu-id="4d992-110">It lists number of total directories, files and their size contained under /a.</span></span>

## <span data-ttu-id="4d992-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d992-111">PARAMETERS</span></span>

### <span data-ttu-id="4d992-112">— Konto</span><span class="sxs-lookup"><span data-stu-id="4d992-112">-Account</span></span>
<span data-ttu-id="4d992-113">Konto usługi Data Lake Store do wykonywania operacji na systemie plików</span><span class="sxs-lookup"><span data-stu-id="4d992-113">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="4d992-114">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="4d992-114">-Concurrency</span></span>
<span data-ttu-id="4d992-115">Wskazuje liczbę plików/katalogów przetworzonych równolegle.</span><span class="sxs-lookup"><span data-stu-id="4d992-115">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="4d992-116">Wartość domyślna będzie obliczana jako Najlepsza nakład pracy na podstawie specyfikacji systemu.</span><span class="sxs-lookup"><span data-stu-id="4d992-116">Default will be computed as a best effort based on system specification.</span></span>

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

### <span data-ttu-id="4d992-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d992-117">-DefaultProfile</span></span>
<span data-ttu-id="4d992-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d992-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d992-119">-Path</span><span class="sxs-lookup"><span data-stu-id="4d992-119">-Path</span></span>
<span data-ttu-id="4d992-120">Ścieżka na określonym koncie Data Lake, które powinno być pobrane.</span><span class="sxs-lookup"><span data-stu-id="4d992-120">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="4d992-121">Może to być plik lub folder w formacie "/folder/file.txt", gdzie pierwszy znak "/" po systemie DNS wskazuje katalog główny systemu plików.</span><span class="sxs-lookup"><span data-stu-id="4d992-121">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

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

### <span data-ttu-id="4d992-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4d992-122">-Confirm</span></span>
<span data-ttu-id="4d992-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d992-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d992-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d992-124">-WhatIf</span></span>
<span data-ttu-id="4d992-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d992-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d992-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4d992-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d992-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d992-127">CommonParameters</span></span>
<span data-ttu-id="4d992-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d992-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d992-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d992-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d992-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d992-130">INPUTS</span></span>

### <span data-ttu-id="4d992-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4d992-131">System.String</span></span>

### <span data-ttu-id="4d992-132">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="4d992-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="4d992-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4d992-133">System.Int32</span></span>

## <span data-ttu-id="4d992-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d992-134">OUTPUTS</span></span>

### <span data-ttu-id="4d992-135">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="4d992-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="4d992-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d992-136">NOTES</span></span>

## <span data-ttu-id="4d992-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d992-137">RELATED LINKS</span></span>
