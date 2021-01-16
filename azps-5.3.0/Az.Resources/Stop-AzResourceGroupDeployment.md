---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
ms.openlocfilehash: fa189637c9c2c1b63ab0e8dd0b00fab3f4505da0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382557"
---
# <span data-ttu-id="42b9d-101">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="42b9d-101">Stop-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="42b9d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42b9d-102">SYNOPSIS</span></span>
<span data-ttu-id="42b9d-103">Anuluje wdrożenie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="42b9d-103">Cancels a resource group deployment.</span></span>

## <span data-ttu-id="42b9d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42b9d-104">SYNTAX</span></span>

### <span data-ttu-id="42b9d-105">StopByResourceGroupDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="42b9d-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42b9d-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="42b9d-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42b9d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="42b9d-107">DESCRIPTION</span></span>
<span data-ttu-id="42b9d-108">Polecenie cmdlet **stop-AzResourceGroupDeployment** anuluje wdrożenie grup zasobów platformy Azure, które zostało uruchomione, ale nie zostało ukończone.</span><span class="sxs-lookup"><span data-stu-id="42b9d-108">The **Stop-AzResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="42b9d-109">Aby zatrzymać wdrożenie, wdrożenie musi mieć niekompletny stan inicjowania obsługi, taki jak obsługa administracyjna, a nie stan wykonania, na przykład zainicjowana obsługa administracyjna lub niepowodzenie.</span><span class="sxs-lookup"><span data-stu-id="42b9d-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="42b9d-110">Zasób platformy Azure to jednostka zarządzana przez użytkownika, taka jak witryna sieci Web, baza danych lub serwer bazy danych.</span><span class="sxs-lookup"><span data-stu-id="42b9d-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="42b9d-111">Grupa zasobów to zbiór zasobów wdrożonych jako jednostka.</span><span class="sxs-lookup"><span data-stu-id="42b9d-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="42b9d-112">Aby wdrożyć grupę zasobów, użyj polecenia cmdlet New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="42b9d-112">To deploy a resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="42b9d-113">Polecenie cmdlet New-AzResource tworzy nowy zasób, ale nie wyzwala operacji wdrażania grupy zasobów, która może zostać zatrzymana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42b9d-113">The New-AzResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="42b9d-114">To polecenie cmdlet powoduje zatrzymanie tylko jednego uruchomionego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="42b9d-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="42b9d-115">Użyj parametru *name* , aby zatrzymać określone wdrożenie.</span><span class="sxs-lookup"><span data-stu-id="42b9d-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="42b9d-116">Jeśli pominięto parametr *name* , polecenie **stop-AzResourceGroupDeployment** wyszukuje uruchomione wdrożenie i zatrzymuje je.</span><span class="sxs-lookup"><span data-stu-id="42b9d-116">If you omit the *Name* parameter, **Stop-AzResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="42b9d-117">Jeśli polecenie cmdlet umożliwia znalezienie kilku uruchomionych wdrożeń, wykonanie polecenia nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="42b9d-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="42b9d-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42b9d-118">EXAMPLES</span></span>

### <span data-ttu-id="42b9d-119">Przykład 1: Rozpoczynanie i zatrzymywanie wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="42b9d-119">Example 1: Starting and stopping a resource group deployment</span></span>

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

## <span data-ttu-id="42b9d-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42b9d-120">PARAMETERS</span></span>

### <span data-ttu-id="42b9d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42b9d-121">-DefaultProfile</span></span>
<span data-ttu-id="42b9d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="42b9d-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42b9d-123">-ID</span><span class="sxs-lookup"><span data-stu-id="42b9d-123">-Id</span></span>
<span data-ttu-id="42b9d-124">Określa identyfikator wdrożenia grupy zasobów, który ma zostać zatrzymany.</span><span class="sxs-lookup"><span data-stu-id="42b9d-124">Specifies the ID of the resource group deployment to stop.</span></span>

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

### <span data-ttu-id="42b9d-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="42b9d-125">-Name</span></span>
<span data-ttu-id="42b9d-126">Określa nazwę wdrożenia grupy zasobów do zatrzymania.</span><span class="sxs-lookup"><span data-stu-id="42b9d-126">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="42b9d-127">Jeśli nie podano tego parametru, to polecenie cmdlet wyszukuje uruchomione wdrożenie w grupie zasobów i zatrzymuje je.</span><span class="sxs-lookup"><span data-stu-id="42b9d-127">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="42b9d-128">Jeśli okaże się, że nie jest uruchomione więcej niż jedno wdrożenie, polecenie nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="42b9d-128">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="42b9d-129">Aby uzyskać nazwę wdrożenia, użyj polecenia cmdlet Get-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="42b9d-129">To get the deployment name, use the Get-AzResourceGroupDeployment cmdlet.</span></span>

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

### <span data-ttu-id="42b9d-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="42b9d-130">-Pre</span></span>
<span data-ttu-id="42b9d-131">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="42b9d-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="42b9d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42b9d-132">-ResourceGroupName</span></span>
<span data-ttu-id="42b9d-133">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="42b9d-133">Specifies the name of the resource group.</span></span>
<span data-ttu-id="42b9d-134">To polecenie cmdlet zatrzymuje wdrożenie grupy zasobów, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="42b9d-134">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="42b9d-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="42b9d-135">-Confirm</span></span>
<span data-ttu-id="42b9d-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42b9d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42b9d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42b9d-137">-WhatIf</span></span>
<span data-ttu-id="42b9d-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42b9d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42b9d-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="42b9d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42b9d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42b9d-140">CommonParameters</span></span>
<span data-ttu-id="42b9d-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42b9d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42b9d-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42b9d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42b9d-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42b9d-143">INPUTS</span></span>

### <span data-ttu-id="42b9d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="42b9d-144">System.String</span></span>

## <span data-ttu-id="42b9d-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42b9d-145">OUTPUTS</span></span>

### <span data-ttu-id="42b9d-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="42b9d-146">System.Boolean</span></span>

## <span data-ttu-id="42b9d-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42b9d-147">NOTES</span></span>

## <span data-ttu-id="42b9d-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42b9d-148">RELATED LINKS</span></span>

[<span data-ttu-id="42b9d-149">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="42b9d-149">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="42b9d-150">Nowe — AzResource</span><span class="sxs-lookup"><span data-stu-id="42b9d-150">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="42b9d-151">Nowe — AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="42b9d-151">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="42b9d-152">Nowe — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="42b9d-152">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="42b9d-153">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="42b9d-153">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="42b9d-154">Test — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="42b9d-154">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


