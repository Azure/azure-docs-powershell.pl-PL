---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 59bc611d63d062d06b3b3bdebe9ac8b0f1349179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719337"
---
# <span data-ttu-id="db594-101">Get-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="db594-101">Get-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="db594-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="db594-102">SYNOPSIS</span></span>
<span data-ttu-id="db594-103">Pobiera zasadę obliczeniową lub listę zasad obliczeniowych usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="db594-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db594-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="db594-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db594-105">Opis</span><span class="sxs-lookup"><span data-stu-id="db594-105">DESCRIPTION</span></span>
<span data-ttu-id="db594-106">**Element get-AzureRmDataLakeAnalyticsComputePolicy** pobiera określoną zasadę obliczeniową usługi Azure Data Lake Analytics lub listę zasad.</span><span class="sxs-lookup"><span data-stu-id="db594-106">The **Get-AzureRmDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="db594-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="db594-107">EXAMPLES</span></span>

### <span data-ttu-id="db594-108">Przykład 1: uzyskiwanie określonych zasad obliczania</span><span class="sxs-lookup"><span data-stu-id="db594-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="db594-109">To polecenie pobiera określoną zasadę obliczeniową z nazwą "Moja zasada" na koncie "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="db594-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="db594-110">Przykład 2: uzyskiwanie listy wszystkich zasad obliczania na koncie</span><span class="sxs-lookup"><span data-stu-id="db594-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="db594-111">To polecenie pobiera listę wszystkich zasad obliczeniowych na koncie "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="db594-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="db594-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="db594-112">PARAMETERS</span></span>

### <span data-ttu-id="db594-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="db594-113">-Account</span></span>
<span data-ttu-id="db594-114">Nazwa konta, z którego mają zostać nadana zasada lub zasady obliczeniowe.</span><span class="sxs-lookup"><span data-stu-id="db594-114">Name of the account to get the compute policy or policies from.</span></span>

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

### <span data-ttu-id="db594-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="db594-115">-Name</span></span>
<span data-ttu-id="db594-116">Nazwa zasad obliczania do pobrania.</span><span class="sxs-lookup"><span data-stu-id="db594-116">Name of the compute policy to get.</span></span>

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

### <span data-ttu-id="db594-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db594-117">-ResourceGroupName</span></span>
<span data-ttu-id="db594-118">Nazwa grupy zasobów, pod którą konto istnieje.</span><span class="sxs-lookup"><span data-stu-id="db594-118">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="db594-119">Opcjonalny i będzie próbować wykryć, czy nie podano.</span><span class="sxs-lookup"><span data-stu-id="db594-119">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="db594-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db594-120">-DefaultProfile</span></span>
<span data-ttu-id="db594-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="db594-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db594-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db594-122">CommonParameters</span></span>
<span data-ttu-id="db594-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db594-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db594-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db594-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db594-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db594-125">INPUTS</span></span>

### <span data-ttu-id="db594-126">System. String</span><span class="sxs-lookup"><span data-stu-id="db594-126">System.String</span></span>

## <span data-ttu-id="db594-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="db594-127">OUTPUTS</span></span>

### <span data-ttu-id="db594-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="db594-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>
<span data-ttu-id="db594-129">System. Collections. Generic. IEnumerable ' 1 [[Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy, Microsoft. Azure. Commands. DataLakeAnalytics, Version = 3.0.0.0, Culture = neutral; PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="db594-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy, Microsoft.Azure.Commands.DataLakeAnalytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="db594-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="db594-130">NOTES</span></span>

## <span data-ttu-id="db594-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db594-131">RELATED LINKS</span></span>

