---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: d35797c007702f66bd462281a2531055524aeff5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718033"
---
# <span data-ttu-id="1651c-101">Remove-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="1651c-101">Remove-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="1651c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1651c-102">SYNOPSIS</span></span>
<span data-ttu-id="1651c-103">Usuwa obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="1651c-103">Removes a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1651c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1651c-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1651c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1651c-105">DESCRIPTION</span></span>
<span data-ttu-id="1651c-106">Polecenie cmdlet **Remove-AzureRmOperationalInsightsWorkspace** usuwa istniejący obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="1651c-106">The **Remove-AzureRmOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="1651c-107">Jeśli ten obszar roboczy był połączony z istniejącym kontem za pośrednictwem parametru *IDKlienta* w czasie tworzenia, oryginalne konto nie zostanie usunięte w portalu usługi Insights.</span><span class="sxs-lookup"><span data-stu-id="1651c-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="1651c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1651c-108">EXAMPLES</span></span>

### <span data-ttu-id="1651c-109">Przykład 1. Usuń obszar roboczy według nazwy</span><span class="sxs-lookup"><span data-stu-id="1651c-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="1651c-110">To polecenie usuwa obszar roboczy o nazwie Moja przestrzeń robocza z grupy zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1651c-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="1651c-111">Przykład 2: Usuwanie obszaru roboczego za pomocą potoku i bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="1651c-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzureRmOperationalInsightsWorkspace -Force
```

<span data-ttu-id="1651c-112">To polecenie używa polecenia cmdlet Get-AzureRmOperationalInsightsWorkspace, aby uzyskać obszar roboczy o nazwie webworkspace, a następnie przekazywać go do polecenia cmdlet **Remove-AzureRmOperationalInsightsWorkspace** przy użyciu operatora potoku w celu usunięcia go.</span><span class="sxs-lookup"><span data-stu-id="1651c-112">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="1651c-113">Ponieważ parametr *Force* jest określony, polecenie nie wyświetla monitu przed usunięciem obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="1651c-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

## <span data-ttu-id="1651c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1651c-114">PARAMETERS</span></span>

### <span data-ttu-id="1651c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1651c-115">-DefaultProfile</span></span>
<span data-ttu-id="1651c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1651c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1651c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1651c-117">-Force</span></span>
<span data-ttu-id="1651c-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1651c-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1651c-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1651c-119">-Name</span></span>
<span data-ttu-id="1651c-120">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="1651c-120">Specifies the name of the workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1651c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1651c-121">-ResourceGroupName</span></span>
<span data-ttu-id="1651c-122">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1651c-122">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1651c-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1651c-123">-Confirm</span></span>
<span data-ttu-id="1651c-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1651c-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1651c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1651c-125">-WhatIf</span></span>
<span data-ttu-id="1651c-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1651c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1651c-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1651c-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1651c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1651c-128">CommonParameters</span></span>
<span data-ttu-id="1651c-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1651c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1651c-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1651c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1651c-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1651c-131">INPUTS</span></span>

### <span data-ttu-id="1651c-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1651c-132">None</span></span>
<span data-ttu-id="1651c-133">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1651c-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1651c-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1651c-134">OUTPUTS</span></span>

## <span data-ttu-id="1651c-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1651c-135">NOTES</span></span>

## <span data-ttu-id="1651c-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1651c-136">RELATED LINKS</span></span>

[<span data-ttu-id="1651c-137">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="1651c-137">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="1651c-138">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="1651c-138">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


