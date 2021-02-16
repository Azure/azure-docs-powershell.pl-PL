---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: 82df573a658fda9af97778e59819e45359c226fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186458"
---
# <span data-ttu-id="71202-101">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="71202-101">Get-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="71202-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71202-102">SYNOPSIS</span></span>
<span data-ttu-id="71202-103">Pobiera wdrożenia do grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="71202-103">Gets the deployments in a resource group.</span></span>

## <span data-ttu-id="71202-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="71202-104">SYNTAX</span></span>

### <span data-ttu-id="71202-105">GetByResourceGroupDeploymentName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="71202-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71202-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="71202-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="71202-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="71202-107">DESCRIPTION</span></span>
<span data-ttu-id="71202-108">Polecenie **cmdlet Get-AzResourceGroupDeployment** pobiera wdrożenia w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="71202-108">The **Get-AzResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="71202-109">Określ parametr *Name (Nazwa)* *lub Id (Identyfikator),* aby filtrować wyniki.</span><span class="sxs-lookup"><span data-stu-id="71202-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="71202-110">Domyślnie **Get-AzResourceGroupDeployment** pobiera wszystkie wdrożenia dla określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="71202-110">By default, **Get-AzResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="71202-111">Zasób platformy Azure to jednostka platformy Azure zarządzana przez użytkownika, taka jak serwer bazy danych, baza danych lub witryna internetowa.</span><span class="sxs-lookup"><span data-stu-id="71202-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="71202-112">Grupa zasobów platformy Azure to zbiór zasobów platformy Azure wdrożonych jako jednostka.</span><span class="sxs-lookup"><span data-stu-id="71202-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="71202-113">Wdrożenie to operacja, która udostępnia do użytku zasoby w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="71202-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="71202-114">Aby uzyskać więcej informacji na temat zasobów platformy Azure i grup zasobów platformy Azure, zobacz New-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71202-114">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="71202-115">To polecenie cmdlet umożliwia śledzenie.</span><span class="sxs-lookup"><span data-stu-id="71202-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="71202-116">Do debugowania użyj tego polecenia cmdlet z Get-AzLog cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71202-116">For debugging, use this cmdlet with the Get-AzLog cmdlet.</span></span>

## <span data-ttu-id="71202-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="71202-117">EXAMPLES</span></span>

### <span data-ttu-id="71202-118">Przykład 1. Uzyskiwanie wszystkich wdrożeń dla grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="71202-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="71202-119">To polecenie pobiera wszystkie wdrożenia dla grupy zasobów ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="71202-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="71202-120">W wynikach przedstawiono wdrożenie blogu WordPress, które używało szablonu galerii.</span><span class="sxs-lookup"><span data-stu-id="71202-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="71202-121">Przykład 2. Uzyskiwanie wdrożenia według nazwy</span><span class="sxs-lookup"><span data-stu-id="71202-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="71202-122">To polecenie pobiera wdrożenie DeployWebsite01 grupy zasobów ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="71202-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="71202-123">Możesz przypisać nazwę do wdrożenia podczas jego tworzenia przy użyciu polecenia cmdlet **New-AzResourceGroup** lub **New-AzResourceGroupDeployment.**</span><span class="sxs-lookup"><span data-stu-id="71202-123">You can assign a name to a deployment when you create it by using the **New-AzResourceGroup** or **New-AzResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="71202-124">Jeśli nie przypiszesz nazwy, polecenia cmdlet będą używać domyślnej nazwy na podstawie szablonu użytego do utworzenia wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="71202-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="71202-125">Przykład 3. Uzyskiwanie wdrożeń wszystkich grup zasobów</span><span class="sxs-lookup"><span data-stu-id="71202-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="71202-126">To polecenie pobiera wszystkie grupy zasobów w subskrypcji przy użyciu Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71202-126">This command gets all resource groups in your subscription by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="71202-127">Polecenie przekazuje grupy zasobów do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="71202-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="71202-128">Bieżące polecenie cmdlet pobiera wszystkie wdrożenia wszystkich grup zasobów w subskrypcji i przekazuje wyniki do polecenia cmdlet Format-Table w celu wyświetlenia wartości właściwości **ResourceGroupName,** **DeploymentName** i **ProvisioningState.**</span><span class="sxs-lookup"><span data-stu-id="71202-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName**, **DeploymentName**, and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="71202-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71202-129">PARAMETERS</span></span>

### <span data-ttu-id="71202-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71202-130">-DefaultProfile</span></span>
<span data-ttu-id="71202-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="71202-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71202-132">— Id</span><span class="sxs-lookup"><span data-stu-id="71202-132">-Id</span></span>
<span data-ttu-id="71202-133">Określa identyfikator wdrożenia grupy zasobów do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="71202-133">Specifies the ID of the resource group deployment to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71202-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="71202-134">-Name</span></span>
<span data-ttu-id="71202-135">Określa nazwę wdrożenia do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="71202-135">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="71202-136">Symbole wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="71202-136">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71202-137">— Przed</span><span class="sxs-lookup"><span data-stu-id="71202-137">-Pre</span></span>
<span data-ttu-id="71202-138">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="71202-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="71202-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71202-139">-ResourceGroupName</span></span>
<span data-ttu-id="71202-140">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="71202-140">Specifies the name of a resource group.</span></span>
<span data-ttu-id="71202-141">Polecenie cmdlet pobiera wdrożenia grupy zasobów, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="71202-141">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="71202-142">Symbole wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="71202-142">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="71202-143">Ten parametr jest wymagany i w każdym z poleceń można określić tylko jedną grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="71202-143">This parameter is required and you can specify only one resource group in each command.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71202-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71202-144">CommonParameters</span></span>
<span data-ttu-id="71202-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71202-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71202-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71202-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71202-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71202-147">INPUTS</span></span>

### <span data-ttu-id="71202-148">System.String</span><span class="sxs-lookup"><span data-stu-id="71202-148">System.String</span></span>

## <span data-ttu-id="71202-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71202-149">OUTPUTS</span></span>

### <span data-ttu-id="71202-150">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="71202-150">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="71202-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="71202-151">NOTES</span></span>

## <span data-ttu-id="71202-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71202-152">RELATED LINKS</span></span>

[<span data-ttu-id="71202-153">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="71202-153">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="71202-154">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="71202-154">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="71202-155">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="71202-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="71202-156">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="71202-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="71202-157">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="71202-157">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="71202-158">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="71202-158">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


