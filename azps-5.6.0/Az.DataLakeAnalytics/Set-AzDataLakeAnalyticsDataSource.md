---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: cb51b1c703d527a2888bd0e80d8cc7a50d044e36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962369"
---
# <span data-ttu-id="9d854-101">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="9d854-101">Set-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="9d854-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d854-102">SYNOPSIS</span></span>
<span data-ttu-id="9d854-103">Modyfikuje szczegóły źródła danych konta Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9d854-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="9d854-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9d854-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d854-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9d854-105">DESCRIPTION</span></span>
<span data-ttu-id="9d854-106">Polecenie **cmdlet Set-AzDataLakeAnalyticsDataSource** modyfikuje szczegóły źródła danych konta usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9d854-106">The **Set-AzDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="9d854-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9d854-107">EXAMPLES</span></span>

### <span data-ttu-id="9d854-108">Przykład 1. Zmienianie klucza dostępu dla źródła danych</span><span class="sxs-lookup"><span data-stu-id="9d854-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="9d854-109">To polecenie zmienia klucz dostępu przechowywany dla źródła danych magazynu obiektów blob platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9d854-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="9d854-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d854-110">PARAMETERS</span></span>

### <span data-ttu-id="9d854-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="9d854-111">-AccessKey</span></span>
<span data-ttu-id="9d854-112">Określa nowy klucz dostępu źródła danych magazynu obiektów blob platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9d854-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="9d854-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="9d854-113">-Account</span></span>
<span data-ttu-id="9d854-114">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9d854-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="9d854-115">— obiekt blob</span><span class="sxs-lookup"><span data-stu-id="9d854-115">-Blob</span></span>
<span data-ttu-id="9d854-116">Określa nazwę źródła danych magazynu obiektów blob platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9d854-116">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="9d854-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d854-117">-DefaultProfile</span></span>
<span data-ttu-id="9d854-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="9d854-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d854-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d854-119">-ResourceGroupName</span></span>
<span data-ttu-id="9d854-120">Określa nazwę grupy zasobów dla konta Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9d854-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="9d854-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d854-121">CommonParameters</span></span>
<span data-ttu-id="9d854-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d854-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d854-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d854-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d854-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d854-124">INPUTS</span></span>

### <span data-ttu-id="9d854-125">System.String</span><span class="sxs-lookup"><span data-stu-id="9d854-125">System.String</span></span>

## <span data-ttu-id="9d854-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d854-126">OUTPUTS</span></span>

### <span data-ttu-id="9d854-127">System.Void</span><span class="sxs-lookup"><span data-stu-id="9d854-127">System.Void</span></span>

## <span data-ttu-id="9d854-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9d854-128">NOTES</span></span>

## <span data-ttu-id="9d854-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d854-129">RELATED LINKS</span></span>

[<span data-ttu-id="9d854-130">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="9d854-130">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="9d854-131">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="9d854-131">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)


