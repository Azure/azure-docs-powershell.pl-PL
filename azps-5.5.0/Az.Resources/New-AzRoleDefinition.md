---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 8916b35da467fb16fd3802b726a7e105093b1c7a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183658"
---
# <span data-ttu-id="14161-101">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="14161-101">New-AzRoleDefinition</span></span>

## <span data-ttu-id="14161-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14161-102">SYNOPSIS</span></span>
<span data-ttu-id="14161-103">Tworzy rolę niestandardową w usłudze Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="14161-103">Creates a custom role in Azure RBAC.</span></span>
<span data-ttu-id="14161-104">Jako dane wejściowe podaj plik definicji roli JSON lub obiekt PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="14161-104">Provide either a JSON role definition file or a PSRoleDefinition object as input.</span></span>
<span data-ttu-id="14161-105">Najpierw użyj polecenia Get-AzRoleDefinition, aby wygenerować obiekt definicji roli planu bazowego.</span><span class="sxs-lookup"><span data-stu-id="14161-105">First, use the Get-AzRoleDefinition command to generate a baseline role definition object.</span></span>
<span data-ttu-id="14161-106">Następnie zmodyfikuj jego właściwości zgodnie z wymaganiami.</span><span class="sxs-lookup"><span data-stu-id="14161-106">Then, modify its properties as required.</span></span>
<span data-ttu-id="14161-107">Na koniec użyj tego polecenia, aby utworzyć rolę niestandardową przy użyciu definicji ról.</span><span class="sxs-lookup"><span data-stu-id="14161-107">Finally, use this command to create a custom role using role definition.</span></span>

## <span data-ttu-id="14161-108">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="14161-108">SYNTAX</span></span>

### <span data-ttu-id="14161-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="14161-109">InputFileParameterSet</span></span>
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14161-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="14161-110">RoleDefinitionParameterSet</span></span>
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14161-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="14161-111">DESCRIPTION</span></span>
<span data-ttu-id="14161-112">Polecenie New-AzRoleDefinition cmdlet tworzy niestandardową rolę w usłudze Azure Role-Based Access Control.</span><span class="sxs-lookup"><span data-stu-id="14161-112">The New-AzRoleDefinition cmdlet creates a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="14161-113">Podaj definicję roli jako dane wejściowe polecenia jako plik JSON lub obiekt PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="14161-113">Provide a role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="14161-114">Definicja roli wprowadzania MUSI zawierać następujące właściwości:</span><span class="sxs-lookup"><span data-stu-id="14161-114">The input role definition MUST contain the following properties:</span></span>
1) <span data-ttu-id="14161-115">DisplayName: nazwa roli niestandardowej</span><span class="sxs-lookup"><span data-stu-id="14161-115">DisplayName: the name of the custom role</span></span>
2) <span data-ttu-id="14161-116">Opis: krótki opis roli podsumowujący dostęp udzielany przez tę rolę.</span><span class="sxs-lookup"><span data-stu-id="14161-116">Description: a short description of the role that summarizes the access that the role grants.</span></span>
3) <span data-ttu-id="14161-117">Akcje: zestaw operacji, do których udziela dostęp rola niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="14161-117">Actions: the set of operations to which the custom role grants access.</span></span>
<span data-ttu-id="14161-118">Użyj Get-AzProviderOperation, aby uzyskać operację dla dostawców zasobów platformy Azure, które mogą być zabezpieczone przy użyciu usługi Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="14161-118">Use Get-AzProviderOperation to get the operation for Azure resource providers that can be secured using Azure RBAC.</span></span>
<span data-ttu-id="14161-119">Poniżej przedstawiono kilka prawidłowych ciągów operacji:</span><span class="sxs-lookup"><span data-stu-id="14161-119">Following are some valid operation strings:</span></span>
 - <span data-ttu-id="14161-120">"\*/read" udziela dostępu do operacji odczytu wszystkich dostawców zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="14161-120">"\*/read" grants access to read operations of all Azure resource providers.</span></span>
 - <span data-ttu-id="14161-121">"Microsoft.Network/\*/read" udziela dostępu do operacji odczytu dla wszystkich typów zasobów u dostawcy zasobów Microsoft.Network platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="14161-121">"Microsoft.Network/\*/read" grants access to read operations for all resource types in the Microsoft.Network resource provider of Azure.</span></span>
 - <span data-ttu-id="14161-122">"Microsoft.Compute/virtualMachines/\*" udziela dostępu do wszystkich operacji maszyn wirtualnych i ich typów zasobów podrzędnego.</span><span class="sxs-lookup"><span data-stu-id="14161-122">"Microsoft.Compute/virtualMachines/\*" grants access to all operations of virtual machines and its child resource types.</span></span>
4) <span data-ttu-id="14161-123">AssignableScopes: zestaw zakresów (subskrypcji platformy Azure lub grup zasobów), w których rola niestandardowa będzie dostępna dla przydziału.</span><span class="sxs-lookup"><span data-stu-id="14161-123">AssignableScopes: the set of scopes (Azure subscriptions or resource groups) in which the custom role will be available for assignment.</span></span>
<span data-ttu-id="14161-124">Za pomocą funkcji AssignableScopes możesz udostępnić niestandardową rolę dla przydziału tylko w potrzebnych subskrypcjach lub grupach zasobów, a nie zaśmiecać środowisko użytkownika dla pozostałych subskrypcji lub grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="14161-124">Using AssignableScopes you can make the custom role available for assignment in only the subscriptions or resource groups that need it, and not clutter the user experience for the rest of the subscriptions or resource groups.</span></span>
<span data-ttu-id="14161-125">Poniżej przedstawiono kilka prawidłowych zakresów, które można przypisać:</span><span class="sxs-lookup"><span data-stu-id="14161-125">Following are some valid assignable scopes:</span></span>
 - <span data-ttu-id="14161-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": umożliwia przypisanie roli w dwóch subskrypcjach.</span><span class="sxs-lookup"><span data-stu-id="14161-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": makes the role available for assignment in two subscriptions.</span></span>
 - <span data-ttu-id="14161-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": umożliwia przypisanie roli w ramach jednej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="14161-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": makes the role available for assignment in a single subscription.</span></span>
 - <span data-ttu-id="14161-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": udostępnia rolę tylko w grupie zasobów sieciowych.</span><span class="sxs-lookup"><span data-stu-id="14161-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": makes the role available for assignment only in the Network resource group.</span></span>
<span data-ttu-id="14161-129">Definicja roli wprowadzania MOŻE zawierać następujące właściwości:</span><span class="sxs-lookup"><span data-stu-id="14161-129">The input role definition MAY contain the following properties:</span></span>
1) <span data-ttu-id="14161-130">NotActions: zbiór operacji, które należy wykluczyć z akcji w celu określenia skutecznych akcji dla roli niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="14161-130">NotActions: the set of operations that must be excluded from the Actions to determine the effective actions for the custom role.</span></span>
<span data-ttu-id="14161-131">Jeśli nie chcesz udzielać dostępu do danej roli niestandardowej za pomocą określonych operacji, wygodnie jest wykluczyć tę operację za pomocą notactions, zamiast określać wszystkie operacje inne niż ta operacja w akcjach.</span><span class="sxs-lookup"><span data-stu-id="14161-131">If there is a specific operation that you do not wish to grant access to in a custom role, it is convenient to use NotActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
2) <span data-ttu-id="14161-132">DataActions: zestaw operacji danych, do których rola niestandardowa udziela dostępu.</span><span class="sxs-lookup"><span data-stu-id="14161-132">DataActions: the set of data operations to which the custom role grants access.</span></span>
3) <span data-ttu-id="14161-133">NotDataActions: zbiór operacji, które należy wykluczyć z akcji Danych w celu określenia skutecznych akcji danych dla roli niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="14161-133">NotDataActions: the set of operations that must be excluded from the DataActions to determine the effective data actions for the custom role.</span></span>
<span data-ttu-id="14161-134">Jeśli nie chcesz udzielać dostępu do danych w roli niestandardowej za pomocą funkcji NotDataActions, możesz ją wykluczyć za pomocą notDataActions, zamiast określać wszystkie operacje inne niż ta operacja w akcjach.</span><span class="sxs-lookup"><span data-stu-id="14161-134">If there is a specific data operation that you do not wish to grant access to in a custom role, it is convenient to use NotDataActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
<span data-ttu-id="14161-135">UWAGA: Jeśli użytkownikowi przypisano rolę określającą operację w notactions, a także inną rolę, udziela dostępu do tej samej operacji — użytkownik będzie mógł wykonać tę operację.</span><span class="sxs-lookup"><span data-stu-id="14161-135">NOTE: If a user is assigned a role that specifies an operation in NotActions and also assigned another role grants access to the same operation - the user will be able to perform that operation.</span></span>
<span data-ttu-id="14161-136">NotActions nie jest regułą odrzucaną — jest to po prostu wygodny sposób na utworzenie zestawu dozwolonych operacji, gdy trzeba wykluczyć określone operacje.</span><span class="sxs-lookup"><span data-stu-id="14161-136">NotActions is not a deny rule - it is simply a convenient way to create a set of allowed operations when specific operations need to be excluded.</span></span>
<span data-ttu-id="14161-137">Poniżej przedstawiono przykładową definicję ról json, która może być dostarczana jako dane wejściowe { "Nazwa": "Zaktualizowano rolę", "Opis": "Może monitorować wszystkie zasoby oraz uruchamiać i ponownie uruchamiać maszyny wirtualne", "Akcje": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action", \] "NotActions": \[ "*/write", \] "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices//blobServices/. containers/blobs/read", \] "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write", \] "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="14161-137">Following is a sample json role definition that can be provided as input { "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "*/write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="14161-138">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="14161-138">EXAMPLES</span></span>

### <span data-ttu-id="14161-139">Przykład 1. Tworzenie przy użyciu funkcji PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="14161-139">Example 1: Create using PSRoleDefinitionObject</span></span>
```powershell
PS C:\> $role = Get-AzRoleDefinition -Name "Virtual Machine Contributor"

PS C:\> $role.Id = $null
PS C:\> $role.Name = "Virtual Machine Operator"
PS C:\> $role.Description = "Can monitor, start, and restart virtual machines."
PS C:\> $role.Actions.RemoveRange(0,$role.Actions.Count)
PS C:\> $role.Actions.Add("Microsoft.Compute/*/read")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/start/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/restart/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/downloadRemoteDesktopConnectionFile/action")
PS C:\> $role.Actions.Add("Microsoft.Network/*/read")
PS C:\> $role.Actions.Add("Microsoft.Storage/*/read")
PS C:\> $role.Actions.Add("Microsoft.Authorization/*/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/resources/read")
PS C:\> $role.Actions.Add("Microsoft.Insights/alertRules/*")
PS C:\> $role.Actions.Add("Microsoft.Support/*")
PS C:\> $role.AssignableScopes.Clear()
PS C:\> $role.AssignableScopes.Add("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

PS C:\> New-AzRoleDefinition -Role $role
```

### <span data-ttu-id="14161-140">Przykład 2. Tworzenie przy użyciu pliku JSON</span><span class="sxs-lookup"><span data-stu-id="14161-140">Example 2: Create using JSON file</span></span>
```powershell
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="14161-141">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14161-141">PARAMETERS</span></span>

### <span data-ttu-id="14161-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14161-142">-DefaultProfile</span></span>
<span data-ttu-id="14161-143">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="14161-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14161-144">-InputFile</span><span class="sxs-lookup"><span data-stu-id="14161-144">-InputFile</span></span>
<span data-ttu-id="14161-145">Nazwa pliku zawierająca jedną definicję roli json.</span><span class="sxs-lookup"><span data-stu-id="14161-145">File name containing a single json role definition.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14161-146">— Rola</span><span class="sxs-lookup"><span data-stu-id="14161-146">-Role</span></span>
<span data-ttu-id="14161-147">Obiekt definicji roli.</span><span class="sxs-lookup"><span data-stu-id="14161-147">Role definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14161-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14161-148">CommonParameters</span></span>
<span data-ttu-id="14161-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14161-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14161-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14161-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14161-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14161-151">INPUTS</span></span>

### <span data-ttu-id="14161-152">Brak</span><span class="sxs-lookup"><span data-stu-id="14161-152">None</span></span>

## <span data-ttu-id="14161-153">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14161-153">OUTPUTS</span></span>

### <span data-ttu-id="14161-154">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="14161-154">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="14161-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="14161-155">NOTES</span></span>
<span data-ttu-id="14161-156">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, zasób, grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="14161-156">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="14161-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14161-157">RELATED LINKS</span></span>

[<span data-ttu-id="14161-158">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="14161-158">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="14161-159">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="14161-159">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="14161-160">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="14161-160">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

[<span data-ttu-id="14161-161">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="14161-161">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

