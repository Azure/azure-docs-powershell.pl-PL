---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 76df1cb780220a09ccc0d571fd88223e746eefe6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238220"
---
# <span data-ttu-id="287b1-101">New-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="287b1-101">New-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="287b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="287b1-102">SYNOPSIS</span></span>
<span data-ttu-id="287b1-103">Tworzy regułę zasad obliczeniowych usługi Data Lake Analytics dla określonej jednostki AAD.</span><span class="sxs-lookup"><span data-stu-id="287b1-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="287b1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="287b1-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="287b1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="287b1-105">DESCRIPTION</span></span>
<span data-ttu-id="287b1-106">**New-AzDataLakeAnalyticsComputePolicy** tworzy określoną regułę zasad obliczania dla określonej jednostki AAD na koncie usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="287b1-106">The **New-AzDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="287b1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="287b1-107">EXAMPLES</span></span>

### <span data-ttu-id="287b1-108">Przykład 1. Tworzenie zasad obliczania przy użyciu tylko jednej reguły</span><span class="sxs-lookup"><span data-stu-id="287b1-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="287b1-109">To polecenie tworzy zasady o nazwie "myPolicy" na koncie "contosoadla" dla użytkownika o identyfikatorze "83cb7ad2-3523-4b82-b909-d478b0d8aea3", dzięki temu nie może przesłać żadnego zadania z więcej niż 5 jednostkami analizy.</span><span class="sxs-lookup"><span data-stu-id="287b1-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="287b1-110">Przykład 2. Tworzenie zasad obliczania z ustawionymi obiema regułami</span><span class="sxs-lookup"><span data-stu-id="287b1-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="287b1-111">To polecenie tworzy zasady o nazwie "myPolicy" na koncie "contosoadla" dla użytkownika o identyfikatorze "83cb7ad2-3523-4b82-b909-d478b0d8aea3", która gwarantuje, że nie będzie mógł przesłać żadnego zadania z więcej niż 5 jednostkami analizy lub o priorytecie niższym niż 100</span><span class="sxs-lookup"><span data-stu-id="287b1-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="287b1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="287b1-112">PARAMETERS</span></span>

### <span data-ttu-id="287b1-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="287b1-113">-Account</span></span>
<span data-ttu-id="287b1-114">Nazwa konta, do których mają być dodawania zasad obliczania.</span><span class="sxs-lookup"><span data-stu-id="287b1-114">Name of the account to add the compute policy to.</span></span>

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

### <span data-ttu-id="287b1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="287b1-115">-DefaultProfile</span></span>
<span data-ttu-id="287b1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="287b1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="287b1-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="287b1-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="287b1-118">Maksymalna liczba jednostek analizy na zadanie w ramach tych zasad.</span><span class="sxs-lookup"><span data-stu-id="287b1-118">The maximum supported analytics units per job for this policy.</span></span>
<span data-ttu-id="287b1-119">Musi zostać określony parametr MinPriorityPerJob lub oba parametry.</span><span class="sxs-lookup"><span data-stu-id="287b1-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="287b1-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="287b1-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="287b1-121">Minimalny obsługiwany priorytet dla każdego zadania w tych zasadach.</span><span class="sxs-lookup"><span data-stu-id="287b1-121">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="287b1-122">Musi zostać określony parametr MaxAnalyticsUnitsPerJob lub oba parametry.</span><span class="sxs-lookup"><span data-stu-id="287b1-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="287b1-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="287b1-123">-Name</span></span>
<span data-ttu-id="287b1-124">Nazwa zasad obliczania, które mają być tworzyć.</span><span class="sxs-lookup"><span data-stu-id="287b1-124">Name of the compute policy to create.</span></span>

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

### <span data-ttu-id="287b1-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="287b1-125">-ObjectId</span></span>
<span data-ttu-id="287b1-126">Identyfikator obiektu usługi Azure Active Directory dla użytkownika lub grupy, do których mają być stosowane zasady.</span><span class="sxs-lookup"><span data-stu-id="287b1-126">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

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

### <span data-ttu-id="287b1-127">-ObjectType</span><span class="sxs-lookup"><span data-stu-id="287b1-127">-ObjectType</span></span>
<span data-ttu-id="287b1-128">Typ obiektu usługi Azure Active Directory dla przekazywanego identyfikatora obiektu.</span><span class="sxs-lookup"><span data-stu-id="287b1-128">The Azure Active Directory object type for the object ID passed in.</span></span>

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

### <span data-ttu-id="287b1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="287b1-129">-ResourceGroupName</span></span>
<span data-ttu-id="287b1-130">Nazwa grupy zasobów, w której istnieje konto.</span><span class="sxs-lookup"><span data-stu-id="287b1-130">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="287b1-131">Opcjonalne i podejmie próbę odnajdowania, jeśli nie zostanie podany.</span><span class="sxs-lookup"><span data-stu-id="287b1-131">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="287b1-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="287b1-132">-Confirm</span></span>
<span data-ttu-id="287b1-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="287b1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="287b1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="287b1-134">-WhatIf</span></span>
<span data-ttu-id="287b1-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="287b1-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="287b1-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="287b1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="287b1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="287b1-137">CommonParameters</span></span>
<span data-ttu-id="287b1-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="287b1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="287b1-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="287b1-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="287b1-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="287b1-140">INPUTS</span></span>

### <span data-ttu-id="287b1-141">System.String</span><span class="sxs-lookup"><span data-stu-id="287b1-141">System.String</span></span>

### <span data-ttu-id="287b1-142">System.Guid</span><span class="sxs-lookup"><span data-stu-id="287b1-142">System.Guid</span></span>

### <span data-ttu-id="287b1-143">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="287b1-143">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="287b1-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="287b1-144">OUTPUTS</span></span>

### <span data-ttu-id="287b1-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="287b1-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="287b1-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="287b1-146">NOTES</span></span>

## <span data-ttu-id="287b1-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="287b1-147">RELATED LINKS</span></span>
