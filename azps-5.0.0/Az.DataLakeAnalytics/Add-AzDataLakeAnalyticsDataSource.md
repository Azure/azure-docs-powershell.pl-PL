---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A38D8BF6-D302-4586-B7AF-4C80B546E96F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: ddb291a72d3c35c79321ddefa0832d46c489998f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305893"
---
# <span data-ttu-id="6bf99-101">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="6bf99-101">Add-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="6bf99-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6bf99-102">SYNOPSIS</span></span>
<span data-ttu-id="6bf99-103">Dodaje źródło danych do konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6bf99-103">Adds a data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="6bf99-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6bf99-104">SYNTAX</span></span>

### <span data-ttu-id="6bf99-105">AddDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6bf99-105">AddDataLakeStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bf99-106">AddBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6bf99-106">AddBlobStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6bf99-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6bf99-107">DESCRIPTION</span></span>
<span data-ttu-id="6bf99-108">Polecenie cmdlet **Add-AzDataLakeAnalyticsDataSource** umożliwia dodanie źródła danych do konta usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6bf99-108">The **Add-AzDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="6bf99-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6bf99-109">EXAMPLES</span></span>

### <span data-ttu-id="6bf99-110">Przykład 1. Dodawanie źródła danych do konta</span><span class="sxs-lookup"><span data-stu-id="6bf99-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="6bf99-111">To polecenie umożliwia dodanie źródła danych usługi Data Lake Store do konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6bf99-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="6bf99-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6bf99-112">PARAMETERS</span></span>

### <span data-ttu-id="6bf99-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="6bf99-113">-AccessKey</span></span>
<span data-ttu-id="6bf99-114">Określa klucz dostępu konta usługi Azure Blob Storage, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="6bf99-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

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

### <span data-ttu-id="6bf99-115">— Konto</span><span class="sxs-lookup"><span data-stu-id="6bf99-115">-Account</span></span>
<span data-ttu-id="6bf99-116">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6bf99-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="6bf99-117">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="6bf99-117">-Blob</span></span>
<span data-ttu-id="6bf99-118">Określa nazwę konta usługi Azure Blob Storage, które ma zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="6bf99-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

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

### <span data-ttu-id="6bf99-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6bf99-119">-DataLakeStore</span></span>
<span data-ttu-id="6bf99-120">Określa nazwę konta usługi Azure Data Lake Store, które ma zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="6bf99-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

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

### <span data-ttu-id="6bf99-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bf99-121">-DefaultProfile</span></span>
<span data-ttu-id="6bf99-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6bf99-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6bf99-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bf99-123">-ResourceGroupName</span></span>
<span data-ttu-id="6bf99-124">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6bf99-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="6bf99-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bf99-125">CommonParameters</span></span>
<span data-ttu-id="6bf99-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bf99-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bf99-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bf99-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bf99-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6bf99-128">INPUTS</span></span>

### <span data-ttu-id="6bf99-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6bf99-129">System.String</span></span>

## <span data-ttu-id="6bf99-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6bf99-130">OUTPUTS</span></span>

### <span data-ttu-id="6bf99-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="6bf99-131">System.Object</span></span>
## <span data-ttu-id="6bf99-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6bf99-132">NOTES</span></span>

## <span data-ttu-id="6bf99-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6bf99-133">RELATED LINKS</span></span>

[<span data-ttu-id="6bf99-134">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="6bf99-134">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="6bf99-135">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="6bf99-135">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


