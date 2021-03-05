---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
ms.openlocfilehash: 3a39e2f341404ac3f6dbb75c27408dd9d9ee2d47
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009153"
---
# <span data-ttu-id="83115-101">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83115-101">Get-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="83115-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83115-102">SYNOPSIS</span></span>
<span data-ttu-id="83115-103">Pobiera szczegółowe informacje o pliku lub folderze w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="83115-103">Gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="83115-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="83115-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83115-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="83115-105">DESCRIPTION</span></span>
<span data-ttu-id="83115-106">Polecenie **cmdlet Get-AzDataLakeStoreItem** pobiera szczegóły pliku lub folderu w magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="83115-106">The **Get-AzDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="83115-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="83115-107">EXAMPLES</span></span>

### <span data-ttu-id="83115-108">Przykład 1. Uzyskiwanie szczegółów pliku ze sklepu Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="83115-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="83115-109">To polecenie pobiera szczegółowe informacje o pliku Test.csv z magazynu Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="83115-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="83115-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83115-110">PARAMETERS</span></span>

### <span data-ttu-id="83115-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="83115-111">-Account</span></span>
<span data-ttu-id="83115-112">Określa nazwę konta sklepu Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="83115-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="83115-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83115-113">-DefaultProfile</span></span>
<span data-ttu-id="83115-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="83115-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83115-115">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="83115-115">-Path</span></span>
<span data-ttu-id="83115-116">Określa ścieżkę sklepu Data Lake Store, z której mają być zbierane szczegóły elementu, zaczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="83115-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="83115-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83115-117">CommonParameters</span></span>
<span data-ttu-id="83115-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83115-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83115-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83115-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83115-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83115-120">INPUTS</span></span>

### <span data-ttu-id="83115-121">System.String</span><span class="sxs-lookup"><span data-stu-id="83115-121">System.String</span></span>

### <span data-ttu-id="83115-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="83115-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="83115-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83115-123">OUTPUTS</span></span>

### <span data-ttu-id="83115-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83115-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="83115-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="83115-125">NOTES</span></span>

## <span data-ttu-id="83115-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83115-126">RELATED LINKS</span></span>

[<span data-ttu-id="83115-127">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83115-127">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="83115-128">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="83115-128">Get-AzDataLakeStoreChildItem</span></span>](./Get-AzDataLakeStoreChildItem.md)

[<span data-ttu-id="83115-129">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83115-129">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="83115-130">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83115-130">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="83115-131">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83115-131">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="83115-132">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83115-132">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="83115-133">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83115-133">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="83115-134">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83115-134">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


