---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: e14e4c1b58b24cb8065681ae806789cd1252a0db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186186"
---
# <span data-ttu-id="c3d02-101">Get-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="c3d02-101">Get-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="c3d02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3d02-102">SYNOPSIS</span></span>
<span data-ttu-id="c3d02-103">Pobiera źródło danych Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c3d02-103">Gets a Data Lake Analytics data source.</span></span>

## <span data-ttu-id="c3d02-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c3d02-104">SYNTAX</span></span>

### <span data-ttu-id="c3d02-105">GetAllDataSources (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c3d02-105">GetAllDataSources (Default)</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3d02-106">GetDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c3d02-106">GetDataLakeStoreAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3d02-107">GetBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c3d02-107">GetBlobStorageAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3d02-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c3d02-108">DESCRIPTION</span></span>
<span data-ttu-id="c3d02-109">Polecenie **cmdlet Get-AzDataLakeAnalyticsDataSource** pobiera źródło danych usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c3d02-109">The **Get-AzDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="c3d02-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c3d02-110">EXAMPLES</span></span>

### <span data-ttu-id="c3d02-111">Przykład 1. Uzyskiwanie źródła danych z konta</span><span class="sxs-lookup"><span data-stu-id="c3d02-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="c3d02-112">To polecenie pobiera źródło danych Data Lake Store o nazwie ContosoAdls z konta Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c3d02-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="c3d02-113">Przykład 2. Uzyskiwanie listy kont usługi Data Lake Store na koncie usługi Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="c3d02-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="c3d02-114">To polecenie pobiera wszystkie konta usługi Data Lake Store z konta Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c3d02-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="c3d02-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3d02-115">PARAMETERS</span></span>

### <span data-ttu-id="c3d02-116">— Konto</span><span class="sxs-lookup"><span data-stu-id="c3d02-116">-Account</span></span>
<span data-ttu-id="c3d02-117">Określa konto usługi Data Lake Analytics, które to polecenie cmdlet pobiera źródła danych.</span><span class="sxs-lookup"><span data-stu-id="c3d02-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="c3d02-118">— obiekt blob</span><span class="sxs-lookup"><span data-stu-id="c3d02-118">-Blob</span></span>
<span data-ttu-id="c3d02-119">Określa nazwę źródła danych magazynu obiektów blob platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c3d02-119">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3d02-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c3d02-120">-DataLakeStore</span></span>
<span data-ttu-id="c3d02-121">Określa nazwę konta w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c3d02-121">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDataLakeStoreAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3d02-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3d02-122">-DefaultProfile</span></span>
<span data-ttu-id="c3d02-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c3d02-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3d02-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3d02-124">-ResourceGroupName</span></span>
<span data-ttu-id="c3d02-125">Określa nazwę grupy zasobów zawierającą źródło danych.</span><span class="sxs-lookup"><span data-stu-id="c3d02-125">Specifies the resource group name that contains the data source.</span></span>

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

### <span data-ttu-id="c3d02-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3d02-126">CommonParameters</span></span>
<span data-ttu-id="c3d02-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3d02-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3d02-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3d02-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3d02-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3d02-129">INPUTS</span></span>

### <span data-ttu-id="c3d02-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c3d02-130">System.String</span></span>

## <span data-ttu-id="c3d02-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3d02-131">OUTPUTS</span></span>

### <span data-ttu-id="c3d02-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="c3d02-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span></span>

### <span data-ttu-id="c3d02-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="c3d02-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span></span>

### <span data-ttu-id="c3d02-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span><span class="sxs-lookup"><span data-stu-id="c3d02-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span></span>

## <span data-ttu-id="c3d02-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c3d02-135">NOTES</span></span>

## <span data-ttu-id="c3d02-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3d02-136">RELATED LINKS</span></span>

[<span data-ttu-id="c3d02-137">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="c3d02-137">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="c3d02-138">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="c3d02-138">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="c3d02-139">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="c3d02-139">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


