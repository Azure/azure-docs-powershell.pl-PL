---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/stop-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: 139b38fed6e768e761631687f06cd833afaa4068
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897218"
---
# <span data-ttu-id="73341-101">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="73341-101">Stop-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="73341-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="73341-102">SYNOPSIS</span></span>
<span data-ttu-id="73341-103">Anuluje wdrożenie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="73341-103">Cancels a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73341-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="73341-104">SYNTAX</span></span>

### <span data-ttu-id="73341-105">StopByResourceGroupDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="73341-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73341-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="73341-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73341-107">Opis</span><span class="sxs-lookup"><span data-stu-id="73341-107">DESCRIPTION</span></span>
<span data-ttu-id="73341-108">Polecenie cmdlet **stop-AzureRmResourceGroupDeployment** anuluje wdrożenie grup zasobów platformy Azure, które zostało uruchomione, ale nie zostało ukończone.</span><span class="sxs-lookup"><span data-stu-id="73341-108">The **Stop-AzureRmResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="73341-109">Aby zatrzymać wdrożenie, wdrożenie musi mieć niekompletny stan inicjowania obsługi, taki jak obsługa administracyjna, a nie stan wykonania, na przykład zainicjowana obsługa administracyjna lub niepowodzenie.</span><span class="sxs-lookup"><span data-stu-id="73341-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="73341-110">Zasób platformy Azure to jednostka zarządzana przez użytkownika, taka jak witryna sieci Web, baza danych lub serwer bazy danych.</span><span class="sxs-lookup"><span data-stu-id="73341-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="73341-111">Grupa zasobów to zbiór zasobów wdrożonych jako jednostka.</span><span class="sxs-lookup"><span data-stu-id="73341-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="73341-112">Aby wdrożyć grupę zasobów, użyj polecenia cmdlet New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="73341-112">To deploy a resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="73341-113">Polecenie cmdlet New-AzureRmResource tworzy nowy zasób, ale nie wyzwala operacji wdrażania grupy zasobów, która może zostać zatrzymana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73341-113">The New-AzureRmResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="73341-114">To polecenie cmdlet powoduje zatrzymanie tylko jednego uruchomionego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="73341-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="73341-115">Użyj parametru *name* , aby zatrzymać określone wdrożenie.</span><span class="sxs-lookup"><span data-stu-id="73341-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="73341-116">Jeśli pominięto parametr *name* , polecenie **stop-AzureRmResourceGroupDeployment** wyszukuje uruchomione wdrożenie i zatrzymuje je.</span><span class="sxs-lookup"><span data-stu-id="73341-116">If you omit the *Name* parameter, **Stop-AzureRmResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="73341-117">Jeśli polecenie cmdlet umożliwia znalezienie kilku uruchomionych wdrożeń, wykonanie polecenia nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="73341-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="73341-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="73341-118">EXAMPLES</span></span>

### <span data-ttu-id="73341-119">Przykład 1: Rozpoczynanie i zatrzymywanie wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="73341-119">Example 1: Starting and stopping a resource group deployment</span></span>

```powershell
PS C:\> New-AzureRmResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg -TemplateFile .\storage-account-create-azuredeploy.json -TemplateParameterFile .\storage-account-create-azuredeploy.parameters.json -AsJob

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmResourceGro...

PS C:\> Stop-AzureRmResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg
True

PS C:\> Get-Job 1

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Failed        True            localhost            New-AzureRmResourceGro...
```

## <span data-ttu-id="73341-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="73341-120">PARAMETERS</span></span>

### <span data-ttu-id="73341-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="73341-121">-ApiVersion</span></span>
<span data-ttu-id="73341-122">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="73341-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="73341-123">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="73341-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="73341-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73341-124">-DefaultProfile</span></span>
<span data-ttu-id="73341-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="73341-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73341-126">-ID</span><span class="sxs-lookup"><span data-stu-id="73341-126">-Id</span></span>
<span data-ttu-id="73341-127">Określa identyfikator wdrożenia grupy zasobów, który ma zostać zatrzymany.</span><span class="sxs-lookup"><span data-stu-id="73341-127">Specifies the ID of the resource group deployment to stop.</span></span>

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

### <span data-ttu-id="73341-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="73341-128">-Name</span></span>
<span data-ttu-id="73341-129">Określa nazwę wdrożenia grupy zasobów do zatrzymania.</span><span class="sxs-lookup"><span data-stu-id="73341-129">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="73341-130">Jeśli nie podano tego parametru, to polecenie cmdlet wyszukuje uruchomione wdrożenie w grupie zasobów i zatrzymuje je.</span><span class="sxs-lookup"><span data-stu-id="73341-130">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="73341-131">Jeśli okaże się, że nie jest uruchomione więcej niż jedno wdrożenie, polecenie nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="73341-131">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="73341-132">Aby uzyskać nazwę wdrożenia, użyj polecenia cmdlet Get-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="73341-132">To get the deployment name, use the Get-AzureRmResourceGroupDeployment cmdlet.</span></span>

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

### <span data-ttu-id="73341-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="73341-133">-Pre</span></span>
<span data-ttu-id="73341-134">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="73341-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="73341-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73341-135">-ResourceGroupName</span></span>
<span data-ttu-id="73341-136">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="73341-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="73341-137">To polecenie cmdlet zatrzymuje wdrożenie grupy zasobów, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="73341-137">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="73341-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="73341-138">-Confirm</span></span>
<span data-ttu-id="73341-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73341-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73341-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73341-140">-WhatIf</span></span>
<span data-ttu-id="73341-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73341-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73341-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="73341-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73341-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73341-143">CommonParameters</span></span>
<span data-ttu-id="73341-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73341-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73341-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73341-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73341-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73341-146">INPUTS</span></span>

### <span data-ttu-id="73341-147">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="73341-147">None</span></span>

## <span data-ttu-id="73341-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="73341-148">OUTPUTS</span></span>

### <span data-ttu-id="73341-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="73341-149">System.Boolean</span></span>

## <span data-ttu-id="73341-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="73341-150">NOTES</span></span>

## <span data-ttu-id="73341-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73341-151">RELATED LINKS</span></span>

[<span data-ttu-id="73341-152">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="73341-152">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="73341-153">Nowe — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="73341-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="73341-154">Nowe — AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="73341-154">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="73341-155">Nowe — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="73341-155">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="73341-156">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="73341-156">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="73341-157">Test — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="73341-157">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


