---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: dcd44f9b43184ffc36d58bd5b65a065d7e81b4b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964778"
---
# <span data-ttu-id="5c408-101">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="5c408-101">Get-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="5c408-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c408-102">SYNOPSIS</span></span>
<span data-ttu-id="5c408-103">Pobiera informacje o koncie usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="5c408-103">Gets information about a Data Lake Analytics account.</span></span>

## <span data-ttu-id="5c408-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5c408-104">SYNTAX</span></span>

### <span data-ttu-id="5c408-105">GetAllInSubscription (domyślne)</span><span class="sxs-lookup"><span data-stu-id="5c408-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c408-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5c408-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5c408-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="5c408-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c408-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5c408-108">DESCRIPTION</span></span>
<span data-ttu-id="5c408-109">Polecenie **cmdlet Get-AzDataLakeAnalyticsAccount** pobiera informacje o koncie usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="5c408-109">The **Get-AzDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="5c408-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5c408-110">EXAMPLES</span></span>

### <span data-ttu-id="5c408-111">Przykład 1. Uzyskiwanie informacji o koncie usługi Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="5c408-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="5c408-112">To polecenie pobiera informacje o koncie o nazwie ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="5c408-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="5c408-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c408-113">PARAMETERS</span></span>

### <span data-ttu-id="5c408-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c408-114">-DefaultProfile</span></span>
<span data-ttu-id="5c408-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="5c408-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c408-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5c408-116">-Name</span></span>
<span data-ttu-id="5c408-117">Określa nazwę konta data lake analytics.</span><span class="sxs-lookup"><span data-stu-id="5c408-117">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="5c408-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c408-118">-ResourceGroupName</span></span>
<span data-ttu-id="5c408-119">Określa nazwę grupy zasobów dla konta Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="5c408-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="5c408-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c408-120">CommonParameters</span></span>
<span data-ttu-id="5c408-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c408-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c408-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c408-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c408-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c408-123">INPUTS</span></span>

### <span data-ttu-id="5c408-124">System.String</span><span class="sxs-lookup"><span data-stu-id="5c408-124">System.String</span></span>

## <span data-ttu-id="5c408-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c408-125">OUTPUTS</span></span>

### <span data-ttu-id="5c408-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="5c408-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

### <span data-ttu-id="5c408-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span><span class="sxs-lookup"><span data-stu-id="5c408-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span></span>

## <span data-ttu-id="5c408-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5c408-128">NOTES</span></span>

## <span data-ttu-id="5c408-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c408-129">RELATED LINKS</span></span>

[<span data-ttu-id="5c408-130">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="5c408-130">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="5c408-131">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="5c408-131">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="5c408-132">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="5c408-132">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="5c408-133">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="5c408-133">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


