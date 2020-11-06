---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A38D8BF6-D302-4586-B7AF-4C80B546E96F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: a3eff47b688f2f426c4f255d400ce1ef73c3c027
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527646"
---
# <span data-ttu-id="6841c-101">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="6841c-101">Add-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="6841c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6841c-102">SYNOPSIS</span></span>
<span data-ttu-id="6841c-103">Dodaje źródło danych do konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6841c-103">Adds a data source to a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6841c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6841c-104">SYNTAX</span></span>

### <span data-ttu-id="6841c-105">Dodawanie konta programu Data Lake Storage</span><span class="sxs-lookup"><span data-stu-id="6841c-105">Add a Data Lake storage account</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6841c-106">Dodawanie konta magazynu obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="6841c-106">Add a Blob storage account</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6841c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6841c-107">DESCRIPTION</span></span>
<span data-ttu-id="6841c-108">Polecenie cmdlet **Add-AzureRmDataLakeAnalyticsDataSource** umożliwia dodanie źródła danych do konta usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6841c-108">The **Add-AzureRmDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="6841c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6841c-109">EXAMPLES</span></span>

### <span data-ttu-id="6841c-110">Przykład 1. Dodawanie źródła danych do konta</span><span class="sxs-lookup"><span data-stu-id="6841c-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="6841c-111">To polecenie umożliwia dodanie źródła danych usługi Data Lake Store do konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6841c-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="6841c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6841c-112">PARAMETERS</span></span>

### <span data-ttu-id="6841c-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="6841c-113">-AccessKey</span></span>
<span data-ttu-id="6841c-114">Określa klucz dostępu konta usługi Azure Blob Storage, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="6841c-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Add a Blob storage account
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6841c-115">— Konto</span><span class="sxs-lookup"><span data-stu-id="6841c-115">-Account</span></span>
<span data-ttu-id="6841c-116">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6841c-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="6841c-117">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="6841c-117">-Blob</span></span>
<span data-ttu-id="6841c-118">Określa nazwę konta usługi Azure Blob Storage, które ma zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="6841c-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Add a Blob storage account
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6841c-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6841c-119">-DataLakeStore</span></span>
<span data-ttu-id="6841c-120">Określa nazwę konta usługi Azure Data Lake Store, które ma zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="6841c-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Add a Data Lake storage account
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6841c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6841c-121">-ResourceGroupName</span></span>
<span data-ttu-id="6841c-122">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6841c-122">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="6841c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6841c-123">-DefaultProfile</span></span>
<span data-ttu-id="6841c-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6841c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6841c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6841c-125">CommonParameters</span></span>
<span data-ttu-id="6841c-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6841c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6841c-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6841c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6841c-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6841c-128">INPUTS</span></span>

## <span data-ttu-id="6841c-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6841c-129">OUTPUTS</span></span>

### <span data-ttu-id="6841c-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6841c-130">None</span></span>

## <span data-ttu-id="6841c-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6841c-131">NOTES</span></span>

## <span data-ttu-id="6841c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6841c-132">RELATED LINKS</span></span>

[<span data-ttu-id="6841c-133">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="6841c-133">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="6841c-134">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="6841c-134">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


