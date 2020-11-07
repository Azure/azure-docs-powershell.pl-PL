---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 1ab8cbd8ead120ecc531e3e252fe2c31a58f10c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716694"
---
# <span data-ttu-id="0a12b-101">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0a12b-101">Get-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="0a12b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0a12b-102">SYNOPSIS</span></span>
<span data-ttu-id="0a12b-103">Pobiera informacje o koncie Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0a12b-103">Gets information about a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a12b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0a12b-104">SYNTAX</span></span>

### <span data-ttu-id="0a12b-105">Wszystkie w abonamentach (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="0a12b-105">All In Subscription (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a12b-106">Cała grupa zasobów</span><span class="sxs-lookup"><span data-stu-id="0a12b-106">All In Resource Group</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0a12b-107">Określone konto</span><span class="sxs-lookup"><span data-stu-id="0a12b-107">Specific Account</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a12b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0a12b-108">DESCRIPTION</span></span>
<span data-ttu-id="0a12b-109">Polecenie cmdlet **Get-AzureRmDataLakeAnalyticsAccount** pobiera informacje o koncie usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0a12b-109">The **Get-AzureRmDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="0a12b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0a12b-110">EXAMPLES</span></span>

### <span data-ttu-id="0a12b-111">Przykład 1: uzyskiwanie informacji o koncie w usłudze Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="0a12b-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="0a12b-112">To polecenie pobiera informacje o koncie o nazwie ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="0a12b-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="0a12b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0a12b-113">PARAMETERS</span></span>

### <span data-ttu-id="0a12b-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0a12b-114">-Name</span></span>
<span data-ttu-id="0a12b-115">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0a12b-115">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a12b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a12b-116">-ResourceGroupName</span></span>
<span data-ttu-id="0a12b-117">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0a12b-117">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a12b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a12b-118">-DefaultProfile</span></span>
<span data-ttu-id="0a12b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0a12b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a12b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a12b-120">CommonParameters</span></span>
<span data-ttu-id="0a12b-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a12b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a12b-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a12b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a12b-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a12b-123">INPUTS</span></span>

## <span data-ttu-id="0a12b-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0a12b-124">OUTPUTS</span></span>

### <span data-ttu-id="0a12b-125">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0a12b-125">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="0a12b-126">Szczegóły określonego konta.</span><span class="sxs-lookup"><span data-stu-id="0a12b-126">The specified account details.</span></span>

### <span data-ttu-id="0a12b-127">Lista<PSDataLakeAnalyticsAccount></span><span class="sxs-lookup"><span data-stu-id="0a12b-127">List<PSDataLakeAnalyticsAccount></span></span>
<span data-ttu-id="0a12b-128">Lista kont w określonej grupie zasobów lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0a12b-128">The list of accounts in the specified resource group or subscription.</span></span>

## <span data-ttu-id="0a12b-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0a12b-129">NOTES</span></span>

## <span data-ttu-id="0a12b-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a12b-130">RELATED LINKS</span></span>

[<span data-ttu-id="0a12b-131">Nowe — AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0a12b-131">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="0a12b-132">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0a12b-132">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="0a12b-133">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0a12b-133">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="0a12b-134">Test — AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0a12b-134">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


