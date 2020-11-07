---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: b0390f4ec9ec7c141e7d059c88d7aeb4b9c8507d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705895"
---
# <span data-ttu-id="6b758-101">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6b758-101">Get-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="6b758-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6b758-102">SYNOPSIS</span></span>
<span data-ttu-id="6b758-103">Pobiera informacje o koncie Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6b758-103">Gets information about a Data Lake Analytics account.</span></span>

## <span data-ttu-id="6b758-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6b758-104">SYNTAX</span></span>

### <span data-ttu-id="6b758-105">GetAllInSubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6b758-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b758-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6b758-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b758-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="6b758-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b758-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6b758-108">DESCRIPTION</span></span>
<span data-ttu-id="6b758-109">Polecenie cmdlet **Get-AzDataLakeAnalyticsAccount** pobiera informacje o koncie usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6b758-109">The **Get-AzDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="6b758-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6b758-110">EXAMPLES</span></span>

### <span data-ttu-id="6b758-111">Przykład 1: uzyskiwanie informacji o koncie w usłudze Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="6b758-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="6b758-112">To polecenie pobiera informacje o koncie o nazwie ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="6b758-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="6b758-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b758-113">PARAMETERS</span></span>

### <span data-ttu-id="6b758-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b758-114">-DefaultProfile</span></span>
<span data-ttu-id="6b758-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6b758-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b758-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6b758-116">-Name</span></span>
<span data-ttu-id="6b758-117">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6b758-117">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="6b758-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b758-118">-ResourceGroupName</span></span>
<span data-ttu-id="6b758-119">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6b758-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="6b758-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b758-120">CommonParameters</span></span>
<span data-ttu-id="6b758-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b758-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b758-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b758-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b758-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b758-123">INPUTS</span></span>

### <span data-ttu-id="6b758-124">System. String</span><span class="sxs-lookup"><span data-stu-id="6b758-124">System.String</span></span>

## <span data-ttu-id="6b758-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6b758-125">OUTPUTS</span></span>

### <span data-ttu-id="6b758-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6b758-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

### <span data-ttu-id="6b758-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span><span class="sxs-lookup"><span data-stu-id="6b758-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span></span>

## <span data-ttu-id="6b758-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6b758-128">NOTES</span></span>

## <span data-ttu-id="6b758-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b758-129">RELATED LINKS</span></span>

[<span data-ttu-id="6b758-130">Nowe — AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6b758-130">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="6b758-131">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6b758-131">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="6b758-132">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6b758-132">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="6b758-133">Test — AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6b758-133">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


