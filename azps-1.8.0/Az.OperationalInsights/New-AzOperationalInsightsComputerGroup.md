---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscomputergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
ms.openlocfilehash: ce3a935dc97e63615e3bb1253fd5eedcb5c702da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708814"
---
# <span data-ttu-id="f3456-101">New-AzOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="f3456-101">New-AzOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="f3456-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3456-102">SYNOPSIS</span></span>
<span data-ttu-id="f3456-103">Tworzy grupę komputerów.</span><span class="sxs-lookup"><span data-stu-id="f3456-103">Creates a computer group.</span></span>

## <span data-ttu-id="f3456-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3456-104">SYNTAX</span></span>

```
New-AzOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3456-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f3456-105">DESCRIPTION</span></span>
<span data-ttu-id="f3456-106">Polecenie cmdlet **New-AzOperationalInsightsComputerGroup** tworzy grupę komputerów w grupie zasobów i lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="f3456-106">The **New-AzOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="f3456-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3456-107">EXAMPLES</span></span>

## <span data-ttu-id="f3456-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3456-108">PARAMETERS</span></span>

### <span data-ttu-id="f3456-109">-Category</span><span class="sxs-lookup"><span data-stu-id="f3456-109">-Category</span></span>
<span data-ttu-id="f3456-110">Określa kategorię grupy komputerów.</span><span class="sxs-lookup"><span data-stu-id="f3456-110">Specifies the category of the computer group.</span></span>

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

### <span data-ttu-id="f3456-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3456-111">-DefaultProfile</span></span>
<span data-ttu-id="f3456-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f3456-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3456-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f3456-113">-DisplayName</span></span>
<span data-ttu-id="f3456-114">Określa nazwę wyświetlaną grupy komputerów.</span><span class="sxs-lookup"><span data-stu-id="f3456-114">Specifies the display name of the computer group.</span></span>

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

### <span data-ttu-id="f3456-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f3456-115">-Force</span></span>
<span data-ttu-id="f3456-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f3456-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f3456-117">-Query</span><span class="sxs-lookup"><span data-stu-id="f3456-117">-Query</span></span>
<span data-ttu-id="f3456-118">Określa zapytanie grupy komputerów.</span><span class="sxs-lookup"><span data-stu-id="f3456-118">Specifies the query of the computer group.</span></span>

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

### <span data-ttu-id="f3456-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3456-119">-ResourceGroupName</span></span>
<span data-ttu-id="f3456-120">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f3456-120">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f3456-121">Polecenie cmdlet tworzy grupę komputer w tej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="f3456-121">The cmdlet creates computer group in this resource group.</span></span>

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

### <span data-ttu-id="f3456-122">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="f3456-122">-SavedSearchId</span></span>
<span data-ttu-id="f3456-123">Określa identyfikator grupy komputerów.</span><span class="sxs-lookup"><span data-stu-id="f3456-123">Specifies the ID of the computer group.</span></span>

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

### <span data-ttu-id="f3456-124">-Version</span><span class="sxs-lookup"><span data-stu-id="f3456-124">-Version</span></span>
<span data-ttu-id="f3456-125">Określa wersję.</span><span class="sxs-lookup"><span data-stu-id="f3456-125">Specifies the version.</span></span>

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

### <span data-ttu-id="f3456-126">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="f3456-126">-WorkspaceName</span></span>
<span data-ttu-id="f3456-127">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="f3456-127">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="f3456-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f3456-128">-Confirm</span></span>
<span data-ttu-id="f3456-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3456-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3456-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3456-130">-WhatIf</span></span>
<span data-ttu-id="f3456-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3456-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3456-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f3456-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3456-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3456-133">CommonParameters</span></span>
<span data-ttu-id="f3456-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3456-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3456-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3456-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3456-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3456-136">INPUTS</span></span>

### <span data-ttu-id="f3456-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f3456-137">System.String</span></span>

### <span data-ttu-id="f3456-138">System. Int64</span><span class="sxs-lookup"><span data-stu-id="f3456-138">System.Int64</span></span>

## <span data-ttu-id="f3456-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3456-139">OUTPUTS</span></span>

### <span data-ttu-id="f3456-140">System .NET. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="f3456-140">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="f3456-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3456-141">NOTES</span></span>

## <span data-ttu-id="f3456-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3456-142">RELATED LINKS</span></span>
