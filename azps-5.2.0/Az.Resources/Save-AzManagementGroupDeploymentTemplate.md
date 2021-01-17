---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azmanagementgroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
ms.openlocfilehash: f45602ad2515a90e39e45edb80ca1cb0bf051f00
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345469"
---
# <span data-ttu-id="e306c-101">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="e306c-101">Save-AzManagementGroupDeploymentTemplate</span></span>

## <span data-ttu-id="e306c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e306c-102">SYNOPSIS</span></span>
<span data-ttu-id="e306c-103">Zapisuje szablon wdrożenia w pliku.</span><span class="sxs-lookup"><span data-stu-id="e306c-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="e306c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e306c-104">SYNTAX</span></span>

### <span data-ttu-id="e306c-105">SaveByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e306c-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzManagementGroupDeploymentTemplate -ManagementGroupId <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e306c-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="e306c-106">SaveByDeploymentObject</span></span>
```
Save-AzManagementGroupDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e306c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e306c-107">DESCRIPTION</span></span>
<span data-ttu-id="e306c-108">Polecenie cmdlet **Save-AzManagementGroupDeploymentTemplate**  zapisuje szablon wdrożenia w pliku JSON dla wdrożenia w grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="e306c-108">The **Save-AzManagementGroupDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at a management group.</span></span>

## <span data-ttu-id="e306c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e306c-109">EXAMPLES</span></span>

### <span data-ttu-id="e306c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e306c-110">Example 1</span></span>
```powershell
PS C:\> Save-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -DeploymentName "TestDeployment"
```

<span data-ttu-id="e306c-111">To polecenie pobiera szablon wdrożenia z TestDeployment i zapisuje go jako plik JSON w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="e306c-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="e306c-112">Przykład 2: uzyskiwanie wdrożenia i zapisywanie jego szablonu</span><span class="sxs-lookup"><span data-stu-id="e306c-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -Name "RolesDeployment" | Save-AzManagementGroupDeploymentTemplate
```

<span data-ttu-id="e306c-113">To polecenie pobiera wdrożenie "RolesDeployment" w grupie zarządzania "myMG" i zapisuje jego szablon.</span><span class="sxs-lookup"><span data-stu-id="e306c-113">This command gets the deployment "RolesDeployment" at the management group "myMG" and saves its template.</span></span>

## <span data-ttu-id="e306c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e306c-114">PARAMETERS</span></span>

### <span data-ttu-id="e306c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e306c-115">-DefaultProfile</span></span>
<span data-ttu-id="e306c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e306c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e306c-117">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="e306c-117">-DeploymentName</span></span>
<span data-ttu-id="e306c-118">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e306c-118">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveByDeploymentName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e306c-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="e306c-119">-DeploymentObject</span></span>
<span data-ttu-id="e306c-120">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e306c-120">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: SaveByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e306c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e306c-121">-Force</span></span>
<span data-ttu-id="e306c-122">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e306c-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e306c-123">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="e306c-123">-ManagementGroupId</span></span>
<span data-ttu-id="e306c-124">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="e306c-124">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e306c-125">-Path</span><span class="sxs-lookup"><span data-stu-id="e306c-125">-Path</span></span>
<span data-ttu-id="e306c-126">Ścieżka wyjściowa pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="e306c-126">The output path of the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e306c-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="e306c-127">-Pre</span></span>
<span data-ttu-id="e306c-128">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="e306c-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e306c-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e306c-129">-Confirm</span></span>
<span data-ttu-id="e306c-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e306c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e306c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e306c-131">-WhatIf</span></span>
<span data-ttu-id="e306c-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e306c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e306c-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e306c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e306c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e306c-134">CommonParameters</span></span>
<span data-ttu-id="e306c-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e306c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e306c-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e306c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e306c-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e306c-137">INPUTS</span></span>

### <span data-ttu-id="e306c-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="e306c-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="e306c-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e306c-139">OUTPUTS</span></span>

### <span data-ttu-id="e306c-140">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="e306c-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="e306c-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e306c-141">NOTES</span></span>

## <span data-ttu-id="e306c-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e306c-142">RELATED LINKS</span></span>
