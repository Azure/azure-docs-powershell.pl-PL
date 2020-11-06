---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 1dfd9c4d55c9898ce9f4b656f53d7606ced11359
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527633"
---
# <span data-ttu-id="0f776-101">New-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="0f776-101">New-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="0f776-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0f776-102">SYNOPSIS</span></span>
<span data-ttu-id="0f776-103">Umożliwia utworzenie reguły zasad obliczania danych usługi Lake Analytics dla określonej jednostki usługi AAD.</span><span class="sxs-lookup"><span data-stu-id="0f776-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f776-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0f776-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxDegreeOfParallelismPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f776-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0f776-105">DESCRIPTION</span></span>
<span data-ttu-id="0f776-106">**Nowe-AzureRmDataLakeAnalyticsComputePolicy** tworzy określoną regułę obliczeniową dla konkretnej jednostki w usłudze AAD na koncie usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0f776-106">The **New-AzureRmDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="0f776-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0f776-107">EXAMPLES</span></span>

### <span data-ttu-id="0f776-108">Przykład 1. Tworzenie zasad obliczeniowych z tylko jedną regułą</span><span class="sxs-lookup"><span data-stu-id="0f776-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxDegreeOfParallelismPerJob 5
```

<span data-ttu-id="0f776-109">To polecenie tworzy zasady o nazwie "moje zasady" na koncie "contosoadla" dla użytkownika o identyfikatorze "83cb7ad2-3523-4b82-b909-d478b0d8aea3", który gwarantuje, że nie mogą przesłać żadnych zadań z większą niż 5 równoległością.</span><span class="sxs-lookup"><span data-stu-id="0f776-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 parallelism.</span></span>

### <span data-ttu-id="0f776-110">Przykład 2: Tworzenie zasad obliczeniowych przy użyciu obu zestawów reguł</span><span class="sxs-lookup"><span data-stu-id="0f776-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxDegreeOfParallelismPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="0f776-111">To polecenie tworzy zasady o nazwie "Moja zasada" na koncie "contosoadla" dla użytkownika o identyfikatorze "83cb7ad2-3523-4b82-b909-d478b0d8aea3", który gwarantuje, że nie mogą przesłać żadnych zadań z większą niż 5 równoległością lub priorytetem niższym niż 100</span><span class="sxs-lookup"><span data-stu-id="0f776-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 parallelism or with a priority lower than 100</span></span>

## <span data-ttu-id="0f776-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0f776-112">PARAMETERS</span></span>

### <span data-ttu-id="0f776-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="0f776-113">-Account</span></span>
<span data-ttu-id="0f776-114">Nazwa konta, do którego mają zostać dodane zasady obliczania.</span><span class="sxs-lookup"><span data-stu-id="0f776-114">Name of the account to add the compute policy to.</span></span>

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

### <span data-ttu-id="0f776-115">-MaxDegreeOfParallelismPerJob</span><span class="sxs-lookup"><span data-stu-id="0f776-115">-MaxDegreeOfParallelismPerJob</span></span>
<span data-ttu-id="0f776-116">Maksymalny obsługiwany stopień równoległości przypadający na zadanie dla tych zasad.</span><span class="sxs-lookup"><span data-stu-id="0f776-116">The maximum supported degree of parallelism per job for this policy.</span></span>
<span data-ttu-id="0f776-117">Należy określić albo ten, MinPriorityPerJob, albo oba parametry.</span><span class="sxs-lookup"><span data-stu-id="0f776-117">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="0f776-118">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="0f776-118">-MinPriorityPerJob</span></span>
<span data-ttu-id="0f776-119">Minimalny obsługiwany priorytet dla każdego zadania dla tych zasad.</span><span class="sxs-lookup"><span data-stu-id="0f776-119">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="0f776-120">Należy określić albo ten, MaxDegreeOfParallelismPerJob, albo oba parametry.</span><span class="sxs-lookup"><span data-stu-id="0f776-120">Either this, MaxDegreeOfParallelismPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="0f776-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0f776-121">-Name</span></span>
<span data-ttu-id="0f776-122">Nazwa zasad obliczania, które mają zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="0f776-122">Name of the compute policy to create.</span></span>

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

### <span data-ttu-id="0f776-123">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0f776-123">-ObjectId</span></span>
<span data-ttu-id="0f776-124">Identyfikator obiektu usługi Azure Active Directory dla użytkownika lub grupy, do którego ma zostać zastosowana zasada.</span><span class="sxs-lookup"><span data-stu-id="0f776-124">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f776-125">-ObjectType</span><span class="sxs-lookup"><span data-stu-id="0f776-125">-ObjectType</span></span>
<span data-ttu-id="0f776-126">Typ obiektu usługi Azure Active Directory dla przekazanego identyfikatora obiektu.</span><span class="sxs-lookup"><span data-stu-id="0f776-126">The Azure Active Directory object type for the object ID passed in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: User, Group, ServicePrincipal

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f776-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f776-127">-ResourceGroupName</span></span>
<span data-ttu-id="0f776-128">Nazwa grupy zasobów, pod którą konto istnieje.</span><span class="sxs-lookup"><span data-stu-id="0f776-128">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="0f776-129">Opcjonalny i będzie próbować wykryć, czy nie podano.</span><span class="sxs-lookup"><span data-stu-id="0f776-129">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="0f776-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0f776-130">-Confirm</span></span>
<span data-ttu-id="0f776-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f776-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f776-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f776-132">-WhatIf</span></span>
<span data-ttu-id="0f776-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f776-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f776-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0f776-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f776-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f776-135">-DefaultProfile</span></span>
<span data-ttu-id="0f776-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0f776-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f776-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f776-137">CommonParameters</span></span>
<span data-ttu-id="0f776-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f776-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f776-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f776-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f776-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f776-140">INPUTS</span></span>

### <span data-ttu-id="0f776-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0f776-141">System.String</span></span>
<span data-ttu-id="0f776-142">System. GUID system. Int32</span><span class="sxs-lookup"><span data-stu-id="0f776-142">System.Guid System.Int32</span></span>

## <span data-ttu-id="0f776-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0f776-143">OUTPUTS</span></span>

### <span data-ttu-id="0f776-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="0f776-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="0f776-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0f776-145">NOTES</span></span>

## <span data-ttu-id="0f776-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f776-146">RELATED LINKS</span></span>

