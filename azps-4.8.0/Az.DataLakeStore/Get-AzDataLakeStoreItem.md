---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
ms.openlocfilehash: ad741d955399b355534074737741b153d8d48690
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062322"
---
# <span data-ttu-id="e3cb5-101">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e3cb5-101">Get-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="e3cb5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e3cb5-102">SYNOPSIS</span></span>
<span data-ttu-id="e3cb5-103">Pobiera szczegóły dotyczące pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e3cb5-103">Gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e3cb5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e3cb5-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3cb5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e3cb5-105">DESCRIPTION</span></span>
<span data-ttu-id="e3cb5-106">Polecenie cmdlet **Get-AzDataLakeStoreItem** pobiera szczegóły pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e3cb5-106">The **Get-AzDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e3cb5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e3cb5-107">EXAMPLES</span></span>

### <span data-ttu-id="e3cb5-108">Przykład 1: uzyskiwanie szczegółowych informacji o pliku z usługi Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="e3cb5-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="e3cb5-109">To polecenie pobiera szczegóły pliku Test.csv z usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e3cb5-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="e3cb5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3cb5-110">PARAMETERS</span></span>

### <span data-ttu-id="e3cb5-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="e3cb5-111">-Account</span></span>
<span data-ttu-id="e3cb5-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e3cb5-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="e3cb5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3cb5-113">-DefaultProfile</span></span>
<span data-ttu-id="e3cb5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e3cb5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3cb5-115">-Path</span><span class="sxs-lookup"><span data-stu-id="e3cb5-115">-Path</span></span>
<span data-ttu-id="e3cb5-116">Określa ścieżkę usługi Data Lake Store, z której należy uzyskać szczegóły elementu, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="e3cb5-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="e3cb5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3cb5-117">CommonParameters</span></span>
<span data-ttu-id="e3cb5-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3cb5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3cb5-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3cb5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3cb5-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3cb5-120">INPUTS</span></span>

### <span data-ttu-id="e3cb5-121">System. String</span><span class="sxs-lookup"><span data-stu-id="e3cb5-121">System.String</span></span>

### <span data-ttu-id="e3cb5-122">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="e3cb5-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="e3cb5-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e3cb5-123">OUTPUTS</span></span>

### <span data-ttu-id="e3cb5-124">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e3cb5-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="e3cb5-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e3cb5-125">NOTES</span></span>

## <span data-ttu-id="e3cb5-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3cb5-126">RELATED LINKS</span></span>

[<span data-ttu-id="e3cb5-127">Eksportowanie — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e3cb5-127">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="e3cb5-128">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="e3cb5-128">Get-AzDataLakeStoreChildItem</span></span>](./Get-AzDataLakeStoreChildItem.md)

[<span data-ttu-id="e3cb5-129">Import — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e3cb5-129">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="e3cb5-130">Dołącz do AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e3cb5-130">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="e3cb5-131">Przenieś — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e3cb5-131">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="e3cb5-132">Nowe — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e3cb5-132">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="e3cb5-133">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e3cb5-133">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="e3cb5-134">Test — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e3cb5-134">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


