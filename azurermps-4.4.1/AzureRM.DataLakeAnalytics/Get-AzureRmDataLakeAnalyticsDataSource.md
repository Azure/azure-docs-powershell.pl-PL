---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: b7f2c6f2077d0b7e9c7510f6984ada15a65d6ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719336"
---
# <span data-ttu-id="45bd0-101">Get-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="45bd0-101">Get-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="45bd0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45bd0-102">SYNOPSIS</span></span>
<span data-ttu-id="45bd0-103">Pobiera źródło danych funkcji Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="45bd0-103">Gets a Data Lake Analytics data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45bd0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45bd0-104">SYNTAX</span></span>

### <span data-ttu-id="45bd0-105">Lista wszystkich źródeł danych (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="45bd0-105">List all data sources (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45bd0-106">Uzyskiwanie konta w usłudze Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="45bd0-106">Get a Data Lake Store account</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45bd0-107">Uzyskiwanie konta magazynu obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="45bd0-107">Get a Blob storage account</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45bd0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="45bd0-108">DESCRIPTION</span></span>
<span data-ttu-id="45bd0-109">Polecenie cmdlet **Get-AzureRmDataLakeAnalyticsDataSource** Pobiera źródło danych usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="45bd0-109">The **Get-AzureRmDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="45bd0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45bd0-110">EXAMPLES</span></span>

### <span data-ttu-id="45bd0-111">Przykład 1: uzyskiwanie źródła danych z konta</span><span class="sxs-lookup"><span data-stu-id="45bd0-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="45bd0-112">To polecenie pobiera źródło danych usługi Data Lake Store o nazwie ContosoAdls z konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="45bd0-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="45bd0-113">Przykład 2: uzyskiwanie listy kont usługi Data Lake Store na koncie usługi Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="45bd0-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="45bd0-114">To polecenie pobiera wszystkie konta usługi Data Lake Store z konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="45bd0-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="45bd0-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45bd0-115">PARAMETERS</span></span>

### <span data-ttu-id="45bd0-116">— Konto</span><span class="sxs-lookup"><span data-stu-id="45bd0-116">-Account</span></span>
<span data-ttu-id="45bd0-117">Określa konto usługi Data Lake Analytics, które to polecenie cmdlet pobiera źródła danych.</span><span class="sxs-lookup"><span data-stu-id="45bd0-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="45bd0-118">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="45bd0-118">-Blob</span></span>
<span data-ttu-id="45bd0-119">Określa nazwę źródła danych magazynu obiektów blob platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="45bd0-119">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a Blob storage account
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45bd0-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="45bd0-120">-DataLakeStore</span></span>
<span data-ttu-id="45bd0-121">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="45bd0-121">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a Data Lake Store account
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45bd0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45bd0-122">-ResourceGroupName</span></span>
<span data-ttu-id="45bd0-123">Określa nazwę grupy zasobów zawierającą źródło danych.</span><span class="sxs-lookup"><span data-stu-id="45bd0-123">Specifies the resource group name that contains the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45bd0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45bd0-124">-DefaultProfile</span></span>
<span data-ttu-id="45bd0-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="45bd0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45bd0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45bd0-126">CommonParameters</span></span>
<span data-ttu-id="45bd0-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45bd0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45bd0-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45bd0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45bd0-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45bd0-129">INPUTS</span></span>

## <span data-ttu-id="45bd0-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45bd0-130">OUTPUTS</span></span>

### <span data-ttu-id="45bd0-131">PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="45bd0-131">PSStorageAccountInfo</span></span>
<span data-ttu-id="45bd0-132">Szczegółowe dane konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="45bd0-132">The specified Azure Storage account details.</span></span>

### <span data-ttu-id="45bd0-133">PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="45bd0-133">PSDataLakeStoreAccountInfo</span></span>
<span data-ttu-id="45bd0-134">Szczegółowe dane konta usługi Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="45bd0-134">The specified Data Lake Store account details</span></span>

### <span data-ttu-id="45bd0-135">Lista<AdlDataSource></span><span class="sxs-lookup"><span data-stu-id="45bd0-135">List<AdlDataSource></span></span>
<span data-ttu-id="45bd0-136">Lista kont magazynu platformy Azure i kont usługi Data Lake Store na określonym koncie usług Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="45bd0-136">The list of both Azure Storage accounts and Data Lake Store accounts in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="45bd0-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45bd0-137">NOTES</span></span>

## <span data-ttu-id="45bd0-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45bd0-138">RELATED LINKS</span></span>

[<span data-ttu-id="45bd0-139">Dodaj-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="45bd0-139">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="45bd0-140">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="45bd0-140">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="45bd0-141">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="45bd0-141">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


