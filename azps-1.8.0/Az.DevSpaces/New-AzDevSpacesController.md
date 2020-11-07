---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: 5c4abfa199a8478c247b6c2b95fe0a3651faa4f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709928"
---
# <span data-ttu-id="9d9d9-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="9d9d9-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="9d9d9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9d9d9-102">SYNOPSIS</span></span>
<span data-ttu-id="9d9d9-103">Utwórz nowy kontroler DevSpaces platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="9d9d9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9d9d9-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d9d9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9d9d9-105">DESCRIPTION</span></span>
<span data-ttu-id="9d9d9-106">Utwórz nowy kontroler DevSpaces platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="9d9d9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9d9d9-107">EXAMPLES</span></span>

### <span data-ttu-id="9d9d9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9d9d9-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="9d9d9-109">Crreate kontroler DevSpaces w usłudze Resources devSpaceResourceGroup przy użyciu nazwy devSpaceName.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-109">Crreate a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="9d9d9-110">Użyj klastra ClusterName jako elementu docelowego dla tego kontrolera.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="9d9d9-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9d9d9-111">PARAMETERS</span></span>

### <span data-ttu-id="9d9d9-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d9d9-112">-AsJob</span></span>
<span data-ttu-id="9d9d9-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9d9d9-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9d9d9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d9d9-114">-DefaultProfile</span></span>
<span data-ttu-id="9d9d9-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d9d9-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9d9d9-116">-Name</span></span>
<span data-ttu-id="9d9d9-117">Nazwa kontrolera DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-117">DevSpaces Controller Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d9d9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d9d9-118">-ResourceGroupName</span></span>
<span data-ttu-id="9d9d9-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d9d9-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="9d9d9-120">-Tag</span></span>
<span data-ttu-id="9d9d9-121">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-121">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d9d9-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="9d9d9-122">-TargetClusterName</span></span>
<span data-ttu-id="9d9d9-123">Nazwa klastra docelowego.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-123">Target Cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d9d9-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d9d9-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="9d9d9-125">Nazwa grupy zasobów docelowych.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-125">Target Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d9d9-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9d9d9-126">-Confirm</span></span>
<span data-ttu-id="9d9d9-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d9d9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d9d9-128">-WhatIf</span></span>
<span data-ttu-id="9d9d9-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d9d9-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d9d9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d9d9-131">CommonParameters</span></span>
<span data-ttu-id="9d9d9-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d9d9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d9d9-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d9d9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d9d9-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d9d9-134">INPUTS</span></span>

### <span data-ttu-id="9d9d9-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9d9d9-135">None</span></span>

## <span data-ttu-id="9d9d9-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9d9d9-136">OUTPUTS</span></span>

### <span data-ttu-id="9d9d9-137">Microsoft. Azure. Commands. DevSpaces. models. PSController</span><span class="sxs-lookup"><span data-stu-id="9d9d9-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="9d9d9-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9d9d9-138">NOTES</span></span>

## <span data-ttu-id="9d9d9-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d9d9-139">RELATED LINKS</span></span>
