---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 32c7478e7e2419a8f83c839efd841f25446a96c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541760"
---
# <span data-ttu-id="acce7-101">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="acce7-101">Get-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="acce7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="acce7-102">SYNOPSIS</span></span>
<span data-ttu-id="acce7-103">Pobiera informacje o koncie Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="acce7-103">Gets information about a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acce7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="acce7-104">SYNTAX</span></span>

### <span data-ttu-id="acce7-105">GetAllInSubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="acce7-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acce7-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="acce7-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="acce7-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="acce7-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acce7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="acce7-108">DESCRIPTION</span></span>
<span data-ttu-id="acce7-109">Polecenie cmdlet **Get-AzureRmDataLakeAnalyticsAccount** pobiera informacje o koncie usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="acce7-109">The **Get-AzureRmDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="acce7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="acce7-110">EXAMPLES</span></span>

### <span data-ttu-id="acce7-111">Przykład 1: uzyskiwanie informacji o koncie w usłudze Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="acce7-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="acce7-112">To polecenie pobiera informacje o koncie o nazwie ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="acce7-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="acce7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="acce7-113">PARAMETERS</span></span>

### <span data-ttu-id="acce7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acce7-114">-DefaultProfile</span></span>
<span data-ttu-id="acce7-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="acce7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="acce7-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="acce7-116">-Name</span></span>
<span data-ttu-id="acce7-117">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="acce7-117">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acce7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acce7-118">-ResourceGroupName</span></span>
<span data-ttu-id="acce7-119">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="acce7-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acce7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acce7-120">CommonParameters</span></span>
<span data-ttu-id="acce7-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acce7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acce7-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acce7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acce7-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="acce7-123">INPUTS</span></span>

### <span data-ttu-id="acce7-124">System. String</span><span class="sxs-lookup"><span data-stu-id="acce7-124">System.String</span></span>

## <span data-ttu-id="acce7-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="acce7-125">OUTPUTS</span></span>

### <span data-ttu-id="acce7-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="acce7-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="acce7-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="acce7-127">NOTES</span></span>

## <span data-ttu-id="acce7-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="acce7-128">RELATED LINKS</span></span>

[<span data-ttu-id="acce7-129">Nowe — AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="acce7-129">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="acce7-130">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="acce7-130">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="acce7-131">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="acce7-131">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="acce7-132">Test — AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="acce7-132">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


