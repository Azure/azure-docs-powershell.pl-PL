---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 1894e5a79660558163d9b95ce49f1736ea002bf9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186195"
---
# <span data-ttu-id="f5727-101">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f5727-101">Get-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="f5727-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5727-102">SYNOPSIS</span></span>
<span data-ttu-id="f5727-103">Pobiera informacje o koncie usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="f5727-103">Gets information about a Data Lake Analytics account.</span></span>

## <span data-ttu-id="f5727-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f5727-104">SYNTAX</span></span>

### <span data-ttu-id="f5727-105">GetAllInSubscription (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f5727-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5727-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f5727-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f5727-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="f5727-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5727-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f5727-108">DESCRIPTION</span></span>
<span data-ttu-id="f5727-109">Polecenie **cmdlet Get-AzDataLakeAnalyticsAccount** pobiera informacje o koncie usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="f5727-109">The **Get-AzDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="f5727-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f5727-110">EXAMPLES</span></span>

### <span data-ttu-id="f5727-111">Przykład 1. Uzyskiwanie informacji o koncie usługi Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="f5727-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="f5727-112">To polecenie pobiera informacje o koncie o nazwie ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="f5727-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="f5727-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5727-113">PARAMETERS</span></span>

### <span data-ttu-id="f5727-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5727-114">-DefaultProfile</span></span>
<span data-ttu-id="f5727-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="f5727-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5727-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f5727-116">-Name</span></span>
<span data-ttu-id="f5727-117">Określa nazwę konta data lake analytics.</span><span class="sxs-lookup"><span data-stu-id="f5727-117">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="f5727-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5727-118">-ResourceGroupName</span></span>
<span data-ttu-id="f5727-119">Określa nazwę grupy zasobów dla konta Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="f5727-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="f5727-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5727-120">CommonParameters</span></span>
<span data-ttu-id="f5727-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5727-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5727-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5727-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5727-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5727-123">INPUTS</span></span>

### <span data-ttu-id="f5727-124">System.String</span><span class="sxs-lookup"><span data-stu-id="f5727-124">System.String</span></span>

## <span data-ttu-id="f5727-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5727-125">OUTPUTS</span></span>

### <span data-ttu-id="f5727-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f5727-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

### <span data-ttu-id="f5727-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span><span class="sxs-lookup"><span data-stu-id="f5727-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span></span>

## <span data-ttu-id="f5727-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f5727-128">NOTES</span></span>

## <span data-ttu-id="f5727-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5727-129">RELATED LINKS</span></span>

[<span data-ttu-id="f5727-130">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f5727-130">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f5727-131">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f5727-131">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f5727-132">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f5727-132">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f5727-133">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f5727-133">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


