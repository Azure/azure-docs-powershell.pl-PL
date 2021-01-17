---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: 82df573a658fda9af97778e59819e45359c226fd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490501"
---
# <span data-ttu-id="a50b5-101">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a50b5-101">Get-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="a50b5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a50b5-102">SYNOPSIS</span></span>
<span data-ttu-id="a50b5-103">Pobiera wdrożenia w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="a50b5-103">Gets the deployments in a resource group.</span></span>

## <span data-ttu-id="a50b5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a50b5-104">SYNTAX</span></span>

### <span data-ttu-id="a50b5-105">GetByResourceGroupDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a50b5-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a50b5-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="a50b5-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a50b5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a50b5-107">DESCRIPTION</span></span>
<span data-ttu-id="a50b5-108">Polecenie cmdlet **Get-AzResourceGroupDeployment** pobiera wdrożenia w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a50b5-108">The **Get-AzResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="a50b5-109">Określ *nazwę* lub parametr *ID* , aby przefiltrować wyniki.</span><span class="sxs-lookup"><span data-stu-id="a50b5-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="a50b5-110">Domyślnie polecenie **Get-AzResourceGroupDeployment** pobiera wszystkie wdrożenia określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a50b5-110">By default, **Get-AzResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="a50b5-111">Zasób platformy Azure jest zarządzaną przez użytkownika jednostką Azure, taką jak serwer bazy danych, baza danych lub witryna sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a50b5-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="a50b5-112">Grupa zasobów platformy Azure to zbiór zasobów platformy Azure wdrożonych jako jednostka.</span><span class="sxs-lookup"><span data-stu-id="a50b5-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="a50b5-113">Wdrożenie to operacja, która powoduje, że zasoby w grupie zasobów są dostępne do użytku.</span><span class="sxs-lookup"><span data-stu-id="a50b5-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="a50b5-114">Aby uzyskać więcej informacji na temat zasobów platformy Azure i grup zasobów platformy Azure, zobacz polecenie cmdlet New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a50b5-114">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="a50b5-115">Za pomocą tego polecenia cmdlet można śledzić śledzenie.</span><span class="sxs-lookup"><span data-stu-id="a50b5-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="a50b5-116">W przypadku debugowania Użyj tego polecenia cmdlet, korzystając z polecenia cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="a50b5-116">For debugging, use this cmdlet with the Get-AzLog cmdlet.</span></span>

## <span data-ttu-id="a50b5-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a50b5-117">EXAMPLES</span></span>

### <span data-ttu-id="a50b5-118">Przykład 1. pobieranie wszystkich wdrożeń dla grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a50b5-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="a50b5-119">To polecenie pobiera wszystkie wdrożenia grupy zasobów ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="a50b5-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="a50b5-120">Wynik przedstawia wdrożenie dla blogu WordPress, który używa szablonu galerii.</span><span class="sxs-lookup"><span data-stu-id="a50b5-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="a50b5-121">Przykład 2: uzyskiwanie wdrożenia według nazwy</span><span class="sxs-lookup"><span data-stu-id="a50b5-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="a50b5-122">To polecenie pobiera DeployWebsite01 wdrożenia grupy zasobów ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="a50b5-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="a50b5-123">Możesz przypisać nazwę do wdrożenia podczas tworzenia go za pomocą poleceń cmdlet **New-AzResourceGroup** lub **New-AzResourceGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="a50b5-123">You can assign a name to a deployment when you create it by using the **New-AzResourceGroup** or **New-AzResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="a50b5-124">Jeśli nie przypiszesz nazwy, aplety poleceń będą dostarczały nazwę domyślną na podstawie szablonu, który jest wykorzystywany do tworzenia wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="a50b5-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="a50b5-125">Przykład 3: pobieranie wdrożeń wszystkich grup zasobów</span><span class="sxs-lookup"><span data-stu-id="a50b5-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="a50b5-126">To polecenie pobiera wszystkie grupy zasobów w ramach subskrypcji przy użyciu polecenia cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a50b5-126">This command gets all resource groups in your subscription by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="a50b5-127">Polecenie przekazuje grupy zasobów do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="a50b5-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a50b5-128">Bieżące polecenie cmdlet pobiera wszystkie wdrożenia wszystkich grup zasobów w ramach subskrypcji i przekazuje wyniki do polecenia cmdlet Format-Table, aby wyświetlić ich wartości właściwości **ResourceGroupName**, **deploymentname** i **ProvisioningState** .</span><span class="sxs-lookup"><span data-stu-id="a50b5-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName**, **DeploymentName**, and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="a50b5-129">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a50b5-129">PARAMETERS</span></span>

### <span data-ttu-id="a50b5-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a50b5-130">-DefaultProfile</span></span>
<span data-ttu-id="a50b5-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a50b5-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a50b5-132">-ID</span><span class="sxs-lookup"><span data-stu-id="a50b5-132">-Id</span></span>
<span data-ttu-id="a50b5-133">Określa identyfikator wdrożenia grupy zasobów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="a50b5-133">Specifies the ID of the resource group deployment to get.</span></span>

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

### <span data-ttu-id="a50b5-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a50b5-134">-Name</span></span>
<span data-ttu-id="a50b5-135">Określa nazwę wdrożenia, które ma zostać pozyskane.</span><span class="sxs-lookup"><span data-stu-id="a50b5-135">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="a50b5-136">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="a50b5-136">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="a50b5-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="a50b5-137">-Pre</span></span>
<span data-ttu-id="a50b5-138">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="a50b5-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a50b5-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a50b5-139">-ResourceGroupName</span></span>
<span data-ttu-id="a50b5-140">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a50b5-140">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a50b5-141">Polecenie cmdlet umożliwia pobieranie wdrożeń dla grupy zasobów określanych przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="a50b5-141">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="a50b5-142">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="a50b5-142">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="a50b5-143">Ten parametr jest wymagany, a w każdym poleceniu można określić tylko dla jednej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a50b5-143">This parameter is required and you can specify only one resource group in each command.</span></span>

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

### <span data-ttu-id="a50b5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a50b5-144">CommonParameters</span></span>
<span data-ttu-id="a50b5-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a50b5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a50b5-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a50b5-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a50b5-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a50b5-147">INPUTS</span></span>

### <span data-ttu-id="a50b5-148">System. String</span><span class="sxs-lookup"><span data-stu-id="a50b5-148">System.String</span></span>

## <span data-ttu-id="a50b5-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a50b5-149">OUTPUTS</span></span>

### <span data-ttu-id="a50b5-150">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a50b5-150">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="a50b5-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a50b5-151">NOTES</span></span>

## <span data-ttu-id="a50b5-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a50b5-152">RELATED LINKS</span></span>

[<span data-ttu-id="a50b5-153">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a50b5-153">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="a50b5-154">Nowe — AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a50b5-154">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="a50b5-155">Nowe — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a50b5-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="a50b5-156">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a50b5-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="a50b5-157">Zatrzymaj — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a50b5-157">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="a50b5-158">Test — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a50b5-158">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


