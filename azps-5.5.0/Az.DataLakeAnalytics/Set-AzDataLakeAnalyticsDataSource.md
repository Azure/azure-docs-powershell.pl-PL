---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 0dd0dfb25959ed3a5753ae6bd19b0500d4742634
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194747"
---
# <span data-ttu-id="70bc4-101">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="70bc4-101">Set-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="70bc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70bc4-102">SYNOPSIS</span></span>
<span data-ttu-id="70bc4-103">Modyfikuje szczegóły źródła danych konta Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="70bc4-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="70bc4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="70bc4-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70bc4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="70bc4-105">DESCRIPTION</span></span>
<span data-ttu-id="70bc4-106">Polecenie **cmdlet Set-AzDataLakeAnalyticsDataSource** modyfikuje szczegóły źródła danych konta usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="70bc4-106">The **Set-AzDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="70bc4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="70bc4-107">EXAMPLES</span></span>

### <span data-ttu-id="70bc4-108">Przykład 1. Zmienianie klucza dostępu dla źródła danych</span><span class="sxs-lookup"><span data-stu-id="70bc4-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="70bc4-109">To polecenie zmienia klucz dostępu przechowywany dla źródła danych magazynu obiektów blob platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="70bc4-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="70bc4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70bc4-110">PARAMETERS</span></span>

### <span data-ttu-id="70bc4-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="70bc4-111">-AccessKey</span></span>
<span data-ttu-id="70bc4-112">Określa nowy klucz dostępu źródła danych magazynu obiektów blob platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="70bc4-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70bc4-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="70bc4-113">-Account</span></span>
<span data-ttu-id="70bc4-114">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="70bc4-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="70bc4-115">— obiekt blob</span><span class="sxs-lookup"><span data-stu-id="70bc4-115">-Blob</span></span>
<span data-ttu-id="70bc4-116">Określa nazwę źródła danych magazynu obiektów blob platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="70bc4-116">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70bc4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70bc4-117">-DefaultProfile</span></span>
<span data-ttu-id="70bc4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="70bc4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70bc4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70bc4-119">-ResourceGroupName</span></span>
<span data-ttu-id="70bc4-120">Określa nazwę grupy zasobów dla konta Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="70bc4-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="70bc4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70bc4-121">CommonParameters</span></span>
<span data-ttu-id="70bc4-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70bc4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70bc4-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70bc4-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70bc4-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70bc4-124">INPUTS</span></span>

### <span data-ttu-id="70bc4-125">System.String</span><span class="sxs-lookup"><span data-stu-id="70bc4-125">System.String</span></span>

## <span data-ttu-id="70bc4-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70bc4-126">OUTPUTS</span></span>

### <span data-ttu-id="70bc4-127">System.Void</span><span class="sxs-lookup"><span data-stu-id="70bc4-127">System.Void</span></span>

## <span data-ttu-id="70bc4-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="70bc4-128">NOTES</span></span>

## <span data-ttu-id="70bc4-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70bc4-129">RELATED LINKS</span></span>

[<span data-ttu-id="70bc4-130">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="70bc4-130">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="70bc4-131">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="70bc4-131">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)


