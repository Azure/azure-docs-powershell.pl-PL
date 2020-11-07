---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A38D8BF6-D302-4586-B7AF-4C80B546E96F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 19b8b5a00e5bcb75b90a91097316dc065afa025b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710070"
---
# <span data-ttu-id="01e3a-101">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="01e3a-101">Add-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="01e3a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="01e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="01e3a-103">Dodaje źródło danych do konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="01e3a-103">Adds a data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="01e3a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="01e3a-104">SYNTAX</span></span>

### <span data-ttu-id="01e3a-105">AddDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="01e3a-105">AddDataLakeStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01e3a-106">AddBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="01e3a-106">AddBlobStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01e3a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="01e3a-107">DESCRIPTION</span></span>
<span data-ttu-id="01e3a-108">Polecenie cmdlet **Add-AzDataLakeAnalyticsDataSource** umożliwia dodanie źródła danych do konta usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="01e3a-108">The **Add-AzDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="01e3a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="01e3a-109">EXAMPLES</span></span>

### <span data-ttu-id="01e3a-110">Przykład 1. Dodawanie źródła danych do konta</span><span class="sxs-lookup"><span data-stu-id="01e3a-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="01e3a-111">To polecenie umożliwia dodanie źródła danych usługi Data Lake Store do konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="01e3a-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="01e3a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="01e3a-112">PARAMETERS</span></span>

### <span data-ttu-id="01e3a-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="01e3a-113">-AccessKey</span></span>
<span data-ttu-id="01e3a-114">Określa klucz dostępu konta usługi Azure Blob Storage, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="01e3a-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddBlobStorageAccount
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01e3a-115">— Konto</span><span class="sxs-lookup"><span data-stu-id="01e3a-115">-Account</span></span>
<span data-ttu-id="01e3a-116">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="01e3a-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="01e3a-117">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="01e3a-117">-Blob</span></span>
<span data-ttu-id="01e3a-118">Określa nazwę konta usługi Azure Blob Storage, które ma zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="01e3a-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01e3a-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="01e3a-119">-DataLakeStore</span></span>
<span data-ttu-id="01e3a-120">Określa nazwę konta usługi Azure Data Lake Store, które ma zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="01e3a-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddDataLakeStorageAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01e3a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01e3a-121">-DefaultProfile</span></span>
<span data-ttu-id="01e3a-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="01e3a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01e3a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01e3a-123">-ResourceGroupName</span></span>
<span data-ttu-id="01e3a-124">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="01e3a-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01e3a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01e3a-125">CommonParameters</span></span>
<span data-ttu-id="01e3a-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01e3a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01e3a-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01e3a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01e3a-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01e3a-128">INPUTS</span></span>

### <span data-ttu-id="01e3a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="01e3a-129">System.String</span></span>

## <span data-ttu-id="01e3a-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="01e3a-130">OUTPUTS</span></span>

### <span data-ttu-id="01e3a-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="01e3a-131">System.Object</span></span>
## <span data-ttu-id="01e3a-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="01e3a-132">NOTES</span></span>

## <span data-ttu-id="01e3a-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01e3a-133">RELATED LINKS</span></span>

[<span data-ttu-id="01e3a-134">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="01e3a-134">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="01e3a-135">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="01e3a-135">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)

