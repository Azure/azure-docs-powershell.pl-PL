---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: 9da5ee691b440ee24933d658dec3c85b1a7c8ced
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897546"
---
# <span data-ttu-id="c9096-101">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c9096-101">Get-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="c9096-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c9096-102">SYNOPSIS</span></span>
<span data-ttu-id="c9096-103">Pobiera wdrożenia w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="c9096-103">Gets the deployments in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9096-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c9096-104">SYNTAX</span></span>

### <span data-ttu-id="c9096-105">GetByResourceGroupDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c9096-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9096-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="c9096-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9096-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c9096-107">DESCRIPTION</span></span>
<span data-ttu-id="c9096-108">Polecenie cmdlet **Get-AzureRmResourceGroupDeployment** pobiera wdrożenia w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c9096-108">The **Get-AzureRmResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="c9096-109">Określ *nazwę* lub parametr *ID* , aby przefiltrować wyniki.</span><span class="sxs-lookup"><span data-stu-id="c9096-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="c9096-110">Domyślnie polecenie **Get-AzureRmResourceGroupDeployment** pobiera wszystkie wdrożenia określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c9096-110">By default, **Get-AzureRmResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="c9096-111">Zasób platformy Azure jest zarządzaną przez użytkownika jednostką Azure, taką jak serwer bazy danych, baza danych lub witryna sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c9096-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="c9096-112">Grupa zasobów platformy Azure to zbiór zasobów platformy Azure wdrożonych jako jednostka.</span><span class="sxs-lookup"><span data-stu-id="c9096-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="c9096-113">Wdrożenie to operacja, która powoduje, że zasoby w grupie zasobów są dostępne do użytku.</span><span class="sxs-lookup"><span data-stu-id="c9096-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="c9096-114">Aby uzyskać więcej informacji na temat zasobów platformy Azure i grup zasobów platformy Azure, zobacz polecenie cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c9096-114">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="c9096-115">Za pomocą tego polecenia cmdlet można śledzić śledzenie.</span><span class="sxs-lookup"><span data-stu-id="c9096-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="c9096-116">W przypadku debugowania Użyj tego polecenia cmdlet, korzystając z polecenia cmdlet Get-AzureRmLog.</span><span class="sxs-lookup"><span data-stu-id="c9096-116">For debugging, use this cmdlet with the Get-AzureRmLog cmdlet.</span></span>

## <span data-ttu-id="c9096-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c9096-117">EXAMPLES</span></span>

### <span data-ttu-id="c9096-118">Przykład 1. pobieranie wszystkich wdrożeń dla grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c9096-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="c9096-119">To polecenie pobiera wszystkie wdrożenia grupy zasobów ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="c9096-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="c9096-120">Wynik przedstawia wdrożenie dla blogu WordPress, który używa szablonu galerii.</span><span class="sxs-lookup"><span data-stu-id="c9096-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="c9096-121">Przykład 2: uzyskiwanie wdrożenia według nazwy</span><span class="sxs-lookup"><span data-stu-id="c9096-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="c9096-122">To polecenie pobiera DeployWebsite01 wdrożenia grupy zasobów ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="c9096-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="c9096-123">Możesz przypisać nazwę do wdrożenia podczas tworzenia go za pomocą poleceń cmdlet **New-AzureRmResourceGroup** lub **New-AzureRmResourceGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="c9096-123">You can assign a name to a deployment when you create it by using the **New-AzureRmResourceGroup** or **New-AzureRmResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="c9096-124">Jeśli nie przypiszesz nazwy, aplety poleceń będą dostarczały nazwę domyślną na podstawie szablonu, który jest wykorzystywany do tworzenia wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="c9096-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="c9096-125">Przykład 3: pobieranie wdrożeń wszystkich grup zasobów</span><span class="sxs-lookup"><span data-stu-id="c9096-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="c9096-126">To polecenie pobiera wszystkie grupy zasobów w ramach subskrypcji przy użyciu polecenia cmdlet Get-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c9096-126">This command gets all resource groups in your subscription by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="c9096-127">Polecenie przekazuje grupy zasobów do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="c9096-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c9096-128">Bieżące polecenie cmdlet pobiera wszystkie wdrożenia wszystkich grup zasobów w ramach subskrypcji i przekazuje wyniki do polecenia cmdlet Format-Table, aby wyświetlić ich wartości właściwości **ResourceGroupName** , **deploymentname** i **ProvisioningState** .</span><span class="sxs-lookup"><span data-stu-id="c9096-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="c9096-129">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c9096-129">PARAMETERS</span></span>

### <span data-ttu-id="c9096-130">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c9096-130">-ApiVersion</span></span>
<span data-ttu-id="c9096-131">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="c9096-131">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="c9096-132">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="c9096-132">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="c9096-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9096-133">-DefaultProfile</span></span>
<span data-ttu-id="c9096-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c9096-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9096-135">-ID</span><span class="sxs-lookup"><span data-stu-id="c9096-135">-Id</span></span>
<span data-ttu-id="c9096-136">Określa identyfikator wdrożenia grupy zasobów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="c9096-136">Specifies the ID of the resource group deployment to get.</span></span>

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

### <span data-ttu-id="c9096-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c9096-137">-Name</span></span>
<span data-ttu-id="c9096-138">Określa nazwę wdrożenia, które ma zostać pozyskane.</span><span class="sxs-lookup"><span data-stu-id="c9096-138">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="c9096-139">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="c9096-139">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="c9096-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="c9096-140">-Pre</span></span>
<span data-ttu-id="c9096-141">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="c9096-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c9096-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9096-142">-ResourceGroupName</span></span>
<span data-ttu-id="c9096-143">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c9096-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="c9096-144">Polecenie cmdlet umożliwia pobieranie wdrożeń dla grupy zasobów określanych przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="c9096-144">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="c9096-145">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="c9096-145">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="c9096-146">Ten parametr jest wymagany, a w każdym poleceniu można określić tylko dla jednej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c9096-146">This parameter is required and you can specify only one resource group in each command.</span></span>

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

### <span data-ttu-id="c9096-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9096-147">CommonParameters</span></span>
<span data-ttu-id="c9096-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9096-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9096-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9096-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9096-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9096-150">INPUTS</span></span>

### <span data-ttu-id="c9096-151">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c9096-151">None</span></span>

## <span data-ttu-id="c9096-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c9096-152">OUTPUTS</span></span>

### <span data-ttu-id="c9096-153">Microsoft. Azure. Commands. ResourceManagement. models.</span><span class="sxs-lookup"><span data-stu-id="c9096-153">Microsoft.Azure.Commands.ResourceManagement.Models.</span></span> <span data-ttu-id="c9096-154">PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c9096-154">PSResourceGroupDeployment</span></span>

## <span data-ttu-id="c9096-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c9096-155">NOTES</span></span>

## <span data-ttu-id="c9096-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9096-156">RELATED LINKS</span></span>

[<span data-ttu-id="c9096-157">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c9096-157">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="c9096-158">Nowe — AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c9096-158">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="c9096-159">Nowe — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c9096-159">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="c9096-160">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c9096-160">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="c9096-161">Zatrzymaj — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c9096-161">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="c9096-162">Test — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c9096-162">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


