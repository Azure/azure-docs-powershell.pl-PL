---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 679c02edde85b9f64eb037d6d30be1e7c36cdeb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551275"
---
# <span data-ttu-id="72dba-101">New-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="72dba-101">New-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="72dba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72dba-102">SYNOPSIS</span></span>
<span data-ttu-id="72dba-103">Umożliwia utworzenie reguły zasad obliczania danych usługi Lake Analytics dla określonej jednostki usługi AAD.</span><span class="sxs-lookup"><span data-stu-id="72dba-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72dba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72dba-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72dba-105">Opis</span><span class="sxs-lookup"><span data-stu-id="72dba-105">DESCRIPTION</span></span>
<span data-ttu-id="72dba-106">**Nowe-AzureRmDataLakeAnalyticsComputePolicy** tworzy określoną regułę obliczeniową dla konkretnej jednostki w usłudze AAD na koncie usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="72dba-106">The **New-AzureRmDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="72dba-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72dba-107">EXAMPLES</span></span>

### <span data-ttu-id="72dba-108">Przykład 1. Tworzenie zasad obliczeniowych z tylko jedną regułą</span><span class="sxs-lookup"><span data-stu-id="72dba-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="72dba-109">To polecenie tworzy zasady o nazwie "Moja zasada" na koncie "contosoadla" dla użytkownika o identyfikatorze "83cb7ad2-3523-4b82-b909-d478b0d8aea3", który gwarantuje, że nie mogą przesłać żadnych zadań z więcej niż 5 jednostkami analitycznymi.</span><span class="sxs-lookup"><span data-stu-id="72dba-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="72dba-110">Przykład 2: Tworzenie zasad obliczeniowych przy użyciu obu zestawów reguł</span><span class="sxs-lookup"><span data-stu-id="72dba-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="72dba-111">To polecenie tworzy zasady o nazwie "moje zasady" na koncie "contosoadla" dla użytkownika o identyfikatorze "83cb7ad2-3523-4b82-b909-d478b0d8aea3", który gwarantuje, że nie mogą przesłać żadnych zadań z więcej niż 5 jednostkami analitycznymi lub o priorytecie niższej niż 100</span><span class="sxs-lookup"><span data-stu-id="72dba-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="72dba-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72dba-112">PARAMETERS</span></span>

### <span data-ttu-id="72dba-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="72dba-113">-Account</span></span>
<span data-ttu-id="72dba-114">Nazwa konta, do którego mają zostać dodane zasady obliczania.</span><span class="sxs-lookup"><span data-stu-id="72dba-114">Name of the account to add the compute policy to.</span></span>

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

### <span data-ttu-id="72dba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72dba-115">-DefaultProfile</span></span>
<span data-ttu-id="72dba-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="72dba-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72dba-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="72dba-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="72dba-118">Maksymalna obsługiwana liczba jednostek analitycznych na zadanie dla tych zasad.</span><span class="sxs-lookup"><span data-stu-id="72dba-118">The maximum supported analytics units per job for this policy.</span></span>
<span data-ttu-id="72dba-119">Należy określić albo ten, MinPriorityPerJob, albo oba parametry.</span><span class="sxs-lookup"><span data-stu-id="72dba-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="72dba-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="72dba-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="72dba-121">Minimalny obsługiwany priorytet dla każdego zadania dla tych zasad.</span><span class="sxs-lookup"><span data-stu-id="72dba-121">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="72dba-122">Należy określić albo ten, MaxAnalyticsUnitsPerJob, albo oba parametry.</span><span class="sxs-lookup"><span data-stu-id="72dba-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="72dba-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="72dba-123">-Name</span></span>
<span data-ttu-id="72dba-124">Nazwa zasad obliczania, które mają zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="72dba-124">Name of the compute policy to create.</span></span>

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

### <span data-ttu-id="72dba-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="72dba-125">-ObjectId</span></span>
<span data-ttu-id="72dba-126">Identyfikator obiektu usługi Azure Active Directory dla użytkownika lub grupy, do którego ma zostać zastosowana zasada.</span><span class="sxs-lookup"><span data-stu-id="72dba-126">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

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

### <span data-ttu-id="72dba-127">-ObjectType</span><span class="sxs-lookup"><span data-stu-id="72dba-127">-ObjectType</span></span>
<span data-ttu-id="72dba-128">Typ obiektu usługi Azure Active Directory dla przekazanego identyfikatora obiektu.</span><span class="sxs-lookup"><span data-stu-id="72dba-128">The Azure Active Directory object type for the object ID passed in.</span></span>

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

### <span data-ttu-id="72dba-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72dba-129">-ResourceGroupName</span></span>
<span data-ttu-id="72dba-130">Nazwa grupy zasobów, pod którą konto istnieje.</span><span class="sxs-lookup"><span data-stu-id="72dba-130">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="72dba-131">Opcjonalny i będzie próbować wykryć, czy nie podano.</span><span class="sxs-lookup"><span data-stu-id="72dba-131">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="72dba-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="72dba-132">-Confirm</span></span>
<span data-ttu-id="72dba-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72dba-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72dba-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72dba-134">-WhatIf</span></span>
<span data-ttu-id="72dba-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72dba-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72dba-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="72dba-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72dba-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72dba-137">CommonParameters</span></span>
<span data-ttu-id="72dba-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72dba-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72dba-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72dba-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72dba-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72dba-140">INPUTS</span></span>

### <span data-ttu-id="72dba-141">System. String</span><span class="sxs-lookup"><span data-stu-id="72dba-141">System.String</span></span>

### <span data-ttu-id="72dba-142">System. GUID</span><span class="sxs-lookup"><span data-stu-id="72dba-142">System.Guid</span></span>

### <span data-ttu-id="72dba-143">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="72dba-143">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="72dba-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72dba-144">OUTPUTS</span></span>

### <span data-ttu-id="72dba-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="72dba-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="72dba-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72dba-146">NOTES</span></span>

## <span data-ttu-id="72dba-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72dba-147">RELATED LINKS</span></span>
