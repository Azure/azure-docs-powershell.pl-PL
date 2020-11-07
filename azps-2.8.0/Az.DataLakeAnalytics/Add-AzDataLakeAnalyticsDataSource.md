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
ms.locfileid: "93705905"
---
# <span data-ttu-id="a617e-101">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="a617e-101">Add-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="a617e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a617e-102">SYNOPSIS</span></span>
<span data-ttu-id="a617e-103">Dodaje źródło danych do konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a617e-103">Adds a data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="a617e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a617e-104">SYNTAX</span></span>

### <span data-ttu-id="a617e-105">AddDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a617e-105">AddDataLakeStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a617e-106">AddBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a617e-106">AddBlobStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a617e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a617e-107">DESCRIPTION</span></span>
<span data-ttu-id="a617e-108">Polecenie cmdlet **Add-AzDataLakeAnalyticsDataSource** umożliwia dodanie źródła danych do konta usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a617e-108">The **Add-AzDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="a617e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a617e-109">EXAMPLES</span></span>

### <span data-ttu-id="a617e-110">Przykład 1. Dodawanie źródła danych do konta</span><span class="sxs-lookup"><span data-stu-id="a617e-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="a617e-111">To polecenie umożliwia dodanie źródła danych usługi Data Lake Store do konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a617e-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="a617e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a617e-112">PARAMETERS</span></span>

### <span data-ttu-id="a617e-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="a617e-113">-AccessKey</span></span>
<span data-ttu-id="a617e-114">Określa klucz dostępu konta usługi Azure Blob Storage, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="a617e-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

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

### <span data-ttu-id="a617e-115">— Konto</span><span class="sxs-lookup"><span data-stu-id="a617e-115">-Account</span></span>
<span data-ttu-id="a617e-116">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a617e-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="a617e-117">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="a617e-117">-Blob</span></span>
<span data-ttu-id="a617e-118">Określa nazwę konta usługi Azure Blob Storage, które ma zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="a617e-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

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

### <span data-ttu-id="a617e-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a617e-119">-DataLakeStore</span></span>
<span data-ttu-id="a617e-120">Określa nazwę konta usługi Azure Data Lake Store, które ma zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="a617e-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

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

### <span data-ttu-id="a617e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a617e-121">-DefaultProfile</span></span>
<span data-ttu-id="a617e-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a617e-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a617e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a617e-123">-ResourceGroupName</span></span>
<span data-ttu-id="a617e-124">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a617e-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="a617e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a617e-125">CommonParameters</span></span>
<span data-ttu-id="a617e-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a617e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a617e-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a617e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a617e-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a617e-128">INPUTS</span></span>

### <span data-ttu-id="a617e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a617e-129">System.String</span></span>

## <span data-ttu-id="a617e-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a617e-130">OUTPUTS</span></span>

### <span data-ttu-id="a617e-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="a617e-131">System.Object</span></span>
## <span data-ttu-id="a617e-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a617e-132">NOTES</span></span>

## <span data-ttu-id="a617e-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a617e-133">RELATED LINKS</span></span>

[<span data-ttu-id="a617e-134">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="a617e-134">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="a617e-135">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="a617e-135">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


