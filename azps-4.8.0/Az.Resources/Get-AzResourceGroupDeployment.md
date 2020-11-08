---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: 1db46630ea4f864e1658eea8b789a79e6050fbbb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062525"
---
# <span data-ttu-id="f3a47-101">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f3a47-101">Get-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="f3a47-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3a47-102">SYNOPSIS</span></span>
<span data-ttu-id="f3a47-103">Pobiera wdrożenia w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="f3a47-103">Gets the deployments in a resource group.</span></span>

## <span data-ttu-id="f3a47-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3a47-104">SYNTAX</span></span>

### <span data-ttu-id="f3a47-105">GetByResourceGroupDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f3a47-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3a47-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="f3a47-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3a47-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f3a47-107">DESCRIPTION</span></span>
<span data-ttu-id="f3a47-108">Polecenie cmdlet **Get-AzResourceGroupDeployment** pobiera wdrożenia w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f3a47-108">The **Get-AzResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="f3a47-109">Określ *nazwę* lub parametr *ID* , aby przefiltrować wyniki.</span><span class="sxs-lookup"><span data-stu-id="f3a47-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="f3a47-110">Domyślnie polecenie **Get-AzResourceGroupDeployment** pobiera wszystkie wdrożenia określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f3a47-110">By default, **Get-AzResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="f3a47-111">Zasób platformy Azure jest zarządzaną przez użytkownika jednostką Azure, taką jak serwer bazy danych, baza danych lub witryna sieci Web.</span><span class="sxs-lookup"><span data-stu-id="f3a47-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="f3a47-112">Grupa zasobów platformy Azure to zbiór zasobów platformy Azure wdrożonych jako jednostka.</span><span class="sxs-lookup"><span data-stu-id="f3a47-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="f3a47-113">Wdrożenie to operacja, która powoduje, że zasoby w grupie zasobów są dostępne do użytku.</span><span class="sxs-lookup"><span data-stu-id="f3a47-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="f3a47-114">Aby uzyskać więcej informacji na temat zasobów platformy Azure i grup zasobów platformy Azure, zobacz polecenie cmdlet New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f3a47-114">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="f3a47-115">Za pomocą tego polecenia cmdlet można śledzić śledzenie.</span><span class="sxs-lookup"><span data-stu-id="f3a47-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="f3a47-116">W przypadku debugowania Użyj tego polecenia cmdlet, korzystając z polecenia cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="f3a47-116">For debugging, use this cmdlet with the Get-AzLog cmdlet.</span></span>

## <span data-ttu-id="f3a47-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3a47-117">EXAMPLES</span></span>

### <span data-ttu-id="f3a47-118">Przykład 1. pobieranie wszystkich wdrożeń dla grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f3a47-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="f3a47-119">To polecenie pobiera wszystkie wdrożenia grupy zasobów ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="f3a47-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="f3a47-120">Wynik przedstawia wdrożenie dla blogu WordPress, który używa szablonu galerii.</span><span class="sxs-lookup"><span data-stu-id="f3a47-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="f3a47-121">Przykład 2: uzyskiwanie wdrożenia według nazwy</span><span class="sxs-lookup"><span data-stu-id="f3a47-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="f3a47-122">To polecenie pobiera DeployWebsite01 wdrożenia grupy zasobów ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="f3a47-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="f3a47-123">Możesz przypisać nazwę do wdrożenia podczas tworzenia go za pomocą poleceń cmdlet **New-AzResourceGroup** lub **New-AzResourceGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="f3a47-123">You can assign a name to a deployment when you create it by using the **New-AzResourceGroup** or **New-AzResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="f3a47-124">Jeśli nie przypiszesz nazwy, aplety poleceń będą dostarczały nazwę domyślną na podstawie szablonu, który jest wykorzystywany do tworzenia wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="f3a47-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="f3a47-125">Przykład 3: pobieranie wdrożeń wszystkich grup zasobów</span><span class="sxs-lookup"><span data-stu-id="f3a47-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="f3a47-126">To polecenie pobiera wszystkie grupy zasobów w ramach subskrypcji przy użyciu polecenia cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f3a47-126">This command gets all resource groups in your subscription by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="f3a47-127">Polecenie przekazuje grupy zasobów do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="f3a47-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f3a47-128">Bieżące polecenie cmdlet pobiera wszystkie wdrożenia wszystkich grup zasobów w ramach subskrypcji i przekazuje wyniki do polecenia cmdlet Format-Table, aby wyświetlić ich wartości właściwości **ResourceGroupName** , **deploymentname** i **ProvisioningState** .</span><span class="sxs-lookup"><span data-stu-id="f3a47-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="f3a47-129">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3a47-129">PARAMETERS</span></span>

### <span data-ttu-id="f3a47-130">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f3a47-130">-ApiVersion</span></span>
<span data-ttu-id="f3a47-131">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="f3a47-131">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="f3a47-132">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="f3a47-132">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="f3a47-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3a47-133">-DefaultProfile</span></span>
<span data-ttu-id="f3a47-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f3a47-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3a47-135">-ID</span><span class="sxs-lookup"><span data-stu-id="f3a47-135">-Id</span></span>
<span data-ttu-id="f3a47-136">Określa identyfikator wdrożenia grupy zasobów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="f3a47-136">Specifies the ID of the resource group deployment to get.</span></span>

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

### <span data-ttu-id="f3a47-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f3a47-137">-Name</span></span>
<span data-ttu-id="f3a47-138">Określa nazwę wdrożenia, które ma zostać pozyskane.</span><span class="sxs-lookup"><span data-stu-id="f3a47-138">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="f3a47-139">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="f3a47-139">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="f3a47-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="f3a47-140">-Pre</span></span>
<span data-ttu-id="f3a47-141">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="f3a47-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f3a47-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3a47-142">-ResourceGroupName</span></span>
<span data-ttu-id="f3a47-143">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f3a47-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="f3a47-144">Polecenie cmdlet umożliwia pobieranie wdrożeń dla grupy zasobów określanych przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f3a47-144">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="f3a47-145">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="f3a47-145">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="f3a47-146">Ten parametr jest wymagany, a w każdym poleceniu można określić tylko dla jednej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f3a47-146">This parameter is required and you can specify only one resource group in each command.</span></span>

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

### <span data-ttu-id="f3a47-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3a47-147">CommonParameters</span></span>
<span data-ttu-id="f3a47-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3a47-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3a47-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3a47-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3a47-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3a47-150">INPUTS</span></span>

### <span data-ttu-id="f3a47-151">System. String</span><span class="sxs-lookup"><span data-stu-id="f3a47-151">System.String</span></span>

## <span data-ttu-id="f3a47-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3a47-152">OUTPUTS</span></span>

### <span data-ttu-id="f3a47-153">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f3a47-153">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="f3a47-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3a47-154">NOTES</span></span>

## <span data-ttu-id="f3a47-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3a47-155">RELATED LINKS</span></span>

[<span data-ttu-id="f3a47-156">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f3a47-156">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="f3a47-157">Nowe — AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f3a47-157">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="f3a47-158">Nowe — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f3a47-158">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="f3a47-159">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f3a47-159">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="f3a47-160">Zatrzymaj — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f3a47-160">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="f3a47-161">Test — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f3a47-161">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


