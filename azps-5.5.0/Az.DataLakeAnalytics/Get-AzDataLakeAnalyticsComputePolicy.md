---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 56b1a9378914a7fa2220e948b64c357b06f6f4dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242731"
---
# <span data-ttu-id="50303-101">Get-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="50303-101">Get-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="50303-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50303-102">SYNOPSIS</span></span>
<span data-ttu-id="50303-103">Pobiera zasady obliczeniowe Data Lake Analytics lub listę zasad obliczania.</span><span class="sxs-lookup"><span data-stu-id="50303-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

## <span data-ttu-id="50303-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="50303-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50303-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="50303-105">DESCRIPTION</span></span>
<span data-ttu-id="50303-106">Usługa **Get-AzDataLakeAnalyticsComputePolicy** otrzymuje określone zasady obliczeniowe usługi Azure Data Lake Analytics lub listę zasad.</span><span class="sxs-lookup"><span data-stu-id="50303-106">The **Get-AzDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="50303-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="50303-107">EXAMPLES</span></span>

### <span data-ttu-id="50303-108">Przykład 1. Uzyskiwanie określonych zasad obliczania</span><span class="sxs-lookup"><span data-stu-id="50303-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="50303-109">To polecenie pobiera określone zasady obliczania o nazwie "myPolicy" na koncie "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="50303-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="50303-110">Przykład 2. Uzyskiwanie listy wszystkich zasad obliczania na koncie</span><span class="sxs-lookup"><span data-stu-id="50303-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="50303-111">To polecenie pobiera listę wszystkich zasad obliczania na koncie "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="50303-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="50303-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50303-112">PARAMETERS</span></span>

### <span data-ttu-id="50303-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="50303-113">-Account</span></span>
<span data-ttu-id="50303-114">Nazwa konta, z których mają być obliczane zasady lub zasady obliczania.</span><span class="sxs-lookup"><span data-stu-id="50303-114">Name of the account to get the compute policy or policies from.</span></span>

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

### <span data-ttu-id="50303-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50303-115">-DefaultProfile</span></span>
<span data-ttu-id="50303-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="50303-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50303-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="50303-117">-Name</span></span>
<span data-ttu-id="50303-118">Nazwa zasad obliczania, które mają być obliczane.</span><span class="sxs-lookup"><span data-stu-id="50303-118">Name of the compute policy to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50303-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50303-119">-ResourceGroupName</span></span>
<span data-ttu-id="50303-120">Nazwa grupy zasobów, w której istnieje konto.</span><span class="sxs-lookup"><span data-stu-id="50303-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="50303-121">Opcjonalne i podejmie próbę odnajdowania, jeśli nie zostanie podany.</span><span class="sxs-lookup"><span data-stu-id="50303-121">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50303-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50303-122">CommonParameters</span></span>
<span data-ttu-id="50303-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50303-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50303-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50303-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50303-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50303-125">INPUTS</span></span>

### <span data-ttu-id="50303-126">System.String</span><span class="sxs-lookup"><span data-stu-id="50303-126">System.String</span></span>

## <span data-ttu-id="50303-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50303-127">OUTPUTS</span></span>

### <span data-ttu-id="50303-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="50303-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="50303-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="50303-129">NOTES</span></span>

## <span data-ttu-id="50303-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50303-130">RELATED LINKS</span></span>
