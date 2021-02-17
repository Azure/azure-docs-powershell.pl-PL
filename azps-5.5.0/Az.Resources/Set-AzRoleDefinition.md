---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: c68ad7def1b94796a020ffd29495e2b4c0b15a60
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183626"
---
# <span data-ttu-id="7dae7-101">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7dae7-101">Set-AzRoleDefinition</span></span>

## <span data-ttu-id="7dae7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7dae7-102">SYNOPSIS</span></span>
<span data-ttu-id="7dae7-103">Modyfikuje rolę niestandardową w usłudze Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="7dae7-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="7dae7-104">Podaj zmodyfikowaną definicję roli jako plik JSON lub jako psRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="7dae7-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="7dae7-105">Najpierw użyj polecenia Get-AzRoleDefinition, aby pobrać rolę niestandardową, którą chcesz zmodyfikować.</span><span class="sxs-lookup"><span data-stu-id="7dae7-105">First, use the Get-AzRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="7dae7-106">Następnie zmodyfikuj właściwości, które chcesz zmienić.</span><span class="sxs-lookup"><span data-stu-id="7dae7-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="7dae7-107">Na koniec zapisz definicję ról przy użyciu tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="7dae7-107">Finally, save the role definition using this command.</span></span>

## <span data-ttu-id="7dae7-108">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7dae7-108">SYNTAX</span></span>

### <span data-ttu-id="7dae7-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="7dae7-109">InputFileParameterSet</span></span>
```
Set-AzRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7dae7-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7dae7-110">RoleDefinitionParameterSet</span></span>
```
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7dae7-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="7dae7-111">DESCRIPTION</span></span>
<span data-ttu-id="7dae7-112">Polecenie Set-AzRoleDefinition aktualizuje istniejącą rolę niestandardową w usłudze Azure Role-Based Access Control.</span><span class="sxs-lookup"><span data-stu-id="7dae7-112">The Set-AzRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="7dae7-113">Podaj zaktualizowaną definicję roli jako dane wejściowe polecenia jako plik JSON lub obiekt PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="7dae7-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="7dae7-114">Definicja roli zaktualizowanej roli niestandardowej MUSI zawierać identyfikator i wszystkie inne wymagane właściwości roli, nawet jeśli nie są aktualizowane: DisplayName, Description, Actions, AssignableScopes.</span><span class="sxs-lookup"><span data-stu-id="7dae7-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="7dae7-115">NotActions, DataActions, NotDataActions są opcjonalne.</span><span class="sxs-lookup"><span data-stu-id="7dae7-115">NotActions, DataActions, NotDataActions are optional.</span></span>
<span data-ttu-id="7dae7-116">Poniżej przedstawiono przykładową zaktualizowaną definicję roli dla programu Set-AzRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Zaktualizowano rolę", "Opis": "Może monitorować wszystkie zasoby oraz uruchamiać i ponownie uruchamiać maszyny wirtualne". "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action", \] "NotActions": \[ "*/write", \] "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" , "NotDataActions": "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" , "NotDataActions": "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \] , "NotDataActions": "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write", \] "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="7dae7-116">Following is a sample updated role definition json for Set-AzRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "*/write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="7dae7-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7dae7-117">EXAMPLES</span></span>

### <span data-ttu-id="7dae7-118">Przykład 1. Aktualizacja przy użyciu funkcji PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="7dae7-118">Example 1: Update using PSRoleDefinitionObject</span></span>
```powershell
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### <span data-ttu-id="7dae7-119">Przykład 2. Tworzenie przy użyciu pliku JSON</span><span class="sxs-lookup"><span data-stu-id="7dae7-119">Example 2: Create using JSON file</span></span>
```powershell
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="7dae7-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7dae7-120">PARAMETERS</span></span>

### <span data-ttu-id="7dae7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dae7-121">-DefaultProfile</span></span>
<span data-ttu-id="7dae7-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="7dae7-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7dae7-123">-InputFile</span><span class="sxs-lookup"><span data-stu-id="7dae7-123">-InputFile</span></span>
<span data-ttu-id="7dae7-124">Nazwa pliku zawierająca jedną definicję roli json do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="7dae7-124">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="7dae7-125">Uwzględnij tylko właściwości, które mają zostać zaktualizowane w JSON.</span><span class="sxs-lookup"><span data-stu-id="7dae7-125">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="7dae7-126">Właściwość Id jest wymagana.</span><span class="sxs-lookup"><span data-stu-id="7dae7-126">Id property is Required.</span></span>

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

### <span data-ttu-id="7dae7-127">— Rola</span><span class="sxs-lookup"><span data-stu-id="7dae7-127">-Role</span></span>
<span data-ttu-id="7dae7-128">Obiekt definicji roli do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="7dae7-128">Role definition object to be updated</span></span>

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

### <span data-ttu-id="7dae7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dae7-129">CommonParameters</span></span>
<span data-ttu-id="7dae7-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dae7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dae7-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7dae7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dae7-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7dae7-132">INPUTS</span></span>

### <span data-ttu-id="7dae7-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7dae7-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="7dae7-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7dae7-134">OUTPUTS</span></span>

### <span data-ttu-id="7dae7-135">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7dae7-135">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="7dae7-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7dae7-136">NOTES</span></span>
<span data-ttu-id="7dae7-137">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, zasób, grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="7dae7-137">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="7dae7-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7dae7-138">RELATED LINKS</span></span>

[<span data-ttu-id="7dae7-139">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="7dae7-139">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="7dae7-140">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7dae7-140">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="7dae7-141">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7dae7-141">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="7dae7-142">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7dae7-142">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

