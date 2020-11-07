---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: a7b47425aad152d8851ff90717698b4c25ef026d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718225"
---
# <span data-ttu-id="2c0c4-101">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2c0c4-101">Get-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="2c0c4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c0c4-102">SYNOPSIS</span></span>
<span data-ttu-id="2c0c4-103">Pobiera szczegóły dotyczące pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2c0c4-103">Gets the details of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c0c4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c0c4-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c0c4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2c0c4-105">DESCRIPTION</span></span>
<span data-ttu-id="2c0c4-106">Polecenie cmdlet **Get-AzureRmDataLakeStoreItem** pobiera szczegóły pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2c0c4-106">The **Get-AzureRmDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="2c0c4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c0c4-107">EXAMPLES</span></span>

### <span data-ttu-id="2c0c4-108">Przykład 1: uzyskiwanie szczegółowych informacji o pliku z usługi Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="2c0c4-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="2c0c4-109">To polecenie pobiera szczegóły pliku Test.csv z usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2c0c4-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="2c0c4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c0c4-110">PARAMETERS</span></span>

### <span data-ttu-id="2c0c4-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="2c0c4-111">-Account</span></span>
<span data-ttu-id="2c0c4-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2c0c4-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="2c0c4-113">-Path</span><span class="sxs-lookup"><span data-stu-id="2c0c4-113">-Path</span></span>
<span data-ttu-id="2c0c4-114">Określa ścieżkę usługi Data Lake Store, z której należy uzyskać szczegóły elementu, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="2c0c4-114">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="2c0c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c0c4-115">-DefaultProfile</span></span>
<span data-ttu-id="2c0c4-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c0c4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c0c4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c0c4-117">CommonParameters</span></span>
<span data-ttu-id="2c0c4-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c0c4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c0c4-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c0c4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c0c4-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c0c4-120">INPUTS</span></span>

## <span data-ttu-id="2c0c4-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c0c4-121">OUTPUTS</span></span>

### <span data-ttu-id="2c0c4-122">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2c0c4-122">DataLakeStoreItem</span></span>
<span data-ttu-id="2c0c4-123">Plik lub folder w określonym podanej ścieżce.</span><span class="sxs-lookup"><span data-stu-id="2c0c4-123">The file or folder at the path specified.</span></span>

## <span data-ttu-id="2c0c4-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c0c4-124">NOTES</span></span>

## <span data-ttu-id="2c0c4-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c0c4-125">RELATED LINKS</span></span>

[<span data-ttu-id="2c0c4-126">Eksportowanie — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2c0c4-126">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2c0c4-127">Get-AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="2c0c4-127">Get-AzureRmDataLakeStoreChildItem</span></span>](./Get-AzureRmDataLakeStoreChildItem.md)

[<span data-ttu-id="2c0c4-128">Import — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2c0c4-128">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2c0c4-129">Dołącz do AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2c0c4-129">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2c0c4-130">Przenieś — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2c0c4-130">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2c0c4-131">Nowe — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2c0c4-131">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2c0c4-132">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2c0c4-132">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2c0c4-133">Test — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2c0c4-133">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


