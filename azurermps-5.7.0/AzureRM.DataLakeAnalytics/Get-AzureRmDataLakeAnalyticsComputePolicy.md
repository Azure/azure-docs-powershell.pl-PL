---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: f19c4f9d39837534ea5ddd5b16daa055ee54aef6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544412"
---
# <span data-ttu-id="ae1bf-101">Get-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="ae1bf-101">Get-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="ae1bf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae1bf-102">SYNOPSIS</span></span>
<span data-ttu-id="ae1bf-103">Pobiera zasadę obliczeniową lub listę zasad obliczeniowych usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ae1bf-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae1bf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae1bf-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae1bf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ae1bf-105">DESCRIPTION</span></span>
<span data-ttu-id="ae1bf-106">**Element get-AzureRmDataLakeAnalyticsComputePolicy** pobiera określoną zasadę obliczeniową usługi Azure Data Lake Analytics lub listę zasad.</span><span class="sxs-lookup"><span data-stu-id="ae1bf-106">The **Get-AzureRmDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="ae1bf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae1bf-107">EXAMPLES</span></span>

### <span data-ttu-id="ae1bf-108">Przykład 1: uzyskiwanie określonych zasad obliczania</span><span class="sxs-lookup"><span data-stu-id="ae1bf-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="ae1bf-109">To polecenie pobiera określoną zasadę obliczeniową z nazwą "Moja zasada" na koncie "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="ae1bf-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="ae1bf-110">Przykład 2: uzyskiwanie listy wszystkich zasad obliczania na koncie</span><span class="sxs-lookup"><span data-stu-id="ae1bf-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="ae1bf-111">To polecenie pobiera listę wszystkich zasad obliczeniowych na koncie "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="ae1bf-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="ae1bf-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae1bf-112">PARAMETERS</span></span>

### <span data-ttu-id="ae1bf-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="ae1bf-113">-Account</span></span>
<span data-ttu-id="ae1bf-114">Nazwa konta, z którego mają zostać nadana zasada lub zasady obliczeniowe.</span><span class="sxs-lookup"><span data-stu-id="ae1bf-114">Name of the account to get the compute policy or policies from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae1bf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae1bf-115">-DefaultProfile</span></span>
<span data-ttu-id="ae1bf-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ae1bf-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae1bf-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ae1bf-117">-Name</span></span>
<span data-ttu-id="ae1bf-118">Nazwa zasad obliczania do pobrania.</span><span class="sxs-lookup"><span data-stu-id="ae1bf-118">Name of the compute policy to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae1bf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae1bf-119">-ResourceGroupName</span></span>
<span data-ttu-id="ae1bf-120">Nazwa grupy zasobów, pod którą konto istnieje.</span><span class="sxs-lookup"><span data-stu-id="ae1bf-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="ae1bf-121">Opcjonalny i będzie próbować wykryć, czy nie podano.</span><span class="sxs-lookup"><span data-stu-id="ae1bf-121">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae1bf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae1bf-122">CommonParameters</span></span>
<span data-ttu-id="ae1bf-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae1bf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae1bf-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae1bf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae1bf-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae1bf-125">INPUTS</span></span>

### <span data-ttu-id="ae1bf-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ae1bf-126">System.String</span></span>

## <span data-ttu-id="ae1bf-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae1bf-127">OUTPUTS</span></span>

### <span data-ttu-id="ae1bf-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="ae1bf-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>
<span data-ttu-id="ae1bf-129">System. Collections. Generic. IEnumerable ' 1 [[Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy, Microsoft. Azure. Commands. DataLakeAnalytics, Version = 3.0.0.0, Culture = neutral; PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ae1bf-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy, Microsoft.Azure.Commands.DataLakeAnalytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ae1bf-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae1bf-130">NOTES</span></span>

## <span data-ttu-id="ae1bf-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae1bf-131">RELATED LINKS</span></span>

