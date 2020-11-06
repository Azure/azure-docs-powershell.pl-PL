---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 8aae62ccbf79f2b3c59f6009aa5233daf00853fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548755"
---
# <span data-ttu-id="0fed7-101">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="0fed7-101">Set-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="0fed7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0fed7-102">SYNOPSIS</span></span>
<span data-ttu-id="0fed7-103">Modyfikuje szczegóły źródła danych konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0fed7-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fed7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0fed7-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fed7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0fed7-105">DESCRIPTION</span></span>
<span data-ttu-id="0fed7-106">Polecenie cmdlet **Set-AzureRmDataLakeAnalyticsDataSource** modyfikuje szczegóły źródła danych konta usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0fed7-106">The **Set-AzureRmDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="0fed7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0fed7-107">EXAMPLES</span></span>

### <span data-ttu-id="0fed7-108">Przykład 1. Zmienianie klucza dostępu dla źródła danych</span><span class="sxs-lookup"><span data-stu-id="0fed7-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="0fed7-109">To polecenie powoduje zmianę klucza dostępu przechowywanego dla źródła danych magazynu obiektów blob platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0fed7-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="0fed7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0fed7-110">PARAMETERS</span></span>

### <span data-ttu-id="0fed7-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="0fed7-111">-AccessKey</span></span>
<span data-ttu-id="0fed7-112">Określa nowy klucz dostępu do źródła danych magazynu obiektów blob platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0fed7-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="0fed7-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="0fed7-113">-Account</span></span>
<span data-ttu-id="0fed7-114">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0fed7-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="0fed7-115">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="0fed7-115">-Blob</span></span>
<span data-ttu-id="0fed7-116">Określa nazwę źródła danych magazynu obiektów blob platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0fed7-116">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="0fed7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fed7-117">-DefaultProfile</span></span>
<span data-ttu-id="0fed7-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0fed7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0fed7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fed7-119">-ResourceGroupName</span></span>
<span data-ttu-id="0fed7-120">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0fed7-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="0fed7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fed7-121">CommonParameters</span></span>
<span data-ttu-id="0fed7-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fed7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fed7-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fed7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fed7-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0fed7-124">INPUTS</span></span>

### <span data-ttu-id="0fed7-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0fed7-125">System.String</span></span>

## <span data-ttu-id="0fed7-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0fed7-126">OUTPUTS</span></span>

### <span data-ttu-id="0fed7-127">System. void</span><span class="sxs-lookup"><span data-stu-id="0fed7-127">System.Void</span></span>

## <span data-ttu-id="0fed7-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0fed7-128">NOTES</span></span>

## <span data-ttu-id="0fed7-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0fed7-129">RELATED LINKS</span></span>

[<span data-ttu-id="0fed7-130">Dodaj-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="0fed7-130">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="0fed7-131">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="0fed7-131">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)


