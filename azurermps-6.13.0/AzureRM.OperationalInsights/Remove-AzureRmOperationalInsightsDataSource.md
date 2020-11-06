---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: e9d5a7443c8a758cdc839826025d51fe57d55420
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547367"
---
# <span data-ttu-id="ff056-101">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="ff056-101">Remove-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="ff056-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ff056-102">SYNOPSIS</span></span>
<span data-ttu-id="ff056-103">Usuwa źródło danych.</span><span class="sxs-lookup"><span data-stu-id="ff056-103">Deletes a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff056-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ff056-104">SYNTAX</span></span>

### <span data-ttu-id="ff056-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ff056-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff056-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ff056-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff056-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ff056-107">DESCRIPTION</span></span>
<span data-ttu-id="ff056-108">Polecenie cmdlet **Remove-AzureRmOperationalInsightsDataSource** usuwa źródło danych.</span><span class="sxs-lookup"><span data-stu-id="ff056-108">The **Remove-AzureRmOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="ff056-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ff056-109">EXAMPLES</span></span>

## <span data-ttu-id="ff056-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ff056-110">PARAMETERS</span></span>

### <span data-ttu-id="ff056-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff056-111">-DefaultProfile</span></span>
<span data-ttu-id="ff056-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ff056-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff056-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ff056-113">-Force</span></span>
<span data-ttu-id="ff056-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ff056-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ff056-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ff056-115">-Name</span></span>
<span data-ttu-id="ff056-116">Określa nazwę źródła danych, które należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="ff056-116">Specifies the name of a data source to delete.</span></span>

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

### <span data-ttu-id="ff056-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff056-117">-ResourceGroupName</span></span>
<span data-ttu-id="ff056-118">Określa nazwę grupy zasobów zawierającej komputery.</span><span class="sxs-lookup"><span data-stu-id="ff056-118">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="ff056-119">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="ff056-119">-Workspace</span></span>
<span data-ttu-id="ff056-120">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff056-120">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ff056-121">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="ff056-121">-WorkspaceName</span></span>
<span data-ttu-id="ff056-122">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff056-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ff056-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ff056-123">-Confirm</span></span>
<span data-ttu-id="ff056-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff056-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff056-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff056-125">-WhatIf</span></span>
<span data-ttu-id="ff056-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff056-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff056-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ff056-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff056-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff056-128">CommonParameters</span></span>
<span data-ttu-id="ff056-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff056-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff056-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff056-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff056-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff056-131">INPUTS</span></span>

### <span data-ttu-id="ff056-132">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ff056-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="ff056-133">Parametry: przestrzeń robocza (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ff056-133">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="ff056-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ff056-134">System.String</span></span>

## <span data-ttu-id="ff056-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ff056-135">OUTPUTS</span></span>

### <span data-ttu-id="ff056-136">System. void</span><span class="sxs-lookup"><span data-stu-id="ff056-136">System.Void</span></span>

## <span data-ttu-id="ff056-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ff056-137">NOTES</span></span>
* <span data-ttu-id="ff056-138">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, operacyjne, Insights</span><span class="sxs-lookup"><span data-stu-id="ff056-138">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="ff056-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff056-139">RELATED LINKS</span></span>

[<span data-ttu-id="ff056-140">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="ff056-140">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="ff056-141">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="ff056-141">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


