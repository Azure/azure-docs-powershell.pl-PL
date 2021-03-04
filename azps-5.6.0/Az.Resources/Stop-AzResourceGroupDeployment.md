---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/powershell/module/az.resources/stop-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
ms.openlocfilehash: 9258c15578aaeae5102a5d60b2f18a8a4f179d76
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967626"
---
# <span data-ttu-id="94226-101">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="94226-101">Stop-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="94226-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94226-102">SYNOPSIS</span></span>
<span data-ttu-id="94226-103">Anulowanie wdrożenia grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="94226-103">Cancels a resource group deployment.</span></span>

## <span data-ttu-id="94226-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="94226-104">SYNTAX</span></span>

### <span data-ttu-id="94226-105">StopByResourceGroupDeploymentName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="94226-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94226-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="94226-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94226-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="94226-107">DESCRIPTION</span></span>
<span data-ttu-id="94226-108">Polecenie **cmdlet Stop-AzResourceGroupDeployment** anuluje wdrożenie grupy zasobów platformy Azure, które zostało rozpoczęte, ale nie ukończone.</span><span class="sxs-lookup"><span data-stu-id="94226-108">The **Stop-AzResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="94226-109">Aby zatrzymać wdrożenie, wdrożenie musi mieć niepełny stan inicjowania obsługi, taki jak inicjowanie obsługi administracyjnej, a nie stan ukończony, taki jak Inicjowanie obsługi administracyjnej lub Zakończone niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="94226-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="94226-110">Zasób platformy Azure to jednostka zarządzana przez użytkownika, taka jak witryna internetowa, baza danych lub serwer bazy danych.</span><span class="sxs-lookup"><span data-stu-id="94226-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="94226-111">Grupa zasobów to zbiór zasobów wdrożonych jako jednostka.</span><span class="sxs-lookup"><span data-stu-id="94226-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="94226-112">Aby wdrożyć grupę zasobów, użyj New-AzResourceGroupDeployment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94226-112">To deploy a resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="94226-113">Polecenie New-AzResource umożliwia utworzenie nowego zasobu, ale nie powoduje wyzwolenia operacji wdrażania grupy zasobów, która może zostać zatrzymana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94226-113">The New-AzResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="94226-114">To polecenie cmdlet zatrzymuje tylko jedno uruchomione wdrożenie.</span><span class="sxs-lookup"><span data-stu-id="94226-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="94226-115">Użyj *parametru Name,* aby zatrzymać określone wdrożenie.</span><span class="sxs-lookup"><span data-stu-id="94226-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="94226-116">Jeśli parametr Name zostanie *pominięty,* parametr **Stop-AzResourceGroupDeployment** wyszuka uruchomione wdrożenie i zatrzyma je.</span><span class="sxs-lookup"><span data-stu-id="94226-116">If you omit the *Name* parameter, **Stop-AzResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="94226-117">Jeśli polecenie cmdlet znajdzie więcej niż jedno uruchomione wdrożenie, polecenie kończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="94226-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="94226-118">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="94226-118">EXAMPLES</span></span>

### <span data-ttu-id="94226-119">Przykład 1. Uruchamianie i zatrzymywanie wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="94226-119">Example 1: Starting and stopping a resource group deployment</span></span>

```powershell
PS C:\> New-AzResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg -TemplateFile .\storage-account-create-azdeploy.json -TemplateParameterFile .\storage-account-create-azdeploy.parameters.json -AsJob

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Running       True            localhost            New-AzResourceGro...

PS C:\> Stop-AzResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg
True

PS C:\> Get-Job 1

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Failed        True            localhost            New-AzResourceGro...
```

## <span data-ttu-id="94226-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94226-120">PARAMETERS</span></span>

### <span data-ttu-id="94226-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94226-121">-DefaultProfile</span></span>
<span data-ttu-id="94226-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="94226-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94226-123">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="94226-123">-Id</span></span>
<span data-ttu-id="94226-124">Określa identyfikator wdrożenia grupy zasobów do zatrzymania.</span><span class="sxs-lookup"><span data-stu-id="94226-124">Specifies the ID of the resource group deployment to stop.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94226-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="94226-125">-Name</span></span>
<span data-ttu-id="94226-126">Określa nazwę wdrożenia grupy zasobów, które ma się zakończyć.</span><span class="sxs-lookup"><span data-stu-id="94226-126">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="94226-127">Jeśli nie określisz tego parametru, to polecenie cmdlet wyszuka uruchomione wdrożenie w grupie zasobów i zatrzyma je.</span><span class="sxs-lookup"><span data-stu-id="94226-127">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="94226-128">Jeśli zostanie znalezione więcej niż jedno uruchomione wdrożenie, polecenie kończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="94226-128">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="94226-129">Aby uzyskać nazwę wdrożenia, użyj Get-AzResourceGroupDeployment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94226-129">To get the deployment name, use the Get-AzResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94226-130">— Przed</span><span class="sxs-lookup"><span data-stu-id="94226-130">-Pre</span></span>
<span data-ttu-id="94226-131">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="94226-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="94226-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94226-132">-ResourceGroupName</span></span>
<span data-ttu-id="94226-133">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="94226-133">Specifies the name of the resource group.</span></span>
<span data-ttu-id="94226-134">To polecenie cmdlet powoduje zatrzymanie wdrożenia grupy zasobów, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="94226-134">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94226-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="94226-135">-Confirm</span></span>
<span data-ttu-id="94226-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="94226-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94226-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94226-137">-WhatIf</span></span>
<span data-ttu-id="94226-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94226-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94226-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="94226-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94226-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94226-140">CommonParameters</span></span>
<span data-ttu-id="94226-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94226-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94226-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94226-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94226-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94226-143">INPUTS</span></span>

### <span data-ttu-id="94226-144">System.String</span><span class="sxs-lookup"><span data-stu-id="94226-144">System.String</span></span>

## <span data-ttu-id="94226-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94226-145">OUTPUTS</span></span>

### <span data-ttu-id="94226-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="94226-146">System.Boolean</span></span>

## <span data-ttu-id="94226-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="94226-147">NOTES</span></span>

## <span data-ttu-id="94226-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94226-148">RELATED LINKS</span></span>

[<span data-ttu-id="94226-149">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="94226-149">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="94226-150">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="94226-150">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="94226-151">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="94226-151">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="94226-152">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="94226-152">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="94226-153">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="94226-153">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="94226-154">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="94226-154">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


