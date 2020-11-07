---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
ms.openlocfilehash: d8ec5eed1b6c955720822e28bf54da68e9aefcac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708805"
---
# <span data-ttu-id="c57b4-101">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="c57b4-101">Remove-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="c57b4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c57b4-102">SYNOPSIS</span></span>
<span data-ttu-id="c57b4-103">Usuwa źródło danych.</span><span class="sxs-lookup"><span data-stu-id="c57b4-103">Deletes a data source.</span></span>

## <span data-ttu-id="c57b4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c57b4-104">SYNTAX</span></span>

### <span data-ttu-id="c57b4-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c57b4-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c57b4-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c57b4-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c57b4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c57b4-107">DESCRIPTION</span></span>
<span data-ttu-id="c57b4-108">Polecenie cmdlet **Remove-AzOperationalInsightsDataSource** usuwa źródło danych.</span><span class="sxs-lookup"><span data-stu-id="c57b4-108">The **Remove-AzOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="c57b4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c57b4-109">EXAMPLES</span></span>

## <span data-ttu-id="c57b4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c57b4-110">PARAMETERS</span></span>

### <span data-ttu-id="c57b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c57b4-111">-DefaultProfile</span></span>
<span data-ttu-id="c57b4-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c57b4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c57b4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c57b4-113">-Force</span></span>
<span data-ttu-id="c57b4-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c57b4-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c57b4-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c57b4-115">-Name</span></span>
<span data-ttu-id="c57b4-116">Określa nazwę źródła danych, które należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="c57b4-116">Specifies the name of a data source to delete.</span></span>

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

### <span data-ttu-id="c57b4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c57b4-117">-ResourceGroupName</span></span>
<span data-ttu-id="c57b4-118">Określa nazwę grupy zasobów zawierającej komputery.</span><span class="sxs-lookup"><span data-stu-id="c57b4-118">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c57b4-119">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="c57b4-119">-Workspace</span></span>
<span data-ttu-id="c57b4-120">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c57b4-120">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c57b4-121">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="c57b4-121">-WorkspaceName</span></span>
<span data-ttu-id="c57b4-122">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c57b4-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c57b4-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c57b4-123">-Confirm</span></span>
<span data-ttu-id="c57b4-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c57b4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c57b4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c57b4-125">-WhatIf</span></span>
<span data-ttu-id="c57b4-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c57b4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c57b4-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c57b4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c57b4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c57b4-128">CommonParameters</span></span>
<span data-ttu-id="c57b4-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c57b4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c57b4-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c57b4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c57b4-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c57b4-131">INPUTS</span></span>

### <span data-ttu-id="c57b4-132">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c57b4-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="c57b4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c57b4-133">System.String</span></span>

## <span data-ttu-id="c57b4-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c57b4-134">OUTPUTS</span></span>

### <span data-ttu-id="c57b4-135">System. void</span><span class="sxs-lookup"><span data-stu-id="c57b4-135">System.Void</span></span>

## <span data-ttu-id="c57b4-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c57b4-136">NOTES</span></span>
* <span data-ttu-id="c57b4-137">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, operacyjne, Insights</span><span class="sxs-lookup"><span data-stu-id="c57b4-137">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="c57b4-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c57b4-138">RELATED LINKS</span></span>

[<span data-ttu-id="c57b4-139">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="c57b4-139">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="c57b4-140">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="c57b4-140">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


