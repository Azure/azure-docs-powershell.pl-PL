---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightscomputergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
ms.openlocfilehash: 60c1db3595c3ca33676fbd874356376981a72407
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541615"
---
# <span data-ttu-id="c5852-101">New-AzureRmOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="c5852-101">New-AzureRmOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="c5852-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c5852-102">SYNOPSIS</span></span>
<span data-ttu-id="c5852-103">Tworzy grupę komputerów.</span><span class="sxs-lookup"><span data-stu-id="c5852-103">Creates a computer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5852-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c5852-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5852-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c5852-105">DESCRIPTION</span></span>
<span data-ttu-id="c5852-106">Polecenie cmdlet **New-AzureRmOperationalInsightsComputerGroup** tworzy grupę komputerów w grupie zasobów i lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c5852-106">The **New-AzureRmOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="c5852-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c5852-107">EXAMPLES</span></span>

## <span data-ttu-id="c5852-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c5852-108">PARAMETERS</span></span>

### <span data-ttu-id="c5852-109">-Category</span><span class="sxs-lookup"><span data-stu-id="c5852-109">-Category</span></span>
<span data-ttu-id="c5852-110">Określa kategorię grupy komputerów.</span><span class="sxs-lookup"><span data-stu-id="c5852-110">Specifies the category of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5852-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5852-111">-DefaultProfile</span></span>
<span data-ttu-id="c5852-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c5852-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5852-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c5852-113">-DisplayName</span></span>
<span data-ttu-id="c5852-114">Określa nazwę wyświetlaną grupy komputerów.</span><span class="sxs-lookup"><span data-stu-id="c5852-114">Specifies the display name of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5852-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c5852-115">-Force</span></span>
<span data-ttu-id="c5852-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c5852-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5852-117">-Query</span><span class="sxs-lookup"><span data-stu-id="c5852-117">-Query</span></span>
<span data-ttu-id="c5852-118">Określa zapytanie grupy komputerów.</span><span class="sxs-lookup"><span data-stu-id="c5852-118">Specifies the query of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5852-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5852-119">-ResourceGroupName</span></span>
<span data-ttu-id="c5852-120">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c5852-120">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c5852-121">Polecenie cmdlet tworzy grupę komputer w tej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="c5852-121">The cmdlet creates computer group in this resource group.</span></span>

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

### <span data-ttu-id="c5852-122">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="c5852-122">-SavedSearchId</span></span>
<span data-ttu-id="c5852-123">Określa identyfikator grupy komputerów.</span><span class="sxs-lookup"><span data-stu-id="c5852-123">Specifies the ID of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5852-124">-Version</span><span class="sxs-lookup"><span data-stu-id="c5852-124">-Version</span></span>
<span data-ttu-id="c5852-125">Określa wersję.</span><span class="sxs-lookup"><span data-stu-id="c5852-125">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5852-126">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="c5852-126">-WorkspaceName</span></span>
<span data-ttu-id="c5852-127">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="c5852-127">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5852-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c5852-128">-Confirm</span></span>
<span data-ttu-id="c5852-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5852-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5852-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5852-130">-WhatIf</span></span>
<span data-ttu-id="c5852-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5852-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5852-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c5852-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5852-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5852-133">CommonParameters</span></span>
<span data-ttu-id="c5852-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5852-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5852-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5852-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5852-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5852-136">INPUTS</span></span>

### <span data-ttu-id="c5852-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c5852-137">System.String</span></span>

### <span data-ttu-id="c5852-138">System. Int64</span><span class="sxs-lookup"><span data-stu-id="c5852-138">System.Int64</span></span>

## <span data-ttu-id="c5852-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c5852-139">OUTPUTS</span></span>

### <span data-ttu-id="c5852-140">System .NET. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="c5852-140">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="c5852-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c5852-141">NOTES</span></span>

## <span data-ttu-id="c5852-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5852-142">RELATED LINKS</span></span>
