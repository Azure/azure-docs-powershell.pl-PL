---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 67cffe7f0cdaebc655eb98321166bb7805844a5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551903"
---
# <span data-ttu-id="64790-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="64790-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="64790-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="64790-102">SYNOPSIS</span></span>
<span data-ttu-id="64790-103">Umożliwia zaktualizowanie reguły zasad obliczania usługi Data Lake Analytics dla określonej jednostki usługi AAD.</span><span class="sxs-lookup"><span data-stu-id="64790-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64790-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="64790-104">SYNTAX</span></span>

```
Update-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxDegreeOfParallelismPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64790-105">Opis</span><span class="sxs-lookup"><span data-stu-id="64790-105">DESCRIPTION</span></span>
<span data-ttu-id="64790-106">**Aktualizacja — AzureRmDataLakeAnalyticsComputePolicy** aktualizuje określoną regułę obliczeniową dla konkretnej jednostki w usłudze AAD na koncie usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="64790-106">The **Update-AzureRmDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="64790-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="64790-107">EXAMPLES</span></span>

### <span data-ttu-id="64790-108">Przykład 1: aktualizowanie jednej reguły w zasadach obliczania</span><span class="sxs-lookup"><span data-stu-id="64790-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxDegreeOfParallelismPerJob 5
```

<span data-ttu-id="64790-109">To polecenie aktualizuje zasady o nazwie "moje zasady" na koncie "contosoadla", aby upewnić się, że użytkownik nie może przesłać żadnych zadań z większą niż 5 równoległością.</span><span class="sxs-lookup"><span data-stu-id="64790-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 parallelism.</span></span>

### <span data-ttu-id="64790-110">Przykład 2: Tworzenie zasad obliczeniowych z aktualizacją obu reguł</span><span class="sxs-lookup"><span data-stu-id="64790-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxDegreeOfParallelismPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="64790-111">To polecenie tworzy zasady o nazwie "Moja zasada" na koncie "contosoadla", aby upewnić się, że użytkownik nie może przesłać żadnych zadań z większą niż 5 równoległością lub priorytetem niższym niż 100</span><span class="sxs-lookup"><span data-stu-id="64790-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 parallelism or with a priority lower than 100</span></span>

## <span data-ttu-id="64790-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64790-112">PARAMETERS</span></span>

### <span data-ttu-id="64790-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="64790-113">-Account</span></span>
<span data-ttu-id="64790-114">Nazwa konta, w którym mają zostać zaktualizowane zasady obliczania.</span><span class="sxs-lookup"><span data-stu-id="64790-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="64790-115">-MaxDegreeOfParallelismPerJob</span><span class="sxs-lookup"><span data-stu-id="64790-115">-MaxDegreeOfParallelismPerJob</span></span>
<span data-ttu-id="64790-116">Maksymalny obsługiwany stopień równoległości przypadający na zadanie dla tych zasad.</span><span class="sxs-lookup"><span data-stu-id="64790-116">The maximum supported degree of parallelism per job for this policy.</span></span> <span data-ttu-id="64790-117">Należy określić albo ten, MinPriorityPerJob, albo oba parametry.</span><span class="sxs-lookup"><span data-stu-id="64790-117">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="64790-118">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="64790-118">-MinPriorityPerJob</span></span>
<span data-ttu-id="64790-119">Minimalny obsługiwany priorytet dla każdego zadania dla tych zasad.</span><span class="sxs-lookup"><span data-stu-id="64790-119">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="64790-120">Należy określić albo ten, MaxDegreeOfParallelismPerJob, albo oba parametry.</span><span class="sxs-lookup"><span data-stu-id="64790-120">Either this, MaxDegreeOfParallelismPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="64790-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="64790-121">-Name</span></span>
<span data-ttu-id="64790-122">Nazwa zasad obliczania do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="64790-122">Name of the compute policy to update.</span></span>

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

### <span data-ttu-id="64790-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64790-123">-ResourceGroupName</span></span>
<span data-ttu-id="64790-124">Nazwa grupy zasobów, pod którą konto istnieje.</span><span class="sxs-lookup"><span data-stu-id="64790-124">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="64790-125">Opcjonalny i będzie próbować wykryć, czy nie podano.</span><span class="sxs-lookup"><span data-stu-id="64790-125">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="64790-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="64790-126">-Confirm</span></span>
<span data-ttu-id="64790-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64790-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64790-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64790-128">-WhatIf</span></span>
<span data-ttu-id="64790-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64790-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64790-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="64790-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64790-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64790-131">-DefaultProfile</span></span>
<span data-ttu-id="64790-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="64790-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64790-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64790-133">CommonParameters</span></span>
<span data-ttu-id="64790-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64790-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64790-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64790-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64790-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64790-136">INPUTS</span></span>

### <span data-ttu-id="64790-137">System. String</span><span class="sxs-lookup"><span data-stu-id="64790-137">System.String</span></span>
<span data-ttu-id="64790-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="64790-138">System.Int32</span></span>

## <span data-ttu-id="64790-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="64790-139">OUTPUTS</span></span>

### <span data-ttu-id="64790-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="64790-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="64790-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="64790-141">NOTES</span></span>

## <span data-ttu-id="64790-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64790-142">RELATED LINKS</span></span>

