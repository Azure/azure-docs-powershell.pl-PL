---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 0dd0dfb25959ed3a5753ae6bd19b0500d4742634
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223998"
---
# <span data-ttu-id="af660-101">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="af660-101">Set-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="af660-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="af660-102">SYNOPSIS</span></span>
<span data-ttu-id="af660-103">Modyfikuje szczegóły źródła danych konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="af660-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="af660-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="af660-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af660-105">Opis</span><span class="sxs-lookup"><span data-stu-id="af660-105">DESCRIPTION</span></span>
<span data-ttu-id="af660-106">Polecenie cmdlet **Set-AzDataLakeAnalyticsDataSource** modyfikuje szczegóły źródła danych konta usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="af660-106">The **Set-AzDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="af660-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="af660-107">EXAMPLES</span></span>

### <span data-ttu-id="af660-108">Przykład 1. Zmienianie klucza dostępu dla źródła danych</span><span class="sxs-lookup"><span data-stu-id="af660-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="af660-109">To polecenie powoduje zmianę klucza dostępu przechowywanego dla źródła danych magazynu obiektów blob platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="af660-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="af660-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="af660-110">PARAMETERS</span></span>

### <span data-ttu-id="af660-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="af660-111">-AccessKey</span></span>
<span data-ttu-id="af660-112">Określa nowy klucz dostępu do źródła danych magazynu obiektów blob platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="af660-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="af660-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="af660-113">-Account</span></span>
<span data-ttu-id="af660-114">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="af660-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="af660-115">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="af660-115">-Blob</span></span>
<span data-ttu-id="af660-116">Określa nazwę źródła danych magazynu obiektów blob platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="af660-116">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="af660-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af660-117">-DefaultProfile</span></span>
<span data-ttu-id="af660-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="af660-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af660-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af660-119">-ResourceGroupName</span></span>
<span data-ttu-id="af660-120">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="af660-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="af660-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af660-121">CommonParameters</span></span>
<span data-ttu-id="af660-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af660-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af660-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af660-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af660-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af660-124">INPUTS</span></span>

### <span data-ttu-id="af660-125">System. String</span><span class="sxs-lookup"><span data-stu-id="af660-125">System.String</span></span>

## <span data-ttu-id="af660-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="af660-126">OUTPUTS</span></span>

### <span data-ttu-id="af660-127">System. void</span><span class="sxs-lookup"><span data-stu-id="af660-127">System.Void</span></span>

## <span data-ttu-id="af660-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="af660-128">NOTES</span></span>

## <span data-ttu-id="af660-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af660-129">RELATED LINKS</span></span>

[<span data-ttu-id="af660-130">Dodaj-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="af660-130">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="af660-131">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="af660-131">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)


