---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: a1e70286364fea53062a75b7ac886834803c3674
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552116"
---
# <span data-ttu-id="73ed6-101">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="73ed6-101">Get-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="73ed6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="73ed6-102">SYNOPSIS</span></span>
<span data-ttu-id="73ed6-103">Pobiera szczegóły dotyczące pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="73ed6-103">Gets the details of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73ed6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="73ed6-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73ed6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="73ed6-105">DESCRIPTION</span></span>
<span data-ttu-id="73ed6-106">Polecenie cmdlet **Get-AzureRmDataLakeStoreItem** pobiera szczegóły pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="73ed6-106">The **Get-AzureRmDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="73ed6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="73ed6-107">EXAMPLES</span></span>

### <span data-ttu-id="73ed6-108">Przykład 1: uzyskiwanie szczegółowych informacji o pliku z usługi Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="73ed6-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="73ed6-109">To polecenie pobiera szczegóły pliku Test.csv z usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="73ed6-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="73ed6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="73ed6-110">PARAMETERS</span></span>

### <span data-ttu-id="73ed6-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="73ed6-111">-Account</span></span>
<span data-ttu-id="73ed6-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="73ed6-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="73ed6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73ed6-113">-DefaultProfile</span></span>
<span data-ttu-id="73ed6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="73ed6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73ed6-115">-Path</span><span class="sxs-lookup"><span data-stu-id="73ed6-115">-Path</span></span>
<span data-ttu-id="73ed6-116">Określa ścieżkę usługi Data Lake Store, z której należy uzyskać szczegóły elementu, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="73ed6-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="73ed6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73ed6-117">CommonParameters</span></span>
<span data-ttu-id="73ed6-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73ed6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73ed6-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73ed6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73ed6-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73ed6-120">INPUTS</span></span>

### <span data-ttu-id="73ed6-121">System. String</span><span class="sxs-lookup"><span data-stu-id="73ed6-121">System.String</span></span>

### <span data-ttu-id="73ed6-122">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="73ed6-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="73ed6-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="73ed6-123">OUTPUTS</span></span>

### <span data-ttu-id="73ed6-124">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="73ed6-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="73ed6-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="73ed6-125">NOTES</span></span>

## <span data-ttu-id="73ed6-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73ed6-126">RELATED LINKS</span></span>

[<span data-ttu-id="73ed6-127">Eksportowanie — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="73ed6-127">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="73ed6-128">Get-AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="73ed6-128">Get-AzureRmDataLakeStoreChildItem</span></span>](./Get-AzureRmDataLakeStoreChildItem.md)

[<span data-ttu-id="73ed6-129">Import — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="73ed6-129">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="73ed6-130">Dołącz do AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="73ed6-130">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="73ed6-131">Przenieś — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="73ed6-131">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="73ed6-132">Nowe — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="73ed6-132">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="73ed6-133">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="73ed6-133">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="73ed6-134">Test — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="73ed6-134">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


