---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleDefinition.md
ms.openlocfilehash: 79b1c647e192e3ce093c084ef89cf8535468727e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542328"
---
# <span data-ttu-id="c357b-101">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c357b-101">New-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="c357b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c357b-102">SYNOPSIS</span></span>
<span data-ttu-id="c357b-103">Tworzy rolę niestandardową w usłudze Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="c357b-103">Creates a custom role in Azure RBAC.</span></span>
<span data-ttu-id="c357b-104">Podaj plik definicji roli JSON lub obiekt PSRoleDefinition jako dane wejściowe.</span><span class="sxs-lookup"><span data-stu-id="c357b-104">Provide either a JSON role definition file or a PSRoleDefinition object as input.</span></span>
<span data-ttu-id="c357b-105">Najpierw użyj polecenia Get-AzureRmRoleDefinition, aby wygenerować obiekt definicji roli punktu odniesienia.</span><span class="sxs-lookup"><span data-stu-id="c357b-105">First, use the Get-AzureRmRoleDefinition command to generate a baseline role definition object.</span></span>
<span data-ttu-id="c357b-106">Następnie zmodyfikuj jej właściwości stosownie do potrzeb.</span><span class="sxs-lookup"><span data-stu-id="c357b-106">Then, modify its properties as required.</span></span>
<span data-ttu-id="c357b-107">Na koniec Użyj tego polecenia, aby utworzyć rolę niestandardową przy użyciu definicji roli.</span><span class="sxs-lookup"><span data-stu-id="c357b-107">Finally, use this command to create a custom role using role definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c357b-108">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c357b-108">SYNTAX</span></span>

### <span data-ttu-id="c357b-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="c357b-109">InputFileParameterSet</span></span>
```
New-AzureRmRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c357b-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c357b-110">RoleDefinitionParameterSet</span></span>
```
New-AzureRmRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c357b-111">Opis</span><span class="sxs-lookup"><span data-stu-id="c357b-111">DESCRIPTION</span></span>
<span data-ttu-id="c357b-112">Polecenie cmdlet New-AzureRmRoleDefinition tworzy rolę niestandardową w kontroli dostępu na platformie Azure Role-Based.</span><span class="sxs-lookup"><span data-stu-id="c357b-112">The New-AzureRmRoleDefinition cmdlet creates a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="c357b-113">Podaj definicję roli jako dane wejściowe polecenia jako plik JSON lub obiekt PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="c357b-113">Provide a role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>

<span data-ttu-id="c357b-114">Definicja roli wejściowej musi zawierać następujące właściwości:</span><span class="sxs-lookup"><span data-stu-id="c357b-114">The input role definition MUST contain the following properties:</span></span>

1) <span data-ttu-id="c357b-115">DisplayName: Nazwa roli niestandardowej</span><span class="sxs-lookup"><span data-stu-id="c357b-115">DisplayName: the name of the custom role</span></span>

2) <span data-ttu-id="c357b-116">Opis: Krótki opis roli, która podsumowuje dostęp przyznany przez rolę.</span><span class="sxs-lookup"><span data-stu-id="c357b-116">Description: a short description of the role that summarizes the access that the role grants.</span></span>

3) <span data-ttu-id="c357b-117">Akcje: zestaw operacji, do których rola niestandardowa udziela dostępu.</span><span class="sxs-lookup"><span data-stu-id="c357b-117">Actions: the set of operations to which the custom role grants access.</span></span>
<span data-ttu-id="c357b-118">Użyj Get-AzureRmProviderOperation, aby uzyskać dostęp do operacji dla dostawców zasobów platformy Azure, które można zabezpieczyć przy użyciu usługi Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="c357b-118">Use Get-AzureRmProviderOperation to get the operation for Azure resource providers that can be secured using Azure RBAC.</span></span>
<span data-ttu-id="c357b-119">Poniżej przedstawiono niektóre prawidłowe ciągi operacji:</span><span class="sxs-lookup"><span data-stu-id="c357b-119">Following are some valid operation strings:</span></span>
 - <span data-ttu-id="c357b-120">"\*/read" udziela dostępu do operacji odczytu wszystkich dostawców zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c357b-120">"\*/read" grants access to read operations of all Azure resource providers.</span></span>
 - <span data-ttu-id="c357b-121">"Microsoft. Network/\*/Read" udziela dostępu do operacji odczytu dla wszystkich typów zasobów w dostawcy zasobów Microsoft. Network na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="c357b-121">"Microsoft.Network/\*/read" grants access to read operations for all resource types in the Microsoft.Network resource provider of Azure.</span></span>
 - <span data-ttu-id="c357b-122">"Microsoft. COMPUTE/virtualMachines//\*" udziela dostępu wszystkim operacjom maszyn wirtualnych i jego podrzędnych typów zasobów.</span><span class="sxs-lookup"><span data-stu-id="c357b-122">"Microsoft.Compute/virtualMachines/\*" grants access to all operations of virtual machines and its child resource types.</span></span>

4) <span data-ttu-id="c357b-123">AssignableScopes: zestaw zakresów (subskrypcje platformy Azure lub grupy zasobów), w których rola niestandardowa będzie dostępna do przypisania.</span><span class="sxs-lookup"><span data-stu-id="c357b-123">AssignableScopes: the set of scopes (Azure subscriptions or resource groups) in which the custom role will be available for assignment.</span></span>
<span data-ttu-id="c357b-124">Korzystając z AssignableScopes, możesz ustawić rolę niestandardową dla przydziałów tylko w przypadku abonamentów lub grup zasobów, które ich potrzebują, a nie nie ma potrzeby nieuwzględniania środowiska użytkownika dla pozostałych subskrypcji lub grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="c357b-124">Using AssignableScopes you can make the custom role available for assignment in only the subscriptions or resource groups that need it, and not clutter the user experience for the rest of the subscriptions or resource groups.</span></span>
<span data-ttu-id="c357b-125">Poniżej przedstawiono niektóre z następujących zakresów, które można przydzielać:</span><span class="sxs-lookup"><span data-stu-id="c357b-125">Following are some valid assignable scopes:</span></span>
 - <span data-ttu-id="c357b-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e"; "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": udostępnia rolę do przypisania w dwóch abonamentach.</span><span class="sxs-lookup"><span data-stu-id="c357b-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": makes the role available for assignment in two subscriptions.</span></span>
 - <span data-ttu-id="c357b-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": udostępnia rolę do przypisania w ramach jednej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c357b-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": makes the role available for assignment in a single subscription.</span></span>
 - <span data-ttu-id="c357b-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": udostępnia rolę do przypisania tylko w grupie zasób sieciowy.</span><span class="sxs-lookup"><span data-stu-id="c357b-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": makes the role available for assignment only in the Network resource group.</span></span>

<span data-ttu-id="c357b-129">Definicja roli wejściowej może zawierać następujące właściwości:</span><span class="sxs-lookup"><span data-stu-id="c357b-129">The input role definition MAY contain the following properties:</span></span>

1) <span data-ttu-id="c357b-130">Noactions: zestaw operacji, które muszą być wykluczone z akcji, aby określić skuteczne działania roli niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="c357b-130">NotActions: the set of operations that must be excluded from the Actions to determine the effective actions for the custom role.</span></span>
<span data-ttu-id="c357b-131">Jeśli istnieje określona operacja, której nie chcesz udzielać dostępu w roli niestandardowej, wygodnie jest użyć funkcji noactions, aby ją wykluczyć, a nie określając wszystkich operacji innych niż określona operacja w działaniach.</span><span class="sxs-lookup"><span data-stu-id="c357b-131">If there is a specific operation that you do not wish to grant access to in a custom role, it is convenient to use NotActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
2) <span data-ttu-id="c357b-132">Akcje danych: zestaw operacji na dane, do których rola niestandardowa udziela dostępu.</span><span class="sxs-lookup"><span data-stu-id="c357b-132">DataActions: the set of data operations to which the custom role grants access.</span></span>
3) <span data-ttu-id="c357b-133">NotDataActions: zestaw operacji, które muszą być wykluczone z akcji dataactions w celu określenia efektywnych akcji dataactions dla roli niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="c357b-133">NotDataActions: the set of operations that must be excluded from the DataActions to determine the effective dataactions for the custom role.</span></span>
<span data-ttu-id="c357b-134">Jeśli istnieje określona operacja na danych, której nie chcesz udzielać dostępu w roli niestandardowej, wygodnie jest używać NotDataActions do jej wykluczania, a nie do określania wszystkich operacji innych niż określona operacja w działaniach.</span><span class="sxs-lookup"><span data-stu-id="c357b-134">If there is a specific data operation that you do not wish to grant access to in a custom role, it is convenient to use NotDataActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>

<span data-ttu-id="c357b-135">Uwaga: Jeśli użytkownikowi przypisano rolę określającą operację w argumentach zagranicowanie, a także przypisana innej roli udziela dostępu do tej samej operacji, użytkownik będzie mógł wykonać tę operację.</span><span class="sxs-lookup"><span data-stu-id="c357b-135">NOTE: If a user is assigned a role that specifies an operation in NotActions and also assigned another role grants access to the same operation - the user will be able to perform that operation.</span></span>
<span data-ttu-id="c357b-136">Nonaruszone nie jest regułą Odmów — jest to wygodna metoda tworzenia zestawu dozwolonych operacji, gdy trzeba wykluczyć konkretne operacje.</span><span class="sxs-lookup"><span data-stu-id="c357b-136">NotActions is not a deny rule - it is simply a convenient way to create a set of allowed operations when specific operations need to be excluded.</span></span>

<span data-ttu-id="c357b-137">Poniżej przedstawiono przykładową definicję roli JSON, którą można podać jako dane wejściowe {"name": "zaktualizowana rola", "opis": "może monitorować wszystkie zasoby i uruchamiać i ponownie uruchamiać maszyny wirtualne", "akcje": " \[ */Read", "Microsoft. ClassicCompute/virtualmachines/Action", "Microsoft. ClassicCompute/virtualmachines/Start/Action" \] ; "zanaruszone": \[ "* /Write" \] ; "akcje danych": \[ "Microsoft. Storage/storageAccounts/blobServices/Containers/BLOB/Read", "NotDataActions": "Microsoft. Storage/storageAccounts/blobServices/Containers \] \[ /BLOB/Write", "AssignableScopes" \] : \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="c357b-137">Following is a sample json role definition that can be provided as input { "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="c357b-138">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c357b-138">EXAMPLES</span></span>

### <span data-ttu-id="c357b-139">Tworzenie przy użyciu PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="c357b-139">Create using PSRoleDefinitionObject</span></span>
```
PS C:\> $role = Get-AzureRmRoleDefinition -Name "Virtual Machine Contributor"
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

          PS C:\> New-AzureRmRoleDefinition -Role $role
```

### <span data-ttu-id="c357b-140">Tworzenie przy użyciu pliku JSON</span><span class="sxs-lookup"><span data-stu-id="c357b-140">Create using JSON file</span></span>
```
PS C:\> New-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="c357b-141">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c357b-141">PARAMETERS</span></span>

### <span data-ttu-id="c357b-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c357b-142">-DefaultProfile</span></span>
<span data-ttu-id="c357b-143">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c357b-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c357b-144">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="c357b-144">-InputFile</span></span>
<span data-ttu-id="c357b-145">Nazwa pliku zawierającego jedną definicję roli JSON.</span><span class="sxs-lookup"><span data-stu-id="c357b-145">File name containing a single json role definition.</span></span>

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c357b-146">-Rola</span><span class="sxs-lookup"><span data-stu-id="c357b-146">-Role</span></span>
<span data-ttu-id="c357b-147">Obiekt definicji roli.</span><span class="sxs-lookup"><span data-stu-id="c357b-147">Role definition object.</span></span>

```yaml
Type: PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c357b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c357b-148">CommonParameters</span></span>
<span data-ttu-id="c357b-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c357b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c357b-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c357b-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c357b-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c357b-151">INPUTS</span></span>

### <span data-ttu-id="c357b-152">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c357b-152">None</span></span>
<span data-ttu-id="c357b-153">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="c357b-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c357b-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c357b-154">OUTPUTS</span></span>

### <span data-ttu-id="c357b-155">Microsoft. Azure. Commands. resources. models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c357b-155">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="c357b-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c357b-156">NOTES</span></span>
<span data-ttu-id="c357b-157">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="c357b-157">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="c357b-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c357b-158">RELATED LINKS</span></span>

[<span data-ttu-id="c357b-159">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="c357b-159">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="c357b-160">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c357b-160">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="c357b-161">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c357b-161">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

[<span data-ttu-id="c357b-162">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c357b-162">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

