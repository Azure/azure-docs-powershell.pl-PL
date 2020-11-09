---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 56b1a9378914a7fa2220e948b64c357b06f6f4dc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305868"
---
# <span data-ttu-id="dd979-101">Get-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="dd979-101">Get-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="dd979-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd979-102">SYNOPSIS</span></span>
<span data-ttu-id="dd979-103">Pobiera zasadę obliczeniową lub listę zasad obliczeniowych usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="dd979-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

## <span data-ttu-id="dd979-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd979-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd979-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dd979-105">DESCRIPTION</span></span>
<span data-ttu-id="dd979-106">**Element get-AzDataLakeAnalyticsComputePolicy** pobiera określoną zasadę obliczeniową usługi Azure Data Lake Analytics lub listę zasad.</span><span class="sxs-lookup"><span data-stu-id="dd979-106">The **Get-AzDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="dd979-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd979-107">EXAMPLES</span></span>

### <span data-ttu-id="dd979-108">Przykład 1: uzyskiwanie określonych zasad obliczania</span><span class="sxs-lookup"><span data-stu-id="dd979-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="dd979-109">To polecenie pobiera określoną zasadę obliczeniową z nazwą "Moja zasada" na koncie "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="dd979-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="dd979-110">Przykład 2: uzyskiwanie listy wszystkich zasad obliczania na koncie</span><span class="sxs-lookup"><span data-stu-id="dd979-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="dd979-111">To polecenie pobiera listę wszystkich zasad obliczeniowych na koncie "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="dd979-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="dd979-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd979-112">PARAMETERS</span></span>

### <span data-ttu-id="dd979-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="dd979-113">-Account</span></span>
<span data-ttu-id="dd979-114">Nazwa konta, z którego mają zostać nadana zasada lub zasady obliczeniowe.</span><span class="sxs-lookup"><span data-stu-id="dd979-114">Name of the account to get the compute policy or policies from.</span></span>

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

### <span data-ttu-id="dd979-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd979-115">-DefaultProfile</span></span>
<span data-ttu-id="dd979-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="dd979-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd979-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dd979-117">-Name</span></span>
<span data-ttu-id="dd979-118">Nazwa zasad obliczania do pobrania.</span><span class="sxs-lookup"><span data-stu-id="dd979-118">Name of the compute policy to get.</span></span>

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

### <span data-ttu-id="dd979-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd979-119">-ResourceGroupName</span></span>
<span data-ttu-id="dd979-120">Nazwa grupy zasobów, pod którą konto istnieje.</span><span class="sxs-lookup"><span data-stu-id="dd979-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="dd979-121">Opcjonalny i będzie próbować wykryć, czy nie podano.</span><span class="sxs-lookup"><span data-stu-id="dd979-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="dd979-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd979-122">CommonParameters</span></span>
<span data-ttu-id="dd979-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd979-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd979-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd979-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd979-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd979-125">INPUTS</span></span>

### <span data-ttu-id="dd979-126">System. String</span><span class="sxs-lookup"><span data-stu-id="dd979-126">System.String</span></span>

## <span data-ttu-id="dd979-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd979-127">OUTPUTS</span></span>

### <span data-ttu-id="dd979-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="dd979-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="dd979-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd979-129">NOTES</span></span>

## <span data-ttu-id="dd979-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd979-130">RELATED LINKS</span></span>
