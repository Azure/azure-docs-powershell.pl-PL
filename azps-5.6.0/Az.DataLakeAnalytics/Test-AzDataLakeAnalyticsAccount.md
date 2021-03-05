---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: b5c1303625676006929a3c2eee80f5d5961bc438
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009162"
---
# <span data-ttu-id="d819f-101">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d819f-101">Test-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="d819f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d819f-102">SYNOPSIS</span></span>
<span data-ttu-id="d819f-103">Sprawdza, czy istnieje konto usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d819f-103">Checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="d819f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d819f-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d819f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d819f-105">DESCRIPTION</span></span>
<span data-ttu-id="d819f-106">Polecenie **cmdlet Test-AzDataLakeAnalyticsAccount** sprawdza, czy istnieje konto Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d819f-106">The **Test-AzDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="d819f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d819f-107">EXAMPLES</span></span>

### <span data-ttu-id="d819f-108">Przykład 1. Testowanie, czy konto istnieje</span><span class="sxs-lookup"><span data-stu-id="d819f-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="d819f-109">To polecenie sprawdza, czy istnieje konto o nazwie ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="d819f-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="d819f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d819f-110">PARAMETERS</span></span>

### <span data-ttu-id="d819f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d819f-111">-DefaultProfile</span></span>
<span data-ttu-id="d819f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d819f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d819f-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d819f-113">-Name</span></span>
<span data-ttu-id="d819f-114">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d819f-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d819f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d819f-115">-ResourceGroupName</span></span>
<span data-ttu-id="d819f-116">Określa nazwę grupy zasobów dla konta Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d819f-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d819f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d819f-117">CommonParameters</span></span>
<span data-ttu-id="d819f-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d819f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d819f-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d819f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d819f-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d819f-120">INPUTS</span></span>

### <span data-ttu-id="d819f-121">System.String</span><span class="sxs-lookup"><span data-stu-id="d819f-121">System.String</span></span>

## <span data-ttu-id="d819f-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d819f-122">OUTPUTS</span></span>

### <span data-ttu-id="d819f-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d819f-123">System.Boolean</span></span>

## <span data-ttu-id="d819f-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d819f-124">NOTES</span></span>

## <span data-ttu-id="d819f-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d819f-125">RELATED LINKS</span></span>

[<span data-ttu-id="d819f-126">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d819f-126">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d819f-127">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d819f-127">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d819f-128">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d819f-128">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)


