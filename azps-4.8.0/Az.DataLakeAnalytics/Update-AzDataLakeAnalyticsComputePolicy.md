---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/update-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 5dd36c9dbd263dc2e5c72cc6d57f95e29c456c41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062329"
---
# <span data-ttu-id="2b304-101">Update-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="2b304-101">Update-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="2b304-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b304-102">SYNOPSIS</span></span>
<span data-ttu-id="2b304-103">Umożliwia zaktualizowanie reguły zasad obliczania usługi Data Lake Analytics dla określonej jednostki usługi AAD.</span><span class="sxs-lookup"><span data-stu-id="2b304-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="2b304-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b304-104">SYNTAX</span></span>

```
Update-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b304-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2b304-105">DESCRIPTION</span></span>
<span data-ttu-id="2b304-106">**Aktualizacja — AzDataLakeAnalyticsComputePolicy** aktualizuje określoną regułę obliczeniową dla konkretnej jednostki w usłudze AAD na koncie usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="2b304-106">The **Update-AzDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="2b304-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b304-107">EXAMPLES</span></span>

### <span data-ttu-id="2b304-108">Przykład 1: aktualizowanie jednej reguły w zasadach obliczania</span><span class="sxs-lookup"><span data-stu-id="2b304-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="2b304-109">To polecenie aktualizuje zasady o nazwie "moje zasady" na koncie "contosoadla", aby upewnić się, że użytkownik nie może przesłać żadnych zadań z więcej niż 5 jednostkami analitycznymi.</span><span class="sxs-lookup"><span data-stu-id="2b304-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="2b304-110">Przykład 2: Tworzenie zasad obliczeniowych z aktualizacją obu reguł</span><span class="sxs-lookup"><span data-stu-id="2b304-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="2b304-111">To polecenie tworzy zasady o nazwie "Moja zasada" na koncie "contosoadla", aby upewnić się, że użytkownik nie może przesłać żadnych zadań z więcej niż 5 jednostkami analitycznymi lub o priorytecie niższej niż 100</span><span class="sxs-lookup"><span data-stu-id="2b304-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="2b304-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b304-112">PARAMETERS</span></span>

### <span data-ttu-id="2b304-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="2b304-113">-Account</span></span>
<span data-ttu-id="2b304-114">Nazwa konta, w którym mają zostać zaktualizowane zasady obliczania.</span><span class="sxs-lookup"><span data-stu-id="2b304-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="2b304-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b304-115">-DefaultProfile</span></span>
<span data-ttu-id="2b304-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2b304-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b304-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="2b304-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="2b304-118">Maksymalna obsługiwana liczba jednostek analitycznych na zadanie dla tych zasad.</span><span class="sxs-lookup"><span data-stu-id="2b304-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="2b304-119">Należy określić albo ten, MinPriorityPerJob, albo oba parametry.</span><span class="sxs-lookup"><span data-stu-id="2b304-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelismPerJob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b304-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="2b304-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="2b304-121">Minimalny obsługiwany priorytet dla każdego zadania dla tych zasad.</span><span class="sxs-lookup"><span data-stu-id="2b304-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="2b304-122">Należy określić albo ten, MaxAnalyticsUnitsPerJob, albo oba parametry.</span><span class="sxs-lookup"><span data-stu-id="2b304-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b304-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2b304-123">-Name</span></span>
<span data-ttu-id="2b304-124">Nazwa zasad obliczania do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="2b304-124">Name of the compute policy to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b304-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b304-125">-ResourceGroupName</span></span>
<span data-ttu-id="2b304-126">Nazwa grupy zasobów, pod którą konto istnieje.</span><span class="sxs-lookup"><span data-stu-id="2b304-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="2b304-127">Opcjonalny i będzie próbować wykryć, czy nie podano.</span><span class="sxs-lookup"><span data-stu-id="2b304-127">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="2b304-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2b304-128">-Confirm</span></span>
<span data-ttu-id="2b304-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b304-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b304-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b304-130">-WhatIf</span></span>
<span data-ttu-id="2b304-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b304-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b304-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2b304-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b304-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b304-133">CommonParameters</span></span>
<span data-ttu-id="2b304-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b304-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b304-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b304-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b304-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b304-136">INPUTS</span></span>

### <span data-ttu-id="2b304-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2b304-137">System.String</span></span>

### <span data-ttu-id="2b304-138">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2b304-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2b304-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b304-139">OUTPUTS</span></span>

### <span data-ttu-id="2b304-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="2b304-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="2b304-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b304-141">NOTES</span></span>

## <span data-ttu-id="2b304-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b304-142">RELATED LINKS</span></span>
