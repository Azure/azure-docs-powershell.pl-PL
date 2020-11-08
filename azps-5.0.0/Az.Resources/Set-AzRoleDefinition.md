---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: c68ad7def1b94796a020ffd29495e2b4c0b15a60
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234277"
---
# <span data-ttu-id="2cbe2-101">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="2cbe2-101">Set-AzRoleDefinition</span></span>

## <span data-ttu-id="2cbe2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2cbe2-102">SYNOPSIS</span></span>
<span data-ttu-id="2cbe2-103">Modyfikuje rolę niestandardową w usłudze Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="2cbe2-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="2cbe2-104">Podaj zmodyfikowaną definicję roli jako plik JSON lub jako PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="2cbe2-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="2cbe2-105">Najpierw użyj polecenia Get-AzRoleDefinition, aby pobrać rolę niestandardową, którą chcesz zmodyfikować.</span><span class="sxs-lookup"><span data-stu-id="2cbe2-105">First, use the Get-AzRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="2cbe2-106">Następnie zmodyfikuj właściwości, które chcesz zmienić.</span><span class="sxs-lookup"><span data-stu-id="2cbe2-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="2cbe2-107">Na koniec Zapisz definicję roli za pomocą tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="2cbe2-107">Finally, save the role definition using this command.</span></span>

## <span data-ttu-id="2cbe2-108">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2cbe2-108">SYNTAX</span></span>

### <span data-ttu-id="2cbe2-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cbe2-109">InputFileParameterSet</span></span>
```
Set-AzRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cbe2-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cbe2-110">RoleDefinitionParameterSet</span></span>
```
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cbe2-111">Opis</span><span class="sxs-lookup"><span data-stu-id="2cbe2-111">DESCRIPTION</span></span>
<span data-ttu-id="2cbe2-112">Polecenie cmdlet Set-AzRoleDefinition aktualizuje istniejącą rolę niestandardową w kontroli dostępu na platformie Azure Role-Based.</span><span class="sxs-lookup"><span data-stu-id="2cbe2-112">The Set-AzRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="2cbe2-113">Wprowadź zaktualizowaną definicję roli jako dane wejściowe polecenia jako plik JSON lub obiekt PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="2cbe2-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="2cbe2-114">Definicja roli zaktualizowanej roli niestandardowej musi zawierać identyfikator i wszystkie inne wymagane właściwości roli, nawet jeśli nie zostały zaktualizowane: DisplayName, Description, Actions, AssignableScopes.</span><span class="sxs-lookup"><span data-stu-id="2cbe2-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="2cbe2-115">Nienaruszone, akcje dataNotDataActions są opcjonalne.</span><span class="sxs-lookup"><span data-stu-id="2cbe2-115">NotActions, DataActions, NotDataActions are optional.</span></span>
<span data-ttu-id="2cbe2-116">Poniżej przedstawiono przykładowy kod JSON zaktualizowanej definicji ról dla Set-AzRoleDefinition {"ID": "52a6cc13-ff92-47a8-a39b-2a8205c3087e"; "nazwa": "zaktualizowana rola", "opis": "może monitorować wszystkie zasoby i uruchamiać i ponownie uruchamiać maszyny wirtualne", "akcje": \[ " */Read", "Microsoft. ClassicCompute/virtualmachines/Action", "Microsoft. ClassicCompute/virtualmachines/Start/Action" \] ; "zanaruszone": \[ "* /Write" \] ; "akcje danych": \[ "Microsoft. Storage/storageAccounts/blobServices/Containers/BLOB/Read", "NotDataActions": "Microsoft. Storage/storageAccounts/blobServices/Containers \] \[ /BLOB/Write", "AssignableScopes" \] : \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="2cbe2-116">Following is a sample updated role definition json for Set-AzRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="2cbe2-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2cbe2-117">EXAMPLES</span></span>

### <span data-ttu-id="2cbe2-118">Przykład 1: aktualizowanie przy użyciu PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="2cbe2-118">Example 1: Update using PSRoleDefinitionObject</span></span>
```powershell
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### <span data-ttu-id="2cbe2-119">Przykład 2: Tworzenie za pomocą pliku JSON</span><span class="sxs-lookup"><span data-stu-id="2cbe2-119">Example 2: Create using JSON file</span></span>
```powershell
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="2cbe2-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2cbe2-120">PARAMETERS</span></span>

### <span data-ttu-id="2cbe2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cbe2-121">-DefaultProfile</span></span>
<span data-ttu-id="2cbe2-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2cbe2-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2cbe2-123">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="2cbe2-123">-InputFile</span></span>
<span data-ttu-id="2cbe2-124">Nazwa pliku zawierającego pojedynczą definicję roli JSON do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="2cbe2-124">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="2cbe2-125">Uwzględnij tylko właściwości, które mają zostać zaktualizowane w notacji JSON.</span><span class="sxs-lookup"><span data-stu-id="2cbe2-125">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="2cbe2-126">Właściwość ID jest wymagana.</span><span class="sxs-lookup"><span data-stu-id="2cbe2-126">Id property is Required.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cbe2-127">-Rola</span><span class="sxs-lookup"><span data-stu-id="2cbe2-127">-Role</span></span>
<span data-ttu-id="2cbe2-128">Obiekt definicji roli do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="2cbe2-128">Role definition object to be updated</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cbe2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cbe2-129">CommonParameters</span></span>
<span data-ttu-id="2cbe2-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cbe2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cbe2-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2cbe2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cbe2-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2cbe2-132">INPUTS</span></span>

### <span data-ttu-id="2cbe2-133">Microsoft. Azure. Commands. resources. models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="2cbe2-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="2cbe2-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2cbe2-134">OUTPUTS</span></span>

### <span data-ttu-id="2cbe2-135">Microsoft. Azure. Commands. resources. models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="2cbe2-135">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="2cbe2-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2cbe2-136">NOTES</span></span>
<span data-ttu-id="2cbe2-137">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="2cbe2-137">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="2cbe2-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2cbe2-138">RELATED LINKS</span></span>

[<span data-ttu-id="2cbe2-139">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="2cbe2-139">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="2cbe2-140">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="2cbe2-140">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="2cbe2-141">Nowe — AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="2cbe2-141">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="2cbe2-142">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="2cbe2-142">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

