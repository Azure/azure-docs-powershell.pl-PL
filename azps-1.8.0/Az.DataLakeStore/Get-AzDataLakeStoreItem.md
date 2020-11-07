---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
ms.openlocfilehash: b3118c11fa794fef71836a580e272ec481c72147
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868540"
---
# <span data-ttu-id="38fcc-101">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="38fcc-101">Get-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="38fcc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="38fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="38fcc-103">Pobiera szczegóły dotyczące pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="38fcc-103">Gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="38fcc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="38fcc-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38fcc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="38fcc-105">DESCRIPTION</span></span>
<span data-ttu-id="38fcc-106">Polecenie cmdlet **Get-AzDataLakeStoreItem** pobiera szczegóły pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="38fcc-106">The **Get-AzDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="38fcc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="38fcc-107">EXAMPLES</span></span>

### <span data-ttu-id="38fcc-108">Przykład 1: uzyskiwanie szczegółowych informacji o pliku z usługi Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="38fcc-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="38fcc-109">To polecenie pobiera szczegóły pliku Test.csv z usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="38fcc-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="38fcc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="38fcc-110">PARAMETERS</span></span>

### <span data-ttu-id="38fcc-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="38fcc-111">-Account</span></span>
<span data-ttu-id="38fcc-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="38fcc-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="38fcc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38fcc-113">-DefaultProfile</span></span>
<span data-ttu-id="38fcc-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="38fcc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38fcc-115">-Path</span><span class="sxs-lookup"><span data-stu-id="38fcc-115">-Path</span></span>
<span data-ttu-id="38fcc-116">Określa ścieżkę usługi Data Lake Store, z której należy uzyskać szczegóły elementu, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="38fcc-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="38fcc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38fcc-117">CommonParameters</span></span>
<span data-ttu-id="38fcc-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38fcc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38fcc-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38fcc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38fcc-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38fcc-120">INPUTS</span></span>

### <span data-ttu-id="38fcc-121">System. String</span><span class="sxs-lookup"><span data-stu-id="38fcc-121">System.String</span></span>

### <span data-ttu-id="38fcc-122">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="38fcc-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="38fcc-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="38fcc-123">OUTPUTS</span></span>

### <span data-ttu-id="38fcc-124">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="38fcc-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="38fcc-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="38fcc-125">NOTES</span></span>

## <span data-ttu-id="38fcc-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38fcc-126">RELATED LINKS</span></span>

[<span data-ttu-id="38fcc-127">Eksportowanie — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="38fcc-127">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="38fcc-128">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="38fcc-128">Get-AzDataLakeStoreChildItem</span></span>](./Get-AzDataLakeStoreChildItem.md)

[<span data-ttu-id="38fcc-129">Import — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="38fcc-129">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="38fcc-130">Dołącz do AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="38fcc-130">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="38fcc-131">Przenieś — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="38fcc-131">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="38fcc-132">Nowe — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="38fcc-132">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="38fcc-133">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="38fcc-133">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="38fcc-134">Test — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="38fcc-134">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


