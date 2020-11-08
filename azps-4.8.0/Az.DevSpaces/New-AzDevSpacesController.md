---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: a99a26060492efbe40bc4a16633ca6a207e093b4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222595"
---
# <span data-ttu-id="2def3-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="2def3-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="2def3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2def3-102">SYNOPSIS</span></span>
<span data-ttu-id="2def3-103">Utwórz nowy kontroler DevSpaces platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2def3-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="2def3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2def3-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2def3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2def3-105">DESCRIPTION</span></span>
<span data-ttu-id="2def3-106">Utwórz nowy kontroler DevSpaces platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2def3-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="2def3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2def3-107">EXAMPLES</span></span>

### <span data-ttu-id="2def3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2def3-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="2def3-109">Utwórz kontroler DevSpaces w devSpaceResourceGroup Resources o nazwie devSpaceName.</span><span class="sxs-lookup"><span data-stu-id="2def3-109">Create a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="2def3-110">Użyj klastra ClusterName jako elementu docelowego dla tego kontrolera.</span><span class="sxs-lookup"><span data-stu-id="2def3-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="2def3-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2def3-111">PARAMETERS</span></span>

### <span data-ttu-id="2def3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2def3-112">-AsJob</span></span>
<span data-ttu-id="2def3-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2def3-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2def3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2def3-114">-DefaultProfile</span></span>
<span data-ttu-id="2def3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2def3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2def3-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2def3-116">-Name</span></span>
<span data-ttu-id="2def3-117">Nazwa kontrolera DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="2def3-117">DevSpaces Controller Name.</span></span>

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

### <span data-ttu-id="2def3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2def3-118">-ResourceGroupName</span></span>
<span data-ttu-id="2def3-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2def3-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="2def3-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="2def3-120">-Tag</span></span>
<span data-ttu-id="2def3-121">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="2def3-121">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="2def3-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="2def3-122">-TargetClusterName</span></span>
<span data-ttu-id="2def3-123">Nazwa klastra docelowego.</span><span class="sxs-lookup"><span data-stu-id="2def3-123">Target Cluster Name.</span></span>

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

### <span data-ttu-id="2def3-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2def3-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="2def3-125">Nazwa grupy zasobów docelowych.</span><span class="sxs-lookup"><span data-stu-id="2def3-125">Target Resource Group Name.</span></span>

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

### <span data-ttu-id="2def3-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2def3-126">-Confirm</span></span>
<span data-ttu-id="2def3-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2def3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2def3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2def3-128">-WhatIf</span></span>
<span data-ttu-id="2def3-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2def3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2def3-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2def3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2def3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2def3-131">CommonParameters</span></span>
<span data-ttu-id="2def3-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2def3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2def3-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2def3-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2def3-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2def3-134">INPUTS</span></span>

### <span data-ttu-id="2def3-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2def3-135">None</span></span>

## <span data-ttu-id="2def3-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2def3-136">OUTPUTS</span></span>

### <span data-ttu-id="2def3-137">Microsoft. Azure. Commands. DevSpaces. models. PSController</span><span class="sxs-lookup"><span data-stu-id="2def3-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="2def3-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2def3-138">NOTES</span></span>

## <span data-ttu-id="2def3-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2def3-139">RELATED LINKS</span></span>
